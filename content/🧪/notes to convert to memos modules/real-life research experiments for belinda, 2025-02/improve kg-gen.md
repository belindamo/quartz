There are also some eng things I’d like to fix up in the module….like

- clustering step could be parallelized which would make it 50x+ faster (it is quite slow now, ~20 seconds for ~20 nodes and ~10 edges)
- clustering of the KG is currently steerable with a “context” str but I think there must be a better way to do this…right now it’s not particularly accurate
- clustering could also better use the source text chunk and relation triples

Other things I’d love to play around with  

- LLM summarized descriptions of clusters
- multi-level cluster, e.g. clusters of clusters.
- clustering using different criteria and seeing how membership differs
- efficient updating of clusters as nodes / edges are updated in graph too
- Test diff clustering algos on our benchmark

TODOs
- [ ] node_labels, edge_labels, ontology
- [ ]  example_relations
- [ ]  cluster
- [ ]  aggregate

## Other things to do
- [ ]  Strict mode where only exact matches from the text are allowed as nodes or edges
- [ ]  Add multi-threading to speed up generation
- [ ]  Add verifier that checks for graph quality after generation
- [ ]  Convert output graph to PyTorch Geometric graph format
- [ ]  Track cost of generation
- [ ]  Given a messages array, specify which roles to use for node or edge generation, or both
- [ ]  Generate a recommended ontology given text