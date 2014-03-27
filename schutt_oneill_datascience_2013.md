# Data Science - schutt and oneill

Let’s define data science beyond a set of best practices used in tech
companies. That’s the definition we started with at the start of the
book. But after going through this exploration, now consider data
science to be beyond tech companies to include all other domains:
neuroscience, health analytics, eDiscovery, computational social
sciences, digital hu‐ manities, genomics, policy...to encompass the
space of all problems that could possibly be solved with data using a
set of best practices discussed in this book, some of which were
initially established in tech companies. 350

data science is a set of best practices used in tech companies,
working within a broad space of problems that could be solved with
data, possibly even at times deserving the name science. Even so, it’s
sometimes nothing more than pure hype, which we need to guard against
and avoid adding to. 350

## Naive Bayes

So how do we use Bayes' law to create a good spam filter? Think about it this way: if the word "Viagra" appears, this adds to the probability that the email is spam. But it's not conclusive yet. We need to see what else is in the email.  Let first focus on just one word at a time, which we generically call "word." Then applying Bayes' Law, we have:

$$p(spam|word) = {p(word|spam) p(spam)}/p(word)$$  99

The righthand side of this equation is computable using enough pre-labeled data.99

In other words, we've boiled ti down to a counting exercise. 100
To do this yourself, go online and download the Enron emails ... Let's build a spam filter on that dataset. This really this means [sic] we're building a new spam filter on top of the spam filter that existed for the employees of Enron. We'll use their definition of spam to train our spam filter. 100

A Spam Filter that Combines Words: Naive Bayes

Each email can be represented by a binary vector, whose _j_th entry is 1 or O depending on whether the _j_th word appears. Note this is a huge-ass vector, considering how many words appears, and we'd probably want to represent it with indices of the words that actually show up. 101

The model's output is the probability that we'd see a given word vector given that we know it's spam (or that it's ham) 101

Denote the email vector to be $x$ and the various entries $x_j$, where the $j$ indexes the words. For now, we can denote "is spam" by $c$, and we have the following model for $p(x|c)$, i.e., the probability that the email's vector looks like this considering it's spam:

$$p(x|c) = \prod_{j} \theta_{jc}^{x_j}(1-\theta_{jc})^{(1-x_j)}$$

The $\theta$ here is the probability that an individual word is present in a spam email 101



We are modeling the words _independently_ (also known as "independent trials"), which is why we take the product on the righthand side of the preceding formula and don't count how many times they are present. That's why it is called "naive," because we know that there are actually certain words that tend to appear together, and we're ignoring this. 101


