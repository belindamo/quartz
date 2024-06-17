---
date: 2024-04-16
notes: "todo: methods section"
draft: "true"
---
## Experiment Length
**Estimated Time To Build:** ? does anyone really know

# Summary

Current top-ranked solutions for the MiniF2F benchmarks rely on some combination of a fine-tuned transformer with light layers of symbolic checks and/or system-2 prompt-based reasoning.  

In this project, I suggest a system that self-builds its long term memory and short term caches based on existing theorem-proving libraries such as those in Lean, Isabelle, and Metamath. This includes (1) self-discovery of a multi-level library of symbolic checks and prompt-based reasoning, (2) long-context retrieval of library components, and (3) synthetic evals to ensure reliability. 

We'll evaluate the system’s ability for informal-to-informal theorem-proving. Since GPT-4 and other similar LLMs have been released, theorem-proving systems have improved a lot on mathematics benchmarks like MATH and MiniF2F. We plan to benchmark against MiniF2F for the formal-to-formal parts of the system, and against IMO official datasets with human reviewers for the end-to-end informal parts.  

Logistically, there is an outstanding challenge called the [AIMO Prize](https://aimoprize.com/) that provides a nice goalpost to aim for. You win the prize if you create an open source model that can win a gold medal in International Math Olympiad, given 8 A-100s for inference over the time period of the traditional human competition.

If this works, this project will demonstrate that a generated IO-based system is an effective way of augmenting a black-box LLM, and that hopefully such a system reaches the performance of an human IMO Gold competitor! 

# Related Work
Here are clusters of research papers that inspire this project:  
- Automated theorem-provers  
	- Draft, Sketch, Prove (2023)  
	- LeanDojo: Theorem Proving with Retrieval-Augmented Language Models (2023)  
	- Auto-formalization of Large Language Models (2022)  
	- Generative Language Modeling for Automated Theorem Proving (2020)  
- Mathematics benchmarks and datasets  
	- LeanDojo (2023)  
	- MiniF2F (2022)  
	- MATH (2021)  
- Growing, interpretable knowledge base  
	- Simulation Intelligence (2022)  
	- Dreamcoder (2020)  
- Reasoning improvements via prompting and black-box  
	- Self-Discover (2024)  
	- GPT-4 with Wolfram Alpha on math problems (2023) 
- Relevant Open Source Language Models  
	- Llemma (2023)  
	- Llama (2023)  
	- lean-gptf (2021)  

# Risks
There are a number of risks. Here are some:  
- Short Timeline: Deadline for AIMO Prize 2024 seems to be around early June 2024. 
- Big jump needed in success rate for AIMO: SoTA Informal-to-formal and Formal-to-formal are at about a 40% success rate, based on Draft, Sketch, Prove (2023). Seems like gold medalists in IMO for informal-to-informal got about 76-100% of questions correct in 2023. This means this proposed solution needs to be nearly twice as good as current benchmark performance.
- Informal-to-informal problems are hard to evaluate: there are theoretically infinite ways to write one proof. Evaluation probably involves finding and collaborating with former IMO competitors since math hard.
- AIMO Prize applies additional compute constraints, on top of a problem that hasn't been solved yet with big LLMs like GPT-4.
	- Still a big gap between current open-source Transformer models will work well enough, given constraint of 8 A100s. 
	- From rough testing, GPT-4 seems to be a way better model than Llama-70b for Lean formalization. 

# Questions for experiments that will de-risk the project

We intend to break down this project into bite-sized pieces. At the very least, solving one of these sub-questions might be valuable. 

- How are we going to measure improvements on informal-to-informal effectively? 
	- Without having to solve a  bunch of IMO problems ourselves  
- How does GPT-4 or GPT-4 + Wolfram Alpha fare on informal-to-informal?
	- Why: Understand how the best performing public LLM does as a baseline  
- Would a knowledge graph of theorems / functions that would be significantly more helpful with (1) test validation (2) retrieval?
	- Why: This approach is relatively unique applied to theorems and knowledge graph RAG seems to improve retrieval on some tasks
	- Why: Theorem paths can be collapsed to shorten the path from one to the other 
	- How: Node = theorem, Edge = connect theorems, Sub-graph = can also be a theorem and a node
	- Example: from Lean’s mathlib
- Could we take the existing math libraries and regenerate them in a way that is more accurate and helpful for a model to navigate to solve Olympiad  questions?  
	- Why: This could be an approach that is unique and may improve performance  
	- Example: Convert existing math libraries from Lean / Isabelle / etc to Python, where LLMs have more training data from.  
- How do we measure the limits of mathematical reliability of a LLM out of the box?
	- Sub-question: How many "9"s do we need? Ex: 99.999% on all variants of the question "What is log 4?"
	- Sub-question: How do we test across the spread of variants for a concept? 
	- Sub-question: what are problems that GPT-4 Function Calling can answer with complete-enough accuracy, e.g. 100% correct given 10,000 varied samples? 
- What types of LLM high-level reasoning prompts would be helpful?  
	- Why: Self-discover paper actually didn’t see a big improvement in MATH benchmark, and I suspect it’s because their prompts were bad for math. Better prompts could be an easy win 
	- Maybe use prompts in Self Discover and openai/evals
- How do long-context models vs. RAG compare?
	- Why: Using long-context models instead of RAG could be an easy win on improving success rate, over an approach like LeanDojo’s RAG approach  

Approaches  
- Use GPT-4 for now for the LLM. Worry about fine-tuning an open source model later  
- Start with easy experiments first, like high-level reasoning prompt
- Test with temperature 0 on all queries, for deterministic output


# Evaluation
Benchmarks will be conducted on the MiniF2F benchmarks for format-to-formal, and against IMO official datasets for the end-to-end informal-to-informal.  