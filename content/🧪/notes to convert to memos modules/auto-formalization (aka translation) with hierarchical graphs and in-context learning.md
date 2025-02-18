
  
  

Problem  

Proof formalization takes a long time. It takes a few weeks to a few years to formalize a single complex proof. de Bryin factor (ratio of difficulty write correct formal:informal proof) is ~20 according to Tao. Dropping this ratio would be transformative to the mathematics field.  

Auto-formalization of proofs help reduce this, but is unreliable at the moment.  

Given an input of a theorem and its informal proof in natural language, convert it to Lean formal proof.  

Bit  

To formalize a proof in recent years, mathematicians have used some combination of tuned RL-based models, verifier, and humans. e.g. AlphaGeometry  

Flip  

Instead, can we use general-purpose LLMs, generated multi-layer DSL, and verifier? No human, no need for fine-tuning models.  

Multi-layer DSL allows reasoning to be:  

traceable: graph paths are easier to debug  

verifiable: apply verifier to absolute certainty of a layer’s correctness  

composable: you can specify a layer’s rules and symbols  

understandable: across a swath of human comprehension levels.  

Instantiate solution  

A.  

Each layer is a DSL computation graph.  

There are 4 layers: human informal proof, human formal proof, Lean pseudocode proof, Lean formal proof  

DSL contains:  

functions, aka logical rules. Edges must be of these types  

primitives, aka data structure. Nodes must be of these types  

B.  

Subgraphs in one layer correspond to subgraphs in another layer. A subgraph may be a single node.  

translation function, aka fuzzy rule.  

C.  

For each sample that runs through layers (order matters),  

Each layer’s functions and primitives are updated  

The translation function between layers are updated  

Method  

Given MiniF2F’s informal to formal dataset, we “train” with each sample in order to update the DSL functions and primitives. (not the specific contents! though we may store the traces of each sample)  

For each sample with a theorem + informal proof + pseudocode + Lean:  

LLM generates appropriate functions and primitives.  

Ensures the functions and primitives are aligned with all the others seen so far.  

Update translation function  

...  

Evaluate  

Use MiniF2F and LeanDojo’s dataset of proofs that are sampled from Lean’s mathlib.**