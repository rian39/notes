burges, svm tutorial

The problem which drove the initial development of SVMs occurs in several guises -
the bias variance tradeoff (Geman and Bienenstock, 1992), capacity control (Guyon et al., 1992), overfitting (Montgomery and Peck, 1992)  122

Roughly speaking, for a given learning task, with a given finite amount of training data, the best generalization performance will be achieved if the right balance is struck between the accuracy attained on that particular training set, and the “capacity” of the machine, that is, the ability of the machine to learn any training set without error. A machine with too much capacity is like a botanist with a photographic memory who, when presented with a new tree, concludes that it is not a tree because it has a different number of leaves from anything she has seen before; a machine with too little capacity is like the botanist’s lazy brother, who declares that if it’s green, it’s a tree. Neither can generalize well. The exploration and formalization of these concepts has resulted in one of the shining peaks of the theory of statistical learning (Vapnik, 1979). 122

Now if a given set of $l$ points can be labeled in all possible $2^l$ ways, and for each labeling, a member of the set ${f (α)}$ can be found which correctly assigns those labels, we say that that set of points is shattered by that set of functions. The VC dimension for the set of functions {f (α)} is defined as the maximum number of training points that can be shattered by {f (α)}. 124 

We will now switch to a Lagrangian formulation of the problem. There are two reasons
for doing this. The first is that the constraints (12) will be replaced by constraints on the Lagrange multipliers themselves, which will be much easier to handle. The second is that in this reformulation of the problem, the training data will only appear (in the actual training and test algorithms) in the form of dot products between vectors. This is a crucial property which will allow us to generalize the procedure to the nonlinear case 129

For the linearly separable case, the support vector algorithm simply looks for
the separating hyperplane with largest margin.  129

Those training points for which the equality in Eq. (12) holds (i.e. those which wind up lying on one of the hyperplanes H1 , H2 ), and whose removal would change the solution found, are called support vectors; 129 

For these machines, the support vectors are the critical elements of the training set. They lie closest to the decision boundary; if all other training points were removed (or moved around, but so as not to cross H1 or H2 ), and training was repeated, the same separating hyperplane would be found. 131

The analogy emphasizes the interesting point that the “most important” data points are the support vectors with highest values of α, since they exert the highest forces on the decision sheet. For the non-separable case, the upper bound αi ≤ C corresponds to an upper bound on the force any given point is allowed to exert on the sheet. This analogy also provides a reason (as good as any other) to call these particular vectors “support vectors”10 . 137

Maximize:
$$L_D \equiv  \sum_i \alpha_i - \frac{1}{2} \sum_{i,j}\alpha_i\alpha_jy_iy_j \mathboldf{x}_i\cdot \mathboldf{x}_j$$
(43)  p.135

First notice that the only way in which the data appears in the training problem, Eqs. (43) - (45), is in the form of dot products, xi · xj . Now suppose we first mapped the data to some other (possibly infinite dimensional) Euclidean space H, using a mapping which we
will call Φ: 138
