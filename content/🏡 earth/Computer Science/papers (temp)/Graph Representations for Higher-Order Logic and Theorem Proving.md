#paper #concept-pamphlet 
2019, Aditya Paliwal, Sarah Loos, Markus Rabe, Kshitij Bansal, Christian Szegedy

wait ok this is such a cool paper!!!! omgggggg 😍😍😍😍😍😍 my peopleeeee
# Notes

The key contribution of **Graph Representations for Higher-Order Logic and Theorem Proving** is >> first application of GNNs to guide higher-order theorem proving, achieving SOTA on the HOList benchmark.
<!--LEARN:VanJiakK-->

In **Graph Representations for Higher-Order Logic and Theorem Proving**, there are two embeddings used: `____` and `___ ` embeddings >> goal, premise
<!--LEARN:X2DKm9O1-->

In **Graph Representations for Higher-Order Logic and Theorem Proving**, the goal embedding by itself is used to the predict `_____` >> the next tactic to apply from a fixed set of 41 tactics.
<!--LEARN:1CVtSbQ6-->

In **Graph Representations for Higher-Order Logic and Theorem Proving**, the goal and premise embeddings are combined together in order to get >> score for the premise. Higher scores indicate the given premise is predicted to be useful for proving a current goal.
<!--LEARN:vfUZB9K0-->

## Helpful practice example

![[Screenshot 2024-11-12 at 11.18.13 AM.png]]





## Key terms


They tried...
- subexpression sharing: share all syntactically equal subexpressions
- leaf sharing: equal leaves of AST are shared
- variable blinding: replace all variable names by x
- random:  add random edges
- top down: remove all edges from nodes to their parents and only keep those to their children
- bottom up: remove all edges from nodes to their children and only keep those to their parents

They tried 41 tactics


- message-passing GNNs hehe
- abstract syntax tree (AST) - graph with directional edges, where each node has edges to its children and parent(s). edges are labeled with child index

## Main contributions
- First use of GNNs for higher-order proof search

## Strengths and Weaknesses of paper
- Strengths
- Weaknesses

## Questions & Discussion Items

- what were the limitations of using GNNs here? why isn't there more work done in this field....
- what does it mean "higher-order" in relation to theorem provers
	- higher-order logic 
		- pros: well-structured, clearly defined grammar
		- cons: still no well-established method to convert formulas into graph-based representations
- **subexpression sharing concrete example?**
- need to see a concrete example....
- **what are the tactics? concretely**
- Uh...this subexpression sharing thing didn't really do that much better than abstract syntax tree??


- how GNN is modified....
	- summing separately over parents and children during aggregation step
- tactic classifier


i like...
- the compressing of expressions. i'd like to understand how this works thoroughly


potential limitations....
- how many hops the best GNNs can do? 

observations
- more hops closes more proofs!


# very very helpful images

reduce sizeof an expression
![[Screenshot 2024-11-12 at 11.13.20 AM.png]]

![[Screenshot 2024-11-12 at 11.18.03 AM.png]]

