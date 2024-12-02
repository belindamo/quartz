#paper #concept-pamphlet 
[[LeanDojo.pdf]]
# Notes

In **LeanDojo: Theorem Proving with Retrieval-Augmented Language Models**, LeanDojo is >> an open-source Lean playground consisting of toolkits, data, models, and benchmarks
<!--LEARN:ltOHbhNF-->


In **LeanDojo: Theorem Proving with Retrieval-Augmented Language Models**, LeanDojo contains fine-grained annotations of premises in proofs, which is >> valuable data for premise selection - a key bottleneck in theorem proving. 
<!--LEARN:Wa7abiBS-->

In **LeanDojo: Theorem Proving with Retrieval-Augmented Language Models**, ReProver (Retrieval-Augmented Prover) is >> an LLM-based prover augmented with retrieval for selecting premises from a vast math library. 
<!--LEARN:PROZRYnn-->

In **LeanDojo: Theorem Proving with Retrieval-Augmented Language Models**, ReProver's Retrieval Augmentation is achieved via a >> Dense Passage Retriever. Given a state as the query and library of candidate premises, this retriever gets a ranked list of $m$ premises.
<!--LEARN:GE4kQDaP-->
## Key terms

- `theorem` or `lemma` in Lean >> a formally proven mathematical statement or proposition. It is a proven fact that can be used in other proofs. 
<!--LEARN:G3XmSQAA-->
- `tactic` in Lean >> a command or method used during the proof process to manipulate the proof state and work towards proving a theorem. It is a proof step. 
<!--LEARN:Stc7Aj0q-->
	- Example tactics:
		- `rw` (rewrite) - substitute equivalent expressions
		- `exact` - proves a goal using an exact term
		- `intro` - introduce assumptions into the context
		- `simp` - simplify expression using known lemmas

q re: tactic vs. theorem...isn't a tactic technically a theorem? 

## Main contributions

Outperforms others on LeanDojo benchmark - 51.2% on LeanDojo benchmark.
26.5% success on MiniF2F

![[Screenshot 2024-11-12 at 12.03.05 PM.png]]

## Strengths and Weaknesses of paper
- Strengths
- Weaknesses
	- (potentially) it's overfitted to leandojo benchmark because it doesn't do quite so well on minif2f

## Questions & Discussion Items

Very cool things

- extracts lots of info that mathlib doesn't have itself
	- file dependencies and ASTs. 
		- AST is made of each file. 
		- Big graph made where nodes are files and edges are import relations. TODO-rr
- all tactics are extracted as proofs! 
- premises are recorded from where it is defined and used


method of retrieval
- dense passage retrieval. and with --
- for a theorem, include premises defined in same file and those imported from other files (tree...)
- 