# SVM: Support Vector Machines, Xue in Xindong Wu, Top 10 Algorithms in Data Mining

However, in many real-world problems, it may be too rigid to require that all points are linearly separable, especially in many complex nonlinear classification cases. 

The kernel trick is another commonly used technique to solve linearly inseparably problems. This issue is to define an appropriate kernel function based on the _inner product_ between the given data, as a nonlinear transformation of data from the input space to a feature space with higher (even infinite) dimension in order to make the problems linearly separable. The underlying justification can be found in _Cover's theorem_ on the separability of patterns; that is, a complex pattern classification problem case in a high-dimensional space is _more likely_ to be linearly separable than in a low dimensional space. 42

