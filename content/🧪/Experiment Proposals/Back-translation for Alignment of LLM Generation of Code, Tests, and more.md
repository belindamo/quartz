---
date: 2024-04-04
draft: "true"
---
## Experiment Length
**Estimated Time To Build:** 3 days

**Sub-experiments:** 
- [[9. How might a set of AI models improve code generation through iterative code and test set generation? 🟢]]

# Summary
*Problem space, Concept that exists, Concept that is being changed, How concept is being changed*

**In this experiment, we suggest a software module to guide the looped generation of (1) test sets and (2) code, to fulfill some reasoning task. The system then self-aligns itself between its generated code and test sets until it reaches complete alignment. With unlimited compute, it is theoretically possible to add infinite numbers of generated items as long as there are no orphan items.** 

It is difficult to ensure accuracy of a language model on a task without any human intervention. Synthetic data is also very difficult to generate effectively. How do we ensure good evaluation of a model’s task effectiveness?

In the past, language model accuracy has been measured against human-curated test set to benchmark. Synthetic training data has been another approach, but it historically hasn’t been fully reliable enough to use as test data.


This is influenced by the concept of back-translation in machine translation. Back-translation in machine translation improves performance by adding a second training run based on synthetically generated data. This is also influenced by prompting techniques like CoT-SC that run multiple threads to solve a problem and that choose the best one. The proposed system "translates" back and forth with combinations of similar solution functions and test sets, until the generated function runs against the generated tests at a 100% pass rate.

Not only that, but this system can also translate across multiple "levels". A simple example generates the output of 2 items: 1 code function and 1 array of test sets. A more complex example includes item combinations of:

- Generated code function
- Generated test set array
- Generated symbolic lexicon 
- Generated sketch (a la Draft, Sketch, Prove)
- Language models
- Prompts
- Ensemble techniques
- Multi-step single model techniques


## A simple example
Let's consider a set of language models M, that are prompted to fulfill a task from set of all possible tasks A (each task is a natural language string that is the input of a user) by creating a python function from the set of all possible python functions B. Also, let P = set of all prompts and T = set of all test sets.

Let's consider how to solve task A_n: 

1. M_a, with a fixed prompt P_x to create a python function, creates initial B_a that seems to fulfill task A_n.
2. M_a, with a fixed prompt P_y to create a test set, creates initial test set T_a that seems to align with task A_n.
3. B_a is run against T_a. 
4. If all tests pass, then it's good. Else, repeat steps 1-3 to regenerating different items in B and T until all tests pass.

You can imagine how different language models from M, fixed prompts from P, test sets from T, amongst other items like different prompting techniques, could be used to generate many variants to reach alignment under. 

# Related Works

- Back-translation, the simple way: translating previously-translated content back into its source language
- [Back-translation with synthetic data](https://aclanthology.org/D18-1045.pdf): "Back-translation first trains an intermediate system on the parallel data which is used to translate the target monolingual data into the source language. The result is a parallel corpus where the source side is synthetic machine translation output while the target is genuine text written by humans. The synthetic parallel corpus is then simply added to the real bitext in order to train a final system that will translate from the source to the target language."
- Chain of Thought with Self-Consistency
- Self-Discover

# Implementation Plan

- Python 
- GPT-4 for LLM: GPT-4 is one of the best performing language models for reasoning

# Evaluation Plan

- Independent Variable
	- Generate synthetic data across multiple levels and execute all code to validate alignment
- Dependent Variable
	- Percentage of successfully generated functions (%)
- Test sets
	- Math and coding tasks. Test sets that could make sense are GSM8K for math and [CodeContests](https://github.com/google-deepmind/code_contests) for programming.
  
# Risks to execute
- It's really expensive to run
- This is effectively like crowdsourcing from many variations of LLM-powered systems. Crowdsourcing is almost never as accurate as an expert though, so the output even after all this alignment might be poor.

# Implications if it works

If this works, there are a few other avenues to explore
- Generate an entire formal system.
- Give initial inputs for items you already know work. For example, give a test set array only and generate a function that works for the test set. 
- [[Generating a series of isomorphisms]]

---

# Misc.

What I'm unsure about
- "With unlimited compute, it is theoretically possible to add infinite numbers of generated items as long as there are no orphan items." -> erm but is it possible to reach alignment in the same big O time

related::[["LLM Operating System"]]