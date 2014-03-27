## mitchell,  machine learning

_Definition_: A computer program is said to **learn** from experience $E$ with respect to some class of tasks $T$ and performance measure $P$, if its performance at tasks in $T$, improves with experience $E$ 2. 

One highly practical Bayesian learning method is the naive Bayes learner, often called the _naive Bayes classifier_. In some domains, its performance has been shown to be comparable to that of neural network and decision tree learning 177

The naive Bayes classifier applies to learning tasks where each instance $x$ is described by a conjunction of attribute values and where the target functino $f(x)$ can take on any value from some finite set $V$. A set of training examples of the target function is provided, and a new instance is presented, described by the tuple of attribute values $<a_1, a_2 ... a_n>$. The learner is asked to predict the target value, or classification, for this new instance. 177

The naive Bayes classifier is based on the simplifying assumption that the attribute values are conditionally independent given the target value. In other words, the assumption is that given the target value of the instance, the probability of observing the conjunction $a_, a_2 ... a_n$ is just the product of the probabilities for the individual attributes: $P(a_1, a_2 ... a_n|v_j) = P(\prod_i P(a_i|v_j)$ 177

Naive Bayes classifier:

$$v_{NB} = \underset{v_j \in V}{\operatorname{argmax}} P(v_j) \prod_i P(a_i|v_j)$$ (6.20) 177

To summarize, the naive Bayes learning method involves a learning step in which the various $P(v_j)$ and $P(a_i|v_j)$ terms are estimated, based on their frequencies over the training data. The set of these estimates corresponds to the learned hypothesis 178

An example: learning to classify text

To illustrate the practical importance of Bayesian learning methods, consider learning problems in which the instances are text documents. For example, we might wish to learn the target concept "electronic news articles that I find interesting," or "pages of the World Wide Web that discuss machine learning topics." In both cases, if a computer could learn the target concept accurately, it could automatically filter the large volume of online text documents to present only the most relevant documents to the user. 180

We present here a general algorithm for learning to classify text, based on the naive Bayes classifier. Interestingly, probabilistic approaches such as the one describe here are among the most effective algorithms currently known for learning to classify text documents. 180

### EM algorithm
We can think of the full description of each instance as the triple $<x_i, z_{i1},z_{i2}>$ where $x_i$ is the observed value of the _i_th instance and where $z_{i1}$ and $z_{i2}$ indicate which of the two Normal distributions was used to generate the value $x_i$.   ... Here $x_i$ is the observed variable in the description of the instance, and $z_{i1}$ and $z_{i2}$ are hidden variables. 192
