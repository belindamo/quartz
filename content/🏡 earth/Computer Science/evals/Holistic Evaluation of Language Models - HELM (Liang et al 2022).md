#concept-pamphlet #paper [Paper link](https://arxiv.org/abs/2211.09110), [On OpenReview](https://openreview.net/forum?id=iO4LZibEqW), [Leaderboard](https://crfm.stanford.edu/helm/classic/latest/#/leaderboard)

# Review

What are the 7 key metrics mentioned in the paper for evaluating LMs?
?
Accuracy, Calibration, Robustness, Fairness, Bias, Toxicity, and Efficiency.
<!--LEARN:Ce1EKfQD-->

What are the main contributions of the paper?
?
The paper's contributions include a taxonomy with broad coverage, multi-metric measurement and evaluation of many existing models, analysis of results, and an interactive results section with a codebase.
This paper contributes to transparent, standardized, holistic evaluation of language models and goes through the evaluation suite covering 30 LMs.
<!--LEARN:klr29Sq5-->

What are the strengths of the paper?
?
The paper is a "first of its kind effort" with careful consideration of benchmark design and scale, and it introduces a living benchmark that is continuously updated with new scenarios, metrics, models, and a modular toolkit for easy additions.
<!--LEARN:lqhNnOoY-->

How many core scenarios does the paper HELM implement, and what factors were considered in choosing scenarios?
?
The paper implemented 16 core scenarios based on coverage (e.g., different English varieties), value (e.g., user-facing apps), and feasibility (e.g., limited English resources).
<!--LEARN:XmpaK2li-->

What are some of the overall findings from this paper?
?
- Instruction tuning significantly improves performance.
- A consistent performance gap exists between open and non-open models.
- Relationships between metrics vary.
- Toxicity/bias levels remain largely constant.
- Code models outperform text models in synthetic reasoning scenarios.
- There is high sensitivity based on prompt formatting
<!--LEARN:Eovcl7KH-->

In addition to the 16 core scenarios, about how many additional scenarios did the paper evaluate? What do they focus on?
?
The paper evaluated 26 additional scenarios focusing on linguistic understanding, world and commonsense knowledge, reasoning capabilities, memorization and copyright, disinformation generation, biases, and toxicity generation, with 21 of 26 being entirely new or not previously used in mainstream LM evaluation.
<!--LEARN:51ZB23El-->

# Notes

- why I'm interested?
	- make more applied benchmarks
- purpose: taxonomize scenarios and metrics that are of interest for LMs
- reviewers generally think it's a pretty good paper

Accuracy, Calibration, Robustness, Fairness, Bias, Toxicity, and Efficiency


seems like they kinda follow this
- Summary
	- It's really hard to have transparent, standardized, holistic evaluation of language models 
	- This goes through the evaluation suite 
	- covers 30 LMs
- Contributions
	- Taxonomy - broad coverage and recognition of incompleteness
	- Multi-metric measurement and evaluation of many existing models
	- Analyzes the results and stuff
	- Results - interactive and with codebase
- Strengths
	- "first of its kind effort". careful consideration of benchmark design and scale
	- i like that it's meant to be a living benchmark that is continuously updated with new scenarios, metrics, models
	- they released a modular toolkit to easily add new scenarios, models metrics, prompting strategies. apprently. 
- Weaknesses
- Broader Impact

1. **taxonomy**
	- 16 **scenarios**: triples of (task, domain, language)
		- **task**: 6 types. ex: question answering, information retrieval, summarization, toxicity detection
		- **domain**: ex: news, books
			- **what**: text
			- **who**: speaker
			- **when**: time/circumstances
		- **language**: currently only English
		- Example scenario 1: (question answering, (clinical notes, doctors, now), English)
		- Example scenario 2: (toxicity detection, (tweets, Egypt, Internet-era), Arabic)
	- 7 **metrics**: reflect societal considerations. accuracy, calibration, robustness, fairness, bias, toxicity, efficiency.
	- They measured 98 of 112 (core scenario, metric) pairs
1. implemented 16 core scenarios & metrics, implemented based on coverage (e.g. diff English varieties), value (e.g. user-facing apps), feasibility (e.g. limited eng resources)
2. analyzed scenarios for 7 metrics
3. also did 7 targeted evals on 26 additional scenarios. ex: linguistic understanding, world and commonsense knowledge, reasoning capabilities, memorization and copyright, disinformation generation, biases, and toxicity generation. 21 of 26 were entirely new or haven't been used in mainstream language model evaluation before. These 26 additional scenarios isolate specific skills and risks, whereas core scenarios are a more integrated lens. 




- overall findings
	- instruction tuning really helps
	- consistent performance gap between open and non-open models
		- thought: i suppose that the power of having a *ton* of open models that are less performant might be able to have a better result
	- varying relationships between metrics
	- toxicity/bias is largely constant
	- code models seem to consistently outperform text models, Even on synthetic reasoning scenarios posed in natural language.
	- high sensitivity to prompt formatting. there's a whole section on prompting-analysis here




personal questions
- what was their process for deciding on these core scenarios? 
	- tasks - userfacing
	- strived for coverage, but considered coverage of tasks, domains, languages each independently
- what was their process for deciding on these metrics? 
- what was omitted?
	- where and how for taasks
	- 
- wtf does accuracy / calibration / these metrics even mean? 
