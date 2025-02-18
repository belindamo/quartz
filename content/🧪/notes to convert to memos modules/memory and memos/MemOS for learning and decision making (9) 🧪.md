
title: How can a hierarchical memory system help people align their values→goals→actions alongside aligning with an LLM-powered system?

problem: People struggle maintaining coherent mapping from values→goals→actions over time. LLMs lack clear mechanisms to help with this value-goal-action alignment. People should be in control of their own prioritization/mapping, and memory. 

bit: Current systems either:

- Store information without value-goal hierarchy
- Jump to AI assistance before self-alignment
- Miss the critical values→goals→subgoals→actions chain
    

flip: 

Provide reasoning traces based on the person’s knowledge base.
Specifically, the hierarchical memory system:

1. Helps person map their own values→goals→actions
2. Is compatible with AI, where it is in the loop to:
	1. Prune
	2. Reflect
	3. Learn
	1. Act
    

instantiate solution: A staged system where:

1. Person builds values→goals→subgoals→actions hierarchy
2. AI suggestions only introduced after clear self-alignment
3. System helps maintain/reflect on these connections using FSRS/recurring schedules
    

method:

- Have an existing knowledge base in evergreen format and confidence tags. 
- Do value hierarchy mapping
- Break into measurable goals/subgoals
- Connect to concrete actions that are validated with external evals    

### principles

"Plain text is preferred"

"Do one thing and do it well" (each program/agent focuses on a single task)

"Everything is a file" (applied to both devices/processes and software functions)

"Script shell automation"

"Silence is golden" (output only meaningful info)

  

### motivations for project

I'd really love to have a good learning and decision making system. I think that this would simply consist of embeddings, knowledge unit graph hierarchies (text first), evals.

Creating a garden. The garden is pruned over time. The system helps bring things up to review. So you are in control of the things you'd like to remember. Recurring vs. remembering for long term. For all levels... for me, I think about my values, my reflections, my learnings, relationship reminders. It is a system for helping align myself with myself, and also for a model to align with myself.

In other words, we may construct a pattern language. I may label how important/confident I am in this. The original pattern language has: Problem, Solution, Related Patterns (in Natural Language).

We may look at pattern languages, evergreen notes, dalio's principles, the Bible...

In this case, we may see that each note may be treated as an eval. Each note asserts how things should be. Each note may have its own criteria. But at the end of the day, we may see that each note is an eval.

The beauty of such a system is that anyone who can read and write may use it. It helps anyone with any set of beliefs align their beliefs, thoughts, and actions. It also helps them align these things with any LLM-powered system that may make decisions or actions on their behalf. This system, I imagine at least to start, relies on in-context learning. The important pieces of this are the retrieved notes and their subgraph; these pieces may provide a traceable reasoning so that the person may make informed decisions for whether to accept or reject the system's suggestions.

RAG, evergreen notes, and so forth already exist, but they do not have mechanisms for long-term human/machine alignment (which also includes human-self, machine-self, and later human-human, machine-machine).

It does seem like natural language text is the best format. Though it is not as precise as code or math, it is richer - natural language compresses many meanings together and may be interpreted differently depending on richer contexts. How beautiful! I also don't see people communicating irl in code, proofs, or binary anytime soon. So natural language text seems like a safe bet.

What can we do once this beautiful garden exists? Well, a lot. 

A person could tend to their own garden - rewriting tidbits, making new notes, adding connections, trimming notes. The system can also do this, either automatically or by providing suggestions to accept, reject, or modify. In tending their garden, the person tends their mind.

A person can admire their garden - recalling bits of information that are delightful to revisit, like an old friend. The system can help bring forward these bits, especially as the garden grows with age. This act brings delight, joy, peace - what makes the contemplative life worth living.

Perhaps a person wants to deeply understand a specific section of their garden. They'll visit it more frequently, with more intensity. The system can help provide a schedule so that the person can focus on understanding as opposed to the logistics of remembering to understand.

Lastly and perhaps most ambitiously (when the time is right), a person takes action based on what they've maintained, observed, and understood about their garden. The system, showing proof of its past performance on particular tasks and with the person's permission, can even do this on the person's behalf. If the person really trusts the system, it could even do these tasks on a recurring schedule, or even autonomously at its discretion.

Thus, we've covered a personal learning, reflection, decision making, and execution system that interleaves each of the 4 components that a human or machine may do. This is only possible because human and system have a shared, rich context that is:

- thoughtfully reviewed: items are brought up at the appropriate times efficiently, based on desired retention and importance. You are in control of your memory.
- life-long: it is evergreen, meaning it is always changing
- explainable to both: you may trace reasoning in natural language that is written for by you
- can be private to the outside world, so it may be intimate and true
- written only with things that you've agreed feel true to you
- version controlled: to mark key milestones and growth