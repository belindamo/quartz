#concept

What is a **backward pass**?
?
A backward pass computes the gradient of the loss function with respect to each weight by chain-rule, starting from the output layer back to the input layer. Weights and biases are updated in response to the loss in the output.
<!--SR:!2024-09-27,7,250-->

### References
1. [[Build micrograd, a scalar-based neural network with Karpathy]]
<!--SR:!2025-01-19,124,290-->

### Notes

https://github.com/maxim5/cs229-2018-autumn/blob/main/notes/cs229-notes-backprop.pdf