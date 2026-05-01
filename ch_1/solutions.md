# Exercises

## Quick notes on terminology 
In Vellerman's terminology, property = law e.g. associative property

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
| T  | F | F | T | T           | T          | F                 | T              |
| T  | F | T | F | T           | T          | T                 | T              | 
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
| P | Q | $Q \lor \neg P$ | $\neg (P \land (Q \lor \neg P))$ | 
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
| P | Q | $(P \| Q)$ (nand) |
|---|---|------------------|
| F | F | T                |
| F | T | T                |
| T | F | T                |
| T | T | F                |

### B 
| P | Q | $(P\|Q)$| $\neg (P \land Q)$|
|---|---|--------|-------------------|
| F | F | T      | T                 |
| F | T | T      | T                 |
| T | F | T      | T                 |
| T | T | F      | F                 |

### C
| P | Q | $\neg P$ | $(P \| P)$ | $P \lor Q$ | $(P \| P) \| (Q \| Q)$ | $P \land Q$ | $(P \| Q) \| (P \| Q)$ |
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
(P \land R) \lor [((\neg R \land P) \lor (\neg R \land Q))] (\text{Distributive law})\\
(P \land R) \lor [(P \land \neg R) \lor (Q \land \neg R)] (\text{Commutative law}) \\
[(P \land R) \lor (P \land \neg R)] \lor (Q \land \neg R) (\text{Associative law})\\
[P \land (R \lor \neg R)] \lor (Q \land \neg R) (\text{Distributive law})\\
[P] \lor (Q \land \neg R) (\text{Tautology laws})
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
\equiv \neg \neg (\neg P \land \neg Q) (\text{DeMorgan's first law})\\
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

Since $\neg\neg P \equiv P, \neg\neg Q \equiv Q$ 

Then 

$
\neg (P \lor Q) \equiv \neg (\neg \neg P \lor \neg \neg Q) (\text{double negation law applied to P and Q})
$
We let $T = \neg P$, and $R = \neg Q$, then 
$
\equiv \neg \neg (T \land R) (\text{DeMorgan's first law})\\
\equiv (T \land R) (\text{double negation law})\\
$
We substitute T and R to obtain 
$
\equiv (\neg P \land \neg Q) (\text{Substitution})\\
$
Therefore 
$
\neg (P \lor Q) \equiv (\neg P \land \neg Q) 
$
This is DeMorgan's second law. 

Hence De Morgan's second law is derivable using De Morgan's first law and the law of double negation. 

## 1.2.14
The goal of this exercise is to show that $[P \land (Q \land R)] \land S \equiv (P \land Q) \land (R \land Q)$ using only associative laws. 

### Preliminaries
We first define associative laws. 

**Associative laws** 
For propositions, P,Q, 
$
\\
P \land (Q \land R) \equiv (P \land Q) \land R\\
P \lor (Q \lor R) \equiv (P \lor Q) \lor R
$


### Derivation 
Using the associative laws we present the proposed derivation. (in case your reader tends to forget!) 

Let P,Q,R,S be propositions. 

Then 
$
\\
[P \land (Q \land R)] \land S \equiv [(P \land Q) \land R] \land S (\text{Associative law})\\
\equiv (P \land R) \land (R \land S) (\text{Associative law})
$

Therefore, we can conclude that $[P \land (Q \land R)] \land S \equiv (P \land Q) \land (R \land Q)$. 

## 1.2.15
Let n represent the number of propositional variables in a table T with $n \in \mathbb{N}$. 

If we assume that truth assignment is an independent choice, then by the fundamental counting principle, the number of rows of T must be $2^n$.

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

## 1.3.1
- a) $D(6,3) \land D(9,3) \land D(15,3)$ 
- b) $D(x,2) \land D(x,3) \land \neg D(x,4)$
- c)$N(x) \land N(y) \land [(P(x) \land \neg P(y)) \lor (\neg P(x) \land P(y))]$ - could also use xor operator 
## 1.3.2
- a) $M(x) \land M(y) \land (T(x,y) \lor T(y,x))$ 
- b) $(B(x) \lor B(y)) \land (R(x) \lor R(y))$
- c) $(B(x) \land R(x)) \lor (B(y) \lor R(y))$
## 1.3.3
- a) $\{x | x is a planet in our solarsystem\}$
- b) $\{x | x is an ivy league uni\}$
- c) $\{x | x is a US state\}$
- d) $\{x | x is a province in Canada\}$
## 1.3.4
- a) $\{x | x \in Z^{+} \land y^2 = x\}$
- b) $\{x | x = 2^y where y \in Z^+\}$
- c) $\{x | x \in Z \land x > 9 \land x < 20\}$
## 1.3.5
- a) $3 \in R \land 13 -2(3) > 1$ - true -  Bound variables: x 
- b) $4 \in R^- \land 13 -2(4) > 1$ - false(first term of conjunction falses) - Bound variables: x
- c) $5 \notin R \land 13 - 2(5) > c$ - false(first term of conjunction false)-  Bound variables: x, free variables: c
## 1.3.6
- a) $(w \in R)\land (13 - 2w > c)$ - bound: x
- b) $(4 \in \mathbb{R} \land 13 - 2(4) \in P) = (4 \in \mathbb{R} \land 13 - 2(4) \text{is a prime})$ where $P = \{y | y \text{is a prime}\}$ bound: x,y
- c) $(4 \text{is a prime} \land 13 - 2(4) > 1)$ bound: x,y - first bound to x then to y
## 1.3.7
- a) $\{0.5, -1\}$
- b) $\{0.5\}$
- c) $\{-1\}$
- d) $\emptyset$
## 1.3.8
- a) $A = \{x | x is a former or current spouse of Elizabeth Taylor \} = \{\text{No idea}\}$
- b) $A = \{x | x is a logical connective \} = \{\neg, \lor, \land\}$
- c) $A = \{x | x is the author of this book\} = \{Daniel Vellerman\}$
## 1.3.9
- a) $A = \{ x \in R |  x^2 -4x + 3 = 0\} = \{1, 3\}$
- b) $A = \{ x \in R | x^2 -2x + 3 = 0\} = \emptyset$
- c) $A = \{x \in R | 5 \in R \land x^2 + 25 < 50\} = \{x \in R | -5 < x < 5\}$
## 1.4.a (theorem)
Direct proof that for any sets A and B, $(A \cup B) \\ B \subseteq A$
0) Obtaning intuition

For intuition, we can draw venn diagrams that represent 3 cases. One for each type of intersection of sets A and B. 

One where A and B are disjoint, one were A = B and one where A and B are not disjoint but also where $A \neq B$. When we do this, we realise that $(A \cup B) \\ B \subseteq A = A$ must be a false statement.  

1) Preliminaries

If $(A \cup B) \\ B$ is a subset of A, then by definition of subsets, every element of $(A \cup B) \\ B$ must be an element of A. We therefore show that $x \in (A \cup B) \\ B \rightarrow x \in A$

2) Direct proof 
Let $x \in (A \cup B) \\ B \rightarrow A$

By the semantics of set operations, we know obtain the following premises:

- $x \in A \lor x \in B$

- $(x \notin B)$

We realize these are statements of the form

Premises 

- $P\lor R$

- $\neg R$

Conclusion 

- $P$

We know that this is a correct conclusion based on section 1.1 p. 9. However, we still show that this is a valid argument by truth table
P | R | $P\lor R$ | $\neg R$ | P  |
--|---|-----------|----------|----| 
F | F |F          | T        | F  | 
F | T |T          | F        | F  |
T | F |T          | T        | T  |
T | T |T          | F        | T  |

## 1.4.1

$A \cap B = \{3,12\} = P$

$(A \cup B) \ C = \{1,12,20,35\} = R$

$A \cup (B \ C) = \{1,3,12,20,35\} = Q$

Disjoint sets: NA 

Subsets: $P \subseteq Q$, $R \subseteq Q$

## 1.4.2
$A \cup B = \{us,g,c,a,f,i,b\}$

$(A \cap B) \ C = \emptyset$

$(B \cap C) \ A = \{f\}$

## 1.4.3
Verified using Venn diagrams

### 1.4.4
Verificed using Venn diagrams 

### 1.4.5
#### a
We show by direct proof that $A \\ (A \cap B) = A \ B$

Let A,B be sets and let $x \in A \\ (A \cap B)$

Then 

Direction $\rightarrow$
$
x \in (A \\ (A \cap B))  

\equiv x \in A \land \neg(x \in A \land x \in B)

\equiv x \in A \land (x \notin A \lor x \notin B) \text{DeMorgans First law appplied}

\equiv (x \in A \land x \notin A) \lor (x \in A \land x \notin B)\text{Distributive law applied}

\equiv x \in A \land x \notin B \text{Since:}x \in A \land x \notin A \text{is false}

\equiv x \in A \\ B \text{By definition of set difference}
$

Direction $\leftarrow$
Note: I've tried simplifying this direction instead of repeating the operations in the first proof in reverse
$
x \in A \\ B 
\equiv x \in A \land x \not B 
$

Therefore 
$
x \notin A \cup B \text{Definition of intersection}
$
And 
$
x \in A \\ A \cup B
$

Hence
$A \\ (A \cap B) = A \ B$

#### b
We show by direct proof that $A \cup (B \cap C) =  (A \cup B) \cap (A \cup C)$

Let A,B,C be sets and let $x \in A \cup (B \cap C)$

Then 

Direction $\rightarrow$ 

$
x \in A \cup (B \cap C) 

\equiv x \in A \lor (x \in B \land x \in C) \text{Apply definition of set intersection and union}

\equiv (x \in A \lor x \in B) \land (x \in A \lor x \in C) \text{Distributive property of disjunctions}

\equiv x \in (A \cup B) \land x \in (A \cup C) \text{Apply definition of set union}

\equiv x \in (A \cup B) \cap (A \cup C) \text{Apply definition of set intersection}
$

Therefore 

$
A \cup (B \cap C) \subseteq (A \cup B) \cap (A \cup C)
$

Direction $\leftarrow$ 

$
x \in (A \cup B) \cap (A \cup C)

\equiv (x \in A \lor x \in B) \land (x \in A \lor x \in C) \text{By definition of set intersection and union} 

\equiv x \in A \lor (x \in B \land x \in C) \text{By distributive property of disjunctions}

\equiv x \in (A \cup (B \cap C)) \text{By definition of set intersection and union}
$

Therefore
$
(A \cup B) \cap (A \cup C) \subseteq A \cup (B \cap C)
$

We can conclude that $A \cup (B \cap C) =  (A \cup B) \cap (A \cup C)$

### 1.4.6
Verified using Venn diagrams 

### 1.4.7
The remaining derivations will be sketched, not prettied. 
A) 
direction $\rightarrow$
$
x \in (A \cup B) \\ C 

\equiv (x \in A \lor x \in B) \land x \notin C \text{Definition of set union and difference}

\equiv (x in A \land x \notin C) \lor (x \in B \land x \notin C)\text{By distributive property}

\equiv x \in (A \\ C) \cup (B \\ C) \text{By definition of set union and difference}
$
We can conclude that $(A \cup B) \\ C \subseteq (A \\ C) \cup (B \\ C)$

direction $\leftarrow$
Similar derivations can be used to show that $(A \\ C) \cup (B \\ C) \subseteq (A \cup B) \\ C$

Thus, $(A \cup B) \\ C = (A \\ C) \cup (B \\ C)$

B) 
$A \cup (B \\ C) = (A \cup B) \\ (C \\ A)$
direction $\rightarrow$

$
x \in A \cup (B \\ C)

\equiv x \in A \lor (x \in B \land x \notin C) \text{Definition of set union and difference}

\equiv (x \in A \lor x \in B) \land (x \in A \lor x \notin C) \text{By distributive property of disjunctions}

\equiv (x \in A \lor x \in B) \land \neg(x \notin A \land x \in C) \text{By DeMorgan's first law}

\equiv (x \in A \lor x \in B) \land \neg(x \in C \\ A) \text{By definition of set difference}

\equiv (x \in A \cup B) \land \neg(x \in C \\ A) \text{By definition of set union}

\equiv x \in (A \cup B) \\ (C \\ A) \text{By definition of set difference}
$
We can conclude that $A \cup (B \\ C) \subseteq (A \cup B) \\ (C \\ A)$
direction $\leftarrow$
is similar to the previous direction

### 1.4.8
A)
Sketch of direct proof that $(A \\ B) \cap C = (A \cap C) \\ B 
Let A,B,C be sets and let $x \in (A \\ B) \cap C$

Then
direction $\rightarrow$
$
x \in (A \\ B) \cap C 

\equiv x \in (A \\ B) \land x \in C \text{Definition of set intersection}

\equiv (x \in A \land x \notin B) \land x \in C \text{Definition of set difference}

\equiv (x \in A \land x \in C) \land x \notin B \text{By associative and commutative properties of conjunctions}

\equiv (x \in A \cap C) \\ B \text{By definition of set intersection and difference}
$

Therefore 
$
(A \\ B) \cap C \subseteq (A \cap C) \\ B
$
direction $\leftarrow$
is similar to the previous direction; we can conclude that $(A \\ B) \cap C = (A \cap C) \\ B$

B) 
Sketch of direct proof that $(A \cap B) \B = \emptyset$

Let A,B be sets and let $x \in (A \cap B) \\ B$

$
x \in (A \cap B) \\ B

\equiv (x \in A \land B) \land x \notin B \text{Intersection + Diff}

\equiv x \in A \land (x \in B \land x \notin B)\text{Contradiction, + Associasitivity}
$

Since $x \in B \land x \notin B$ is a contradiction, $(A \cap B) \\ B = \emptyset

C) 
Direction $\rightarrow$

$
x \in A \\ (A \\ B)

\equiv x \in A \land \neg (x \in A \land x \notin B)

\equiv x \in A \land (x \notin A \lor x \in B)

\equiv (x \in A \land \notin A) \lor (x \in A \land x \in B)

\equiv (x \in A \land x \in B)

\equiv x \in A \cap B
$

Therefore $A \\ (A \\ B) \subseteq A \cap B

Other implication proved similarly

### 1.4.9
a) $(x \in A \land x \notin B) \land x \notin C$

b) 
$
x \in A \land \neg (x \in B \land x \notin C)

\equiv x \in A \land (x \notin B \lor x \in C) \text{DeMorgan}

\equiv (x \in A \land x \notin B) \lor (x \in A \land x \in C) \text{Distributive law}
$

c) 
$
(x \in A \land x \notin B) \lor (x \in A \land x \in C)
$

d) - Suspected we can simplify, since no equivalence found?
$
(x \in A \land x \notin B) \and (x \in A \land x \notin C)

\equiv (x \in A \land x \notin B \and x \in A) \land x \notin C \text{Associative law}

\equiv (x \in A \land x \in A \land x \notin B) \land x \notin C \text{Commutative law}

\equiv (x \in A \land x \notin B) \land x \notin C \text{Identity law}


$

e)
$
x \in A \land \neg(x \in B \lor x \in C)

\equiv x \in A \land (x \notin B \land x \notin C) \text{DeMorgan}

\equiv (x \in A \land x \in B) \land x \notin C \text{Associative law}
$

Conclusion: 
$
a \equiv \equiv d \equiv e

b \equiv c
$

### 1.4.10
a) This exercises shows how dangerous it is to assume that a biimplication is true based on an implication
$
A = \{1,2\}

B = \{2,3\}

(A \cup B) \\ B = \{1\}
$

b)
We show by direct proof that $(A \cup B) \\ B = A \\ B$
Let A,B be sets, and let:

Implication $\rightarrow$
$
x \in (A \cup B) \\ B 

\equiv (x \in A \lor x \in B) \land x \notin B \text{Union and difference}

\equiv (x \in A \land x \notin B) \lor (x \in B \land x \notin B) \text{Distributive property of disjunctions}

\equiv x \in A \land x \notin B \text{Since $x \in B \land x \notin B$ is a contradiction}

\equiv x \in A \\ B \text{By definition of set difference}
$

Implication $\leftarrow$
$
x \in A \\ B

\equiv x \in A \land x \notin B \text{Definition of set difference}

\equiv (x \in A \land x \notin B) \lor (x \in B \land x \notin B) \text{Distributive property of disjunctions}

\equiv (x \in A \lor x \in B) \land x \notin B \text{Distributive property of disjunctions}

\equiv x \in (A \cup B) \\ B \text{Definition of set union and difference}
$

### 1.4.11
a) If A and B are disjoint sets, then all possible critieria are fulfilled.
b) A counterexample where sets A, B are not disjoint. 
$
A = \{1,2\}, B = \{2,3\}

(A \\ B) \\ B = \{1\}, \text{This is not set A}

A \\ B = \{1\}, A \cup B = {1,2,3} \text{These three sets are not the same}
$

### 1.4.12
a) There is no region in the figure corresponding to $(A \cap D) \ (B \cup C)$. 
Removing $B \cup C$ from the diagram removes all elements from $A \cap D$

b) Yes, drawn on paper (drawn A,B and C as intersecting circles. Draw D as intersecting all sets and the intersections, but leave some room in each intersection, and be sure to give D a little room to represent non-overlapping elements)

### 1.4.13
a) By drawing the venn diagram for A,B,C, then you realize that $(A \cup B) \\ C \subseteq A \land (B \\ C)$

b)$ A = \{1,2\}, B = \{2,3\}, C = \{1,3\}$

### 1.4.14
Drawn on paper. Note that $A \Delta B = (A \\ B) \cup (B \\ A)$

### 1.4.15 - Done by Venn diagram
Verified on paper

### 1.4.16 - Done by Venn diagram
Verified on paper

### 1.4.17 - Verified by Venn Diagram
a) $C \\ B$
b) $(A \\ B) \\ C$ - TODO: did not agree with solution of others, must check again
c) $A \cup B$

### 1.5.1 
a) $(S \lor \neg E) \rightarrow \neg H$
b) $(H \land F) \rightarrow D$
c) $(F \rightarrow D) \land (H \rightarrow D)$
d) $Q(x) \rightarrow (Prime(x) \rightarrow Odd(x))$

### 1.5.2 
a) $H \rightarrow (A \land P)$
b) $M \rightarrow (C \land D)$
c) $\neg S \rightarrow D$
d) $(D(x,4) \lor D(x,6) \rightarrow \neg P(x))$ where x is the predicate "x is a prime"

### 1.5.3
a) $R \rightarrow (W \land \neg S)$
b) $$

### 1.5.4
### 1.5.5
### 1.5.6
### 1.5.7
### 1.5.8
### 1.5.9
### 1.5.10
### 1.5.11
### 1.5.12