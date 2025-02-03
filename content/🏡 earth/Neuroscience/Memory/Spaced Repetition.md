#concept-pamphlet 
#todo: review these too, continuing on the 3 day article
- RMSE
- HLR
- to add to [[Probability & Statistics]]


- [[🏡 earth/Neuroscience/Memory/Spaced Repetition/spaced repetition|spaced repetition]]

![[Screenshot 2024-07-29 at 12.19.28 PM.png]]

fsrs combines \____ with \____
[[SR/memory/AhzfP2mB.md|?]]
machine learning techniques, universal memory formulas
what is fsrs? >> Free Spaced Repetition Scheduler algorithm. It is an open source algorithm.
<!--LEARN:Qvil3HNH-->







what is the purpose of any spaced repetition algorithm?
[[SR/memory/L6SrOMQP.md|?]]
To help learners efficiently form long-term memories.


How do spaced repetition intervals differ with different levels of familiarity?
[[SR/memory/VpqzpMWo.md|?]]
Shorter intervals are used for unfamiliar material while longer ones are used for familiar material.


What is the role of automation/algos in spaced repetition?
[[SR/memory/5q6QPmvf.md|?]]
They automate tracking of memory states and efficient scheduling of reviews


What is the primary limitation of the SM-0 algorithm?
[[SR/memory/cPeoO74g.md|?]]
It uses a page of notes as the unit for review, making it unsuitable for tracking memory retention at a more granular level


Why did Wozniak use new materials each time he sought to establish a new review interval in his experiments?
[[SR/memory/AtkA91ep.md|?]]
To ensure uniformity in the intervals of prior reviews.


What are the advantages of breaking material down into smaller parts, for the SM-2 algorithm?
[[SR/memory/noNjmiFw.md|?]]
It allows the algorithm to find the right schedule for each individual piece of information.



What is a primary difference between SM-0 and SM-2 algorithm, besides the fact that SM-2 uses bite-sized QA pairs?
[[SR/memory/kTF5QjXm.md|?]]
SM-2 also uses Ease Factor and grades.


What's the primary difference between SM-2 and SM-4 algorithm?
[[SR/memory/fp6zuQLs.md|?]]
SM-2 algorithm doesn't account for the whole lifetime of the card. SM-4 has a matrix to represent the whole memory lifetime of a card.


In SM-4, what is the main idea, practically speaking w.r.t. reviews behind Optimal Interval matrix?
![[Pasted image 20240729122702.png]]
[[SR/memory/M8Q3VgZv.md|?]]
The main idea is that if the OI matrix says to wait X days and learner actually waits X+Y days and still remembers with a high grade, then the OI value should be changed to something between X and X+Y.
If the learner can remember something after waiting X+Y days and get a good score, the old OI value was probably too short! :p
Rows = how easy the material is
Columns = how many times you've seen it.
This matrix is continuously updated during reviews.


stability in the DSR model [[SR/memory/RoXm8oTS.md|>>]]  time required for the probability of recall for a particular memory to decline from 100% to 90%


retrievability in the DSR model [[SR/memory/EkqaXnsk.md|>>]] probability of recalling a specific memory at a given moment


difficulty in the DSR model [[SR/memory/aC41tVFU.md|>>]] the inherent complexity associated with a particular memory


what are the 3 components in the 3 component model of memory? [[SR/memory/K4yzdYPa.md|>>]] stability, retrievability, difficulty/complexity


In spaced repetition algo,
$$
I_1
$$
is...
[[SR/memory/JxTYkA4s.md|?]]
Initial interval after the first review


In spaced repetition algo,
$$
C_1
$$
is...
[[SR/memory/yr2HwyA3.md|?]]
Stability increase (SInc). Ratio of successive intervals, from the i-th interval and the preceding (i - 1)th interval


What is this equation
$$
R_n(t) = \exp\left[\cfrac{t\ln{0.9}}{I_1\prod\limits_{i=2}^{n}C_i}\right]
$$
[[SR/memory/AMUbx0oC.md|?]]
Retrievability of any given memory at time `t`.
This accounts for spaced repetition algorithms and memory models.


What are some advantages of FSRS vs. SM-2 Anki?
[[SR/memory/cG6ZHOOk.md|?]]
- 20-30% fewer reviews than with Anki's default algo
- better at schedulign cards with delays


What is one way you can think about a memory event in probabilistic terms?
[[SR/memory/fsRTcgb6.md|?]]
A memory event is a single random experiment with only 2 possible outcomes and its success probability equals retrievability


What is considered a reasonable % retention to set for SR?
[[SR/memory/NjgC2Vyw.md|?]]
70-97% retention


# References
1. https://github.com/open-spaced-repetition/fsrs4anki/wiki/Spaced-Repetition-Algorithm:-A-Three%E2%80%90Day-Journey-from-Novice-to-Expert