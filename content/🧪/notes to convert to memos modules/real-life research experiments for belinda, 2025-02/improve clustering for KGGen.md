Right now the clustering steps are
1. The entire entities list is passed in context to the LLM, and it attempts to extract a single cluster. An optional cluster-instruction string may be passed to decide how to cluster. The default instructions account for close synonyms and differences in tense and plurality. 
2. Validate the single cluster using an LLM-as-a-Judge call with a binary response. If it passes, then add the cluster and remove the cluster entities from the entities list. 3 
3. Assign a label to the cluster that most closely captures the shared meaning of entities in the cluster. 
4. Repeat steps 1–3 until n loops happen without a successful cluster extraction. 
5. Remaining entities are checked batch-by-batch, with batch size b, for whether they should be added to an existing cluster. 
6. For each new addition to a cluster, validate the cluster once more using an LLM-as-a-Judge call with a binary response. 
7. Repeat steps 5–6 until there are no remaining entities to check

I want to change this so that this can be done without a prerequisite being that the entire entities/edges list can be passed in context. It shouldn't need to do that