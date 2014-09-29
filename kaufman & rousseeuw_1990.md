Kaufman, L. & Rousseeuw, P.J. Finding Groups in Data. (Wiley Online Library: 1990). 
Partitioning vs hierarchical
Computing dissimilarites (DAISY)
Partitioning around medoids (PAM)
Clustering Large Applications (CLARA)
Fuzzy Analysis (FANNY)
Agglomerative Nesting (AGNES)
Divisive Analysis (DIANA)
Monothetic Analysis (MONA)

Cluster analysis is the art of finding groups in data. 1

Such groups are called clusters, and to discover them is the aim of cluster analysis. 1

The reason for this variety of methods is probably two fold … 
Automatic classification is a very young scientific discipline in vigorous development, as can be seen from the thousands of articles scattered over many periodicals (mainly jounrnals of statistics, biology, psychometrics, computer science and marketing). 
The second main reason for the diversity of algorithms is that there exists no general definition of a cluster, and in fact there are several kinds fo them: spherical clusters, drawn-out clusters, linear clusters and so on.  3

Clustering algorithms typically operate on either of two input structures. 3 … aan n-by-p matrix, where the rows correspond to the objects and columns to the attributes.  … The second structure is a collection of proximities that must be available in all pairs of objects. These proximities make up an n-by-n table. 4
We shall consider tow types of proximities , namely dissimilarities (which measure how far objects are away from each other) and similarities (which measure how much they resemble each other) 4. 
To avoid this dependence on the choice of measurement units, one has the option of standardizing the data. 6
The next step is to compute distances between the objects, in order to quantify their degree of dissimilarity. It is necessary to have a distance for each pair of objects I and j. The most popular choice is the Euclidean distance. 11
Another well-known metric is the city block or Manhattan distance. … The Manhattan distance was used in cluster analysis context by Carmichael and Sneaht (1969). 12
In all this, it should be noted that a variable not containing any relevant information (say, the telephone number of each person) is worse than useless, because it will make the clustering less apparent. The occurrence of several such “trash variables” will kill the whole clustering because they yield a lot of random terms in the distances, thereby hiding the useful information provided by the other variables. 14

Dissimilarities can be obtained in several ways. Often they can be computed from variables that are binary, nominal, ordinal, interval, or a combination of these. … Also, dissimilarities can be simple subjective ratings of how much certain objects differ from each other, from the point of view of one or more observers. 17
 Similarity coefficient: The more objects I and jare alike (or close), the larger s(i,j)  becomes. 20
In order to define similarities between variables, we can again resort to the Pearson or the Spearman correlation coefficient. 21
Suppose the data consist of a similarity matrix but one wants to apply a clustering algorithm designed for dissimilarities. Then it is necessary to transform the similarities into dissimilarities. 21

Binary variables have only two possible outcomes (or states). 22 
When computing a similarity s(i,j)  or a dissimilarity d(i,j) between two objects I  and j, one draws a 2-by-2 contingency talbe
The binary variable “sex” possesses the possible states “male” and “female.” Both are equally valuable and carry the same weight. There is no preference for which outcome should be coded as 0 and which as 1. Such a variable is called symmetric. .. For symmetric variables, it is natural to work with invariant similarities.23
The most well known of these [invariant similarities] is the simple matching coefficient, which looks for the percentage of matches. 25 See Zubin, 1938, Dumas, 1955,  Sokal & Michener, 1958, Sneanth 1962). Also called the M-coefficient or affinity index 25

When working with asymmetric binary variables, we need other proximity coefficients. By convention, we shall always code the most important outcome (which is typically the rarest one) by 1, and the other 0. 26
The most famous noninvariant coefficient is due to Jaccard (1908) and looks like the simple matching coefficent, except for leaving out d entirely. 26
When both symmetric and asymmetric binary variables occur in the same data set, one can apply the “mixed variables” approach. 27
Nominal variables
By far the most common way of measuring the similarity or dissimilarity between some objects I and j  that are characterized through nominal variables is to the simple matchign approach (Sokal & Michener, 1958).  Simply matching dissimilarities can be computed by means of the program DAISY. 29
Ordinal variables
A discrete ordinal variable looks like a nominal variable, only now the M states are ordered in a meaningful sequence. The codes 1 …. M are no longer arbitrary.  29
Ordinal variables are very useful for registing subjective assessments of qualities that cannot be measured objectivity. 29
Mixed variables
Data with mixed variables can be treated in several ways …. In our opinion, the most convenient approach is to combine the different variables into a single proximity matrix, as was proposed by Ducker (1965) (Rubin, 1967) and (Colless 1967). The definition of (Gower, 1971a) takes care of interval, nominal, and binary data 35.

Discussion of Gower’s formula shows how it handles all the different data types sensibly (35) The computations can performed with the program DAISY 35
?daisy in R gives a good description of this
Which clustering algorithm to choose?
A partitioning methods constructs k  clusters.  … k  is given by the user. Indeed the algorithm will construct a partition with as many clusters as desired. Of course not all values of k  lead to “natural” clusterings, so it is advisable to run the algorithm several times with different values of k and to select that k for which certain characteristics or graphics look best, or to retain the clustering that appears to give rise to the most meaningful interpretation.  38

The program PAM clusters objects that are measured on p interval-scaled variables, and it can also be applied when the input data is a dissimilarity matrix (set up by DAISY) 40
To be exactl, the average distance (or average dissimilarity) of the representative object to all other objects of the same cluster is being minimized.  For this reason, such an optimal representative objects we call the medoid  of the cluster, and the method of partitioning around medoids we call the k-medoid  technique. 40-
