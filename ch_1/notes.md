## Definitions (as precisely as I can!)

### Statement
A statement is a declarative statement that is either true or false. 

### Mathematical deduction 
A process of deriving conclusions from premises e.g. axioms(atomic rules), definitions, previously proved lemmas(subresults), or theorems (major reslts) 

### Argument 
Assume we want to prove that a statement S is true (often a theorem or a lemma). 

Using helper statements P,Q,R,$\dots$, we can show that S must follow from P,Q,R,$\dots$ assuming that these statements are true.   

### Well-formedness
A statment can be well-formed if it does not violate the syntax of mathematical statements.

## Operators and notiation
### Connective symbols  
| Symbol(Syntax)            | Meaning(Semantics)| Natural language expression (not 1-1 correspondence!) | Mathematical  
| -----------               | -----------       | -----------   
| $P \lor Q$: Disjunction   | or                | Either P or Q
| $P \land Q$: Conjunction  | and               | P and Q, Both P and Q
| $\neg P$: Negation        | not               | Not P 

## Logical properties
Validity: Whenever all premises are true, the conclusion must be true. - Valid, but not sound. Think syntactically valid. 
Soundness: A conclusion is sound if it is valid and all of its premises are true in the real world. Think syntactically and semantically valid. 
Completeness: TODO: DEFINE!

"All birds can fly, penguins are birds, therefore penguins can fly" is valid, but not sound.\\
"2 < 3. Therefore 3 is an integer." Invalid (and since sound is the stronger condition, unsound)\\
"Bob can stand. Storks can stand. Therefore Bob is a stork."(Valid, but unsound, it is never possible for bob to be a stork)\\ 
