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

## 1.1.)3
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

## 1.2.6 - TODO: fix table bug here
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
| P | Q | $\neg P$ | $(P | P)$ | $P \lor Q$ | $(P | P) | (Q | Q)$ | $P \land Q$ | $(P | Q) | (P | Q)$ |
|---|---|----------|-----------|------------|---------------------|-------------|---------------------|   
| F | F | T        | T         | F          | F                   | F           | F                   |
| F | T | T        | T         | T          | T                   | F           | F                   |
| T | F | F        | F         | T          | T                   | F           | F                   |
| T | T | F        | F         | T          | T                   | T           | T                   |

## 1.2.7
Already completed, see [1.1.9](/ch_1/solutions.md#1.1.9). 

## 1.2.8
| P | Q | $(P \land Q) \lor (\neg P \land \neg Q)$| $\neg P \lor Q$    | $(P \lor \neg Q) \land (Q \lor \neg P)$ | $\neg(P \lor Q)$ | $(Q \land P) \lor \neg P$ |
|---|---|-----------------------------------------|--------------------|-----------------------------------------|------------------|---------------------------|
| F | F | T                                       | T                  | T                                       | T                | T                         |
| F | T | F                                       | T                  | F                                       | F                | T                         |               
| T | F | F                                       | F                  | F                                       | F                | F                         |
| T | T | T                                       | T                  | T                                       | F                | T                         |
Remember that propositions are equivalent if their truth value assignment is identical. 

Using this truth table, we conclude that: 
- a), c) are equivalent
- b), e) are equivalent
- d) is not equivalent to any proposition.


## 1.2.9
| P | Q | R | $(P \lor Q) \land (\neg P \lor \neg Q)$ | $(P \lor Q) \land (\neg P \land \neg Q)$ |  $(P \lor Q) \lor (\neg P \lor \neg Q)$ | $(P \land (Q \lor \neg R)) \lor (\neg P \lor R)$ |
|---|---|---|-----------------------------------------|------------------------------------------|-----------------------------------------|--------------------------------------------------|
| F | F | F | F                                       | F                                        | T                                       | T                                                |   
| F | F | T | F                                       | F                                        | T                                       | T                                                |
| F | T | F | T                                       | F                                        | T                                       | T                                                |
| F | T | T | T                                       | F                                        | T                                       | T                                                |
| T | F | F | T                                       | F                                        | T                                       | T                                                |
| T | F | T | T                                       | F                                        | T                                       | T                                                |
| T | T | F | F                                       | F                                        | T                                       | T                                                |
| T | T | T | F                                       | F                                        | T                                       | T                                                |

Using this truth table, we can determine the following results about propostions a), b), c), d)
- a) Is neither a tautology nor a contradiction.  
- b) Is a contradiction 
- c) Is a tautology
- d) Is a tautology 

## 1.2.10
Left as extra exercise. 

## 1.2.11
### A 
$
\neg(\neg P \land \neg Q) \equiv \neg \neg P \lor \neg \neg Q (\text{DeMorgan})\\
\equiv P \land Q (\text{Double negation law})
$

### B 
$
(P \land Q) \lor (P \land \neg Q) \equiv P \land (Q \lor \neg Q) (\text{Distributive law})\\
\equiv P (\text{Tautology law})
$

### C 
$
\neg (P \land \neg Q) \lor (\neg P \land Q) \equiv (\neg P \lor \neg \neg Q) \lor (\neg P \land Q) (\text{DeMorgan})\\
\equiv (\neg P \lor Q) \lor (\neg P \land Q) \text{Double negation law}\\
\equiv \neg P \lor (Q \lor (\neg P \land Q)) (\text{associative law})\\
\equiv \neg P \lor (Q \lor (Q \land \neg P)) (\text{commutative law})\\
\equiv \neg P \lor Q (\text{absorption law}) 
$
Remember that these are LAWs not suggestions, if propositons are not on this exact form, the laws CANNOT be applied (especially relevant with the absorption law)

## 1.2.12
### A 
$
\neg (\neg P \lor Q) \lor (P \land \neg R) \equiv (P \land \neg Q) \lor (P \land \neg R) (\text{DeMorgan + Double negation law})\\
\equiv P \land (\neg Q \lor \neg R) \text{Distributive law} \\
\equiv P \land \neg(Q \land R) \text{DeMorgan} 
$

### B 
$
\neg(\neg P \land Q) \lor (P \land \neg R) \equiv (P \lor \neg Q) \lor (P \land \neg R) (\text{DeMorgan + Double negation law})\\
\equiv (\neg Q \lor P ) \lor (P \land \neg R) (\text{Commutative law})\\
\equiv \neg Q \lor (P \lor (P \land \neg R)) (\text{Associative law})\\
\equiv \neg Q \lor P (\text{Absorption law})
$

### C 
$
(P \land R) \lor [\neg R \land (P \lor Q)]\\
$

## 1.2.13
### FIRST ATTEMPT - this is for you to see some progress in your proof making
We show that the result for propositions, P, Q

$
\neg (P \lor Q) \equiv (\neg P \land \neg Q)
$
Know as DeMorgan's second law, is derivable using DeMorgan's first law and the law of double negation. 

### Preliminaries

**De Morgan's first law** 

For any P,Q, De Morgan's first law states that the negation of the conjunction of P and Q is logically equivalent to the disjunction of the negation of P and the negation of Q. 

$
\neg(P \land Q) \equiv \neg P \lor \neg Q
$

NOTE: Here is a shorter more precise wording of the same law. 
For any propositions, P,Q, 

$
\neg(P \land Q) \equiv \neg P \lor \neg Q
$

This is known as DeMorgan's first law. 

**The law of double negation** 

For any proposition P, 

$
\neg \neg P \equiv P
$

This is known as the law of double negation. 

**Derivation** 
Let P, Q be propositions. 
Then
$
\neg (P \lor Q) \equiv \neg (\neg \neg P \lor \neg \neg Q) (\text{double negation law})\\
\equiv \neg \neg (\neg P \and \neg Q) (\text{DeMorgan's first law})\\
\equiv (\neg P \land \neg Q) (\text{double negation law})\\
$
The last derivation allows us to conclude that 
$
\neg (P \lor Q) \equiv (\neg P \land \neg Q) 
$
This is exactly the definition of DeMorgan's second law. 

### SECOND ATTEMPT 
The goal of this exercise is to show that DeMorgan's second law is derivable using De Morgan's first law and the law of double negation. 

### Preliminaries 
We first define necessary laws. 

**De Morgan's first law** 

For any propositions, P,Q, 

$
\neg(P \land Q) \equiv \neg P \lor \neg Q
$

**De Morgan's second law**

For any propositions, P, Q 

$
\neg (P \lor Q) \equiv (\neg P \land \neg Q)
$

**The law of double negation** 

For any proposition P, 

$
\neg \neg P \equiv P
$


**Derivation** 

We show that Morgan's second law is deivable using De Morgan's first law and the law of double negation. 

Let P, Q be propositions. 

Then

$
\neg (P \lor Q) \equiv \neg (\neg \neg P \lor \neg \neg Q) (\text{double negation law})\\
\equiv \neg \neg (\neg P \land \neg Q) (\text{DeMorgan's first law})\\
\equiv (\neg P \land \neg Q) (\text{double negation law})\\
$
The last dervation allows us to conclude that 
$
\neg (P \lor Q) \equiv (\neg P \land \neg Q) 
$
This is exactly the definition of DeMorgan's second law. 

Therefore we conclude that De Morgan's second law is derivable using De Morgan's first law and the law of double negation. 

## 1.2.14

## 1.2.15
Let n represent the number of propositional variables in a table T with $n \in \mathbb{N}$. 

If we assume that truth assignment is an independent choice, then by the foundamental counting principle, the number of rows of T must be $2^n$.

## 1.2.16
| P | Q | ??? |
|---|---|-----| 
| F | F | T   | 
| F | T | F   |
| T | F | T   |
| T | T | T   |

Let ??? = $P \lor \neg Q$

## 1.2.17
| P | Q | ??? |
|---|---|-----|
| F | F | F   |
| F | T | T   |
| T | F | T   |
| T | T | F   |

Let ??? = $(\neg P \land Q) \lor (P \land \neg Q)$ 


## 1.2.18
### A 
If the conclusion of an argument is a tautology, then for any cases where the premises are true, the conclusion is true.  
Thus, the argument is valid.  

### B 
If the conclusion of an argument is a contradiction, then there must be a least one case of all premises being true while the conclusion is false. 
Thus, the arguement is invalid. 

### C
If one of the premises is a tautology, we cannot conclude anyhthing about the validity of an argument, though the premise is redundant. 
If one of the premises is a contradiction, it is never the case that all premsises are true. Therefore, the argument is vacously valid. 


NOT DONE YET:  
- 1.2.12 - C
- 1.2.14 