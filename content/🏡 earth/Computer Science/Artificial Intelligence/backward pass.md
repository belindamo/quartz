#concept

What is a **backward pass**?
[[SR/memory/crCTPzrN.md|?]]
A backward pass computes the gradient of the loss function with respect to each weight by chain-rule, starting from the output layer back to the input layer. Weights and biases are updated in response to the loss in the output.


### References
1. [[Build micrograd, a scalar-based neural network with Karpathy]]

### Notes

https://github.com/maxim5/cs229-2018-autumn/blob/main/notes/cs229-notes-backprop.pdf