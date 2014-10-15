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

\begin {equation}
\label {eq: topic_model}
p(\theta, \mathbf{z, w} | \alpha, \beta) = p(\theta | \alpha) \prod p(z_n | \theta)p(w_n | z_n , \beta),
\end {equation}
[@Blei_2003, 996]

there are three levels to the LDA representation. The parameters $\alpha$ and $\beta$ are corpus- level parameters, assumed to be sampled once in the process of generating a corpus. The variables $\theta_d$ are document-level variables, sampled once per document. Finally, the variables $z_dn$ and $w_dn$ are word-level variables and are sampled once for each word in each document.
It is important to distinguish LDA from a simple Dirichlet-multinomial clustering model. A classical clustering model would involve a two-level model in which a Dirichlet is sampled once for a corpus, a multinomial clustering variable is selected once for each document in the corpus, and a set of words are selected for the document conditional on the cluster variable. As with many clustering models, such a model restricts a document to being associated with a single topic. LDA, on the other hand, involves three levels, and notably the topic node is sampled repeatedly within the document. Under this model, documents can be associated with multiple topics. 997

 LDA is a simple model, and although we view it as a competitor to methods such as LSI and pLSI in the setting of dimensionality reduction for document collections and other discrete cor- pora, it is also intended to be illustrative of the way in which probabilistic models can be scaled up to provide useful inferential machinery in domains involving multiple levels of structure. In- deed, the principal advantages of generative models such as LDA include their modularity and their extensibility.1015
