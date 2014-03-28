# Segaran_programming_collective_2007

Ch 6 Document filtering

This chapter will demonstrate how to classify documents based on their contents, a very practical application of machine intellgience and one that is becomign more widespread. Perhaps the most useful and well-known application of document filtering is the elimination fo spam. 117

The classifiers discussed in this chapter learn how to classify a document by being trained. 119

Once you have the probabilities of a document in a category containing a particular word, you need a way to combine the individual word probabilities to get the probability that an entire document belongs in a given category. 123

you can't actually use the probability created by the naive Bayesian classifier as the actual probability that a document belongs in a category, because the assumption of independence makes it inaccurate. 124

To use the naive Bayesian classifier, you'll first have to determine the probaiblity of an entire document being given a classification.  124