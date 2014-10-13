by taking the de Finetti theorem seriously, we can capture significant intra-document statistical structure via the mixing distribution. 995

A word is the basic unit of discrete data, defined to be an item from a vocabulary indexed by
{1, . . . ,V }. We represent words using unit-basis vectors that have a single component equal to one and all other components equal to zero. Thus, using superscripts to denote components, the vth word in the vocabulary is represented by a $V$ -vector $w$ such that $w^v = 1$ and $w^u = 0$ for $u = v$ 995

A document is a sequence of $N$ words denoted by $w = (w_1 , w_2 , . . . , w_N )$, where $w_n$ is the nth word in the sequence. 995

Latent Dirichlet allocation (LDA) is a generative probabilistic model of a corpus. The basic idea is that documents are represented as random mixtures over latent topics, where each topic is characterized by a distribution over words. 996

LDA assumes the following generative process for each document **w** in a corpus D :
1. Choose N ∼ Poisson(ξ).
2. Choose θ ∼ Dir(α).
3. For each of the N words w_n :
(a) Choose a topic z_n ∼ Multinomial(θ).
(b) Choose a word w_n from p(w_n | z_n , β), a multinomial probability conditioned on the topic $z_n$ 996

