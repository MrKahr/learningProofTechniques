# Important reflections 

## Natural language is really hard to unambgiously map to logical statements 
- [See the use of both, neither, nor etc](/ch_1/solutions.md#1.1.4)

## A compiler for logical languages will have to include 
- NOTE: You are moving in the direction of formal verification, proof systems - know that logic languages very well exist, and you should build your own
- For some intro see https://www.usenix.org/legacy/publications/library/proceedings/dsl97/full_papers/klarlund/klarlund.pdf 
- A syntax checker - maybe static analysis of well-formedness? 
- A small set of appropriate types (maybe (logic) variable, state?)
- An AST 

## The following logical properties are very important in computer science
- Validity
- Soundness

## Logic insights
- There are many different kinds of logics that are supersets of each other - it works similarly to problem classes in comp. sci. e.g. NP, NP-hard, NP-complete etc.

## Proof insigts 
### Biimplication 
- It is sometimes much harder to prove a proposition in one direction than in another. Try the other direction if the first direction seems too hard.