#concept


What is a **step value,** in the context of training neural nets?
[[SR/memory/eeGGv8BA.md|?]]
How much to 'step' with each pass
It indicates how much the weights and biases are adjusted during each iteration of gradient descent. The step value determines the actual adjustment made to model parameters in a single optimization step.
It is typically computed as the product of the learning rate and the gradient (i.e., step value = learning rate × gradient).
 If step is too big, you can step too far and destabilize training and explode the loss
 If step is too small, learning is really slow


### References
1. [[Build micrograd, a scalar-based neural network with Karpathy]]

### Notes




