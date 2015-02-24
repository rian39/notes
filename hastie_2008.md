Hastie 2008
[@hastie_elements_2009]

Qualitative variables are typically represented numerically by codes. The easiest case is when there are only two classes or categories, such as “success” or “failure,” “survived” or “died.” These are often represented by a single binary digit or bit as 0 or 1, or else by −1 and 1. For reasons that will become apparent, such numeric codes are sometimes referred to as targets. When there are more than two categories, several alternatives are available. The most useful and commonly used coding is via dummy variables. Here a K-level qualitative variable is represented by a vector of K binary variables or bits, only one of which is “on” at a time. Although more compact coding schemes are possible, dummy variables are symmetric in the levels of the factor. We will typically denote an input variable by the symbol X. If X is

Our goal is to find a useful approximation $\hat(f)(x)$ to the function $f(x)$ that underlies the predictive relationship between input and output.  28

For some problems a deterministic relationship does hold. Many of the classification problems studied in machine learning are of this form, where the response surface can be thought of as a coloured map defined in $\mathbb{R}^p$

However with too much fitting, the model adapts itself too closely to the training data, and will not generalize well (i.e., have large test error). ... In contrast, if the model is not complex enough, it will underfit and may have large bias, again resulting in poor generalization. 38

The logistic regression model arises from the desire to model the posterior probabilities of the _K_ classes via linear functions in $x$, while at the same time ensuring that they sum to one and remain in $[0,1]$ 119

...

$$Pr(G=K|X=x) = \frac{1}{1+\sum_{l=1}^{K-1}exp(\beta_l0 + \beta_l^Tx)}$$ [@hastie_elements_2009, 119]

## model assessment

The generalization performance of a learning method relates to its prediction capability on independent test data. Assessment of this performance is extremely important in practice, since it guides the choice of learning method or model, and gives us a measure of the quality of the ultimately chosen model. 219 

## Trees

Tree-based methods partition the feature space into a set of rectangles and then fit a simple model (like a constant) in each one. They are conceptually simple yet powerful. 305
 
The full dataset sits at the top of the tree. Observations satisfying the conditions at each junction are assigned to the left branch and the others to the right branch. The terminal nodes or leaves of the tree correspond to the regions $R1$, $R2$,... $R5$. 305

A key advantage of the recursive binary tree is its interpretability. The feature space partition is fully described a by single tree.  ... This representation is popular among medical scientists, perhaps because it mimics the way a doctor thinks.  The tree stratifies the population into strata of high and low outcome, on the basis of patient characteristics 306-7.

How large should we grow the tree? Clearly a large tree might overfit the data, while a small tree might not capture the important structure. Tree size is a tuning parameter governing the model's complexity, and the optimal tree size should be adaptively chosen from the data.  307-308


"Of all the well-known learning methods, decision trees comes closest to meeting the requirements for serving as an off-the-shelf procedure for data-mining" [@hastie_elements_2009, 352]

One major problem with trees is their high variance. Often a small change in the data can result in a very different series of splits, making interpretation somewhat precarious. The major reason for this instability is the hierarchical nature of the process: the effect of an error in the top split is propagated down to all of the splits below it.  312

Boosting is one of the most powerful learning ideas  introduced in the last twenty years.  ... The motivation for boosting was a procedure that combines the outputs of many "weak" classifiers to produce a powerful "committee."

[the] _support vector machine_ ... produces nonlinear boundaries by constructing a linear boundary in a large transformed version of the feature space. 417

The _support vector machine_ classifier is an extension of this idea, where the dimension of the enlarged space is allowed to get very large, infinite in some cases. It seems that the computations would become prohibitive. It would also seem that with sufficient basis functions, the data would be separable, and overfitting would occur. 423



## quotes relating cancer microarray

With supervised learning there is a clear measure of success or lack thereof, that can be used to judge adequacy in particular situations and to compare the effectiveness of different methods over various situations. Lack of success is directly measured by expected loss over the  joint distribution $Pr(X,Y)$. This can be estimated in a variety of ways including cross-validation. In the context of unsupervised learning, there is no such direct measure of success. 486-7

This uncomfortable situation has led to heavy proliferation of proposed methods, since effectiveness is a matter of opinion and cannot be verified directly. 487

We apply K-means clustering to the human tumor microarray data de-
scribed in Chapter 1. This is an example of high-dimensional clustering. 512

The data are a 6830 × 64 matrix of real numbers, each representing an
expression measurement for a gene (row) and sample (column). Here we
cluster the samples, each of which is a vector of length 6830, correspond-
ing to expression values for the 6830 genes.  513


Bagging or _bootstrap aggregation_ ... is  a technique for reducing the variance of an estimated prediction function. Bagging seems to work especially well for high-variance, low-bias procedures such as trees. 587

The essential idea in bagging is to average many noisy but approximately unbiased models, and hence reduce the variance. Trees are ideal candidates for bagging, since they can capture complex interaction structures in the data, and if grown sufficiently deep, have relatively low bias. 587

The idea in random forests is to improve the variance reduction of bagging by reducing the correlation between the trees, without increasing the variance too much. This is achieved in the tree-growing process through random selection of the input variables. 588
 etc.,
The ideas is that even though the data may be high-dimensional, involved mixed variables, etc., the promixity plot gives an indication of which observations are effectively close together in the eyes of the random forest classifier 595.

## Bayes

It is especially appropriate when the dimension p of the feature space is high, making density estimation unattractive. The naive Bayes model assumes that given a class $G = j$, the features $X_k$ are independent 211

While this assumption is generally not true, it does simplify the estimation
dramatically:
• The individual class-conditional marginal densities $f_{jk}$ can each be estimated separately using one-dimensional kernel density estimates. This is in fact a generalization of the original naive Bayes procedures, which used univariate Gaussians to represent these marginals. • If a component $X_j$ of $X$ is discrete, then an appropriate histogram estimate can be used. This provides a seamless way of mixing variable types in a feature vector. 211

Despite these rather optimistic assumptions, naive Bayes classifiers often outperform far more sophisticated alternatives. The reasons are related to Figure 6.15: although the individual class density estimates may be biased, this bias might not hurt the posterior probabilities as much, especially near the decision regions. In fact, the problem may be able to withstand considerable bias for the savings in variance such a “naive” assumption earns. 211


# quotes relating to neural networks

Projection pursuit and neural network models consist of sums of non-linearly transformed linear models. 18
As we make clear in this section, they are just nonlinear statistical models, much like the projection pursuit regression model discussed above. A neural network is a two-stage regression or classification model, typ- ically represented by a network diagram as in Figure 11.2. This network applies both to regression or classification. 392

