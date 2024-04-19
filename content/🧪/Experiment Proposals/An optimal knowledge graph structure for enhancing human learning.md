## Experiment Length
**Estimated Time To Build:** 3 days

## Summary
This experiment aims to identify the optimal structure for a knowledge graph that enhances human learning by being human-readable and traversable by both humans and machines. 

The focus is on designing a graph where each node and edge contains unique identifiers and helpful descriptions. 

To use this for a concrete example, we will construct a knowledge graph from educational materials such as lecture slides in PDF format, allowing users to query course-related information and trace content generation back to specific nodes. From the graph, we will be able to create section handouts in Markdown with clear citations.


## Related Work
I've previously played around with hierarchical generation of knowledge without any input text [here](https://justanexperiment.com/graph).

Researchers like Yohei on Twitter and Andrew Ng have also highlighted knowledge graphs as effective data representation to structure vast data sets in a manner that is accessible and meaningful to end-users.

- [Instagraph](https://github.com/yoheinakajima/instagraph) 
- [Mindgraph](https://twitter.com/yoheinakajima/status/1769019899245158648?t=J2NhvibXYhYKfNhyE9gEJQ)
- Andrew Ng's [Knowledge Graphs for RAG course](https://twitter.com/AndrewYNg/status/1767941813820862655)

## Plan

### Instantiate Solution: The Graph
This software tool that ingests PDFs and constructs a knowledge graph. The initial focus is on developing the architecture of the knowledge graph, avoiding progression to interface design or user testing stages.

Fields
- Node
	- `title`: unique id in natural language
	- `description`: informative description with citations
	- `citations`: array of citations
	- `edges`: array of edges
- Edge
	- `title`: one of `is a sub-concept of`, `is a super-concept of`, `is an adjacent concept of`
	- `citations`: array of citations that justify why this edge exists

### Method
1. **Input Collection:** Gather educational materials from introductory courses.
2. **Parsing and Analysis:** Utilize large language models (LLMs) to extract key concepts and relationships from the collected materials.
3. **Graph Construction:** Create nodes for identified concepts and establish edges for relationships. The edge types include 'is a sub-concept of', 'is a super-concept of', and 'is an adjacent concept of', which will facilitate the structured interconnectivity within the graph.
4. **Target Material Generation**


## Evaluation Plan

- **Dependent Variables (DV):** The accuracy of the knowledge graph in reflecting the conceptual structure of the source materials, and the quality of the target materials generated from the graph.
- **Independent Variables (IV):** The implementation of a knowledge graph structured with specific node and edge types between the source and target materials. 
- **Task:** Conversion of educational materials into the knowledge graph and subsequent content generation from the graph. 
- **Threats:** Potential risks include inaccurate extraction of concepts and variability in the quality of source materials, which could impact the reliability and usability of the knowledge graph.

## Implications

The proposed knowledge graph structure aims to improve how educational content is created with LLMs so that it is debuggable and maintains a human expert in the loop in the process of creating content. A "stack trace" can be generated from the knowledge graph to trace information back to its origins within the graph, hopefully providing a robust mechanism for ensuring the accuracy and integrity of educational materials. This structure holds promise not only in educational settings but could also be adapted for broader applications where data explainability and traceability are critical.

Also, knowledge graphs are fun and underrated in my opinion! Maybe this will spread the word of how great they are ^^ 