#concept 

langgraph >> a library for building stateful, multi-actor applications with LLMs [1]

compiled graph is turned into >> series of runnables
<!--SR:!2024-08-29,1,230-->

graphState in LangGraph >> how updates from each node gets merged into graph state. Uses reducers.
<!--SR:!2024-09-01,4,270-->

the `agent` node in the Langgraph tutorial is >>  a function that calls model. decides which actions to take based on response. note it can really have any name
<!--SR:!2024-09-01,4,270-->

the `tool` node in Langgraph tutorial is >> a function that is executed with specified structured output as parameter
<!--SR:!2024-09-01,4,270-->
### References
1. https://langchain-ai.github.io/langgraphjs/

### Notes

