---
date: 2024-04-01
---

# Summary
*Problem space, Concept that exists, Concept that is being changed, How concept is being changed*

A common problem in browser script automation is ensuring the reliability of script execution given that a site's DOM can change with minimal notice. DOM changes occur whenever the site owner deploys a new change or renders front-end elements based on server-side data. This problem persists regardless of whether browser automation is AI-powered or a manually written script. 

Currently, some amount of human monitoring, or "human-in-the-loop", is still required to ensure successful task completion. Is there a way to greatly reduce the need of a human in the loop? 

In this experiment, we propose transitioning responsibility from human monitoring of an AI instance over the entire task to minimal monitoring of an AI instance for specific steps to verify a task. 

On the first run of a task, the LLM-powered system will create a browser script by having a human approve its steps in detail, step by step. The system stores the browser script with anonymized user variables, to use for future runs. Notably, future runs can be run by the same user or a different user. **Updates to a task script are crowdsourced. Whenever there is a DOM change for any user, the system will run a test against the user's execution of the task script, ideally on the user's device.** At scale, this crowdsourcing approach ensures a near continuous run of tests for each task. 

This takes inspiration from crowdsourcing initiatives like ReCAPTCHA. This also takes inspiration from the virtual DOM of front-end web frameworks like React.js. Similarly, we can create a tree of all tasks that correlates with the rendered page. We can use an AI instance to trim that tree and detect changes in specific elements that are relevant to the task at hand. 

# Related Works
- MultiON: A browser automation assistant platform.
- Selenium and Puppeteer: Tools for browser automation.

# Implementation Plan
1. A large language model generates a browser automation script. The generated automation code is suitable for both cloud and local deployment, and can also be used to generate validation tests.
2. Parts of the browser automation script are regenerated upon test failures. (Probably need some manual revision)

# Evaluation Plan
*Independent and dependent variables, Industry standard metrics and datasets to compare against*

- **Independent Variable (IV)**: 
	- Use of LLM for browser script automation, error detection, anonymizing of user data, and important DOM changes.
- **Dependent Variable (DV)**: 
	- Task success rate (%) over multiple iterations, over time
	- Rate of improvement (type: normalized number?) of task success rate, based on number of task runs
	- Other specific measures
		- Success rate (%) of user in creating browser script on the first run
		- Success rate (%) of LLM to correctly distinguish between significant and insignificant DOM tree diffs for future runs
		- Error rate in correct anonymization of user data per page (%)

# Risks to execute
- Proper anonymization of user data
- Inability to capture errors effectively in tests and AI-generated tree.
- Bot detection measures blocking information

# Implications if it works
This is a system that becomes more robust the more people that use it. I'd personally consider this system a success if for 1 task, it can reduce the task error rate by 2 orders of magnitude.


---
# misc. 

Potential issues with this proposal
- Not sure if my assumption is correct that people are actually implementing "human-in-the-loop" with an AI system traversing the web successfully in production. I'd imagine yes? Enterprise automation is more developed than consumer since there is more direct $ to be made there. And my understanding is that for consumer use cases, human-in-the-loop AI browser automation is nascent (<1 year old). 
- "At scale, this crowdsourcing approach will ensure a near continuous run of tests for each task. " -> Not sure if continuous run is important? 
- What happens when someone searches a task that does not have an exact match to previous tasks? Shortcut by using a technique like RAG to find similar tasks and use them as few-shot examples to create a browser script?
- Idea: Catch errors before users run into them by conducting 24/7 validation tests that detect diffs, (Github Actions? VM?) to ensure task consistency and functionality. 
- Which tasks work robustly enough to start with? DMV?

related::[[Back-translation for alignment of LLM generation of code,  tests, and more]]