Download Link: https://assignmentchef.com/product/solved-cs-754-assignment-5
<br>
Advanced Image Processing




<ol>

 <li>Consider an inverse problem of the form y = ?-L(x) + η where y is the observed degraded and noisy image, x is the underlying image to be estimated, η is a noise vector, and ?-L represents a transformation operator. In case of denoising, this operator is represented by the identity matrix. In case of compressed sensing, it is the sensing matrix, and in case of deblurring, it represents a convolution. The aim is to estimate x given y and ?-L as well as the noise model. This is often framed as a Bayesian problem to maximize p(x|y, ?-L) ∝ p(y|x, ?-L)p(x). In this relation, the first term in the product on the right hand side is the likelihood term, and the second term represents a prior probability imposed on x.</li>

</ol>

With this in mind, we refer to the paper ‘User assisted separation of reflections from a single image using a sparsity prior’ by Anat Levin, IEEE Transactions on Pattern Analysis and Machine Intelligence. Answer the following questions:

<ul>

 <li>In Eqn. (7), explain what <sub>Aj→</sub> and bj represent, for each of the four terms in Eqn. (6).</li>

 <li>In Eqn. (6), which terms are obtained from the prior and which terms are obtained from the likelihood? What is the prior used in the paper? What is the likelihood used in the paper?</li>

 <li>Why does the paper use a likelihood term that is different from the Gaussian prior? [7+12+6=25 points]</li>

</ul>

<ol start="2">

 <li>Consider compressive measurements of the form y = 4x + η under the usual notations with y E R<sup>m</sup>, 4 E R<sup>mxn</sup>,m &lt;&lt; n, x E R<sup>n</sup>, η ∼ N(0, <sub>σ2Imxm).</sub> Instead of the usual model of assuming signal sparsity in an orthonormal basis, consider that x is a random draw from a zero-mean Gaussian distribution with known covariance matrix Σ<strong><sub>x</sub></strong> (of size n × n). Derive an expression for the maximum a posteriori (MAP) estimate of x given y, 4, Σ<strong><sub>x</sub></strong>. Also, run the following simulation: Generate Σ<strong><sub>x</sub></strong> = UΛU<sup>T</sup> of size 128 × 128 where U is a random orthonormal matrix, and Λ is a diagonal matrix of eigenvalues of the form ci−<sup>α</sup> where c = 1 is a constant, i is an index for the eigenvalues with 1 i n and α is a decay factor for the eigenvalues. Generate 10 signals from N(0, Σ<strong><sub>x</sub></strong>). For m E {40, 50,64,80, 100, 120}, generate compressive measurements of the form y = 4x + η for each signal x. In each case, 4 should be a matrix of iid Gaussian entries with mean 0 and variance 1/m, and σ = 0.01× the average absolute value in 4x. Reconstruct x using the MAP formula, and plot the average RMSE versus m for the case α = 3 and α = 0. Comment on the results – is there any difference in the reconstruction performance when α is varied? If so, what could be the reason for the difference? [25 points]</li>

</ol>




<ol start="3">

 <li>Read through the proof of Theorem 3.3 from the paper ‘Guaranteed Minimum-Rank Solutions of Linear Matrix Equations via Nuclear Norm Minimization’ from the homework folder. This theorem refers to the optimization problem in Eqn. 3.1 of the same paper. Answer all the questions highlighted within the proof. You may directly use linear algebra results quoted in the paper without proving them from scratch, but mention very clearly which result you used and where. [12 × 2 +1 = 25 points]</li>

 <li>Read section 1 of the paper ‘Exact Matrix Completion via Convex Optimization’ from the homework folder. Answer the following questions: (1) Why do the theorems on low rank matrix completion require that the singular vectors be incoherent with the canonical basis (i.e. columns of the identity matrix)? (2) How would this coherence condition change if the sampling operator were changed to the one in Eqn. 1.13 of the paper? [10 points]</li>

 <li>Read section 5.9 of the paper ‘Low-Rank Modeling and Its Applications in Image Analysis’ from the home­work folder. You will find numerous image analysis or computer vision applications of low rank matrix modelling and/or RPCA, which we did not cover in class. Your task is to glance through any one of the papers cited in this section and answer the following: (1) State the title and venue of the paper; (2) Briefly explain the problem being solved in the paper; (3) Explain how low rank matrix recovery/completion or RPCA is being used to solve that problem. Write down the objective function being optimized in the paper with meaning of all symbols clearly explained. [5 + 10 = 15 points]</li>

</ol>