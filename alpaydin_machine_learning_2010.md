# alpaydin_machine_learning_2010


## Naive Bayes

If the inputs are independent, we have the graph shown in ... which is called the _naive Bayes' classifier_, because it ignores possible dependences, namely, correlations, among the inputs and reduces a multivariate problem to a group of univariate problems. 397

It is as if we first pick a class $C$ at random by sampling from $P(C)$, and then having fixed $C$, we pick as $\mathbf{x}$ by sampling from $p(\mathbf{x}|C)$. ... For example, in text categorization, generating a text may be thought of as the process where an author decides to write a document on a certain topic and then chooses the set of words accordingly. 398


## neural net 
 It is as if the error propagates from the output _y_ back to the inputs and hence the name _backpropagation_ was coined 250

Perhaps the most important contribution of research on neural networks is this synergy that bridged various disciplines, epsecially statistics and engineering. It is thanks to this that the field of machine learning is now well established. 274

\begin {equation}
\label {eq:nonlinear_sigmoid}
z_h = \frac{1}{1 + exp{[-(\sum_{j=1}^d} w_{hj} x_{j} + w_{h0})]}, h = 1 ...,H
\end {equation}
[@Alpaydin_2010, 246]

\begin {equation}
\label {eq:nn_classifier}
y_t = \frac{1}{1+exp([-(\sum_{h=1}^{H}v_hz_h^t + v+0]}
\end {equation}

[@Alpaydin_2010, 252]
