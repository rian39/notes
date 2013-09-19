Hastie 2008
[@hastie_elements_2009]

Our goal is to find a useful approximation $\hat(f)(x)$ to the function $f(x)$ that underlies the predictive relationship between input and output.  28

For some problems a deterministic relationship does hold. Many of the classification problems studied in machine learning are of this form, where the response surface can be thought of as a coloured map defined in $\mathbb{R}^p$


The logistic regression model arises from the desire to model the posterior probabilities of the _K_ classes via linear functions in $x$, while at the same time ensuring that they sum to one and remain in $[0,1]$ 119

...

$$Pr(G=K|X=x) = \frac{1}{1+\sum_{l=1}^{K-1}exp(\beta_l0 + \beta_l^Tx)}$$ [@hastie_elements_2009, 119]

Tree-based methods partition the feature space into a set of rectangles and then fit a simple model (like a constant) in each one. They are conceptually simple yet powerful. 305
 
The full dataset sits at the top of the tree. Observations satisfying the conditions at each junction are assigned to the left branch and the others to the right branch. The terminal nodes or leaves of the tree correspond to the regions $R1$, $R2$,... $R5$. 305

A key advantage of the recursive binary tree is its interpretability. The feature space partition is fully described a by single tree.  ... This representation is popular among medical scientists, perhaps because it mimics the way a doctor thinks.  The tree stratifies the population into strata of high and low outcome, on the basis of patient characteristics 306-7.

How large should we grow the tree? Clearly a large tree might overfit the data, while a small tree might not capture the important structure. Tree size is a tuning parameter governing the model's complexity, and the optimal tree size should be adaptively chosen from the data.  307-308


"Of all the well-known learning methods, decision trees comes closest to meeting the requirements for serving as an off-the-shelf procedure for data-mining" [@hastie_elements_2009, 352]


[the] _support vector machine_ ... produces nonlinear boundaries by constructing a linear boundary in a large transformed version of the feature space. 

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


