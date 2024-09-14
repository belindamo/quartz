#concept-pamphlet 

Key question of CS238: how do we automate the process of good decision making?

Based on this graph, what are the 4 sources of uncertainty in decision making?
![[decision loop.png]]
?
Our focus is on agents that interact intelligently to achieve their objectives over time. Given the past sequence of observations, `o1, . . . , o_t` and knowledge of the environment, the agent must choose an action at that best achieves its objectives in the presence of various sources of uncertainty, including the following:
-   outcome uncertainty, where the effects of our actions are uncertain,
-   model uncertainty, where our model of the problem is uncertain,
-   state uncertainty, where the true state of the environment is uncertain, and
-   interaction uncertainty, where the behavior of the other agents interacting in  the environment is uncertain.

---

intention of reading this book: for anything that can be described as input -> output, how can I and others make informed decisions in uncertain (chaotic?) environments that maximize towards an intention?


---

methods for designing decision making agents (5)


Fields (8): economics, psychology, neuroscience, computer science, engineering, mathematics, operations research, societal impact
Another one unlisted...self-fulfillment

q: how are linear programming, dynamic programming, and queuing theory related to operations research? (p12)


Each of the 5 methods has varying level of how much the designer and automata interact with each other:
?
- explicit programming. decision tree paths
- supervised learning. 
- optimization. 
- planning. 
- reinforcement learning. 

What are the downsides of automating away decisions?
?
- it's also automating away nuance, and taste for nuance. 
- it overweights to what's already happened, rather than what might happen. 
- Black swans are not accounted for


![[238 - page 1.png]]