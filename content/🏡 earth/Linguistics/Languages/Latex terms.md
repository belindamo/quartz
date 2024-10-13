#concept-pamphlet

What is the LaTeX code for the greater than or equal to symbol?
?
`\geq`
$$
\geq
$$

What is the LaTeX code for the less than or equal to symbol?
?
`\leq`
$$
\leq
$$

What is the LaTeX code for the not equal to symbol?
?
`\neq`
$$
\neq
$$

What is the LaTeX code for the approximately equal to symbol?
?
`\approx`
$$
\approx
$$

What is the LaTeX code for the tilde symbol?
?
`\sim`
$$
\sim
$$

What is the LaTeX code for the right arrow symbol?
?
`\Rightarrow`
$$
\Rightarrow
$$

What is the LaTeX code for the square root of 42?
?
`\sqrt{42}`
$$
\sqrt{42}
$$

What is the LaTeX code for the infinity symbol?
?
`\infty`
$$
\infty
$$

What is the LaTeX code for this symbol?
$$
\lambda
$$
?
`\lambda`

What is the LaTeX code for  these symbols?
$$
\mu, \sigma
$$
?
`\mu`, `\sigma`

What is the LaTeX code for this symbol?
$$
\Phi(0)
$$
?
`\Phi(0)`

What is the LaTeX code for the this symbol?
$$
\Sigma
$$
?
`\Sigma`

What is the LaTeX code for this symbol?
$$
\theta
$$
?
`\theta`

What is the LaTeX code for the bar X and hat X symbols?
$$
\bar{X}, \hat{X}
$$
?
`\bar{X}`, `\hat{X}`


What is the LaTeX code for the dots here:
$$
1,2,\cdots,n
$$
?
`\cdots`


What is the LaTeX code for verbatim text 'my_function()'?
?
`\verb|my_function()|`
$$
\verb|my_function()|$$

What is the LaTeX code for a fraction with units in the numerator and denominator?
?
`\frac{1}{1}`
$$
\frac{1}{2}$$

What is the LaTeX code for summation from i equals 0 to n?
?
`\sum_{i=0}^{n} i`
$$\sum_{i=0}^{n} i
$$

What is the LaTeX code for product from i equals 0 to n?
?
`\prod_{i=0}^{n} i`
$$\prod_{i=0}^{n} i
$$

What is the LaTeX code for the probability of A intersect B?
?
`P(A \cap B)`$$
P(A \cap B)
$$

What is the LaTeX code for the probability of A union B?
?
`P(A \cup B)`
$$P(A \cup B)
$$

What is the LaTeX code for the binomial coefficient?
?
`\binom{n}{k}`
$$\binom{n}{k}
$$
^This is `n! / ( k! (n-k)! )`. Also pronounced "n choose k". Also seen as `C(n,k)`

What is the LaTeX code for the conditional probability of A given B complement?
?
`P(A|B^C)`$$
P(A|B^C)
$$
Complement is all probabilities not in B

What is the LaTeX code for the probability of meow given cat??
`P(\textrm{meow } | \textrm{ cat})`
$$
P(\textrm{meow } | \textrm{ cat})
$$
What is the LaTeX code for the probability of a condition less than or equal to 5.0?
?
`P(\textrm{cond} \leq 5.0)`
$$
P(\textrm{cond} \leq 5.0)
$$
What is the LaTeX code for A times B?
?
`A \times B`
$$
A \times B
$$


What is the LaTeX code for a Normal random variable X with mean 0 and variance 1?
?
`X \sim \mathcal{N}(\mu = 0, \sigma^2 = 1)`
$$
X \sim \mathcal{N}(\mu = 0, \sigma^2 = 1)
$$


What is the LaTeX code for an integral from -1 to 1 of x squared dx?
?
`\int_{-1}^{1} x^2 dx`
$$
\int_{-1}^{1} x^2 - 2x + 1 dx
$$


What is the LaTeX code for the evaluation of the integral from -1 to 1 of x squared dx, with brackets?
?
`\left[ x^2 \right]_{-1}^1`
$$
\left[ x^2 \right]_{-1}^1
$$


What is the LaTeX code for a double integral?
?
`\iint`
`\iint_{0}^{1} {xy} dy dx`
$$
\iint_{0}^{1} xy dy dx$$
What is the LaTeX code for the evaluation of a double integral?
?
`\left.` expression `\right|_{0}^{1}
Example:`\left. \frac{3}{4}y^2 \right|_{-1}^{x}`
$$
\left. \frac{2}{3}y \right|_{-1}^{x}
$$

What is the LaTeX code for a 2x2 matrix with elements a, b, c, and d?
$$
\begin{bmatrix} a & b \\ c & d \end{bmatrix}
$$
?
`\begin{bmatrix} a & b \\ c & d \end{bmatrix}`
What is the LaTeX code for the correlation coefficient?
$$
\rho
$$
?
`\rho`


What is the LaTeX code for a group of equations aligned?
?
`\begin{align*`, `&=`, `\\`, `end{align*}`
Example:
```
\begin{align*} 
P(X=x|Y=1,W=P_1)  &= \frac{P(X=x,Y=1 | W=P_1)}{P(Y=1|W=P_1)} \\ 
&= P(X=x|W=P_1) \\ 
&= \binom{5}{x}(0.1)^x(0.9)^{5-x} \\ 
P(X=x|Y=1,W=P_2)  
&= \frac{P(X=x,Y=1 | W=P_2)}{P(Y=1|W=P_2)} \\ 
&= P(X=x|W=P_2) \\ 
&= \binom{5}{x}(0.1)^x(0.9)^{5-x} 
\end{align*}
```
$$
\begin{align*}
P(X=x|Y=1,W=P_1)
&= \frac{P(X=x,Y=1 | W=P_1)}{P(Y=1|W=P_1)} \\
&= P(X=x|W=P_1) \\
&= \binom{5}{x}(0.1)^x(0.9)^{5-x} \\
P(X=x|Y=1,W=P_2)
&= \frac{P(X=x,Y=1 | W=P_2)}{P(Y=1|W=P_2)} \\
&= P(X=x|W=P_2) \\
&= \binom{5}{x}(0.1)^x(0.9)^{5-x}
\end{align*}
$$


---
# Other cards that are cool but don't need to be reviewed

What is the LaTeX code for a Bernoulli random variable X with parameter p?

`X \sim \textrm{Ber}(p)`
$$
X \sim \textrm{Ber}(p)
$$


What is the LaTeX code for a Binomial random variable X with parameters n and p?

`X \sim \textrm{Bin}(n,p)`
$$
X \sim \textrm{Bin}(n,p)
$$


What is the LaTeX code for a Poisson random variable X with lambda equal to 0?

`X \sim \textrm{Poi}(\lambda=0)`
$$
X \sim \textrm{Poi}(\lambda=0)
$$


What is the LaTeX code for an Exponential random variable X with lambda equal to 0?

`X \sim \textrm{Exp}(\lambda=0)`
$$
X \sim \textrm{Exp}(\lambda=0)
$$



What is the LaTeX code for a Beta random variable theta with parameters a and b?

`\theta \sim \textrm{Beta}(a,b)`
$$
\theta \sim \textrm{Beta}(a,b)
$$



What is the LaTeX code for a double integral from 0 less than y less than x less than 1 of x over y dy dx?

`\iint_{0<y<x<1} \frac{x}{y} dy dx`
$$
\iint_{0<y<x<1} \frac{x}{y} dy dx
$$


What is the LaTeX code for the evaluation of a double integral from 0 less than y less than x less than 1 of x over y dy dx?

`\left. \frac{2}{3}y - \frac{3}{4}y^2 \right|_{-1}^{x}`
$$
\left. \frac{2}{3}y - \frac{3}{4}y^2 \right|_{-1}^{x}
$$


What is the LaTeX code for the variance of X?

\textrm{Var}(X)
$$
\textrm{Var}(X)
$$


What is the LaTeX code for the covariance of X and Y?

\textrm{Cov}(X,Y)
$$
\textrm{Cov}(X,Y)
$$


# Latex playground

equation editor: https://editor.codecogs.com/
cheatsheet: https://wch.github.io/latexsheet/latexsheet.pdf
another cheatsheet: [[(source) latex cheatsheet.pdf]]

```
> [!theorem] Title
> Content

> [!corollary]
> Content
```

> [!theorem] Title
> Content


> [!corollary] Title
> Content

```
> [!thm] Title
> Content

> [!cor]
> Content
```
> [!thm] Title
> Content

> [!cor]
> Content> [!thm] Title
> Content

> [!cor]
> Content


| Environment name | Alias |
| ---------------- | ----- |
| axiom            | axm   |
| definition       | def   |
| lemma            | lem   |
| proposition      | prp   |
| theorem          | thm   |
| corollary        | cor   |
| claim            | clm   |
| assumption       | asm   |
| example          | exm   |
| exercise         | exr   |
| conjecture       | cnj   |
| hypothesis       | hyp   |
| remark           | rmk   |
|                  |       |


> $$
> \begin{align}
> a &= b \\
>   &= c
> \end{align}
> $$


