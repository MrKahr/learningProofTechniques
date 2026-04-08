# NOTE: 
All definitions from Daniel Vellerman unless otherwise noted!
Note also, terminology in logic can be very confusing because there are so many different levels of formality. 

## Logic 
### Proposition
A proposition is a declarative senetence that is either true or false. 

Propositions may either be atomic (also known as simple), or molecular (also know as compound) (be built from subpropositions using logical connectives).

In formal logic, we represent propositions using logical formulae i.e. the syntax. 

### Argument 
An argument is a collection of propositions called premises, that entail the truth of some proposition called the conclusion.

An argument is valid iff the truth of the premises entails the truth of the conclusion. 

In practice, we show that the truth of a proposition S (often a theorem or a lemma), is follows from a series of premeses $P_1, \dots, P_n$. 

### Logic notation 
Arguments are often presented in the form:
$
\\
P_1 \\
P_2 \\
(P_3, \dots, P_n) \\
--- \\
\therefore C$\
This is read as: "by the premises $P_1, P_2, \dots P_n$, the conclusion $C$ follows.

Using formal notation, we can write $P_1, \dots, P_n \vdash C$. (Derivable in the current system we are working with, dont confuse this with semantic entailment!) 

### Mathematical deduction 
A process of deriving conclusions from premises which may incldue axioms(atomic rules), definitions, previously proved lemmas(subresults), or theorems (major reslts) 

### Logical properties
- Validity: Whenever all premises are true, the conclusion must be true. - Valid, but not sound. Think syntactically valid. 

- Soundness: A conclusion is sound iff it is valid and all of its premises are true in the real world. Think syntactically and semantically valid. 

- Completeness: TODO: DEFINE!

#### Example arguments
"All birds can fly, penguins are birds, therefore penguins can fly" is valid, but not sound.

"2 < 3. Therefore 3 is an integer." Invalid (and since sound is the stronger condition, unsound)

"Bob can stand. Storks can stand. Therefore Bob is a stork."(Valid, but unsound, it is never possible for bob to be a stork)

### Propositonal logic/zeroth order
Formal system to reason about propositions using logical connectives ($\lor, \land, \neg, \leftrightarrow \rightarrow$). $n > 2$ is an example of a claim that is NOT a propositon.

### Predicate logic/first order logic 
Formal system to reason about propositions, and members of a domain using both logical connectives, and quantifiers.

### Second order logic 
Formal system to reason about propositions, members of a domain, as well as sets, relations, or functions.  

### Third order logic 
Formal system to reason about propostions, members of a domain, sets, relations, functions AND sets of sets, or relations of relations. 

### Higher-order logic
Formal system to reason about the nth layer of abstraction e.g. sets of sets of sets of sets $\dots$. 

## Mathematical modelling of logic 

### Propositonal variables 
A variable S that is assigned either true or false.

### Truth assignment
A truth assignment for a set $S$ of propositional variables is a function $f: S -> \{T,F\}$ (https://www.ucl.ac.uk/~ucahmto/0005_2021/Ch1.S3.html) - One representation of S could be S = {Q, R}

### Logical formula
An mathematical expression used to represent a proposition. 

### Well-formedness
A formula can be well-formed if it does not violate the syntax of propositional formulae.

### Logical connectives (0'th order logic)
| formula(Syntax)            | Meaning(Semantics)| Natural language expression (not 1-1 correspondence!) |
| -----------                | -----------       | -----------                                           |     
| $P \lor Q$: Disjunction    | or                | Either P or Q  (inclusive)                            |      
| $P \land Q$: Conjunction   | and               | P and Q, Both P and Q                                 |
| $\neg P$: Negation         | not               | Not P                                                 |
| $P \implies Q$             | implies           | If P then Q                                           |
| $P \doublearrow Q$         |                   | P iff Q                                               |


## Truth value 
A truth assignment f is a function of statement s to a truth value $T \in {T, F}$. One formalism $f : S \rightarrow T$. 

## Equivalence 
We say that formulae $s$ and $p$ are equivalent iff they are assigned the same truth value for every combination of truth assignment to their atmoic variables. We denote this $s \equiv p$. 

## Truth table 
A truth table is a representation of the boolean assignment function $f$, for some logical formula. It depicts all combinations of assignments to atomic propostional variables and the corresponding truth value assigned to compound formulae as a result of this assignment.  

## Important results and properties
### Propositional logic law (0'th order)
$
\\
\neg (P \land Q) \equiv \neg P \lor \neg Q (DeMorgan)\\
\neg (P \lor V) \equiv \neg P \land \neg Q (DeMorgan)\\
P \land Q \equiv Q \land P(Commutativity) - Swapping position of operands is allowed \\
P \lor Q \equiv Q \lor P(Commutativity) \\
P \land (Q \land R) \equiv (P \land Q) \land R (Associativity) - Grouping same operands differently is allowed = parenthesis is redundant\\
P \lor (Q \lor R) \equiv (P \lor Q) \lor R (Associativity)\\
P \land P \equiv P (Idempotency) - Performing the same operation multiple times yields the same result\\
P \lor P \equiv P (Idempotency)\\
P \land (Q \lor R) \equiv (P \land Q) \lor (P \land R)(Distributivity)\\
P \lor (Q \and R) \equiv (P \lor Q) \land (P \lor R)\\
P \lor (P \land Q) \equiv P(Absorption)\\
P \land (P \lor Q) \equiv P\\
\neg \neg P \equiv P (Double negation)\\
P \land tautology \equiv P, P \lor tautology \equiv tautology, \neg (tautology) \equiv contradiction (tautology laws)\\
P \land contradiction \equiv contradiction, P \lor contradiction \euqiv P, \neg(contradiction) \equiv tautology (contradiction laws)
$ 

These laws can be verified by using truth tables - skipped for laws completed previously.
| P | Q | R | $P \land (Q \lor R)$ |  $(P \land Q) \lor (P \land R)$ | 
| F | F | T | F                    | F                               |
| F | T | F | F                    | F                               |
| F | T | T | F                    | F                               |
| T | F | F | F                    | F                               |
| T | F | T | T                    | T                               |
| T | T | F | T                    | T                               |
| T | T | T | T                    | T                               |

### Variable 
A variable is a symbolic represention of a number and can be used in predicates e.g. P(x) or D(x,y). Statements that contain variables can be combined using logical connectives e.g. $D(x,y) \lor D(x,z)$. 

### Free and bound variables
Free variables are objects that a statement says something about and can change the truth value of a statement depending on choice of variable. Bound or dummy variables help express an idea about a set and should not be thought of as any particular object. Bound variables can always be replaced without changing the meaning of a statement. 

## Set theory 
### A set 
A set is a collection of objects. Each of these objects is refered to as an element of the set.
It is either the case that an element belongs to a set $\in$ or  it does not $\notin$ which is determined by some elementhood test e.g. x is a prime. 

### Set builder notation 
A set is often represented using set builder notation in the form $A = \{x | x is a prime\}$. 
This notation is read: "The set A consists of elements such that these elements are prime numbers", where the latter statement is the elementhood test. s

### The truth set of a statement
The truth set of statement P(x) is the set of all values of x that make the predicate P(x) true. In set builder notation this would be $T = \{x | P(x)\}$

### Universe 
The set of all possible values for variables. This is refered to as the universe of discourse and sometimes not explicitly defined. 
Some common universes include $\mathbb{R}, \mathbb{Q}$

### Truth sets and universe of discourse 
If you have a tautological statement using predicates, then for the truth set T, $T = U$ with U being the universe of discourse. 

### Operations on sets
Note that the statements in each definition are elementhood tests.
#### Set intersection 
The intersection of sets A and B is defined as: 
$A \cap B = \{x | x \in A \text{and} x \in B\}$ 
"The set of elements which are elements of both A and B"

#### Set Union 
The union of sets A and B is defined as: 
$A \cup B = \{x | x \in A \text{or} x \in B\}$ 
"The set of elements which are elements A or B"

#### Set difference 
The difference of sets A and B are defined as:
$A \\ B = \{x | x \in A \text{and} x \notin B\}$
"The set of elements which are elements of A but not of B"

#### Symmetric set difference 
The symmetric difference of sets A and B are defined as: 
$A \Delta B = (A \cup B) \\ (A \cup B) = \{x | x \in A \text{xor} x \in B\}$
"The set of elements which are elements of either A or B but not both

#### Geometric/visual representation of sets
Sets are often visualized using a venn diagram. 
A venn digram is rectangle with an arbitrary number of circles in its interior. 
The rectangle represents the universe of discourse. 
Each circle's interior represents the members of a set. 
In the case the circles intersect, then the area of each intersection represents a set whose elements are elements of each intersecting circle. 
[BILLED MANGLER]

#### Corespondence between different forms 
Let A and B be truth sets of predicates $P(x), R(x)$ then by defition 
$T = A \cup B = x \in P(x) \land x \in R(x) = \{x | x \in P(x) \land x \in R(x)\}$
This definition illustrates that there is a correspondence between set operators and logical connectives, meaning we can choose either type of expression to work with. 
We note that logical connectives should NEVER be used to perform operations on sets. 
$\cup$ is NOT $\land$. 
One use to show the equivalence of statements such as $x \in A \cap (B \cup C) \equiv x \in (A \cap B) \cup (A \cap C)$

### Subset
Suppose A and B are sets. We say that A is a subset of B if every element of A is also an element of B. We denote this as $A \subseteq B$

### Disjointedness 
Suppose that A and B are sets. We say that A and B are disjoint if they share no elements. 

### Key points
You CANNOT infer that a conclusion is true simply because its premises are (p. 19) -> always check conclusions carefully

Validity determines whether a conclusion follows from premises - i.e. whether there is even some pattern to exploit, not whether it makes sense to exploit it! - In all possible worlds.

There are two kinds of variables, one numeric (e.g. x) and one boolean (e.g. S,Q). 

