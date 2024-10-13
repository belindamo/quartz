#concept-pamphlet  #paper
[Paper, 2021](https://dl.acm.org/doi/pdf/10.1145/3453483.3454080) [Paper 2020](https://arxiv.org/pdf/2006.08381)
Use 2021 paper!

# Review

In Dreamcoder 2021, what is X? >> Set of tasks<!--SR:!2024-09-08,66,288-->

In Dreamcoder 2021, what are D and 𝜃? Imagine what an element in each looks like.
?
D is library of programs. D is equipped with a real-valued weight vector 𝜃. Together, they define a distribution over programs, written `P[𝜌|D, 𝜃]`
An element in D is a typed 𝜆-calculus expression.
An element of 𝜃 is a real number, which is the probability of using a single element of D, given a single task X.
<!--SR:!2024-11-30,117,268-->

In Dreamcoder 2021, what is the equation to represent the joint distribution over the library and latent variables? (equation 1)
?
![[Screenshot 2024-06-08 at 10.36.46 AM.png]]
where P[D, 𝜃] is a prior distribution over languages and parameters and P[𝑥 |𝜌] scores the likelihood of a task 𝑥 ∈ 𝑋 given a program 𝜌. 1
<!--SR:!2024-08-08,9,190-->


In Dreamcoder 2021, what is the equation to represent the solution of the Dreamcoder problem? (equation 2)
hint:argmax
?
It is the optimal language and weight vector:
![[Screenshot 2024-06-08 at 10.38.34 AM.png]]
the lambda calculus function and weight vector where the integral of the joint distribution is maximized
<!--SR:!2024-08-09,8,170-->
In Dreamcoder 2021, what is the equation to represent the approximation of the joint distribution, meant to make the program set finite? (equation 3)
?
We make a particle based approximation to Eq. 1 and instead marginalize over a finite beam of programs, with one beam per task, collectively written {B\_𝑥 }\_(𝑥 ∈𝑋) . This particle-based approximation is written ℒ(D, 𝜃, {B\_𝑥 }) and acts as a lower bound on the joint density: 𝐽 (D, 𝜃) ≥ ℒ, where ℒ is
![[Screenshot 2024-06-08 at 10.40.13 AM.png]]
In all of our experiments we set the maximum beam size |B𝑥 | to 5. Wake and sleep phases correspond to alternate maximization of ℒ w.r.t. {B_𝑥 }_𝑥 ∈𝑋 , D, and 𝜃.
Basically, having the program be represented by beam because easier
<!--SR:!2024-08-24,29,210-->
In Dreamcoder 2021, in relation to L, what does the wake phase do?
?
The wake phase maximizes L with respect to the beams.
Here (D, 𝜃) is fixed and we want to find new programs to add to the beams so that ℒ increases the most (and therefore best approximates 𝐽 (D, 𝜃)). ℒ most increases by finding programs where P[𝑥 |𝜌]P[𝜌|D, 𝜃] ∝ P[𝜌|𝑥, D, 𝜃] is large, i.e., programs with high posterior probability, which we use as the search objective during waking. Unlike EC2 , during each wake cycle we sample a random minibatch of tasks to try to solve, rather than trying to solve every task at each wake
<!--SR:!2024-08-17,22,190-->
In Dreamcoder 2021, in relation to L, what does the sleep (abstraction) phase do?
?
It maximizes L with respect to the library.
![[Screenshot 2024-06-25 at 11.17.59 PM.png]]
<!--SR:!2024-08-20,15,170-->
In Dreamcoder 2021, in relation to L, what does the sleep (dreaming) phase do?
?
Sleep (Dreaming): tractably maxing ℒ w.r.t. the beams. Here we train 𝑄(𝑝|𝑥) to assign high probability to programs 𝑝 where P[𝑥 |𝜌]P[𝜌|D, 𝜃] is large, because incorporating those programs into the beams will most increase ℒ. In the sections that follow, we elaborate on how these phases are realized
<!--SR:!2024-08-13,8,150-->
What are the two sources of self-supervised data used to train a recognition network?
?
The two sources of self-supervised data used to train a recognition network are: 1. replays of programs already discovered during waking, and fantasies and 2. random programs assembled from members of learned library *L*.
Replays ensure that the recognition model is trained on the actual tasks it needs to solve, and does not forget how to solve them, while fantasies provide a large and highly varied dataset to learn from, and are critical for data efficiency: becoming a domain expert is not a few-shot learning problem, but nor is it a big data problem.
 (4)
 "Replays ensure that the recognition model is trained on the actual tasks it needs to solve, and does not forget how to solve them, while fantasies provide a large and highly varied dataset to learn from, and are critical for data efficiency." (4)
The two steps involved in the 'Sleep' phase are: 1. Abstraction / Replay: Grow DSL (generative model) and 2. Dreaming / Fantasy: Train neural network (recognition model) on "fantasy", programs sampled from the generative model.
<!--SR:!2024-09-14,50,230-->
What kind of tasks was Dreamcoder (2021) tested on? (it's ok if this is rough)
?
- **list processing**
- **text editing**
- **regexes**
- **logo graphics**
- **block towers**
- **symbolic regression**
- **recursive programming**
- **physical laws**
![[Screenshot 2024-05-20 at 11.47.29 AM.png]]
<!--SR:!2024-08-11,47,250-->


In Dreamcoder, how big is the input corpus for a task? Why is this significant?
?
100-200 tasks. This is too few examples for a high-capacity neural network, but once model learns library customized to the domain, it can draw unlimited samples or 'dreams' to train the recognition network, faciliating sample-efficient learning. (4)
<!--SR:!2024-10-11,77,250-->
For the sleep state, Dreamcoder trains a recognition network on (*A, B*) pairs. What are A and B?
?
(program, task)
<!--SR:!2024-08-15,42,250-->
Why do I feel computer programs are a significant way to represent tasks?
?
In this context, programs represent knowledge in a way that is mutually understandable by deterministic functions, LLMs, and humans.
<!--SR:!2024-11-17,104,250-->
What are the two different kinds of domain expertise mentioned in the notes?
?
The two different kinds of domain expertise mentioned are: 1. Explicit declarative knowledge - DSL (probabilistic generative model) and 2. Implicit procedural knowledge - NN (neural network recognition model).
<!--SR:!2024-08-30,61,270-->


Data structure that leverages sharing to compactly represent many alternative versions of the same program.
<!--SR:!2024-05-31,2,230-->


What is an **E-graph**?
?
An e-graph is a data structure that stores an equivalent relation over the terms of some language. In a deterministic way, it stores equivalence relations over the terms of some formal system.
Source: https://en.wikipedia.org/wiki/E-graph
<!--SR:!2024-11-04,89,224-->
How can you tell if 2 e-nodes are equivalent??
They are in the same e-class
<!--SR:!2024-08-21,19,224-->
In math, what is an invariant?
?
A property of a math object that remains the same, even after operations/transformations are applied to that object
Source: https://en.wikipedia.org/wiki/Invariant_(mathematics)
<!--SR:!2024-09-17,53,244-->
What is a **version space** in Dreamcoder?
?
**Version space** is a data structure that compactly represents a large set of programs so that you can search a predefined space of hypotheses, **viewed as a set of logical sentences.**
(it's ok if this doesn't make complete sense yet! let's keep marking this as 'hard' until it all makes sense)
Formally, the hypothesis space is a [disjunction](https://en.wikipedia.org/wiki/Logical_disjunction "Logical disjunction")
![{\displaystyle H_{1}\lor H_{2}\lor ...\lor H_{n}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/851ab04beb741bde44f94420c75da1fd2e0a958b)
(i.e., either hypothesis 1 is true, or hypothesis 2, or any subset of the hypotheses 1 through n)
The benefits of using version space is that it supports efficient set operations like union, intersection, and membership checking.
In Dreamcoder, it compactly represent a set of programs. For Dreamcoder, they use 𝜆-calculus with some additional primitives.
The union operator (⊎) intuitively represents a nondeterministic choice between a collection of alternatives. It allows the notation above to compactly represent large sets of programs.
Example: the version space `(𝜆⊎{$0, 7}) (⊎ {4, 9})` encodes four different expressions: `(𝜆$0)4, (𝜆$0)9, (𝜆7)4, and (𝜆7)9`. We refer to the set of expressions encoded by a version space as its **extension**.
DEFINITION:
A version space is either- A deBuijn index: written *$i*, for *i* a natural number
- A primitive, such as the number 42 or the function map
- An abstraction: written 𝜆𝑣, where *v* is a version space
- An application: written (f x), where both f and x are version spaces
- A union ⊎𝑉 , where 𝑉 is a set of version spaces
- The empty set, ∅
- The set of all 𝜆-calculus expressions, Λ
(6)
<!--SR:!2024-08-25,20,190-->

What is a **leaf** in a version space, in Dreamcoder?
?
(keep reviewing until it makes sense!)
By a **leaf** we mean either a primitive or a deBuijn index:
- A deBuijn index: written *$i*, for *i* a natural number
- A primitive, such as the number 42 or the function map
 A leaf is also a version space.
<!--SR:!2024-08-19,14,161-->

What is the **extension** of a version space *v*? ?
(it's ok if this doesn't make complete sense yet! let's keep marking this as 'hard' until it all makes sense)
The extension is the set of expressions encoded by a version space.
It is written ⟦𝑣⟧ and is defined recursively as:
⟦𝜌⟧ = {𝜌} , if 𝜌 a leaf      ⟦Λ⟧ = Λ      ⟦∅⟧ = ∅
⟦𝜆𝑣⟧ = {𝜆𝑒 : 𝑒 ∈ ⟦𝑣⟧}        ⟦⊎𝑉 ⟧ = {𝑒 : 𝑣 ∈ 𝑉 , 𝑒 ∈ ⟦𝑣⟧}
⟦(𝑣1 𝑣2)⟧ = {(𝑒1 𝑒2) : 𝑒1 ∈ ⟦𝑣1⟧, 𝑒2 ∈ ⟦𝑣2⟧}
The data structures we use to represent version spaces also support efficient membership checking, which we write as 𝑒 ∈ ⟦𝑣⟧. Important for our purposes, it is also efficient to extract the smallest member of a version space’s extension in terms of a new libraryśi.e., extracting the most compressive member of a version space given a new library. We define extract(𝑣|D) as calculating arg min𝜌 ∈⟦𝑣⟧ size(𝜌|D), where size(𝜌|D) for program 𝜌 and library D is the size of the syntax tree of 𝜌, when members of D are counted as having size 1 (Fig. 5A).
![[Screenshot 2024-06-08 at 10.29.33 AM.png]]
<!--SR:!2024-08-16,11,170-->


What is inverse 𝛽-reduction in Dreamcoder? What phase is it used?
?
It's used in the sleep(abstraction) phase to refactor a program.
Inverse 𝛽-reduction is an operator over version spaces that calculates the set of n-step refactorings of a program 𝜌.
We call this operator 𝐼 𝛽𝑛, because it inverts 𝛽-reduction 𝑛 times, writing 𝐼 𝛽𝑛 (𝜌) for a version space encoding 𝑛-step refactorings of program 𝜌. This operator should satisfy:
![[Screenshot 2024-06-25 at 11.24.56 PM.png]]
(it's ok if this doesn't make complete sense yet! let's keep marking this as 'hard' until it all makes sense)
<!--SR:!2024-09-05,29,190-->⟦𝐼 𝛽𝑛 (𝜌)⟧ =  𝜌 ′ : 𝜌 ′ −→𝛽 𝜌 ′′ −→𝛽 · · · −→𝛽 | {z } ≤ 𝑛 times 𝜌 (5)

We define 𝐼 𝛽𝑛 in terms of another operator, 𝐼 𝛽′ , which performs a single step of refactoring (Fig. 5B); in particular, we want to define 𝐼 𝛽′ so that its extension obeys"
⟦𝐼 𝛽′ (𝑣)⟧ =  𝜌 ′ : 𝜌 ′ −→𝛽 𝜌 ∀𝜌 ∈ ⟦𝑣⟧ (6)
<!--SR:!2024-06-21,1,130-->

What are some ideas for improving on Dreamcoder??
- Seed with existing libraries/natural language resources. For example, learning MATH's mathlib.
- Seed with applied task data to make this actually useful
- Use LLMs
<!--SR:!2024-12-10,125,250-->

What is inductive program synthesis?
?
Inductive program synthesis is the process of automatically generating computer programs that satisfy a given specification, typically provided as a set of input-output examples. The system learns to generalize from these specific examples to create a program that not only works for the given instances but also applies correctly to new, unseen situations. This approach leverages techniques from artificial intelligence and machine learning to derive algorithms that can solve complex tasks without explicit programming for each task.
<!--SR:!2024-09-21,57,223-->
----



# Notes
version space learning https://en.wikipedia.org/wiki/Version_space_learning
e-graph https://en.wikipedia.org/wiki/E-graph

### Summary 
- We train a recognition network on (program, task) pairs drawn from two sources of self-supervised data: 
	- 1. replays of programs discovered during waking, and fantasies
	- 2. programs drawn from L. 
	- Replays ensure that the recognition model is trained on the actual tasks it needs to solve, and does not forget how to solve them, while fantasies provide a large and highly varied dataset to learn from, and are critical for data efficiency: becoming a domain expert is not a few-shot learning problem, but neither is it a big data problem

My hot takes
- I think by defining these programs, we can also pull out emergent properties from them that can then be used to define level hierarchies within the generated Ls.

My questions:
- how are programs sampled from L? 
- where are there massive datasets of ANY data where it is: natural language|program in system|data with type defined in system -> number|program in system|data with type defined in system (NO natural language)
	- the union of these sets are the evals. hoard em
- how were the names of the functions created if it was purely symbolic? (my guess is they were added afterwards)

- but...on evals, in ~2020 it answered maybe 82% correct...not great. the programs are still lossy af. 
	- **what bit to flip in order to make this be 100% for purely deterministic functions, and near 100% / better than human for others?**
- to learn 'origami' functional programming took Dreamcoder a year of CPU time

philosophically: "programs represent knowledge in a way that is mutually understandable by deterministic functions, LLMs, and humans"


- 2018 paper on
	- list processing: created 236 list manipulation tasks, 38 new subroutins, rediscovered filter function
	- text editing: trained on 109 auto-generated text editing tasks, created DSL with 12 new functions and solved training tasks, tested on 108 text editing problems from a programming competition and solving went from 3.7%->74.1% after training.
	- symbolic regression: to observe points on the curve of a function and write a program to fit those points. no outcomes listed here
- how it is described
	- wake cycle: try to solve as many problems as you can. D, theta are fixed. find new programs to add to beam. enumerate programs written in current DSL in order of their probability according to neural network
	- sleep-abstraction cycle: consolidate code abstractions. 
	- dream sleep cycle: train recognition model to predict distribution over programs in the current DSL, to help improve program search. assign high probability to programs that have high prior probability according to DSL. 


- 2020 paper
	- know where neural networks are useful vs functional programs! 

- 2021 paper on
	- list processing
	- text editing
	- regexes
	- logo graphics
	- block towers
	- symbolic regression
	- recursive programming
	- physical laws
![[Screenshot 2024-05-20 at 11.06.34 AM.png]]



---

## Related materials
- [[The "wake-sleep" algorithm for unsupervised neural networks (Hinton et. al 1995)]]
- [[How to grow a mind: Statistics, structure, and abstraction (Tenenbaum et al, 2011)]]
- [[Human-level concept learning through probabilistic program induction (Lake, Tenenbaum 2015)]]
- [[Papers i don't understand well enough yet but want to]]
- Performance was compared against Exploration-Compression algorithm
	- [[Library Learning for Neurally-Guided Bayesian Program Induction (Ellis, Tenenbaum 2018)]]
	- [[Papers i don't understand well enough yet but want to]]


![[Screenshot 2024-05-20 at 10.48.24 AM.png]]


## sections
## 2.4 Bayesian view
Section 2.4, titled "A Bayesian View," in the context of the DreamCoder framework, provides a probabilistic formulation of the inductive program synthesis problem as a Bayesian inference problem. Here's a breakdown and explanation of the key concepts and processes outlined in this section:

### Bayesian Framework Overview
The section describes DreamCoder's approach to program synthesis using a Bayesian framework where:
- **D** represents the library of program components (functions).
- **θ** represents parameters that define how likely these components are used.
- **X** represents the set of tasks (or problems) to be solved.
- **ρ** represents programs that solve these tasks.

### Objective
The primary objective is to find the library **D** and parameters **θ** that maximize the probability of observing the given data (tasks), encapsulated by the joint probability distribution **J(D, θ)**. The formula provided is:

\[ J(D, \theta) = P[D, \theta] \prod_{x \in X} \left[ \sum_{\rho} P[x|\rho] P[\rho|D, \theta] \right] \]

- **P[D, θ]**: The prior probability of the library and parameters, reflecting our initial beliefs about these components before seeing any actual tasks.
- **P[x|ρ]**: The likelihood of task x given a program ρ, measuring how well the program solves the task.
- **P[ρ|D, θ]**: The probability of a program given the library and parameters, reflecting how programs are generated from the library components.

### Inference and Optimization
The Bayesian view focuses on using this formulation to perform inference and optimization:
- **Inference**: Determining the most likely library and parameters given the tasks.
- **Optimization**: Adjusting the library and parameters to increase the likelihood of the observed tasks, thereby improving the synthesis engine's capability.


### Challenges and Solutions
- **Marginalization Over Programs**: The exact computation of **J(D, θ)** requires marginalizing over an infinite set of possible programs, which is computationally infeasible. Instead, DreamCoder uses a particle-based approximation, where only a finite subset of promising programs (a beam) is considered.
- **Wake-Sleep Algorithm**: The wake-sleep algorithm is adapted for iterative improvement:
  - **Wake Phase**: Proposing changes to the current programs to better solve the tasks, keeping the library and parameters fixed.
  - **Sleep Phase**: Improving the library (by extracting common patterns from successful programs) and refining the recognition model (parameters) based on the learned programs.

### Bayesian Optimization
Ultimately, the section describes how DreamCoder uses a Bayesian approach to iteratively refine both its model of program synthesis (the library) and its ability to generate programs efficiently. This iterative process leverages the strengths of Bayesian inference to handle uncertainty and incorporate new knowledge systematically, thereby improving the system's performance over time.

By adopting this Bayesian view, DreamCoder not only aims to synthesize programs that solve given tasks but also evolves a sophisticated understanding of how different programming constructs can be combined, enhancing its ability to tackle increasingly complex problems.


## Concrete example!

![[Screenshot 2024-05-23 at 5.59.56 PM.png]]

---

