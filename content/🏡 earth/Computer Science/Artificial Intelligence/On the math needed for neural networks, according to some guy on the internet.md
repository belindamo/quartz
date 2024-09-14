#concept-pamphlet 
#todo fill out

[What math do you need to know to learn machine learning?](https://www.quora.com/What-math-do-you-need-to-know-to-learn-machine-learning?no_redirect=1)

As others mentioned before, it will mostly boil down to Statistics and Linear Algebra. However, I am very surprised how vague answers are.

There are lots of different techniques that you can specialise in so I’ll try mentioning some places where you can start. Hopefully, it will make you realise, that there is a lot to cover and how you can start doing that.

# Topics 


## Linear Algebra

Topics:

- Vectors & Matrices
- Matrix Multiplication & Transformations
- Eigenvector analysis
- Linear Equation Systems

Good place to learn:

- [Precalculus | Khan Academy](https://www.khanacademy.org/math/precalculus/ "www.khanacademy.org")
- [Linear Algebra | Khan Academy](https://www.khanacademy.org/math/linear-algebra "www.khanacademy.org")
- [Linear Algebra](https://ocw.mit.edu/courses/mathematics/18-06-linear-algebra-spring-2010/index.htm "ocw.mit.edu")
- [http://cs229.stanford.edu/section/cs229-linalg.pdf](http://cs229.stanford.edu/section/cs229-linalg.pdf "cs229.stanford.edu")

## Calculus

Basically, you need to be able to do derivative and integration inside out.

Topics:

- Differentiation
- Chain Rule
- Partial Derivatives
- Integrals

Good places to learn:

- [AP Calculus AB | Khan Academy](https://www.khanacademy.org/math/ap-calculus-ab "www.khanacademy.org")
- [Multivariable Calculus | Khan Academy](https://www.khanacademy.org/math/multivariable-calculus "www.khanacademy.org")

## Statistics

Probably, the most important thing is to have a pretty decent grasp on probability density and mass functions (PDFs and PMFs) for most of the common distributions (like Gaussian, Binomial, or Exponential family).

In the end, if you know statistics really well, you can make any machine learning problem into a statistics problem. I would even claim, that the current machine learning developments (apart from deep learning) are just rediscovery of statistics with the computation power of modern computers.

Also, I will skip things like expected value, variance, and etc. because that’s basics.

Topics:

- Distributions and their CDFs and PDFs:
- Binomial
- Poisson
- Exponential family
- Gaussian distribution in particular
- Calculating CDFs from PDFs
- Bayes Rule
- Naive Bayes
- Markov Chains
- Belief Networks (or Graphical Models in General)

Good places to learn:

- [Statistics and probability](https://www.khanacademy.org/math/statistics-probability "www.khanacademy.org")
- [Probability | Statistics and probability | Math | Khan Academy](https://www.khanacademy.org/math/statistics-probability/probability-library "www.khanacademy.org")
- [Journey into information theory](https://www.khanacademy.org/computing/computer-science/informationtheory "www.khanacademy.org")
- [http://cs229.stanford.edu/section/cs229-prob.pdf](http://cs229.stanford.edu/section/cs229-prob.pdf "cs229.stanford.edu")

## Optimisation

And finally optimisation. I would say it’s just a part of Calculus (and it would look like that Khan agrees) but whatever. Here you want to be able to find the minimum or either the maximum of some function.

Topics:

- Gradient Descent
- Stochastic (Online) Gradient Descend
- Expectation Maximization

Good places to learn:

- [Derivative applications](https://www.khanacademy.org/math/calculus-home/derivative-applications-calc "www.khanacademy.org")
- [Machine Learning - Stanford University | Coursera](https://www.coursera.org/learn/machine-learning "www.coursera.org") (note: it seems that Andrew Ng is in love with gradient descend so it is covered there pretty well)

## What’s next?

There is a lot of material online for machine learning online but the problem with it is that most of it is very shallow and, honestly, it isn’t worth your time.

However, I would go with the following courses:

[Machine Learning - Stanford University | Coursera](https://www.coursera.org/learn/machine-learning "www.coursera.org") - A great introductory course to Machine Learning by Andrew Ng. It will cover some statistics and fair amount of linear algebra. Additionally, it exposes you to some decent optimisation basics.

[Probabilistic Graphical Models | Coursera](https://www.coursera.org/specializations/probabilistic-graphical-models "www.coursera.org") - Pretty tough course by Daphne Koller. You might also want to check out a book, that the course is based on [Probabilistic Graphical Models](http://pgm.stanford.edu/ "pgm.stanford.edu") . The course will give you some decent intro to Bayesian Probabilistic Models.

[Neural Networks for Machine Learning - University of Toronto | Coursera](https://www.coursera.org/learn/neural-networks "www.coursera.org") - Neural Nets by Jeff Hinton. If this course is anything as it was before, take it only if you are really interested in neural nets. It makes you do some proper maths, to realise how do those nets actually work. I wouldn’t take it as a beginner.

However, that course doesn’t cover some newer development in DeepNets so you might want to see [CS224d: Deep Learning for Natural Language Processing](http://cs224d.stanford.edu/syllabus.html "cs224d.stanford.edu") or [CS231n Convolutional Neural Networks for Visual Recognition](http://cs231n.github.io/ "cs231n.github.io") to cover things like RNNs and LSTMs.

A quick peek

What it would take you to solve these?

1. Solve Xw=b for w where X is data matrix and w is a weight vector and b is a target value (constant).
2. Calculate Kullback-Leibler divergence between p(x)=N(x|μ,σ2)and q(x)=N(x|m,s2).
3. Prove p(x,y|z)=p(x|z)p(y|x,z)

Given all of this, you should be good enough to know where to go next.

Good Luck

I am pretty sure I’ve missed some important stuff but I am also sure that this will set you on the right track.

Good luck!