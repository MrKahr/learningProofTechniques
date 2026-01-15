# NOTE: 
All definitions from Daniel Vellerman unless otherwise noted!
Note also, terminology in logic can be very confusing because there are so many different levels of formality. 

## Logic 
### Proposition
A proposition is a declarative senetence that is either true or false. 

Propositions may either be atomic (simple), or compound (be built from subpropositions using logical connectives).

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
Formal system to reason about propositions using logical connectives ($\lor, \land, \neg, \doublearrow \arrow$). $n > 2$ is an example of a claim that is NOT a propositon.

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
A truth assignment for a set $S$ of propositions variables is a function $f: S -> \{T,F\\}$(https://www.ucl.ac.uk/~ucahmto/0005_2021/Ch1.S3.html)

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
We say that formulae $s$ and $p$ are equivalent iff they are assigned the same truth value for every combination of truth values to the . We denote this $s \equiv p$. 

## Truth table 
A tabl

## Important results
### Propositional logic law (0'th order)
$
\\
\neg (P \land Q) \equiv \neg P \lor \neg Q (DeMorgan)\\
\neg (P \lor V) \equiv \neg P \land \neg Q (DeMorgan)\\
P \land Q \equiv Q \land P(Commutativity) - Swapping position of operands is allowed \\
P \lor Q \equiv Q \lor P(Commutativity) \\
P \land (Q \land R) \equiv (P \land Q) \land R (Associativity) - Grouping operands differently is allowed, parenthesis is redundant, (but occasionally helpful!)\\
P \lor (Q \lor R) \equiv (P \lor Q) \lor R (Associativity)\\
P \land P \equiv P (Idempotency) - Performing the same operation multiple times yields the same result\\
P \lor P \equiv P (Idempotency)\\
\neg \neg P \equiv P (Double negation)
$ 

These laws can be verified by using truth tables - skipped because completed previously. 

### Key points
You CANNOT infer that a conclusion is true simply because its premises are (p. 19) -> always check conclusions carefully

Validity determines whether a conclusion follows from premises - i.e. whether there is even some pattern to exploit, not whether it makes sense to exploit it! - In all possible worlds.

