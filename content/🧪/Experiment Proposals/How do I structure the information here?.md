---
draft: "true"
---

🌳 I want to be able to document and compound my existing knowledge, so that I can evolve valuable insights over time. 🌳

We are going to start by organizing the 🌳, 🧪, 🔗, and their internal folders first! 


# How do 🌳, 🔗, 🧪 interact? 
- 🌳 - **Knowledge**. Insights that can be structured as concept graphs.
- 🔗 - **Writing**. Insights that are better structured in other ways like an essay or story. 
- 🧪 - **Experiments**. Experiments to form insights. Or just to mess around 🤸🏻‍♀️

Internal folders are for my eyes only, whereas external folders contain things I would feel comfortable (enough) to have everyone else in the world see its contents.

# Organization Methods in the vault
There are a few different methods of organization in this Obsidian vault:

- **Hierarchical folders for themes** 🗂️
	- Folders represent themes, like `🌳`, `learn`, `my self`
- **Tags** 🏷️
	- Tags represent:
		- Problems in 🌳, 🧪, 🔗: A problem implies a solution.
			- Format: `#${problem id}`
			- Ex: `#a1`.  `#a1` + `source` is the source note
			- Problem id is formatted with `${character that represents the problem space}${iteration number for this statement of problem space}` and can contain nested subproblems in the future, though this quickly gets complicated so we'll try to minimize that for now. See [[Problems tree - AO#Versioning]] for details
		- Experiments in 🌳, 🧪, 🔗: An experiment is meant to find a solution to a problem.
			- Format: `#${experiment id}-${project name}-${problem ids}`
			- Ex: `#e0-tinymath-a1` `#e0-tinymath-a1` + `source` is the source note
		- Projects in 🌳, 🧪, 🔗: A project is an experiment that contains multiple experiments.
			- Format: `#proj-${project name}-${problem ids}`
			- Ex: `#proj-tinymath-a1`. `#pr-tinymath-a1` + `source` is the source note in 🧪
		- Concept Note type in 🌳: at the moment, this is just #concept  and the subtypes of concepts which are #concept-statement, #concept-question  and #concept-pamphlet. EVERY concept note should have one of these
			- #concept: e.g. title: `math`. Note that it is lowercase.
			- #concept-statement: e.g. title: `Products are the happy marriage of art and distribution`
			- #concept-question: e.g. title: `What does the architecture of a transformer look like?`
			- #concept-pamphlet : e.g. title: `Fencing`. Note that it is uppercase.
	- Note that themes like `#math` are taken out because these tags are redundant given connections. Themes should be able to be inferred by the links of concepts. e.g. [[learn/math/math]] would have an explicitly-defined relationship to [[Gödel's incompleteness theorem]], even if through an additional level or two. 
- **Connections**
	- Connections are edges to connect any association between two pages. 
	- Ideally, all these connections should have explicitly-defined relationships via Excalibrain.

# What does a good experiment look like?
It should follow the template. Latest ones are in [[Experiment System Changelog]].

# What does a good Concept Note look like? 
**Concept Notes** are Notes that are in a structured format because I want to either **retrieve**, **reference**, or **memorize** them over time. They are atomic. These will typically avoid stream-of-thought notes in those in the `grow` and `daily` folders.

Ideally, every Concept Note should be structured as follows:

![[concept note]]

The fields are:
- Tags: show the note type
- Show parents/children/related: using Excalibrain
- Self definition: >1 sentence definition in my own words of the note
- Source definition: >1 sentence definition from >=1 reputable source 
- Source(s): this may be either other notes or external links. External links should have some explanation if it is just url
- Spaced Repetition: this includes mnemonic and spaced repetition, if any

# How are problems, experiments, projects,  concepts, and statements connected to each other?

- Problems scope areas of exploration / learning to gain insights
- Experiments test Problems
- Statements, Questions come out of Experiments that test Problems
- Projects consist of a series of Experiments and are longer term
- Concepts, Statements, Questions, and Pamphlets are all part of a learning graph that is associated with an Experiment, Problem, or Project

# What's the purpose of highly structuring everything in this way? 
Being more detailed, the purpose is that I will be able to do the following:
- Have structured data that allows for increased speed/accuracy of **memory learning, retention, and retrieval**. 
	- This structured data can be used to:
		- Create spaced repetition flashcards
		- Create sense-based mnemonics. Usually they are visual-based.
	- This resulting memory system can be used for life-long retention.
- Have structured data that I can use as a base to eventually auto-generate learning graphs 
- Have structured data that is on the limits of human explainability

Related: [[Experiment System Changelog]]


