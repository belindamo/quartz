#concept

`softmax` function turns a vector of $K$ real values (model predictions) into... (visualize equation)
[[SR/memory/0yyEeoCd.md|?]]
$K$ probabilities that sum to 1.
$$
softmax(z)[i] = \frac{e^{z[i]}}{\sum_{j=1}^{K}{e^{z[j]}}}
$$
It is used as an [[activation function]] 
![[Pasted image 20240917160005.png]]
 `softmax` in a neural network is often used as the last activation function of a neural network to normalize output of a network to a probability distribution over predicted output classes.



standard (unit) `softmax` equation where
- sigma is the output. a vector of real numbers that is normalized between 0 and 1
- z is input vector
- K is vector length
[[SR/memory/AsQ6mokE.md|?]]
$$
\sigma(\mathbf{z})_i = \frac{e^{z_i}}{\sum_{j=1}^K e^{_j}}
$$



intuitively...softmax is great as an activation function because it is non-linear, so... [[SR/memory/4jiHb6Kz.md|>>]] you are maximizing the difference in the dot product between vectors. and normalize across all dot products



### References
1. 

### Notes




