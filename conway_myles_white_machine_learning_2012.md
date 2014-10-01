# conway_myles_white_machine_learning_2012

Naive Bayes

At its core, text classification is a 20th century application of the 18th century concept of _conditional probability_. A conditional probability is the likelihood of observing some thing given some other thing we already know about. 77

The text classifcation algorithm we're going to use in this chapter, called the Naive Bayes classifier, looks for difference of this sort by searching through text for words that are either (a) noticeably more likely to occur in spam message, or (b) noticeabily more likely to occur in ham messages. ... If you see many words that more likely to occur in spam than ham and very few words that are more likely to occur in ham than spam, that should be strong evidence that email as a whole is spam. 77

How much more likely a message needs to be to merit being labeled spam depends upon an additional piece of information: the base rate of seeing spam messages.  This base rate information is usually called the _prior_. 77

For our purposes, we will use a very simply rule: assign a very small probability to terms that are not in the training set. 85

That said, the false-positive and false-negative rates found in the test data are far too high for any production spam filter. 90 ....  One way we might improve results, then, would be simply to alter our prior beliefs to reflect this fact and recalculate the predicted probabilities 91
