---
content_type: page
description: This page includes lecture notes and readings for each lecture.
draft: false
title: Lecture Notes and Readings
uid: dc60f1da-e984-4045-b07c-af4129d934e0
---
Lecture notes were prepared by Paige Bright under the guidance of Professors Edelman and Johnson. {{% resource_link "b67b8d11-1918-467a-bb76-1cfdb8289174" "Full Course Notes (PDF)" %}}   
The notes are also available on {{% resource_link "d1dad955-1ef3-4cd9-92e5-043bb9d7d234" "arXiv.org" %}}, along with any updates and citing information.

## Lecture 1

### Outline

**Part 1:** Overview, applications, and motivation.

**Part 2:** Rethinking derivatives as linear operators: f(x + dx) - f(x) = df = f′(x)\[dx\] — f′ is the {{% resource_link "f844443e-309c-4d50-b2bb-3881b83c56d4" "linear operator" %}} that gives the change df in the output from a "tiny" change dx in the inputs, to first order in dx (i.e. dropping higher-order terms). When we have a scalar function f(x) ∈ ℝ of vector inputs x ∈ ℝⁿ, then this gives us a "row vector" f′(x) since f′(x)dx is a scalar, which we interpret as the transpose of the gradient ∇f (which we call a "column" vector), i.e. df = (∇f) ⋅ dx = (∇f)ᵀdx. When we have a vector function f(x) ∈ ℝᵐ of vector inputs x ∈ ℝⁿ, then f'(x) is a linear operator that takes n inputs to m outputs, which we can think of as an m × n matrix called the {{% resource_link "cc78952a-fe94-438b-9fed-cf1a8f53b6f2" "Jacobian matrix" %}} (typically covered only superficially in {{% resource_link "03cb8060-ce30-41b4-a501-1d8957951bc5" "*18.02 Multivariable Calculus*" %}}.)

### Lecture Notes and Slides

- *Course notes: Chapter 1, and Chapter 2, Sections 2.1–2.3*
- Chapter 1: {{% resource_link "532b0906-f056-4c35-8800-db8207fd5011" "Lecture 1, Part 1 Notes: Overview and Motivation (PDF)" %}}  
- Part 1 Slides: {{% resource_link "db5aaa4c-5321-46b2-8ef2-55b2a072adeb" "Introduction (PDF)" %}}
- Chapter 2: {{% resource_link "d80e29bd-e7c8-4feb-836e-6afa2914ccde" "Lecture 1, Part 2 Notes: Derivatives as Linear Operators (PDF)" %}} 

### Further Readings

- {{% resource_link "537f647f-9d46-494d-9cec-d6cb72e874f8" "matrixcalculus.org" %}} is a fun site to play with derivatives of matrix and vector functions. 
- {{% resource_link "d9f27dce-157c-4cde-8233-0f6789cea8d6" "*The Matrix Cookbook* (PDF)" %}} has a lot of formulas for these derivatives, but no derivations.
- Notes on {{% resource_link "5fe6d429-d2a8-4d52-a3d5-930accbddbfe" "Vector and Matrix Differentiation (PDF)" %}} from *6.S087 Special Subject in Electrical Engineering and Computer Science* (IAP 2021) are helpful.
- **Fancier math:** The perspective of derivatives as linear operators is sometimes called a {{% resource_link "d9923c9d-3800-4ffa-9600-32729c06dd6b" "Fréchet derivative" %}} and you can find lots of very abstract (what I'm calling "fancy") presentations of this online, chock full of weird terminology whose purpose is basically to generalize the concept to weird types of vector spaces. The "little-o notation" o(δx) we're using here for "infinitesimal asymptotics" is closely related to the {{% resource_link "08ec776b-bc65-48ca-897a-63fc70a563ca" "Big *O* notation" %}} used in computer science, but in computer science people are typically taking the limit as the argument (often called "n") becomes very large instead of very small. A fancy name for a row vector is a "covector" or {{% resource_link "c9d00f7e-c325-4a06-bd35-a9b82d9da917" "linear form" %}}, and the fancy version of the relationship between row and column vectors is the {{% resource_link "2ce57120-50aa-4e06-902c-dd9131bd9d53" "Riesz representation theorem" %}}, but until you get to non-Euclidean geometry you may be happier thinking of a row vector as the transpose of a column vector.

## Lecture 2

### Outline

**Part 1:** Continued discussing derivatives as linear operators, starting with Jacobian matrices. Reviewed the sum rule d(f + g) = df + dg, the product rule d(fg) = (df)g + f(dg), and the chain rule for f(g(x)) (f'(x) = g'(h(x))h'(x), where this is a composition of two linear operations, performing h' then g' — g'h' ≠ h'g'!). For functions from vectors to vectors, the chain rule is simply the product of Jacobians. Moreover, as soon as you compose 3 or more functions, it can make a huge difference whether you multiply the Jacobians from left to right ("reverse-mode", or "backpropagation", or "adjoint differentiation") or right to left ("forward-mode"). Showed, for example, that if you have many inputs but a single output (as is common in machine learning and other types of optimization problems), that it is vastly more efficient to multiply left-to-right than right-to-left, and such "backpropagation algorithms" are a key factor in the practicality of large-scale optimization. Finally, began talking about functions in more general vector spaces, such as functions with **matrix inputs and/or outputs**. For example, considered f(A) = A³, giving d(A³) = f′(A)\[dA\] = A²(dA) + A(dA)A + (dA)A² (≠3A²dA!), and f(A) = A⁻¹, giving d(A⁻¹) = -A⁻¹(dA)A⁻¹.

**Part 2:** Began going into more detail on matrix-valued functions, and their relationship to the "Jacobian matrix" picture. Converting f′(A) to a conventional "Jacobian matrix" in such cases requires converting matrices A into column vectors vec(A), a process called "vectorization" of the matrix (by a common convention: simply stacking the matrix by columns). Linear operators like f′(A)\[dA\] = AdA + dAA can then be expressed as "ordinary" matrices via {{% resource_link "30b27c8f-8619-4436-9ddf-af799c0c40cb" "Kronecker products" %}}.

### Lecture Notes and Other Resources

- *Course notes: Chapter 2, Sections 2.4–2.6, and Chapter 3*
- Part 0: {{% resource_link "03190bfa-feb9-4cc9-9b10-c7fb9b0a4fb4" "Examples of Linear and Nonlinear Transformations of ℝ² via Images (try it online)" %}}
- Part 1: Derivatives as Linear Operators (continued) 
    - Chapter 2: {{% resource_link "d80e29bd-e7c8-4feb-836e-6afa2914ccde" "Lecture 1, Part 2 Notes: Derivatives as Linear Operators (PDF)" %}} 
- Chapter 3: {{% resource_link "98865698-8f4e-4766-9e15-a2d0d1d8f14d" "Lecture 2, Part 2 Notes: Jacobians of Matrix Functions (PDF)" %}} 
- Part 2 (Matrix Jacobians via {{% resource_link "844b8704-6d07-47a4-9604-df208c14cc64" "Vectorization" %}}): {{% resource_link "e4620a02-1348-4ed9-a7f8-57a10ed21e8b" "Two by Two Matrix Jacobians (HTML)" %}} {{% resource_link "d6549c38-24d1-4cad-85ba-b7be4bf7f9e1" "(Pluto notebook source code)" %}}

### Further Readings

- The terms "forward-mode" and "reverse-mode" differentiation are most prevalent in {{% resource_link "a867daa3-d854-4ec9-9dd6-1b431d59869f" "automatic differentiation" %}} (AD), which we will cover later in this course. 
- You can find many, many articles online about {{% resource_link "01a9fb24-74e3-4a20-be77-485726ec1470" "backpropagation" %}} in neural networks. 
- There are many other versions of this, e.g. in differential geometry the derivative linear operator (multiplying Jacobians and perturbations dx right-to-left) is called a {{% resource_link "e24abf9d-0f50-42b5-a3f0-b289507a9b6d" "pushforward" %}}, whereas multiplying a gradient row vector (covector) by a Jacobian left-to-right is called a {{% resource_link "44500d4e-0002-41f9-8521-34cac016ab01" "pullback" %}}. 
- The video on {{% resource_link "d379a0bb-a947-45b9-a8bc-34c5e9791b8b" "Understanding Automatic Differentiation (in Julia) (YouTube)" %}} by {{% resource_link "1730842c-131f-4e1f-bea7-792396f7fd1c" "Dr. Mohamed Tarek" %}} also starts with a similar left-to-right (reverse) vs right-to-left (forward) viewpoint and goes into how it translates to Julia code, and how you define custom chain-rule steps for Julia AD.

## Lecture 3

### Outline

**Part 1:** Continued from Lecture 2: matrix functions, Jacobians, vectorizations, and Kronecker products. More examples of matrix functions, including LU factorization and 2 × 2 eigenproblems.

**Part 2:** Finite-difference methods: viewing f(x + δx) – f(x) as an approximation for f'(x)δx on a computer. This is extremely useful as a quick check of a hand-derived derivative (which is very error-prone for complicated functions), and can also be used as a replacement for analytical derivatives in a pinch. Analyzed two sources of error: truncation error (from the non-infinitesimal δx) and roundoff error (from the finite precision of computer arithmetic).

### Lecture Notes and Other Resources

- *Course notes: Chapter 3 and Chapter 4* 
- Part 1 (Lecture 2 Part 2 continued)
    - Chapter 3: {{% resource_link "98865698-8f4e-4766-9e15-a2d0d1d8f14d" "Lecture 2, Part 2 Notes: Jacobians of Matrix Functions (PDF)" %}} 
-  {{% resource_link "e4620a02-1348-4ed9-a7f8-57a10ed21e8b" "Two by Two Matrix Jacobians (HTML)" %}} {{% resource_link "d6549c38-24d1-4cad-85ba-b7be4bf7f9e1" "(Pluto notebook source code)" %}}
- Chapter 4: {{% resource_link "6ba1e5b8-0fb9-454e-9a1c-372bfcbaae9a" "Lecture 3, Part 2 Notes: Finite-Difference Approximations (PDF)" %}} 
- Part 2: {{% resource_link "2eb4df92-c4c5-4c85-8856-cc26d537bdd7" "Finite Difference (Jupyter notebook)" %}}

### Further Readings

- Wikipedia has a useful list of {{% resource_link "5fb89e3a-e97f-45be-b3ab-07236d6bb527" "properties of the matrix trace" %}}. 
- The "matrix dot product" introduced today is also called the {{% resource_link "64c73c8b-4b3f-4ab7-b7a3-bbfd78dde082" "Frobenius inner product" %}}, and the corresponding norm ("length" of the matrix viewed as a vector) is the {{% resource_link "95dcf417-43f1-4f5c-ba91-3a6354dfc7b4" "Frobenius norm" %}}. 
- When you "flatten" a matrix A by stacking its columns into a single vector, the result is called {{% resource_link "844b8704-6d07-47a4-9604-df208c14cc64" "vec(A)" %}}, and many important linear operations on matrices can be expressed as {{% resource_link "30b27c8f-8619-4436-9ddf-af799c0c40cb" "Kronecker products" %}}. 
- {{% resource_link "d9f27dce-157c-4cde-8233-0f6789cea8d6" "*The Matrix Cookbook* (PDF)" %}} has lots of formulas for derivatives of matrix functions. 
- There is a lot of information online on {{% resource_link "fdc57961-aed5-451d-b467-e4ece31e5b4c" "finite difference" %}}, {{% resource_link "bec59407-2b38-4fa0-a84e-788b1e43de9e" "18.303 Notes on Finite Differences (PDF)" %}}, or {{% resource_link "4a610e68-eed5-4a62-87cc-d45c1c5a8256" "Section 5.7 of Numerical Derivatives (PDF)" %}}. 
- The Julia {{% resource_link "88db0219-7934-46a2-bd41-b8da6f4704da" "FiniteDifferences.jl" %}} package provides lots of algorithms to compute finite-difference approximations; a particularly robust and powerful way to obtain high accuracy is to employ {{% resource_link "6938875a-f445-4615-88c5-32d4e3a66e33" "Richardson extrapolation" %}} to smaller and smaller δx. If you make δx too small, the finite precision (#digits) of {{% resource_link "efc0d52f-19b1-4da7-acf5-8c31a03565a5" "floating-point arithmetic" %}} leads to {{% resource_link "06763fe7-a375-420e-8600-6bd1c08c5096" "catastrophic cancellation" %}} errors.

## Lecture 4

### Outline

**Part 0:** To begin with, spent a few minutes talking about the last few sections of the {{% resource_link "2eb4df92-c4c5-4c85-8856-cc26d537bdd7" "Finite Difference (Jupyter notebook)" %}} from last lecture: higher-order finite-difference rules and finite differences in higher dimensions (e.g. for gradients).

**Part 1:** Generalizing **gradients** to scalar functions f(x) for x in arbitrary vector spaces x ∈ V. The key thing is that we need not just a vector space, but an **inner product** x ⋅ y (a "dot product", also denoted ⟨x,y⟩ or ⟨x|y⟩); V is then formally called a {{% resource_link "bc91865c-0a71-47cb-b77c-9fe9808a5349" "Hilbert space" %}}. Then, for any scalar function, since df = f'(x)\[dx\] is a linear operator mapping dx ∈ V to scalars df ∈ ℝ (a "{{% resource_link "c9d00f7e-c325-4a06-bd35-a9b82d9da917" "linear form" %}}"), it turns out that it {{% resource_link "2ce57120-50aa-4e06-902c-dd9131bd9d53" "*must* be a dot product" %}} of dx with "something", and we call that "something" the gradient! That is, once we define a dot product, then for any scalar function f(x) we can define ∇f by f'(x)\[dx\] = ∇f ⋅ dx. So ∇f is always something with the same "shape" as x (the {{% resource_link "78d84470-aa95-4ad0-a8a3-b2bc74b93bf1" "steepest-ascent" %}} direction).

Defined the most obvious inner product of m × n matrices: the {{% resource_link "64c73c8b-4b3f-4ab7-b7a3-bbfd78dde082" "Frobenius inner product" %}} A\\(\cdot\\)B = sum(A\\(\cdot\ast\\)B) = trace(AᵀB) = vec(A)ᵀvec(B), the sum of the products of the matrix entries. This also gives us the "Frobenius norm" ‖A‖² = A ⋅ A = trace(AᵀA) = ‖vec(A)‖², the square root of the sum of the squares of the entries. Using this, we can now take the derivatives of various scalar functions of matrices, e.g. we considered

- f(A) = ‖A‖ ⥰ ∇f = A/‖A‖
- f(A) = xᵀAy ⥰ ∇f = xyᵀ (for constant x, y)
- f(A) = det(A) ⥰ ∇f = det(A)(A⁻¹)ᵀ = {{% resource_link "d62a483e-7446-4738-aa84-7b888d6b9304" "adjugate" %}}(A)ᵀ: we will prove this later

**Part 2:** Applications of derivatives to multivariate root-finding and optimization. A key fact enabling large-scale optimization, i.e. min f(x) where f is a scalar function of *many* parameters x, is that computing ∇f has about the same cost as f, using what is variously called "reverse-mode" or "adjoint" or "backpropagation" differentiation algorithms, which essentially boil down to evaluating the chain rule **left to right**. Went through a few examples of this, oriented more at engineering/physics optimization (and "topology optimization").

### Lecture Notes and Slides

- *Course notes: Section 5.1, and Chapter 6*
- Chapter 5: {{% resource_link "7af616b9-bb47-4b92-88fb-f01a4faed704" "Lecture 4, Part 1 Notes: Derivatives in General Vector Spaces (PDF)" %}} 
- Chapter 6: {{% resource_link "6d55b3ea-f560-4129-9386-11f2f0f329e6" "Lecture 4, Part 2 Notes: Nonlinear Root-Finding, Optimization, and Adjoint Differentiation (PDF)" %}} 
- Part 2 Slides: {{% resource_link "f46d4277-f227-44f7-a6dd-7176e7d45df4" "Nonlinear Root-Finding, Optimization, and Adjoint-Method Differentiation (PDF)" %}}

### Further Readings (Part 2)

- Prof. Steven Johnson gave another {{% resource_link "b5918a21-91bd-4e47-b8af-4cda12a3c05a" "overview of optimization problems (PDF)" %}} in *18.335 Introduction to Numerical Methods*. 
- There are many textbooks on nonlinear programming, including {{% resource_link "c492cb03-3f2a-4eeb-97dc-5174083862fe" "*Nonlinear Programming*" %}} (by Bertsekas) and specialized books on {{% resource_link "8bf62ddb-a05e-4a62-878c-fc7330df904c" "*Convex Optimization*" %}} (by Boyd and Vandenberghe), {{% resource_link "ca30bb8d-1d10-405d-aa85-b83750e1be58" "*Introduction to Derivative-Free Optimization*" %}} (by Conn, Scheinberg, and Vicente), etc. 
- A useful review of topology-optimization methods can be found in {{% resource_link "e5c78f86-ac98-44ae-bac5-4c63900fb85f" "Topology Optimization Approaches" %}} (by Sigmund and Maute). 
- See the {{% resource_link "9a77ab27-d3bb-4c20-8604-68049bee5dfc" "Notes on Adjoint Methods (PDF)" %}} and {{% resource_link "c0bc583d-e863-4532-8b0e-92d560c64d84" "The Adjoint Method for Differentiating Complex Computations (PDF)" %}} from *18.335 Introduction to Numerical Methods*. 

## Lecture 5

### Lecture Notes and Other Resources

- *Course notes: Section 5.2, Chapter 7, and Sections 8.1–8.2*
- Part 0: Norms and Derivatives: Why a Norm of the Input and Output Are Needed to Define a Derivative
- Chapter 7:{{% resource_link "0bf49c20-75d0-4e15-a605-390ec1f204e1" "Lecture 5, Part 1 Notes: Derivative of Matrix Determinant and Inverse (PDF)" %}}  
- Part 1: {{% resource_link "8b8dc58b-622f-4fdb-8fb5-c1471efcfe7f" "Derivative of Matrix Determinant and Inverse (HTML)" %}} {{% resource_link "58261f48-bbeb-4a98-b042-4ce2be056a03" "(Julia source code)" %}}
- Part 2: {{% resource_link "0d694db0-d49e-4316-939e-8a4001f6aaa2" "Forward-Mode Automatic Differentiation via Dual Numbers (Jupyter notebook)" %}}
- Chapter 8: {{% resource_link "dd866538-0b2b-491b-85f9-005b8cbc7673" "Lecture 5, Part 3 Notes: Forward and Reverse-Mode Automatic Differentiation (PDF)" %}} 

### Further Readings (Part 1)

- There are lots of discussions of the {{% resource_link "f6a5c441-c4df-4721-96b6-1c1092ffa087" "derivative of a determinant" %}} online, involving the {{% resource_link "d62a483e-7446-4738-aa84-7b888d6b9304" "\"adjugate\" matrix" %}} det(A)A⁻¹. Not as well documented is that the gradient of the determinant is the cofactor matrix widely used for the {{% resource_link "5290b4e8-e45b-458f-8113-3277370b6bf9" "Laplace expansion" %}} of a determinant. The formula for the {{% resource_link "1c2c7e97-822a-4a29-90d3-365bf39c9581" "derivative of log(det A)" %}} is also nice, and logs of determinants appear in surprisingly many applications (from statistics to quantum field theory). 
- {{% resource_link "d9f27dce-157c-4cde-8233-0f6789cea8d6" "*The Matrix Cookbook* (PDF)" %}} contains many of these formulas, but no derivations. 
- A nice application of d(det(A)) is solving for eigenvalues λ by applying Newton's method to det(A - λI) = 0, and more generally one can solve det(M(λ)) = 0 for any function Μ(λ) — the resulting roots λ are called {{% resource_link "7739793b-b8db-4da4-bd6d-aa94456884b4" "nonlinear eigenvalues" %}} (if M is nonlinear in λ), and one can apply Newton's method using the determinant-derivative formula here.

### Further Readings (Part 2)

- Googling "automatic differentiation" will turn up many, many resources—this is a huge practical field these days. {{% resource_link "d5ce3763-d0a2-484a-ae0b-ce80727580f6" "ForwardDiff.jl" %}} (described in detail by "{{% resource_link "9ebabf06-4524-4ad5-a573-cc8b5c37cb53" "Forward-Mode Automatic Differentiation in Julia" %}}") uses {{% resource_link "68b7aa40-2fe5-47e1-81bd-a0b941e3d284" "dual number" %}} arithmetic similar to lecture to compute derivatives.
- See also the article "{{% resource_link "02e7253c-009a-49b0-8b5a-03f6e6a5dea4" "How to Differentiate with a Computer" %}}," or google "dual number automatic differentiation" for many other reviews. 

### Further Readings (Part 3)

- See {{% resource_link "e2546e73-4dee-4057-b788-6b594ddcbf5c" "Backpropagation through Back Substitution with a Backslash (PDF)" %}} about backpropagation on graphs, this blog post on {{% resource_link "35101fd9-1d1b-4530-ab82-7a1a9855d781" "calculus on computational graphs" %}} for a gentle review, and Columbia University’s {{% resource_link "417b57f4-2631-49c7-a390-7a5a085e7f8c" "Course Notes on Computational Graphs, and Backpropagation (PDF)" %}} for a more formal approach. 
- Implementing automatic reverse-mode AD is much more complicated than defining a new number type, unfortunately, and involves a lot more intricacies of compiler technology. See also Chris Rackauckas's blog post on {{% resource_link "cae1a0d1-407b-4a5a-afd9-b14303a063d0" "Engineering Trade-Offs in Automatic Differentiation: from TensorFlow and PyTorch to Jax and Julia" %}}, and Chris's discussion post on {{% resource_link "af953c1e-6a42-40c8-a763-cb19935f3a6e" "AD limitations" %}}.

## Lecture 6

### Lecture Notes and Slides

- *Course notes: Chapter 9 and Chapter 10*
- Chapter 9: {{% resource_link "1fb6c24e-c6b5-41f7-9405-56f9ff7bb689" "Lecture 6, Part 1a Notes: Differentiating ODE Solutions (PDF)" %}} 
- Part 1 Slides: {{% resource_link "1a34cc63-b920-4b86-80da-3c0f7566b9d5" "An Introduction to (Local) Sensitivity Analysis for (Ordinary) Differential Equations (PDF)" %}} (Courtesy of Frank Schäfer. Used with permission.)
- Chapter 10: {{% resource_link "4eca7e53-5fc8-49db-b808-e09685ee385e" "Lecture 6, Part 1b Notes: Calculus of Variations (PDF)" %}} 

### Further Readings (Part 1)

- A classic reference on adjoint-method (reverse-mode/backpropagation) differentiation of ODEs (and generalizations thereof), using notation similar to that used today, is {{% resource_link "a4197afa-076e-4ae8-b439-c455af79809d" "Adjoint Sensitivity Analysis for Differential-Algebraic Equations: The Adjoint DAE System and Its Numerical Solution" %}} ({{% resource_link "5875a7c3-8478-4d8e-aa3a-1a993a1c0628" "PDF" %}}). 
- See also the {{% resource_link "b33423e9-613a-4eda-b67e-c954c61d934b" "SciMLSensitivity.jl package" %}} for sensitivity analysis with Chris Rackauckas's amazing {{% resource_link "fc79ba97-4aa3-4f2c-aaa2-8a9bb6036b1b" "DifferentialEquations.jl software suite" %}} for numerical solution of ODEs in Julia, along with his notes {{% resource_link "094a693b-8dee-4494-8ecc-2750f14d0850" "Differentiable Programming and Neural Differential Equations" %}}. 
- There is a nice YouTube lecture on {{% resource_link "b14cb376-9f82-44bf-9e50-c97e88d39dd9" "Adjoint State Method for an ODE" %}}, again using a similar notation. 
- A *discrete* version of this process is {{% resource_link "ad1b7c9a-680f-4cd8-a9db-b550fe336760" "adjoint methods and sensitivity analysis for recurrence relations (PDF)" %}} (MIT course notes), in which case one obtains a reverse-order "adjoint" recurrence relation.

### Further Readings (Part 2)

- There are many resources on the {{% resource_link "340c35e4-dbc7-4976-917b-af5d5763c428" "\"calculus of variations\"" %}}, which refers to derivatives of f(u) = ∫F(u,u′,…)dx for functions u(x), but we saw that it is essentially just a special case of our general rule df = f(u + du) - f(u) = f′(u)\[du\] = ∇f ⋅ du when du lies in a vector space of functions. Setting ∇f to find an extremum of f(u) yields an {{% resource_link "5993a627-ed9e-4700-ba62-15d9c3c1e81c" "Euler–Lagrange equation" %}}, the most famous examples of which are probably {{% resource_link "b57765a2-fc2d-44de-a937-bfa0ca11f303" "Lagrangian mechanics" %}} and also the {{% resource_link "bbc19180-f10f-476b-95c6-04710b84044d" "Brachistochrone problem" %}}, but it also shows up in many other contexts such as {{% resource_link "11784f09-0d6e-4495-ad31-0465cc768ec8" "optimal control" %}}. 
- A very readable textbook on the subject is {{% resource_link "f14ca1d0-71f8-43af-a57b-53a67e535d1f" "*Calculus of Variations* by Gelfand and Fomin" %}}.

## Lecture 7

### Lecture Notes

- *Course notes: Chapter 11 and Chapter 12*
- Chapter 11: {{% resource_link "ffdcd720-dc4b-467a-861a-a6ff79ab6ff4" "Lecture 7, Part 1 Notes: Derivative of Random Functions (PDF)" %}} 
- Lecture 7, Part 1 Guest Lecture Notes: {{% resource_link "c66c314f-efc2-4a08-9982-e966fb2400c6" "Derivatives of Random Functions (PDF)" %}} (Courtesy of Gaurav Arya. Used with permission.)
- Chapter 12: {{% resource_link "7724967d-1b72-4498-b202-440d7437d3eb" "Lecture 7, Part 2 Notes: Second Derivatives, Bilinear Forms, and Hessian Matrices (PDF)" %}} 

### Further Readings (Part 1)

- The idea of computing gradients of programs with a sampleable random output is called {{% resource_link "7aa9ff8e-6c43-4dca-98c4-affdebeccafc" "Monte-Carlo Gradient Estimation" %}}; the link leads to a nice survey.
- This {{% resource_link "88e16317-93e2-49e1-ad84-0ffcbccca5c0" "Stack Exchange answer" %}} gives a concise, worked-out example of the reparameterization trick applied to a toy program.
- {{% resource_link "84300166-0f2f-4ef4-85cd-dc0c49d4fb16" "The frontier of simulation-based inference" %}} gives an overview of stochastic simulations across many domains of science, and discusses attempts to deal with the fact that it is much easier to sample them than to exactly compute a "likelihood."
- {{% resource_link "d35387c9-f9c6-4d5f-97e6-3924bf053de5" "Auto-Encoding Variational Bayes" %}} introduces the variational autoencoder, and introduces the reparameterization trick for use in training it.
- {{% resource_link "6a8e3013-0a22-4e69-be3b-6c388da647ab" "Automatic differentiation of programs with discrete randomness" %}} describes an approach for generalizing derivatives of continuous random functions based on the "reparameterization trick" to discrete random functions. {{% resource_link "753b69b7-b74d-4968-a345-59c4dac8ac17" "StochasticAD.jl" %}} is an associated code package that implements the stochastic triples we played with at the end of class.

### Further Readings (Part 2)

- {{% resource_link "c8d4076e-d995-4a61-a5c0-d431d7d1aa66" "Bilinear forms" %}} are an important generalization of quadratic operations to arbitrary vector spaces, and we saw that the second derivative can be viewed as a {{% resource_link "19cbdea8-7b72-4596-b6a6-36e8f0ea4d4c" "symmetric bilinear forms" %}}. This is closely related to a {{% resource_link "b04ffc02-02a5-4595-84ca-42679d686ff3" "quadratic form" %}}, which is just what we get by plugging in the same vector twice, e.g. the f''(x)\[δx,δx\]/2 that appears in quadratic approximations for f(x + δx) is a quadratic form. The most familiar multivariate version of f''(x) is the {{% resource_link "9967c78b-5d56-4862-bf1c-c4d8bbd4ef65" "Hessian matrix" %}}; Khan Academy has an elementary {{% resource_link "81985ef7-7f8a-445e-847c-0924308e6f36" "quadratic approximation" %}}.
- {{% resource_link "3eee53b6-20cd-4a09-95cc-2d9755a6ddfb" "Positive-definite" %}} Hessian matrices, or more generally {{% resource_link "f2f2c542-63cc-437f-ac3d-3f8c262e86fa" "definite quadratic forms" %}} f″, appear at extrema (f′ = 0) of scalar-valued functions f(x) that are local minima; there a lot {{% resource_link "067b8e69-584f-4684-994c-7b017b9ecd6b" "more formal treatments (PDF)" %}} of the same idea, and conversely Khan Academy has the {{% resource_link "a5e6ca09-0e07-494d-9618-7726c344145b" "simple 2-variable version" %}} where you can check the sign of the 2 × 2 eigenvalues just by looking at the determinant and a single entry (or the trace). There's a nice {{% resource_link "5c42ef7c-cbcb-4fae-91e4-efc1ae1740fa" "Stack Exchange discussion" %}} on why an {{% resource_link "fda90643-f358-48ba-847d-01ceee953e3f" "ill-conditioned" %}} Hessian tends to make steepest descent converge slowly; some Toronto {{% resource_link "7977a917-1bb5-46fe-b8a2-accd503537b2" "Optimization (PDF)" %}} may also be helpful.
- See e.g. these Stanford notes on {{% resource_link "28fae44e-be55-4fce-bc37-355584fb4a09" "Sequential Convex Programming (PDF)" %}} using trust regions (sec. 2.2). See 18.335 notes on {{% resource_link "f00369a4-1ff1-4ee0-91b1-b553ae0173b5" "Quasi-Newton Optimization: Origin of the BFGS Update (PDF)" %}}. The fact that a quadratic optimization problem in a sphere has {{% resource_link "fdd0b79a-1c9f-43de-bd2e-d2e1af52e2b6" "strong duality" %}} and hence is efficiently solvable is discussed in section 5.2.4 of the {{% resource_link "a07b7ced-21c2-4f9b-b226-941a347eac27" "*Convex Optimization*" %}}. There has been a lot of work on {{% resource_link "146ad57d-4236-4780-bd93-ea8a8258f5df" "automatic Hessian computation" %}}, but for large-scale problems you can ultimately only compute Hessian–vector products efficiently in general, which are equivalent to a directional derivative of the gradient, and can be used e.g. for {{% resource_link "940a096e-b787-49dd-a361-43fb8f54e0e3" "Newton–Krylov methods" %}}.

## Lecture 8

### Lecture Notes and Other Resources

- *Course notes: Chapter 13, and Chapter 8, Sections 8.3-8.4, and Chapter 14*
- Chapter 13: {{% resource_link "c135bd06-d239-432f-9f85-c1a607636ad3" "Lecture 8, Part 1 Notes: Derivatives of Eigenproblems (PDF)" %}} 
- Part 1: {{% resource_link "6163a704-8b0c-4c28-bee4-c2e0cf2bd0cf" "Derivatives of Eigenproblems (HTML)" %}} {{% resource_link "4753711e-3fce-40a0-9a52-4a7fdf51a06f" "(Julia source code)" %}}
- Part 2: Forward and Reverse-Mode Automatic Differentiation on Computational Graphs (continued from Lecture 5) and {{% resource_link "6c6dfd9a-bc8e-4cdd-a987-04514fbfbedc" "interactive notebook (HTML)" %}}
- Chapter 14: {{% resource_link "e46f9d46-cd58-4cca-91d5-2ec64ff054c9" "Lecture 8, Part 3 Notes: Where We Go From Here (PDF)" %}} 

### Further Readings (Part 1)

- Computing derivatives on curved surfaces ("manifolds") is closely related to {{% resource_link "501ce292-a373-4f8f-bcdc-3a8b052fafa5" "tangent spaces" %}} in differential geometry. The effect of constraints can also be expressed in terms of {{% resource_link "805c92c3-891b-4f2e-9439-6f7bf6cce54e" "Lagrange multipliers" %}}, which are useful in expressing optimization problems with constraints (see also chapter 5 of {{% resource_link "a07b7ced-21c2-4f9b-b226-941a347eac27" "*Convex Optimization*" %}} by Boyd and Vandenberghe). In physics, first and second derivatives of eigenvalues and first derivatives of eigenvectors are often presented as part of {{% resource_link "36f649a4-67b8-4a7d-853c-0842c2a6a723" "\"time-independent\" perturbation theory" %}} in quantum mechanics, or as the {{% resource_link "8a79edbd-088f-4582-ae6d-4457c6e135cd" "Hellmann–Feynmann theorem" %}} for the case of dλ. The derivative of an eigenvector involves *all* of the other eigenvectors, but a much simpler "vector–Jacobian product" (involving only a single eigenvector and eigenvalue) can be obtained from left-to-right differentiation of a *scalar function* of an eigenvector, as reviewed in the {{% resource_link "9a77ab27-d3bb-4c20-8604-68049bee5dfc" "Notes on Adjoint Methods for 18.335 (PDF)" %}}.

### Further Readings (Part 2)

- See Lecture 5, above.

### Further Readings (Part 3)

There are many topics that we did not have time to cover, even in 16 hours of lectures. If you came into this class thinking that taking derivatives is easy and you already learned everything there is to know about it in first-year calculus, hopefully we've convinced you that it is an enormously rich subject that is impossible to exhaust in a single course. Some of the things it might have been nice to include are:

- When AD hits something it can't handle, you may have to write a custom Jacobian–vector product (a "Jvp", "frule", or "pushforward") in forward mode, and/or a custom rowvector–Jacobian product (a "vJp", "rrule", "pullback", or Jacobianᵀ–vector product) in reverse mode. In Julia with Zygote AD, this is done using {{% resource_link "cc9f4166-ed0a-4dd9-a5aa-f7e0e844be58" "the ChainRules packages" %}}. In Python with JAX, this is done with {{% resource_link "035477aa-fbea-461d-93a1-57b3edbd45d0" "`jax.custom_jvp`" %}} and/or {{% resource_link "cc511ed6-a53e-4b47-bdd0-050b87c8eb31" "`jax.custom_vjp`" %}}, respectively. In principle this is straightforward, but the APIs can take some getting used to because of the generality that they support.
- For functions f(z) of complex arguments z (complex vector spaces), you cannot take "ordinary" complex derivatives whenever the function involves the conjugate z̄ (e.g. for |z|, Re z, or Im z); this *must* occur if f(z) is purely real-valued (and not constant). One option is to write z = x + iy and treat f(z) as a two-argument function f(x,y) with real derivatives, but this can be awkward if your problem is "naturally" expressed in terms of complex variables (e.g. in the {{% resource_link "b2170fdb-3e8b-44b3-99ce-b159404e7fc1" "Fourier frequency domain" %}}). A common alternative is "CR calculus" (or "Wirtinger calculus"), in which you write df = (∂f/∂z)dz + (∂f/∂z̄)dz̄ as if z and z̄ were independent variables. This can be extended to gradients, Jacobians, steepest-descent, and Newton iterations, for example. A nice review can be found in {{% resource_link "4e87930d-8eb3-4ffb-be19-e4015a60a406" "The Complex Gradient Operator and the CR-Calculus" %}} by Ken Kreuz-Delgado.
- Many, many more derivative results for matrix functions and factorizations can be found in the literature, some of them quite tricky to derive. For example, a number of references are listed in this GitHub issue for the {{% resource_link "ac82ff59-82d6-4bd5-bce0-97d0d090953a" "ChainRules package" %}}.
- Another important generalization of differential calculus is to derivatives on curved manifolds and differential geometry, leading to the {{% resource_link "e98c686c-bb4c-4f38-a1b6-faf3b46cee2c" "exterior derivative" %}}.
- When differentiating eigenvalues λ of matrices A(x), a complication arises at eigenvalue crossings (multiplicity k > 1), where in general the eigenvalues (and eigenvectors) cease to be differentiable. (More generally, this problem arises for any {{% resource_link "3be3f830-8c8c-4f2a-b20c-25ca05e3c301" "implicit function" %}} with a repeated root.) In this case, one option is to use an expanded definition of sensitivity analysis called a **generalized gradient** (a k × k matrix-valued linear operator G(x)\[dx\] whose eigenvalues are the perturbations dλ); see e.g. {{% resource_link "932604f6-9405-4615-ac31-af6c10c5c2f9" "Cox (1995)" %}}, {{% resource_link "897037aa-8465-4c1e-94a3-914a6d73978b" "Seyranian et al. (1994)" %}}, and {{% resource_link "6e0859e4-588b-4771-8396-534f75155aa6" "Stechlinski (2022)" %}}. (Physicists call this idea {{% resource_link "a00885aa-aaa4-47ae-b911-b0cfeaadefa1" "degenerate perturbation theory (PDF)" %}}.) A recent formulation of similar ideas is called a **lexicographic directional derivative**; see {{% resource_link "7c659a80-ed66-4c39-b98a-1d917f790567" "Nesterov (2005)" %}} and {{% resource_link "76aa21a3-11a0-47e5-ac50-08bce5345348" "Barton et al. (2017)" %}}. Sometimes, optimization problems involving eigenvalues can be reformulated to avoid this difficulty by using {{% resource_link "ef9291b5-073e-4950-beba-d148af4b5258" "SDP" %}} constraints {{% resource_link "f1cdbf58-8253-4370-a637-ca372756b764" "(Men et al. 2014)" %}}. For a {{% resource_link "80764357-5bf1-4c30-9133-695b243075be" "defective matrix" %}} the situation is worse: even the generalized derivatives blow up, because dλ is proportional to the *square root* of the perturbation ‖dA‖.
- Famous generalizations of differentiation are the {{% resource_link "6f146c0e-e752-4834-ad3d-44566184df86" "\"distributional\"" %}} and {{% resource_link "c438c6a6-a046-46d3-a271-6661f72a0133" "\"weak\"" %}} derivatives, for example to obtain {{% resource_link "9e761e07-b038-4ab9-b5a4-f973c3480ba1" "Dirac delta \"functions\"" %}} by differentiating discontinuities. This requires changing not only the definition of "derivative" but also *changing the definition of "function,"* as reviewed in {{% resource_link "9ec6a326-c2f5-4a1f-b65a-ff223de1b970" "When Functions Have No Value(s): Delta Functions and Distributions (PDF)" %}}.