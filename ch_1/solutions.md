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
P = Jane will win the math prize, Q = Jane will win the chemestry prize, R = Pete will win the math prize, T = Pete will win the chemestry prize. 
To solve this problem, consider all possible combinations of true premises. IF the conclusion is ever false, while the premises are true, then it cannot a correct conclusion. 
- a) $\neg (P \land R), (P \lor R),  Q, R$
| P | Q | R | ¬(P ∧ R) | (P ∨ R) | Q | R |
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

