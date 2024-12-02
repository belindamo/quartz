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
what is fsrs? >> Free Spaced Repetition Scheduler algorithm. It is an open source algorithm.
<!--LEARN:1jFo2Pz5-->






what is the purpose of any spaced repetition algorithm?
?
To help learners efficiently form long-term memories.
<!--LEARN:U1NKx3Jp-->

How do spaced repetition intervals differ with different levels of familiarity?
?
Shorter intervals are used for unfamiliar material while longer ones are used for familiar material.
<!--LEARN:TbiizYMG-->

What is the role of automation/algos in spaced repetition?
?
They automate tracking of memory states and efficient scheduling of reviews
<!--LEARN:ZFIxNoIC-->

What is the primary limitation of the SM-0 algorithm?
?
It uses a page of notes as the unit for review, making it unsuitable for tracking memory retention at a more granular level
<!--LEARN:8E9k4bnG-->

Why did Wozniak use new materials each time he sought to establish a new review interval in his experiments?
?
To ensure uniformity in the intervals of prior reviews.
<!--LEARN:yqKXf5kA-->

What are the advantages of breaking material down into smaller parts, for the SM-2 algorithm?
?
It allows the algorithm to find the right schedule for each individual piece of information.
<!--LEARN:bIv2og9H-->


What is a primary difference between SM-0 and SM-2 algorithm, besides the fact that SM-2 uses bite-sized QA pairs?
?
SM-2 also uses Ease Factor and grades.
<!--LEARN:Ob977Exi-->

What's the primary difference between SM-2 and SM-4 algorithm?
?
SM-2 algorithm doesn't account for the whole lifetime of the card. SM-4 has a matrix to represent the whole memory lifetime of a card.
<!--LEARN:ZLgx6Vh7-->

In SM-4, what is the main idea, practically speaking w.r.t. reviews behind Optimal Interval matrix?
![[Pasted image 20240729122702.png]]
?
The main idea is that if the OI matrix says to wait X days and learner actually waits X+Y days and still remembers with a high grade, then the OI value should be changed to something between X and X+Y.
If the learner can remember something after waiting X+Y days and get a good score, the old OI value was probably too short! :p
Rows = how easy the material is
Columns = how many times you've seen it.
This matrix is continuously updated during reviews.
<!--LEARN:6v8IqEU1-->

stability in the DSR model >>  time required for the probability of recall for a particular memory to decline from 100% to 90%
<!--LEARN:o32uNcNA-->

retrievability in the DSR model >> probability of recalling a specific memory at a given moment
<!--LEARN:aBCUmuBd-->

difficulty in the DSR model >> the inherent complexity associated with a particular memory
<!--LEARN:callHK5J-->

what are the 3 components in the 3 component model of memory? >> stability, retrievability, difficulty/complexity
<!--LEARN:15PPovDS-->

In spaced repetition algo,
$$
I_1
$$
is...
?
Initial interval after the first review
<!--LEARN:0WmNBzgx-->

In spaced repetition algo,
$$
C_1
$$
is...
?
Stability increase (SInc). Ratio of successive intervals, from the i-th interval and the preceding (i - 1)th interval
<!--LEARN:1HgBepeh-->

What is this equation
$$
R_n(t) = \exp\left[\cfrac{t\ln{0.9}}{I_1\prod\limits_{i=2}^{n}C_i}\right]
$$
?
Retrievability of any given memory at time `t`.
This accounts for spaced repetition algorithms and memory models.
<!--LEARN:Jxmdvu4E-->

What are some advantages of FSRS vs. SM-2 Anki?
?
- 20-30% fewer reviews than with Anki's default algo
- better at schedulign cards with delays
<!--LEARN:n4sgS13Y-->

What is one way you can think about a memory event in probabilistic terms?
?
A memory event is a single random experiment with only 2 possible outcomes and its success probability equals retrievability
<!--LEARN:wnWRgMbN-->

What is considered a reasonable % retention to set for SR?
?
70-97% retention
<!--LEARN:4WZNxG4F-->

# References
1. https://github.com/open-spaced-repetition/fsrs4anki/wiki/Spaced-Repetition-Algorithm:-A-Three%E2%80%90Day-Journey-from-Novice-to-Expert