#concept

`softmax` turns a vector of $K$ real values (model predictions) into
?
$K$ probabilities that sum to 1.
$$
softmax(z)[i] = \frac{e^{z[i]}}{\sum_{j=1}^{K}{e^{z[j]}}}
$$
It is used as an [[activation function]] 
![[Pasted image 20240917160005.png]]
<!--SR:!2024-09-28,8,250-->
use of `softmax` in a neural network >> It is often used as the last activation function of a neural network to normalize output of a network to a probability distribution over predicted output classes.<!--SR:!2024-09-23,4,270-->


standard (unit) `softmax` equation where
- sigma is the output. a vector of real numbers that is normalized between 0 and 1
- z is input vector
- K is vector length
?
$$
\sigma(\mathbf{z})_i = \frac{e^{z_i}}{\sum_{j=1}^K e^{_j}}
$$
<!--SR:!2024-09-24,4,228-->


re:224w, intuitively...softmax is great because you are maximizing the difference in the dot product between vectors. and normalize across all dot products


### References
1. 

### Notes




