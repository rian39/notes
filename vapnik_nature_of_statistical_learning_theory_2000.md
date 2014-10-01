# vapnik_nature of statistical learning theory 2000

new function estimation methods have been created where a high dimensionality of the unknown function does not always require a large number of observations in order to obtain a good estimate. The new methods control generalization using capacity factors that do not necessarily depend on the dimensionality of the space vii

In contrast to classical methods of statistics where in order to control performance one decreases the dimensionality of a feature space, the SVM dramatically increases dimensionality and relies on the so-called large margine factor.  vii

Geometrically speaking, the perceptron divides the space $X$ into two parts separated by a piecewise linear surface. ... Learning in this model means finding appropriate coefficients for all neurons using given training data. 7

In this book we consider the learning problem as a problem of finding a desired dependence using a _limited_ number of observations. 17

We describe the general model of learning from examples through three components:
(i) A generator (G) of random vectors $x E R^n$, drawn independently from a fixed by unknown probability distribution function $F(x)$
(ii) A supervisor (S) who returns an output value $y$ to every input vector $x$, according to a conditional distribution function $F(y|x)$, also fixed by unknown
(iii) A learning machine (LM) capable of implementing a set of functions $f(x, \alpha), \alpha E \Lambda$
The problem of learning is that of choosing from the given set of functions  $f(x, \alpha), \alpha E \Lambda$, the one that best approximates the supervisor's response. 17

In order to choose the best available approximation to the supervisor's response, one measures the _loss_ or discrepancy, $L(x, f(x, \alpha))$ between the response $y$ of the supervisor to a given input $x$ and the response  $f(x,a)$ provided by the learning machine. 18

The problem is to use the sample to find the function from the set of admissable functions that minimizes the probability of error. 31

In the framework of the classical paradigm all models of function estimation are based on the maximum likelihood function. It forms an inductive engine in the classical paradigm.  24

The VC dimension of the set of functions (rather than the number of parameters) is responsible for the generalization ability of learning machines. This opens remarkable opportunities to overcome the "curse of dimensionality" 83

learning is a problem of _function estimation_ on the basis of empirical data 291

Mostly, however, we face another situation.  ... In other words, we face the problem of estimating the _values of the unknown function at given points._ 291

The matter is that in solving the function estimation problem in both computational statistics (say pattern recognition, regression, density estimation) and in computation mathematics(...), the first step is describing (parameterizing) a set of functions in which one is looking for a solution 297

