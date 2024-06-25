Test select combinations of these 5 variables: 

**Concept subject x Representation captureMethod x Representation captureModality x Representation type x Representation type config**

## Subject

```
{
	symbolic: [ 
		'Math' // Math, Physics
		| 'Programming' // Computer science
		| 'Natural Language' // French, English, law, Biology
		| 'Processes' // Multistep. Chemistry, Biology
	]
}
```

## Concept

```
{
	id: string // as opposed to typical ids, this should be memorable
	subject: Subject,
	sources: string[],
}
```

## Representation of concept

```
{
	concept: Concept
	captureMethod: [ // single select
		| 'human-only' // user only
		| 'complete' // user gives a prompt and AI completes. no change.
		| 'complete-edit' // user gives a prompt, AI completes, user edits
		| 'conversation' // chat conversation
	],
	captureModality: [ // May select 1+
		'verbal',
		'type',
		'handwrite'
	],
	notes: Note, // Note can be text, image, audio, etc.
	type: Flashcard | MemoryPalace,
	options: {} // options to input into the type 
}
```

#### Variations
- Two-sided flashcard
- Visual image 

# Measures
These measures must be tracked to improve over time.

## Track
- Time to learn a concept
- Correlation between a concept and a representation
- Average time to review a card
- Lifetime time to review a card


- Test results??? how to make sure the card is actually representative of the concept?? concept scaffolding...
- need reputable resources to scaffold
	- wikipedia



methods: 
- linear regression
- viz techniques


# Questions to consider
- Do you *really* want to remember this concept long term? 

# What I'll be testing on
- [[my learning curricula]]
- [[my memory]]
- [[memory cards]]
- [memory journal](https://docs.google.com/spreadsheets/d/1CWCd17Dk8VmWZ6-u91tPv5IoJu5wgEX_IjGImzuQrcc/edit?gid=943526167#gid=943526167)
- learn folder
- concepts in the 🌳 folder

---

https://gwern.net/spaced-repetition#background-testing-works

materials that seem to benefit from testing spaced repetition style:
![[Screenshot 2024-06-24 at 3.01.38 PM.png]]

---
# Misc.

what's immediately most useful to people? 
- learn language vocab
- pass a test to be credible in some field - GRE, LSAT, step 1, SAT, etc.

what's most useful for me?
- learn math
- learn deep learning
- have scaffolding for remembering things i learned in the past, at least the things i want to learn

