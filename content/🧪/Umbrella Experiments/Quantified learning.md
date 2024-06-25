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

# Questions to consider
- Do you *really* want to remember this concept long term? 
