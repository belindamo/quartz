#paper #concept-pamphlet 

# Notes

DiffPool addresses this type of representation of graphs >> allowing for *hierarchical* representations of graphs. In order words, subgraph classification. 
<!--LEARN:rsimFhaa-->

Diffpool is a module that allows for >> differentiable graph pooling to generate hierarchical graph representations and combine with various GNNs in an e2e fashion. 
<!--LEARN:QsMgz06F-->

What are some advantages of Diffpool?
?
- e2e trainable
- can be combined with different GNN architectures
- learn interpretable hierarchical structures
- computationally efficient
- permutation invariant
<!--LEARN:AO9re44t-->

In DiffPool, there are 2 separate GNNs at each layer: one for generating `____` and one for generating `____` .
?
In DiffPool, there are 2 separate GNNs at each layer: one for generating **node embeddings** and one for generating **cluster assignment matrices**.
<!--LEARN:WP0PyHs3-->



## Key terms
- graph neural networks
- Diffpool - differentiable graph pooling module that generates hierarchical representations of graphs and can be combined with various graph neural network architectures in e2e fashion

## Main contributions

- DiffPool - pooling module with hierarchical graphs
- How it works
	- soft cluster assignment for nodes at each layer of a deep GNN. map nodes to a set of clusters which becomes coarsened input for next GNN layer

## Strengths and Weaknesses of paper
- Strengths
- Weaknesses

## Questions & Discussion Items
