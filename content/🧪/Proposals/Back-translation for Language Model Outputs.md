
**Problem**

It is difficult to ensure accuracy of a language model on a task without any human intervention. Synthetic data is also very difficult to generate effectively. How do we ensure good evaluation of a model’s task effectiveness?

**Set up bit**

In the past, language model accuracy has been measured against human-curated test set to benchmark. Synthetic training data has been another approach, but it historically hasn’t been fully reliable enough to use as test data.

**Flip the bit**

In this experiment, we suggest a simple executive-control module to guide the looped generation of both (1) test sets and (2) code that will allow the system to self-align itself to fulfill any reasoning tasks. 

This is influenced by the concept of back-translation, which has been shown to improve the quality of machine translation. Backtranslation in machine translation “brute-forces” performance improvements by using synthetic data on a second training run. Similarly, this system "translates" back and forth multiple times with multiple combinations of similar solutions/test sets. 

**Instantiate solution**
Here is a simple example of how this would work. 

Let's consider a set of language models M, that are prompted to fulfill a task from set of all possible tasks A (each represented as a natural language string and that is the input of the system user) by creating a python function from set of all possible python functions B. Also, let P = set of all prompts and T = set of all test sets.

Let's consider how to solve task A[a1]: 

1. M[m1] creates initial B[b1] with prompt P[p1] that would seem to fulfill task A[a1].
2. M[m1] creates initial T[t1] with prompt P[p2] that would seem to provide test sets for task A[a1].
3. T[t1] is run against B[b1]. 
4. If all tests pass, then it's good. Else, generate variations of repeat steps 1-3 with new prompts until all tests pass.
5.  If you'd like to, M[m2...mn] are also used for steps above and then also compared until all functions and tests generated pass. 

**Evaluate**

To start, this could be tested on GSM8K and [CodeContests](https://github.com/google-deepmind/code_contests) test sets for math and programming tasks respectively. 
  

**Implications**

If this leads to some level of improvement in output, then I'd posit that this approach of looping to ensure “alignment” can work on various other modules, not just between test sets and functions. For instance: 

- Generate a sketch like in Draft, Sketch, Prove, and align that with the function and test sets. 
- Generate a symbolic lexicon in the process, like Dreamcoder, and align that with function and test sets.
  

**Related concepts & works**

- Back-translation, the simple way: translating previously translated content back into its source language
- [Back-translation with synthetic data](https://aclanthology.org/D18-1045.pdf): "Back-translation first trains an intermediate system on the parallel data which is used to translate the target monolingual data into the source language. The result is a parallel corpus where the source side is synthetic machine translation output while the target is genuine text written by humans. The synthetic parallel corpus is then simply added to the real bitext in order to train a final system that will translate from the source to the target language."
- Chain of Thought with Self consistency
