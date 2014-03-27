# Breiman 2001, Random Forests

A random forest is a classifier consisting of a collection of tree-structured classifiers $\{h(x, \Theta_k ), k = 1, . . .\}$ where the $\{ \Theta_k \}$ are independent identically distributed random vectors and each tree casts a unit vote for the most popular class at input $\mathbf{x}$. 6

For random forests, an upper bound can be derived for the generalization error in terms of two parameters that are measures of how accurate the individual classifiers are and of the dependence between them. The interplay between these two gives the foundation for understanding the workings of random forests.  7

The forests studied here consist of using randomly selected inputs or combinations of inputs at each node to grow each tree.  10

Although the bound is likely to be loose, it fulfills the same suggestive function for random
forests as VC-type bounds do for other types of classifiers. It shows that the two ingredients
involved in the generalization error for random forests are the strength of the individual
classifiers in the forest, and the correlation between them in terms of the raw margin func-
tions. 9


> It shows that the two ingredients involved in the generalization error for random forests are the strength of the individual
classifiers in the forest, and the correlation between them in terms of the raw margin functions [@breiman_random_2001, 9]

To improve accuracy, the randomness injected has to minimize the correlation $\overline\rho$ while maintaining strength. The forests studied here consist of using randomly selected inputs or combinations of inputs at each node to grow each tree. The resulting forests give accuracy 10

Our results indicate that better (lower generalization error) random forests have lower correlation between classifiers and higher strength. The randomness used in tree construction has to aim for low correlation $\overline\rho$̄ while maintaining reasonable strength. 20
