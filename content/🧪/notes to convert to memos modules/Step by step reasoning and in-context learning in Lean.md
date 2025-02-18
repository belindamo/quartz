
title: How can we create subfield-specific step-by-step reasoning datasets from Lean theorem proofs to encourage “intuition” from LLMs?

problem: Current automated theorem provers lack fine-grained control of LLM’s “intuitive” reasoning that may make unexpected leaps in reasoning

bit: Lean has formal proofs but doesn't expose intermediate reasoning steps. RAG systems like ReProver extract from adjacent files and imports for a given theorem.

flip:  Use theorem graph neighborhood for in-context learning

solution: 

- Extract and structure step-by-step reasoning from Lean mathlib theorems. Identify non-obvious but useful intermediate lemmas
    
- These are classified based on subfields (e.g. set theory). 
    
- Make datasets based on subfields and compress these into DsPy prompt to combine with ReProver retrieved data for in-context learning. 
    
- Apply DsPy prompt to different subfields
    
- (maybe) use LLMs with different prompts/examples 
    

  

other ideas

- Could also try training a NN based on that data
    
- Train a better version of ReProver
    
- Diff combinations of subfield data
    

  

key insight

- DsPy only needs 50-100 examples to work properly
    

**