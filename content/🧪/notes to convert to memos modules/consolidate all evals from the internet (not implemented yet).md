
For existing evals:

1. Gather all evals on the internet (make free)

2. Convert them to input-output w/ their own Pydantic types.

3. Generate a graph using dependencies using LLMs.

4. Retrieve proper evals from it given a query + optionally some context

5. Give them to... but also, use them for new evals.

a. generate SO for eval shape

b. generate examples

6. New evals are then strongly typed, based on prior evals, & there is reasoning for why it was made the way it is, & it can get added to the graph.
