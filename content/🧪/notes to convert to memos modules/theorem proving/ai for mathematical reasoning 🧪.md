## Experiment: Back-translation for Language Model Outputs

Problem
It is difficult to ensure accuracy of a language model on a task without any human intervention. Synthetic data is also very difficult to generate effectively. How do we ensure good evaluation of a model’s task effectiveness?

  
Set up bit
In the past, language model accuracy has been measured against human-curated test set to benchmark. Synthetic training data has been another approach, but it historically hasn’t been fully reliable enough to use as test data.

  

Flip the bit
In this experiment, we suggest a simple executive-control module to guide the looped generation of both (1) test sets and (2) code that will allow the system to self-align itself to fulfill any reasoning tasks. 

  

This is influenced by the concept of back-translation, which has been shown to improve the quality of machine translation. Backtranslation in machine translation “brute-forces” performance improvements by using synthetic data on a second training run. Similarly, this system "translates" back and forth multiple times with multiple combinations of similar solutions/test sets.

  

Instantiate solution

Here is a simple example of how this would work. 

Let's consider a set of language models M, that are prompted to fulfill a task from set of all possible tasks A (each represented as a natural language string and that is the input of the system user) by creating a python function from set of all possible python functions B. Also, let P = set of all prompts and T = set of all test sets.

  

Let's consider how to solve task A[a1]: 

1. M[m1] creates initial B[b1] with prompt P[p1] that would seem to fulfill task A[a1].

2. M[m1] creates initial T[t1] with prompt P[p2] that would seem to provide test sets for task A[a1].

3. T[t1] is run against B[b1]. 

4. If all tests pass, then it's good. Else, generate variations of repeat steps 1-3 with new prompts until all tests pass.

5.  If you'd like to, M[m2...mn] are also used for steps above and then also compared until all functions and tests generated pass. 

  

Evaluate

To start, this can be tested on GSM8K and [CodeContests](https://github.com/google-deepmind/code_contests) test sets for math and programming tasks respectively. 

  

Implications

If this leads to some level of improvement in output, then I'd posit that this approach of looping to ensure “alignment” can work on various other modules, not just between test sets and functions. For instance: 

  

- Generate a sketch like in Draft, Sketch, Prove, and align that with the function and test sets. 
    
- Generate a symbolic lexicon in the process, like Dreamcoder, and align that with function and test sets.
    

  

Related concepts & works

- Back-translation, the simple way: translating previously translated content back into its source language
    
- [Back-translation with synthetic data](https://aclanthology.org/D18-1045.pdf): "Back-translation first trains an intermediate system on the parallel data which is used to translate the target monolingual data into the source language. The result is a parallel corpus where the source side is synthetic machine translation output while the target is genuine text written by humans. The synthetic parallel corpus is then simply added to the real bitext in order to train a final system that will translate from the source to the target language."
    
- Chain of Thought with Self consistency
    

  
  

## Papers

  

Most similar papers

- Dreamcoder
    
- AlphaCode
    
- AlphaGeometry
    
- GPT-F
    
- Thor
    
- AlphaGo/AlphaGoZero
    
- Draft, Sketch, Prove (2023) [https://arxiv.org/pdf/2210.12283.pdf](https://arxiv.org/pdf/2210.12283.pdf)
    
- LeanDojo (2023)
    

  

Using GPT-4 / LLMs for "intuition"

- Testing GPT-4 with Wolfram Alpha and Code Interpreter plug-ins on math and science problems [https://arxiv.org/abs/2308.05713](https://arxiv.org/abs/2308.05713)
    
- Advancing mathematics by guiding human intuition https://www.nature.com/articles/s41586-021-04086-x
    

  

Prompting

- Self-Discover [https://arxiv.org/pdf/2402.03620.pdf](https://arxiv.org/pdf/2402.03620.pdf)
    

- use on IMO datasets?
    

- Augmented language models: a survey (2023) [https://arxiv.org/abs/2302.07842](https://arxiv.org/abs/2302.07842)
    
- Let's verify step by step [https://arxiv.org/abs/2305.20050](https://arxiv.org/abs/2305.20050)
    
- "ensemble refinement" as a prompting strategy, Med-PaLM2 (2023) [https://arxiv.org/pdf/2305.09617.pdf](https://arxiv.org/pdf/2305.09617.pdf)
    
- self consistency [https://arxiv.org/abs/2203.11171](https://arxiv.org/abs/2203.11171)
    
- Chain of Thought (CoT) (2022) [https://proceedings.neurips.cc/paper_files/paper/2022/file/9d5609613524ecf4f15af0f7b31abca4-Paper-Conference.pdf](https://proceedings.neurips.cc/paper_files/paper/2022/file/9d5609613524ecf4f15af0f7b31abca4-Paper-Conference.pdf)
    
- Show your Work (2021) https://arxiv.org/pdf/2112.00114.pdf
    
- step-back prompting
    
- Other methods: self-consistency, self-refine, recitation-augmentation, dialogue enabled reasoning
    

  

Language models

- General
    

- Llama-7b, Llama-65b
    

- For math
    

- Llemma-7b, Llemma-34b https://paperswithcode.com/paper/llemma-an-open-language-model-for-mathematics
    

  

Current theorem proving SoA

- Benchmarks [https://paperswithcode.com/sota/automated-theorem-proving-on-minif2f-test](https://paperswithcode.com/sota/automated-theorem-proving-on-minif2f-test)
    

- Draft, Sketch, Prove
    
- Thor [https://arxiv.org/pdf/2205.12615v1.pdf](https://arxiv.org/pdf/2205.12615v1.pdf)
    
- GPT-f
    
- Lean GPT-f
    
- Llemma
    
- PACT
    

  

More on the dreamcoder side

- coarse then fine  [https://arxiv.org/abs/2305.00909](https://arxiv.org/abs/2305.00909)
    
- symbolic behavior in AI [https://arxiv.org/abs/2102.03406](https://arxiv.org/abs/2102.03406)
    
- 9 motifs of scientific computing [https://arxiv.org/abs/2112.03235](https://arxiv.org/abs/2112.03235)
    
- Program synthesis [https://arxiv.org/abs/2108.07732](https://arxiv.org/abs/2108.07732)
    
- Matrix for lots of APIs [https://arxiv.org/pdf/2303.16434.pdf](https://arxiv.org/pdf/2303.16434.pdf)
    
- Phillip colella 7 dwarves 
    
- How Operating Systems work https://www.cs.bham.ac.uk/~exr/lectures/opsys/10_11/lectures/os-dev.pdf
    

  

Code for dreamcoder side

- Parsel [https://github.com/ezelikman/parsel](https://github.com/ezelikman/parsel)
    
- Dreamcoder https://github.com/CatherineWong/dreamcoder
    

  

Math datasets

- MATH (NeurIPS 2021) https://github.com/hendrycks/math 
    
- mathlib lean4
    
- Metamath
    
- Also libs for: Isabelle, Hol Light
    
- gsm8k: [https://arxiv.org/pdf/2110.14168v2.pdf](https://arxiv.org/pdf/2110.14168v2.pdf)
    

  

IMO datasets

- miniF2F [https://github.com/openai/miniF2F](https://github.com/openai/miniF2F)
    

- fixed version from facebook lol [https://github.com/facebookresearch/minif2f](https://github.com/facebookresearch/minif2f)
    

-  informal datasets
    

- https://www.imo-official.org/problems/IMO2020SL.pdf algebra, combinatorics, geometry, number theory
    

- problems https://www.imo-official.org/problems.aspx
    

  
  

Misc. related

- [https://cdn.openai.com/papers/Formal_Mathematics_Statement_Curriculum_Learning__ICML_2022.pdf](https://cdn.openai.com/papers/Formal_Mathematics_Statement_Curriculum_Learning__ICML_2022.pdf)
    
- This guy did a lit review on SoTA theorem proving [https://docs.google.com/document/d/19NrA_uTYHkPEv7872rzlpIzWQN_OPcuimp4ARPmK-nM/edit](https://docs.google.com/document/d/19NrA_uTYHkPEv7872rzlpIzWQN_OPcuimp4ARPmK-nM/edit)
    
- Beyond imitation game (how much does size matter) https://arxiv.org/abs/2206.04615
    

- 

  
  

# Logs

  

## 2024-03-20

 todos:

-  Run evals on ‘./datasets/GSM8K/test_100.jsonl’. See run_all() function in run_gs8mk_evals.py
	- CoT-SC, gpt-3.5-turbo-0125
	- CoT-SC, gpt-4-0613
	- CoT-SC, claude-3-opus-20240229
	- CoT-SC, claude-3-sonnet-20240229
- Proposal + Wireframes for chat.lmsys.org 2.0
- Implement Back-translation experiment
- Erik meeting
    

## 2024-03-18

What has been done?

- Integrations for most basic models (Claude & GPT)
    
- Basic implementations of things like CoT-SC
    
- Fine tuning on GSM8K problems for gpt-3.5-turbo 
    

  

Todo:

- Run full eval set on GSM8K
    

- How to run?
    

- CoT-SC
    
- Vanilla   
    
- Fine-tuned models
    

- gpt-3.5-turbo-0125
    

- 100
    
- 1000
    
- 7473 (problems)
    

  
  
