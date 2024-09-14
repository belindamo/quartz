#concept-pamphlet #paper [2024 Paper](https://arxiv.org/pdf/2403.04132) 

# Notes
## Key terms
- **Bradley-Terry model**
- **BT-coefficients**
- **win matrix estimation**
	- matrix that shows likelihood of a model winning
- **active sampling rule**: to choose the model pair a ∈ A proportionally to the reduction in confidence interval size by sampling that pair:
	- this is the rule to decide which model pair to show
	- ![[Screenshot 2024-07-02 at 3.10.04 PM.png]]
- **anomalous user detection**


limitations...
- all chats are treated the same. 1 big bucket of chats, 1 win matrix estimation for all chats

## Main contributions of the paper

how is data gathered? >> user can ask a question and get answer from 2 anon LLMs. User casts vote for model preferred, and then identity is revealed

- question: what statistical techniques do they use to estimate the ranking over models as reliably / sample-efficiently as possible? 
	- sampling algorithm: select model pairs to accelerate convergence of rankings
- in the first year since Apr 2023 release, how many votes from how many users does chatbot arena  have? >> 240k votes, 90k users
- how did they encourage usage? 
	- over 50 SOTA models for free from OpenAI, Google, Anthropic, Mistral, Hugging Face, and various universities
	- community engaged by routinely updating leaderboard, releasing datasets, tweets, publish blogs
- public release?
	- human preference dataset with over 100k pairwise votes collected from Chatbot Arena

human preference dataset format
?
![[Screenshot 2024-07-01 at 10.20.26 PM.png]]

- Elo rating: accelerate ranking convergence and detect abnormalities

other papers
- elo
	- Bai et al 2022. anthropic HH
	- boubdir et al 2023. 
	- Kopf et al 2023. OpenAssistant conversations 
	- learning to rank: Liu et al 2009

uses Bradley-Terry model, which is a standard model used for pair-wise comparison, where the probability of one item being preferred over another is modeled using a logistic function of the difference in their parameters.
In the Bradley-Terry model, Ht ∈ {0, 1}, and the probability model m beats model m′ is modeled via a logistic relationship:
![[Screenshot 2024-07-02 at 3.07.49 PM.png]]
where ξ is an M-length vector of so-called BT coefficients. Without loss of generality, we take ξ1 = 0 (since the model is invariant to addition in ξ). Our goal is to estimate the population Bradley-Terry coefficients, i.e., those that minimize the binary cross-entropy:
![[Screenshot 2024-07-02 at 3.08.05 PM.png]]
where ℓ is the binary cross-entropy loss, `ℓ(h, p) = −(h log(p) + (1 − h) log(1 − p))`.


https://chatgpt.com/share/e/7070dc80-6fdb-43e3-ace1-658917577253
## Pros and Cons of the paper
- Strengths
	- 
- Weaknesses
	- 

## Questions & Discussion Items 



