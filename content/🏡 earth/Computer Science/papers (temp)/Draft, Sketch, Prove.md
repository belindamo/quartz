#paper #concept-pamphlet 

# Notes

Draft, Sketch, and Prove (DSP) is a method that does this >> a method that maps informal proofs to formal proof sketches, and uses the sketches to guide an automated prover by directing its search to easier sub-problems.
<!--LEARN:B4mxSwSL-->


In Draft, Sketch, Prove, the 3 stage process involves these models at each stage:
?
1. LLM to draft statement->informal proof
2. LLM to autoformalize informal->formal sketch
3. Proof automation tool (Sledgehammer) and Set of simple tactics to verify formal sketch->verified proof.
	1. Sledgehammer translates Isabelle/HOL's higher order logic into simpler logic, then sends it to multiple traditional ATPs like Z3, CVC4. These use symbolic reasoning/logical inference tools
<!--LEARN:TVagHRQE-->

## Key terms

## Main contributions

This automated prover that is guided by sketches enhances performance from 20.9% to 39.3% on a collection of math competition problems.


## Strengths and Weaknesses of paper
- Strengths
- Weaknesses

## Questions & Discussion Items

Method.
For each problem they:
- Generate 100 informal proofs with language models
- Make 100 autoformalization attempts
- Run Sledgehammer with a 120-second timeout

%% TODO-rr : consider using ATP like Z3, CVC4, etc. %%