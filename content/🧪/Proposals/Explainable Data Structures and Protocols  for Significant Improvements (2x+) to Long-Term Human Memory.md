# Summary

Today the average person does not have a structured explainable database within their own mind, and collectively humans lack the type of database that can be augmented by fellow humans’ and computers’ databases in an scalable and explainable manner. This applies both to short-term and long-term memory. 

This proposal is a mesh of known human memory techniques across history and basic computer data structure knowledge. **This combination into a set of structures and protocols seems like it could increase the following by 2x+:** 

- **Human long-term memory retention of text**
- **Human memory retrieval speed and accuracy of text**

Though the below are harder to measure, it seems reasonably likely that this framework will also aid in:

- **Space efficiency of human memory storage** 
- **Augmentation of a person’s learning, retention, and recall alongside a computer or AI system**

In this proposal, we discuss isomorphic data structures shareable between combinations of human and machine long-term memory. The main components are: a computer memory schema, a human memory schema, and a protocol for the interaction of any of the 3 combinations of schemas. With this memory schema established, a person can then augment their learning, retention, and recall with a LLM-powered system that generates material following the schema, based on some reputable source material.

# Related Works
### There are old techniques to improve human short-term and long-term memory used by memory experts today

A fascinating point of human history is that variations of memory palaces and other techniques were discovered independently throughout the globe, from England to the Polynesian Islands. These memory techniques include pegs, memory palaces, and lukasa boards. Techniques that are multimodal are usually more effective, including visual, spatial, kinesthetic, and aural representations of data. Narratives and unique visualizations also improve efficacy. 

The method of loci was documented in about 500 BC from the Ancient Greek poet Simonides of Ceos , although it is likely that forms of using loci and other techniques existed prior in both Greece and other parts of the world. [18] The “science” of memory emerged in about 1850, starting with Hermann Ebbinghaus’s memory retention experiments. [18] 

Today, memory techniques are most widely used in professions that require large amounts of memorization like medicine, in memory competitions, or in oral cultures like the Australian Aboriginals. 

For example, medical students use engaging visual scenes to memorize. With a combination of memory palaces and spaced repetition, one medical learning company Sketchy touts that 96% of their students who use Sketchy have higher exam scores. [15] Here is an example of a scene that is used for USMLE prep:

![](https://lh7-us.googleusercontent.com/iM6XvZxG4lYACzOnVoqYsWA0Sg2IJRA0UD-m8UzHVS3ZAZfCAaNcTAlgqHVUfr8WZtyjkz_JxaxwhJBm-y7xynajoWWgx6BbArTXjZZRqPsetD9H8m1FWEEyT35WQpITW7wDORxUy_39A23uQqJfITc)
[14]

Sketchy’s success for future surgeons demonstrates memory techniques have practical application in the modern world.

There are additional opportunities for technique improvement. World record holders for memory competitions can memorize 630 digits in 5 minutes, 224 people’s names in 15 minutes, or 7485 binary digits in 30 minutes. [16] It has been observed that the world’s best memorizers do not have different brains from the average person’s, but rather it was their use of techniques such as the method of loci that led to substantially improved memorization abilities. [19] 

Spaced repetition is a complementary tool with memory palaces to retain memorizations long-term, by utilizing Ebbinghaus’ forgetting curve. Since Ebbinghaus established the experimental study of memory, additional techniques for human long term and short term memory have been studied in neuroscience. 

Limitations of human memory techniques are distracting or meaningless images, as well as potentially inefficient methods that encode the same information in multiple modalities or symbols. 

### Machines are much faster at deterministic computation 

With rough napkin math, computers in 2023 are at least 17 million times faster at computing deterministic functions than humans. 

Since the first substantial computer in 1946, the capabilities of a single unassisted computer to compute arithmetic with 100% accuracy, barring hardware issues, has exceeded that of any single unassisted human given the same amount of time. [2] While it remains unclear how to measure human compute and memory, based on empirical data it remains true since the ENIAC that any deterministic function that can be calculated by a human can be computed more quickly by a non-theoretical computer. 

Per Moore’s observation, compute capabilities have roughly doubled every two years since 1970. [1] From 1971 to 2019, commercial microprocessors have increased their number of transistors from approximately 2,300 to 39.54 billion. [6, 7] This means that microprocessors have increased their number of transistors by a factor of approximately 17 million. 

### Analogy between CRUD and human memory operations

Analogous to computer memory, human memory can be broken down into encoding, storing, and retrieving information. [17] From an educational lens, these are respectively named learning, retention, and recall.

The fundamental data operations of a REST API are CRUD: Create, Read, Update, and Delete. Similarities are most apparent between between the first half of CRUD representing explainable machine memory and human memory:

- Create : Encoding
- Read : Retrieving

The analogy breaks down with the Update and Delete methods. A person cannot consciously choose to delete a single memory. As for updating, neuroscience research seems to show that memory updating happens in concurrence with encoding, storing, and retrieving.

Another difference is that character-level accuracy in retrieval is taken as a given for computers at the CRUD level of abstraction. This is not necessarily the case for humans.

# Implementation Plan: A shared schema between mutual explainable human memory (MEHM) and mutually explainable computer memory (MECM)

## Definitions
- Loops: Processes that lead back to themselves. 
- Level-crossing: Loops that cross layers.
- Strange Loops: Level-crossing processes that lead back to themselves.
- Isomorphism: A mapping or correspondence between two structures in such a way that each element in one structure has a corresponding element in the other structure. [18]
- Keyword: a string used to access a specific human memory structure.
- Explainable: An adjective to describe a concept that can be stored and retrieved in a similar enough format. It is similar enough based on the concept’s domain and the retriever’s objective(s), memory capabilities, and the external tools they have at their disposal for the objective(s). 
- Mutually explainable (ME): a concept that is explainable to both humans and computers. For a more precise definition, we consider a concept to be explainable if it can be understood by any college-educated American in 2024 or computed by a 15-inch M2 chip 2024 Macbook Air. 

## Design considerations

Assume the following are traits shared by both human and computer data structures in this configuration:

- Nodes are accessible by keywords
- Recursively decomposable
- Uniquely, recursive decomposability means theoretically infinite higher and lower levels. For integers:
	- Level 0 = base
	- Levels [-infinity, -1] = higher levels
	- Levels [1, infinity] = lower levels
- Version history 
- Annotatable base
- Multimodal
- Uses memory techniques that balance needs for space efficiency, speed of learning and retrieval, within the context of some objective
- Decision-making mechanism for prioritizing knowledge to store is based on (1) observable truth, (2) credibility, (3) useful outcomes
- Reduce loss between combinations of human and machine schemas
- Deterministic finite automata with version control?

![](https://lh7-us.googleusercontent.com/KDPB-x0xVPKhywjK8MtcrP8h_jqTyLx8M__jXXssIvUw5eY5GJqhPJh0znzkUenH7yZSXeHydRJmsL-iRZlAZIRmfHrkQbs06zyia4tAv-K9tPS4T9g2C4EDPwxj-FnGZvitXjWwETSBDb52kpnv0Mg)

[Pseudocode for finding a loci in a recursively decomposable memory structure](https://www.figma.com/file/UlWaYeg7cColl3iFy8VGab/Explainable-Data-Structures-for-MEHM-and-CEHM?type=whiteboard&node-id=12-998&t=yGNh4c50F4qSaI1M-4) 
## Schemas

Consider the following schemas for Mutually Explainable Memory:
![](https://lh7-us.googleusercontent.com/ULIsgzkAebtWNfz5X6lA8zowOxo98h8WT33Cy2L_D5GgnqB_mk_l8UYGE7-ZOulV21uLYhJBFFspor317ScfKmRzIZDBmU9U2boEnwiP1T3FUO2djr8sZE-g4TegpDW7a57osW2OotEmJmsoSWyf4OQ)

[Locus in human memory](https://www.figma.com/file/UlWaYeg7cColl3iFy8VGab/Explainable-Data-Structures-for-MEHM-and-CEHM?type=whiteboard&node-id=1-777&t=yGNh4c50F4qSaI1M-4) 

**![](https://lh7-us.googleusercontent.com/QgoLGqnHmlnpHhklEqfFHIayGhvjUGLYaoWesD_4yHsSzlsglY9wzjA69_MBi7aTNBh443fFiwEV_dD4mL6_jldsXAp-O9Faq-Qh4aFm75yqpTpL6t5zH4O3zLgMZRkEzJlc-UCy1MX8nKWog6FfBbs)**

[Scene in human memory](https://www.figma.com/file/UlWaYeg7cColl3iFy8VGab/Explainable-Data-Structures-for-MEHM-and-CEHM?type=whiteboard&node-id=1-855&t=yGNh4c50F4qSaI1M-4)

![](https://lh7-us.googleusercontent.com/XMtahWYtjGsGI47YLRC6HHv2vlAsMD3OehS7oPjECSD2ZKjxPStyKhQH9AqSSJ0XtnnDi1YjlMpsDOFvZJ_-9pc5oVW4AcG26vDttf52VxzEb07tZyVO7yWyZ_IzHcG7rRSdPWgPIxYYyRKpQMnPSKE)

Sketch of [Crossing levels](https://www.figma.com/file/UlWaYeg7cColl3iFy8VGab/Explainable-Data-Structures-for-MEHM-and-CEHM?type=whiteboard&node-id=1-855&t=yGNh4c50F4qSaI1M-4) 

Note that level-crossing loops, scene-crossing, same-scene loops are all allowed.
## Isomorphisms between MEHM and MECM
Memory techniques can roughly be linked to these data structures:

| MEHM                              | MECM                                        |
| --------------------------------- | ------------------------------------------- |
| Narrative Scroll                  | Linked List                                 |
| Memory Scene, Visual Alphabet     | Hash Map / Hash Table / Object / Dictionary |
| Memory Palace                     | Graph                                       |
| Peg Method                        | Array                                       |
| Bestiary                          | Unordered Set                               |
| PAO, Major System, Dominic System | String / Integer / Float                    |

Against, by definition an isomorphism is not strictly equal to its source. For different applications and domains, we may consider differing flexibility of isomorphisms. I speculate that the greater the flexibility in isomorphism, the less efficient the method. 

On another point, the more isomorphisms that a source has, the more long-lasting that method may be. 

## Protocol for combinations of ME human and computer interaction


![](https://lh7-us.googleusercontent.com/LeKB_MURLqfIKKUMlDHQS1-4B1KxQ-iBwAc8jyxNYZ2t89zhrhan4fDyy2HwlD6SwS61x26MuCjF31dG1AadRL9_nOht2hs6qK7lyfoAp_xp4PuT67RZr2rU6PyUz-ihDu_7mfBoBtvq7Ki5Xby5oM4)

[3 interactions](https://www.figma.com/file/UlWaYeg7cColl3iFy8VGab/Explainable-Data-Structures-for-MEHM-and-CEHM?type=whiteboard&node-id=1-776&t=yGNh4c50F4qSaI1M-4): computer to computer, human to computer, human to human

Taking into account the schemas for human and computer memory from 2.2 and 3.2 respectively, we propose the following protocol for interaction.

# Evaluation Plan

Roughly, we'd like to measure:

- Speed in memory learning and retrieval
	- Quantity and speed benchmarks from standard beginner memorizers to current world records for memory
- Long-term retention
- Group organization
- Cross-Agent communication across Human and Computer instances
- Retention of rich multi-modal information
- Effective Distribution at Scale

I still need to research what the industry standards look like to measure these well! 

# Risks to execute

The following topics require further thought and experimentation: 
- What are the limits of the mediums of knowledge that can be represented in this structure? e.g. highly abstract fields such as physics haven't benefited much from memory techniques in the past
- How does speed retrieval change as the number of levels increases? 
- Risks of level-crossing loops
- How to address for Update and Delete equivalents in human memory. e.g. How do you make updates to memorized areas?
- Recursion is memory intensive for computers and it lends that it may also be so for humans
- What does a shortcut for human memory retrieval look like?
- Self-reference
- Long-term retention mechanisms
- Propagation mechanisms
- How to measure human memory limitations?
- **Important**: how can we use LLM-powered systems to generate data that follows this shared schema and speed up the creation of a memory base?
- **Important**: the role of spaced repetition for long-term retention

# Implications if it works
People everywhere are able to learn way faster!

# Citations

[1] [https://en.wikipedia.org/wiki/Moore%27s_law](https://en.wikipedia.org/wiki/Moore%27s_law)

[2] [https://homepage.cs.uri.edu/faculty/wolfe/book/Readings/Reading03.htm#:~:text=First%20Computers&text=The%20first%20substantial%20computer%20was,like%20previous%20automated%20calculators%2Fcomputers](https://homepage.cs.uri.edu/faculty/wolfe/book/Readings/Reading03.htm#:~:text=First%20Computers&text=The%20first%20substantial%20computer%20was,like%20previous%20automated%20calculators%2Fcomputers).

[3] [https://en.wikipedia.org/wiki/G%C3%B6del_numbering](https://en.wikipedia.org/wiki/G%C3%B6del_numbering)

[4] [https://www.cnn.com/videos/business/2022/05/11/ibm-deep-blue-computer-beats-garry-kasparov-chess-champion-1997-vault-jg-orig.cnn#:~:text=More-,In%201997%2C%20an%20IBM%20computer%20beat%20a%20chess,champion%20for%20the%20first%20time&text=%22He%20can't%20believe%20it,IBM's%20computer%20named%20Deep%20Blue](https://www.cnn.com/videos/business/2022/05/11/ibm-deep-blue-computer-beats-garry-kasparov-chess-champion-1997-vault-jg-orig.cnn#:~:text=More-,In%201997%2C%20an%20IBM%20computer%20beat%20a%20chess,champion%20for%20the%20first%20time&text=%22He%20can't%20believe%20it,IBM's%20computer%20named%20Deep%20Blue).

[5] [https://www.scientificamerican.com/article/google-engineer-claims-ai-chatbot-is-sentient-why-that-matters/](https://www.scientificamerican.com/article/google-engineer-claims-ai-chatbot-is-sentient-why-that-matters/) ““I I didn’t know exactly what it was, which is this computer program we built recently, I’d think it was a 7-year-old, 8-year-old kid that happens to know physics,” he told the Washington Post.”

[6] http://scihi.org/intel-4004-microprocessor/#:~:text=Intel%204004%20Design,built%20of%20approximately%202%2C300%20transistors.

[7] [https://www.guru3d.com/news-story/amd-epyc-rome-cpus-contain-hold-almost-40-billion-transistors-per-chip.html#:~:text=A%20Rome%20CPU%20consists%20of,has%20only%209.89%20billion%20transistors](https://www.guru3d.com/news-story/amd-epyc-rome-cpus-contain-hold-almost-40-billion-transistors-per-chip.html#:~:text=A%20Rome%20CPU%20consists%20of,has%20only%209.89%20billion%20transistors).

[8] [https://en.wikipedia.org/wiki/Explainable_artificial_intelligence](https://en.wikipedia.org/wiki/Explainable_artificial_intelligence)

[9] Acronym inspired by LIPS - LIPS Is Pretty Simple [https://lips.js.org/](https://lips.js.org/)

[10] [https://www.spiceworks.com/tech/devops/articles/application-programming-interface/#:~:text=Step%201%3A,originally%20requested%20it](https://www.spiceworks.com/tech/devops/articles/application-programming-interface/#:~:text=Step%201%3A,originally%20requested%20it).

[11] [https://en.wikipedia.org/wiki/Communication_protocol](https://en.wikipedia.org/wiki/Communication_protocol)

[12] [https://developer.nvidia.com/blog/best-practices-explainable-ai-powered-by-synthetic-data/](https://developer.nvidia.com/blog/best-practices-explainable-ai-powered-by-synthetic-data/)

[https://www.ibm.com/watson/explainable-ai#:~:text=Explainable%20artificial%20intelligence%20(XAI)%20is,expected%20impact%20and%20potential%20biases](https://www.ibm.com/watson/explainable-ai#:~:text=Explainable%20artificial%20intelligence%20(XAI)%20is,expected%20impact%20and%20potential%20biases).

[https://cloud.google.com/explainable-ai](https://cloud.google.com/explainable-ai)

[13] [https://www.psych.ualberta.ca/~cml/papers/Legge_et_al_2012.pdf](https://www.psych.ualberta.ca/~cml/papers/Legge_et_al_2012.pdf)

[14] [https://www.sketchy.com/explore/medical](https://www.sketchy.com/explore/medical)

[15] [https://www.sketchy.com/](https://www.sketchy.com/)

[16] [https://en.wikipedia.org/wiki/World_Memory_Championships#WMSC_world_champions_(2017%E2%80%93present)](https://en.wikipedia.org/wiki/World_Memory_Championships#WMSC_world_champions_(2017%E2%80%93present))

[17] [https://www.jneurosci.org/content/29/41/12711](https://www.jneurosci.org/content/29/41/12711) Squire, L. R. (2009). Memory and brain systems: 1969–2009. J. Neurosci. 29, 12711–12716. doi: 10.1523/jneurosci.3575-09.2009

[18] Hofstadter

[19] Memory history [https://www.sciencefocus.com/the-human-body/memory-a-timeline-of-discoveries/](https://www.sciencefocus.com/the-human-body/memory-a-timeline-of-discoveries/)


---

# Misc.
- [*Longer, messier version on GDocs*](https://docs.google.com/document/d/1sbyuGx8mNOJVPqbUSmoDNqQyJEXJybvT-KkUkXaI5Nk/edit)
- [Figma Diagrams](https://www.figma.com/file/UlWaYeg7cColl3iFy8VGab/Explainable-Data-Structures-for-MEHM-and-CEHM?type=whiteboard&node-id=0-1&t=yGNh4c50F4qSaI1M-0)
- Inspiration from Hofstatder’s GEB, Godel, Turing, and many interesting lectures and conversations across the Bay Area
