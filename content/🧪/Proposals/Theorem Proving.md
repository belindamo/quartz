---
date: 2024-02-20
---
# Summary
Theorem-proving was one of the first proposed applications for machines, and especially given the release of large language models, these systems have been steadily improving performance on mathematics benchmarks such as MATH and MiniF2F.  

Current top-ranked solutions for the MiniF2F benchmarks rely on some combination of a fine-tuned transformer with light layers of symbolic checks and/or system-2 prompt-based reasoning.  

In this project, we suggest that (1) self-discovery of a multi-level library of symbolic checks and prompt-based reasoning, and (2) long-context retrieval of library components, will drastically improve the performance of a LLM-powered theorem-proving system.  

We introduce an Operating System for LLMs, that self-builds this library based on existing theorem-proving libraries such as those in Lean, Isabelle, and Metamath.  

To evaluate the Operating System’s ability, we will benchmark against MiniF2F for the formal-to-formal parts of the system, and against IMO official datasets for the end-to-end informal parts.  

If this works, this project will demonstrate that a generated IO-based system is an effective way of augmenting a black-box LLM, and that hopefully such a system reaches the performance of an human IMO Gold competitor!  

# Related Work
Here are the clusters of research papers that have inspired this  
project:  
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

---

The following is for the project team.  

# Risks
There are a number of risks. Here are some:  
- Short Timeline: Deadline for AIMO seems to be around early June. That gives us about 3 months to build this project  
- Informal-to-formal and Formal-to-formal is pretty far off in benchmarks - like 40% from one of the most recent papers, Draft, Sketch, Prove (2023)  
- Informal-to-informal end-to-end is hard to evaluate. Need to understand the IMO problems to do that, and this is also time-consuming  
- Seems like gold medalists in IMO got about 76-100% of questions correct in 2023. So our proposed solution needs to be nearly twice as good as current benchmark performance  
- Playing around with it, GPT-4 seems to be a way better model than Llama-70b for Lean formalization. Not sure if open-source models will work well enough, given constraint of 8 A100s.  
- Competing teams: I think OpenAI and Meta have entire teams working on this problem too lol. With access to a lot of compute. We should have a strong justification why our architecture/approach is unique / creatively novel to warrant beating them  

# Experiments & Approaches to De-Risk
There are many ways we might generate such a multi-level  
library. Since this is a large experiment, unlike other research  
papers, we propose several potential experiments to de-risk our approach.  

Questions to generate experiments on:  
- Question: How are we going to measure improvements on informal-to-informal effectively? Without having to solve a  bunch of IMO problems ourselves  
- Question: how does GPT-4 or GPT-4 + Wolfram Alpha fare on informal-to-informal?
	- Why: Understand how the best performing public LLM does as a baseline  
- Question: Is there a mathlib graph of theorems / functions  that would be significantly more helpful with (1) test validation (2) retrieval?
	- Why: This could be an approach that is unique and may improve performance  
	- How: Node = theorem, Edge = connect theorems, Sub-graph = can also be a theorem and a node.  
- Question: Could we take the existing math libraries and  regenerate them in a way that is certainly accurate and more helpful for a model to navigate to solve Olympiad  questions?  
	- Why: This could be an approach that is unique and may improve performance  
- Question: what are problems that GPT-4 Function Calling can answer with complete-enough accuracy, e.g. 100%  correct given 10,000 varied samples? ex: "What is log 4?".  Intention here is to understand the limits of mathematical  reliability of a LLM out of the box.  
- Question: what types of LLM high-level reasoning prompts  would be helpful?  
	- Why: Self-discover paper actually didn’t see a big improvement in MATH benchmark, and I suspect it’s because their prompts were bad for math. Better prompts could be an easy win 
- Question: do long-context retrieval models work way better than RAG for this problem?  
	- Why: This could be an easy win over something like LeanDojo’s RAG approach  

Approaches  
- Use GPT-4 for now for the LLM. Worry about fine-tuning an open source model later  
- Start with easy experiments first, like high-level reasoning prompt


# Evaluation
Benchmarks will be conducted on the MiniF2F benchmarks for format-to-formal, and against IMO official datasets for the end-to-end informal-to-informal.  