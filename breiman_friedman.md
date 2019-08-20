# Breiman & Friedman, 1984

Define the measurements $(x_1, x_2, ...)$ made on a case as the _measurement vector_ $\mathbf{x}$ corresponding to the case. Take the _measurement space_ $\mathcal{X}$ to be defined as containing all possible measurement vectors. 3

Suppose that the cases or objects fall into $J$ classes. Number the classes $1, 2, ..., J$ and let $C$ be the set of classes; that is $C = \{1, ..., J\}$. 3

A classifier or classification rule is a function $d(\mathbf{x})$ defined on $\mathcal{X}$ so that for every $\mathbf{x}$, $d(\mathbf{x})$ is equal to one of the numbers $1, 2, ..., J$. 4

What makes  a data set interesting is not only its size but also its complexity, where complexity can include such considerations as:

High dimensionality
A mixture of data types
Nonstandard data structure

and, perhaps most challenging, nonhomogeneity; that is, different relationships hold between variables in different parts of the measure space. 7 {#datasets}-7

Along with complex data sets comes "the curse of dimensionality" (a phrase due to Bellman, 1961). The difficulty is that the higher the dimensionality, the sparser and more spread apart are the data points. Ten points on the unit interval are not distant neighbors. But 10 points on a 10-dimensional unit rectangle are like oases in the desert. 7

_the complexity of a data set increases rapidly with increasing dimensionality_ 8

The first problem in tree construction is how to use $\mathcal{L}$ to determine the binary splits of $\mathcal{X}$ into smaller pieces. The fundamental idea is to select each split of a subset so that the data in each of the descendant subsets are "purer" than the data in the parent subset. 23

That is, the node impurity is largest when all classes are equally mixed together in it, and smallest when the node contains only one class. 24

Then the goodness of the split is defined to be the decrease in impurity 25.

The goodness of split criterion was originally derived from an impurity function. 32

An impurity function is a function $\phi$ defined on the,  set of J-tuples of numbers $(p_1, ..., p_j)$ satisfying $p_j \geq 0$, $j=1, ..., J,  \sum{p_j} = 1$ with the properties
(i) $\phi$ is a maximum only at the point $(\frac1{ j}, \frac1{j}, ... \frac1{j})$,
(ii) $\phi$ achieves its minimum only at the points $(1,0, ..., 0), (0,1,0, ..., 0), ..., (0, 0, ..., 0, 1)$
(iii) $\phi$ is a symmetric function of $p_1, ..., p_j$
32 

Given an impurity function $\phi$, define the impurity measure $i(t)$ of any node $t$ as

$$i(t) = \phi(p(1|t), p(2|t), ..., p(J|t))$$ 
32

$C(i|j)$ is the cost of misclassifying a class $j$ object as class $i$ object and satisfies:
(i) $C(i|j) >= 0, i i \neq j$
(ii) $C(i|j) = 0, i = j$  35
