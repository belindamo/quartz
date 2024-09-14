#concept-pamphlet 
#todo: review these too, continuing on the 3 day article
- RMSE
- HLR
- to add to [[Probability & Statistics]]


- [[🏡 earth/Neuroscience/Memory/Spaced Repetition/spaced repetition|spaced repetition]]

![[Screenshot 2024-07-29 at 12.19.28 PM.png]]

fsrs combines \____ with \____
?
machine learning techniques, universal memory formulas
<!--SR:!2024-08-22,17,299-->

what is fsrs? >> Free Spaced Repetition Scheduler algorithm. It is an open source algorithm.
<!--SR:!2024-10-03,66,270-->






what is the purpose of any spaced repetition algorithm?
?
To help learners efficiently form long-term memories.
<!--SR:!2024-09-17,20,250-->

How do spaced repetition intervals differ with different levels of familiarity?
?
Shorter intervals are used for unfamiliar material while longer ones are used for familiar material.
<!--SR:!2024-10-07,40,290-->

What is the role of automation/algos in spaced repetition?
?
They automate tracking of memory states and efficient scheduling of reviews
<!--SR:!2024-10-10,43,290-->

What is the primary limitation of the SM-0 algorithm?
?
It uses a page of notes as the unit for review, making it unsuitable for tracking memory retention at a more granular level
<!--SR:!2024-10-30,63,310-->

Why did Wozniak use new materials each time he sought to establish a new review interval in his experiments?
?
To ensure uniformity in the intervals of prior reviews.
<!--SR:!2024-10-15,48,290--> 

What are the advantages of breaking material down into smaller parts, for the SM-2 algorithm?
?
It allows the algorithm to find the right schedule for each individual piece of information.
<!--SR:!2024-10-09,42,290-->


What is a primary difference between SM-0 and SM-2 algorithm, besides the fact that SM-2 uses bite-sized QA pairs?
?
SM-2 also uses Ease Factor and grades.
<!--SR:!2024-09-03,6,270-->

What's the primary difference between SM-2 and SM-4 algorithm?
?
SM-2 algorithm doesn't account for the whole lifetime of the card. SM-4 has a matrix to represent the whole memory lifetime of a card.
<!--SR:!2024-10-20,53,290-->

In SM-4, what is the main idea, practically speaking w.r.t. reviews behind Optimal Interval matrix?
![[Pasted image 20240729122702.png]]
?
The main idea is that if the OI matrix says to wait X days and learner actually waits X+Y days and still remembers with a high grade, then the OI value should be changed to something between X and X+Y.
If the learner can remember something after waiting X+Y days and get a good score, the old OI value was probably too short! :p
Rows = how easy the material is
Columns = how many times you've seen it.
This matrix is continuously updated during reviews.
<!--SR:!2024-09-27,30,259-->


stability in the DSR model >>  time required for the probability of recall for a particular memory to decline from 100% to 90%
<!--SR:!2024-09-24,27,259-->

retrievability in the DSR model >> probability of recalling a specific memory at a given moment
<!--SR:!2024-09-19,22,259-->

difficulty in the DSR model >> the inherent complexity associated with a particular memory
<!--SR:!2024-09-30,33,279-->

what are the 3 components in the 3 component model of memory? >> stability, retrievability, difficulty/complexity
<!--SR:!2024-11-10,74,319-->

In spaced repetition algo,
$$
I_1
$$
is...
?
Initial interval after the first review
<!--SR:!2024-10-29,62,319-->


In spaced repetition algo,
$$
C_1
$$
is...
?
Stability increase (SInc). Ratio of successive intervals, from the i-th interval and the preceding (i - 1)th interval
<!--SR:!2024-08-30,2,250-->

What is this equation
$$
R_n(t) = \exp\left[\cfrac{t\ln{0.9}}{I_1\prod\limits_{i=2}^{n}C_i}\right]
$$
?
Retrievability of any given memory at time `t`.
This accounts for spaced repetition algorithms and memory models.
<!--SR:!2024-10-17,50,299-->

What are some advantages of FSRS vs. SM-2 Anki?
?
- 20-30% fewer reviews than with Anki's default algo
- better at schedulign cards with delays
<!--SR:!2024-08-20,18,299-->

What is one way you can think about a memory event in probabilistic terms?
?
A memory event is a single random experiment with only 2 possible outcomes and its success probability equals retrievability
<!--SR:!2024-08-14,13,279-->

What is considered a reasonable % retention to set for SR?
?
70-97% retention
<!--SR:!2024-08-17,15,299-->

# References
1. https://github.com/open-spaced-repetition/fsrs4anki/wiki/Spaced-Repetition-Algorithm:-A-Three%E2%80%90Day-Journey-from-Novice-to-Expert