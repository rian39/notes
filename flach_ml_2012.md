# flach_machine_2012

The key question in machine learning is how to model the relationship between $X$ and $Y$. The statistician's approach is to assume that there is some underlying random proecess that generates the values for these variables, according to a well-defined but unknown probability distribution. We want to use the data to find out more about this distribution. 25

Likelihood function $P(X|Y)$ - the probability of an event we know has occurred ($X$), conditioned on something we don't know anything about ($Y$) 27

the Likelihood function plays an important role in statistical machine learning. It establishes what is called a _generative model_: a probabilistic model from which we can sample values of all variables involved. 29

_marginal Likelihoods_ 29

One might call the independence assumption that allows us to decompose joint likelihoods into a product of marginal likelihoods 'naive' -- which is exactly what machine learners do when they refer to this simplified Bayesian classifier as _naive Bayes_. 30 

We have some idea what a probabilistic model looks like, but how do we learn such a model? In many case this will be a matter of estimating the model parameters from data, which is usually achieved by straightforward counting.30                         

Geometric models are constructed in Cartesian instance spaces, using geometric concepts such as planes and distances. The prototypical geometric model is the basic linear classifier, which constructs a decision plan orthogonal to the line connecting the positive and negative centres of mass. Probabilistic models view learning as a process of reducing uncertainty using data. For instance, a Bayesian classifier models the posterior distribution $P(Y|X)$ (or its counterpart, the likelihood function $P(X|Y)$) which tells me the class distribution $Y$ after observing the features values $X$. Logical models are the most 'declarative' of the three, employing if-then rules built from logical conditions to single out homogeneous areas in instance space. 47

Discriminative probabilistic models: they model the posterior probability distribution $P(Y|X)$, where $Y$ is the target variable and $X$ are the features. Thatis, given $X$ they return a probability distribution over $Y$
The other main class of probabilistic models are called _generative_ models. They model the joint distribution $P(X,Y)$ of the target $Y$ and the feature vector $X$. Once we have access to this joint distribution we can derive any conditional or marginal distribution involving the same variables. 262

Such models are called 'generative' because we can sample from the joint distribution to obtain new data points together with their labels. 263

The key point is that _probabilities do not have to be interpreted as estimates of relative frequencies, but can carry the more general meaning of (possibly subject) degrees of belief. 265

A good probabilistic treatment of a machine learning problem achieves a balance between solid theoretical foundations and the pragmatism required to obtain a workable solution. 273

## Training a naive Bayes model

Train a probabilistic model usually involves estimating the parameters of the distributions used in the model. The parameter of a Bernoulli distribution can be estimated by counting the number of successes $d$ in $n$ trials and setting $\hat\theta  = d/n$. In other words, we count, for each class, how many e-mails contain the word in question. 279

Many other variations of the naive Bayes classifier exist. In fact, what is normally understood as 'the' naive Bayes classifier employs neither a multinomial nor a multivariate Bernoulli modle, but rather a multivariate categorical model. 280

In summary, the niave Bayes model is a popular model for dealing with textual, categorical and mixed categorical/real-valued data. Its main shortcoming as a probabilistic model -- poorly calibrated probability estiamtes -- are outweighed by a generally good ranking performpance. Another apparent paradox with naive Bayes is that it isn't particularly Bayesian at all! ... Personally, I think the essence of naive Bayes is the decomposition of joint likelihoods into marginal likelihoods. This decomposition is evocatively visualised by the Scottish tartan pattern 281

Features, also call attributes, are defined as mappings $f_i: \mathcal{I} \rightarrow \mathcal{F}_i$ from the instance space $\mathcal{i}$ to the feature domain $\mathcal{F}_i$. We can distinguish features by their domain. 298