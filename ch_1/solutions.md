# Exercises

## 1.1.1
a) 
Let P = We'll have a reading assignment, Q = we'll have homework problems, R = we'll have a test
- $(P \lor Q) \land \neg(Q \land R)$ 

b) 
Let P = You'll go skiing, Q = there'll be snow
- $\neg P \lor (P \land \neg Q)$

c) 
Let P = $\sqrt(7) < 2$, Q = $\sqrt(7) = 2$
- $\neg (P \land Q)$

## 1.1.2
a) P = John will tell the truth, Q = John will tell the truth 
- $(P \land J) \lor \neg(P \land Q)$ 

b) P = I'll have fish, Q = I'll have chicken, R = I'll have mashed potatoes
- $(P \lor Q) \land \neg(P \land R)$

c) P = 3 is a common divisor of 6, Q = ($\dots$) 9, R = ($\dots$) 15 
- $P \land Q \land R$

## 1.1.3
A = Alice is in the room, B = Bob is in the room 
- a) $\neg (A \land B)$ 
- b) $\neg A \land \neg B$
- c) $\neg A \lor  \neg B$ - $\equiv a)$
- d) $\neg (A \lor B)$ - Neither negates the whole statement/formulae! (compare to c)

## 1.1.4 
A = Ralph is tall, B = Ed is tall, Q = Ralph is handsome, R = Ed is handsome
- a) $(A \land B) \lor (Q \land R)$
- b) $(A \lor Q) \land (B \lor R)$
- c) $\neg(A \lor Q) \land \neg(B \lor R)$ 
- d) $\neg((A \land R) \lor (B \land R))$

## 1.1.5 
a) and c) are well-formed statements/formulae.

## 1.1.6
Let P = I will buy pants, S = I will buy the shirt
- a) I will not buy the pants without buying the shirt
- b) I will neither buy the shirt nor the pants
- c) I will not buy both the shirt or I will not buy the pants

## 1.1.7
Let S = Steve is happy, G = George is happy. 
- a) Either Steve or george is happy and either Steve or george is unhappy
- b) Either steve is happy or Steve is happy and George isn't or George is not happy 
- c) Either Steve is happy or George is happy and Steve or George is unhappy. 
## 1.1.8
Let T = Taxes will go up, D = The deficit will go up.
- a) Taxes will go up or the deficit will go up 
- b) Taxes and the deficiet won't both go up and it is not the case the both Taxes and the deficient will go down. 
- c) Either taxes will go up and the deficient goes down or the deficiet goes up and taxes go down. 

## 1.1.9
A hint to building these tables is to "flip" truth values like you would in binary counting!
ALSO, truth is not the same as either soundness or validity!

### A 
P = Jane will win the math prize, Q = Jane will win the chemestry prize, R = Pete will win the math prize, T = Pete will win the chemestry prize. 
To solve this problem, consider all possible combinations of true premises. IF the conclusion is ever false, while the premises are true, then it cannot a correct conclusion. 
- PREMISES: $\neg (P \land R), (P \lor R),Q$,  CONCLUSION: $R$

| P | Q | R | $P \land R$ | $P \lor R$ | Q | R |
|---|---|---|-----------|----------|---|---|
| T | T | T | F | T | T | T |
| T | T | F | T | T | T | F |
| T | F | T | F | T | F | T |
| T | F | F | T | T | F | F |
| F | T | T | T | T | T | T |
| F | T | F | T | F | T | F |
| F | F | T | T | T | F | T |
| F | F | F | T | F | F | F |

Row 2: Premises are true without the conclusion being true -> The argument is not valid!

### B
P = The main course will be fish, Q = The main course will be beef, R = The vegetable will be peas, T = The vegetable will be corn
PREMISES: $P \lor Q$, $R \lor T$ CONCLUSION: $Q \land R$ - Please note that the logical expressions are NOT modelled as exclusive or, but this interpretation does make sense; you can't have both the fish and the meat at the same time!

| P  | Q | R | T |  $P \lor Q$ | $R \lor T$ |$\neg(P \land T)$  |$\neg(Q \land R)$ 
| ---|---|---|---|-------------|------------|-------------------| -----------------|
| F  | F | F | F | F           | F          | T                 | T              |
| F  | F | F | T | F           | T          | T                 | T              |
| F  | F | T | F | F           | T          | T                 | T              |
| F  | F | T | T | F           | T          | T                 | T              |
| F  | T | F | F | T           | F          | T                 | T              |
| F  | T | F | T | T           | T          | T                 | T              |
| F  | T | T | F | T           | T          | T                 | F              | 
| F  | T | T | T | T           | T          | T                 | F              |
| T  | F | F | F | T           | F          | T                 | T              |
¦ T  | F | F | T | T           | T          | F                 | T              |
¦ T  | F | T | F | T           | T          | T                 | T              | 
| T  | F | T | T | T           | T          | F                 | T              |
| T  | T | F | F | T           | F          | T                 | T              |
| T  | T | F | T | T           | T          | F                 | T              |
| T  | T | T | F | T           | T          | T                 | F              |
| T  | T | T | T | T           | T          | F                 | F              | 
This argument is not valid, see line 93!

### C
P = John is telling the truth, Q = Bill is telling the truth, R = Sam is telling the truth
- c) PREMISES: $(P \lor Q), (\neg P \lor \neg R)$, CONCLUSION: $(P \lor \neg R)$ 

| P | Q | R |$(P \lor Q)$ | $(\neg P \lor \neg R)$ | $(P \lor \neg R)$ | 
|---|---|---|-------------|------------------------|-------------------|
| F | F | F | F           | T                      | T                 |
| F | F | T | F           | T                      | F                 |
| F | T | F | T           | T                      | T                 |
| F | T | T | T           | T                      | F                 | 
| T | F | F | T           | T                      | T                 |
| T | F | T | T           | F                      | T                 |
| T | T | F | T           | T                      | T                 |
| T | T | T | T           | F                      | T                 |
This argument is not valid! See line 112!

P = sales will go up, Q = boss will be happy, R = expenses will go up 
- d) PREMSISES: $(P \land Q), (R \land \neg Q)$ CONCLUSION: $\neg(P \land R)$, rest of the truth table left as exercise. 

## 1.2.1
In the truth table exercises, it is sometimes easier to create a dummy boolean variable whose assigned truth value is identical to that of a compound formula. 
### A
| P | Q | $\neg P \lor Q$ | 
|---|---|-----------------|
| F | F | T               | 
| F | T | T               |
| T | F | F               | 
| T | T | T               |

### B 
| S | G | $S \lor G$ = A | $\neg S \lor \neg G$ = B | $A \land B$ | 
|---|---|----------------|--------------------------|-------------|
| F | F | F              |  T                       | F           |
| F | T | T              |  T                       | T           |
| T | F | T              |  T                       | T           |
| T | T | T              |  F                       | F           |
That's equivalent to xor - exactly one atomic propositon is true in the molecular proposition!

## 1.2.2
### A 
| P | Q | $Q \lor \neg P$ | $\neg (P \land (Q \lor \neg P)) | 
|---|---|-----------------|-------------------------------|
| F | F | T               | T                             | 
| F | T | T               | T                             |
| T | F | F               | T                             |
| T | T | T               | F                             |

### B 
| P | Q | R | $P \lor Q$ | $\neg P \lor R$ | $(P \lor Q) \land (\neg P \lor R)$|
|---|---|---|------------|-----------------|-----------------------------------|
| F | F | F | F          | T               | F                                 |
| F | F | T | F          | T               | F                                 | 
| F | T | F | T          | T               | T                                 |
| F | T | T | T          | T               | T                                 |
| T | F | F | T          | F               | F                                 |
| T | F | T | T          | T               | T                                 |
| T | T | F | T          | F               | F                                 |
| T | T | T | T          | T               | T                                 |


## 1.2.3
### A 
| P | Q | P + Q |
|---|---|-------|
| F | F | F     |
| F | T | T     |
| T | F | T     |
| T | T | F     |

### B
We saw one of these expressions in [2.1.1](/ch_1/solutions.md#2.1.1), but we shall see if we cannot simplify the expression a bit!
| P | Q | $\neg(Q \land P) \land (P \lor Q)$ | $(\neg Q \lor \neg P) \land (P \lor Q)$ |  
|---|---|------------------------------------|-----------------------------------------|
| F | F | F                                  | F                                       |
| F | T | T                                  | T                                       |
| T | F | T                                  | T                                       |
| T | T | F                                  | F                                       |

## 1.2.4
Use of deMorgan to simplify - deMorgan is extremely useful!
| P | Q | $P \lor Q$ | $\neg(\neg P \land \neg Q)$  |
|---|---|------------|------------------------------|
| F | F | F          | F                            |
| F | T | T          | T                            |
| T | F | T          | T                            |
| T | T | T          | T                            |

## 1.2.5 
### A 
Creating the nor expression
| P | Q | $P \downarrow Q$ |
|---|---|------------------| 
| F | F | T                |
| F | T | F                |
| T | F | F                |
| T | T | F                |

### B 
Essentially, what we are training here is finding equivalent expressions, and normal forms which are easier for the computer to compute (conjunctions can be short circuited)
| P | Q | $P \downarrow Q$ | $\neg (P \lor Q)$|
|---|---|------------------|------------------|
| F | F | T                | T                |
| F | T | F                | F                |
| T | F | F                | F                |
| T | T | F                | F                |

### C
| P | Q | $P \lor Q$       | $(P \downarrow Q) \downarrow (P \downarrow Q)$      | $P \land Q$|$(P \downarrow P) \downarrow (Q \downarrow Q)$ | $\neg P$  | $P \downarrow P$|
|---|---|------------------|-----------------------------------------------------|------------|-----------------------------------------------|-----------|-----------------|
| F | F | F                | F                                                   | F          | F                                             | T         | T               | 
| F | T | T                | T                                                   | F          | F                                             | T         | T               |             
| T | F | T                | T                                                   | F          | F                                             | F         | F               |              
| T | T | T                | T                                                   | T          | T                                             | F         | F               |               

## 1.2.6
### A 
| P | Q | $(P | Q)$ (nand) |
|---|---|------------------|
| F | F | T                |
| F | T | T                |
| T | F | T                |
| T | T | F                |

### B 
| P | Q | $(P|Q)$| $\neg (P \land Q)$|
|---|---|--------|-------------------|
| F | F | T      | T                 |
| F | T | T      | T                 |
| T | F | T      | T                 |
| T | T | F      | F                 |

### C 

## 1.2.7

## 1.2.8

## 1.2.9

## 1.2.10

## 1.2.11

## 1.2.12

## 1.2.13

## 1.2.14

## 1.2.15

## 1.2.16

## 1.2.17

## 1.2.18