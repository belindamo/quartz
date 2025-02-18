---
tags:
  - joy
  - external-experiment
  - virtuous-loop
type:
  - proposal-only
claim type:
  - bounding x
theme:
  - agents
  - duplicate-self
est. time: One week
problem: There has yet to be a breakout consumer version of an A.I. assistant that can be used for practical granular tasks like admin tasks.
bit: Existing agents are browser-based and require step-by-step task walkthroughs, placing the initiation and mental load on the user.
flip: Tasks are done in the background without the user needing to initiate or think about them, with a user-friendly interface.
instantiate solution: A mobile browser application accessible via phone number, offering a suite of localized tasks and background task execution for tasks like paying parking tickets. Utilize Next.js, Tailwind with ShadCN for CSS, and GPT for creating the agent. Automation may use Selenium or network requests.
method: Develop a mobile browser application using Next.js, Tailwind, ShadCN, and GPT. Automate tasks with Selenium or network requests.
evaluation: Success based on regular usage by three friends known for receiving parking tickets over one week and one month periods.
implications: Developing successful agents could lead to more agents that automate manual tasks, improving quality of life.
related works: Multion and Zapier.
eval plan:
  - IV: Local-first data storage, mobile browser-based access, agent-initiated interactions.
  - DV: User retention and perceived usefulness.
  - Task: Develop a suite of agents for tasks like paying parking tickets.
  - Threats: Feasibility of running agents locally and automation robustness for tasks.
---

try writing using AI..


I’ve been thinking about doing a personal assistant that is effectively a clone of yourself, where you feed it in all of your personal data 
It’s all local first and therefore private. User has full control of their data  
Sooo no server storage costs :p and also more ethical imo 
Voice first interface


Flow:
1. User connects their obsidian, google cal, social media accounts, etc. Auth tokens for these accounts are the only thing this software stores
2. This data is converted to embeddings. These are stored locally on user device by default, or their choice of cloud storage
3. Knowledge graphs are generated to scaffold the embeddings for easier search and human explainability (I can share more on this later to explain)
4. User has a finite set of tasks that they can choose. For example, “I want to buy a suitable coat on Amazon for the winter”. We have existing evals for each task, and that can be run to ensure this works
5. Knowledge graph retrieves context scope/embeddings -> RAG runs on scoped embeddings ->  this updates the prompt so it personalizes the agent run (like searching Amazon for a beige peacoat instead of a coat)
6. Agent does the task, although it always stops right before entering any personal identifying info on the site, or doing a purchase action


How is this project distributed? 
- a series of publicity events on the tasks! Each task can be publicized 
- TikTok is a hella strong viral channel that is underutilized with AI products because engineers don’t understand the social value of TikTok lol

I have a really good idea of what distribution through insta/tiktok would look like lol. I see these small businesses that do demos of their products all the time on their pages, but with physical products. And they restock their products only every Sunday and sell out hella fast.


There is one more part of this, which is regarding a self organizing hierarchical system of components, where each component could be a function, model, or variable. Models are retrained upon self organization 



Flow:
1. User connects their obsidian, google cal, social media accounts, etc. Auth tokens for these accounts are the only thing this software stores
2. This data is converted to embeddings. These are stored locally on user device by default, or their choice of cloud storage
3. Knowledge graphs are generated to scaffold the embeddings for easier search and human explainability (I can share more on this later to explain)
4. User has a finite set of tasks that they can choose. For example, “I want to buy a suitable coat on Amazon for the winter”. We have existing evals for each task, and that can be run to ensure this works
5. Knowledge graph retrieves context scope/embeddings -> RAG runs on scoped embeddings ->  this updates the prompt so it personalizes the agent run (like searching Amazon for a beige peacoat instead of a coat)
6. Agent does the task, although it always stops right before entering any personal identifying info on the site, or doing a purchase action


related::[[AI Theorem Proving for International Math Olympiad Problems]]