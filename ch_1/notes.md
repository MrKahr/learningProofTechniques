# NOTE: 
All definitions from Daniel Vellerman unless otherwise noted!

## Logic 
### Statement
A statement is a declarative statement that is either true or false. 

Statements may either be simple, or consist of substatements i.e. compounds and are modelled using logical/propositional formulae.

### Argument 
An argument is a collection of statements (premises) that entail the truth of some statement (conclusion).

In practice it often works like this: 

Assume we want to prove that a statement S is true (often a theorem or a lemma). 

Using helper statements called premises, we can show that statement S must follow from these assuming that these statements are true.   

### Logic notation 
Arguments are often presented in the form:
$
\\
P_1 \\
P_2 \\
(P_3, \dots, P_n) \\
--- \\
\therefore C$\
They can be read as: "by the premises $P_1, P_2, \dots P_n$, the conclucion $C$ follows.

### Mathematical deduction 
A process of deriving conclusions from premises e.g. axioms(atomic rules), definitions, previously proved lemmas(subresults), or theorems (major reslts) 

### Logical properties
- Validity: Whenever all premises are true, the conclusion must be true. - Valid, but not sound. Think syntactically valid. 

- Soundness: A conclusion is sound if it is valid and all of its premises are true in the real world. Think syntactically and semantically valid. 

- Completeness: TODO: DEFINE!

#### Example arguments
"All birds can fly, penguins are birds, therefore penguins can fly" is valid, but not sound.

"2 < 3. Therefore 3 is an integer." Invalid (and since sound is the stronger condition, unsound)

"Bob can stand. Storks can stand. Therefore Bob is a stork."(Valid, but unsound, it is never possible for bob to be a stork)


## Mathematical modelling of logic 
### Well-formedness
A formula can be well-formed if it does not violate the syntax of logical formulae. 

## Operators and notiation
### Connective symbols  
| formula(Syntax)            | Meaning(Semantics)| Natural language expression (not 1-1 correspondence!) |
| -----------                | -----------       | -----------                                           |     
| $P \lor Q$: Disjunction    | or                | Either P or Q  (inclusive)                            |      
| $P \land Q$: Conjunction   | and               | P and Q, Both P and Q                                 |
| $\neg P$: Negation         | not               | Not P                                                 |


## Truth value 
A truth assignment f is a function of statement s to a truth value $T \in {T, F}$. One formalism $f : S \rightarrow T$. 

## Equivalence 
We say that formulae $s$ and $p$ are equivalent iff they are assigned the same truth value for every combination of truth values to the . We denote this $s \equiv p$. 

## Important results

### Common logical expressions and their truth value 

### Laws 
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
These laws can be verified by creating their truth tables - This is skipped, because I have done so in a class.

### Key points
You CANNOT infer that a conclusion is true simply because its premises are (p. 19) -> always check conclusions carefully

Validity determines whether a conclusion follows from premises - i.e. whether there is even some pattern to exploit, not whether it makes sense to exploit it! - In all possible worlds.