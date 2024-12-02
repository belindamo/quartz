#concept 

The Chomsky hierarchy contains `___` classes of `___` to describe increasingly complex languages
?
4, formal grammars
<!--LEARN:8PXFw8l5-->

The 4 classes of the Chomsky hierarchy, from most complex to simplest.
- `___` enumerable (turing machine)
- context-sensitive (turing machine but with finite tape)
- `____` (finite state, finite memory)
- regular (finite state)
?
![[Pasted image 20230801100034.png]]
In the Chomsky hierarchy, the simplest grammars are regular, and can be accommodated by finite state automata.  The next most complicated are context-free grammars, which can be processed by pushdown automata (a device that is a finite state automaton with a finite internal memory).  Next are the context-sensitive grammars, which are the domain of linear bounded automata (i.e., a device like a Turing machine, but with a ticker tape of bounded length).  The most complex grammars are the phrase structure grammars, which can only be dealt with by Turing machines. [2]
### References
1. https://en.wikipedia.org/wiki/Chomsky_hierarchy
2. http://www.bcp.psych.ualberta.ca/~mike/Pearl_Street/Dictionary/contents/C/Chomhier.html#:~:text=The%20most%20complex%20grammars%20are,theoretical%20proposals%20within%20cognitive%20science.
<!--LEARN:zgpxtGiA-->

### Notes

children [[context-sensitive grammar]], [[recursively enumerable grammar]], [[context-free grammar]], [[regular grammar]]
#### Self Definition 
The Chomsky hierarchy contains 4 classes of formal grammars to describe increasingly complex languages.
 
#### Source Definition

The **Chomsky hierarchy** (infrequently referred to as the **Chomsky–Schützenberger hierarchy** in the fields of [formal language theory](https://en.wikipedia.org/wiki/Formal_language "Formal language"), [computer science](https://en.wikipedia.org/wiki/Computer_science "Computer science"), and [linguistics](https://en.wikipedia.org/wiki/Linguistics "Linguistics"), is a [containment hierarchy](https://en.wikipedia.org/wiki/Hierarchy#Containment_hierarchy "Hierarchy") of classes of [formal grammars](https://en.wikipedia.org/wiki/Formal_grammar "Formal grammar"). A formal grammar describes how to form strings from a language's vocabulary (or alphabet) that are valid according to the language's syntax. Linguist [Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky "Noam Chomsky") theorized that four different classes of formal grammars existed that could generate increasingly complex languages. Each class can also completely generate the language of all inferior classes.
