---
content_type: page
description: This page includes course meeting times, prerequisites, course description,
  topics, and calendar.
draft: false
title: Syllabus
uid: c649638c-8d02-4221-ba19-ebc202192803
---
## Course Meeting Times

Lectures: 3 sessions / week, 2 hours / session

## Prerequisites

Courses in linear algebra (such as [*18.06 Linear Algebra*](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/)) and multivariate calculus (such as [*18.02 Multivariable Calculus*](https://ocw.mit.edu/courses/18-02sc-multivariable-calculus-fall-2010/))

## Course Description

We all know that calculus courses such as [*18.01 Single Variable Calculus*](https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/) and [*18.02 Multivariable Calculus*](https://ocw.mit.edu/courses/18-02sc-multivariable-calculus-fall-2010/) cover univariate and vector calculus, respectively. Modern applications such as machine learning and large-scale optimization require the next big step, "matrix calculus" and calculus on arbitrary vector spaces.

This class covers a coherent approach to matrix calculus showing techniques that allow you to think of a matrix holistically (not just as an array of scalars), generalize and compute derivatives of important matrix factorizations and many other complicated-looking operations, and understand how differentiation formulas must be re-imagined in large-scale computing. We will discuss reverse/adjoint/backpropagation differentiation, custom vector-Jacobian products, and how modern automatic differentiation is more computer science than calculus (it is neither symbolic formulas nor finite differences).

## Topics

Here are some of the topics covered:

- Derivatives as linear operators and linear approximation on arbitrary vector spaces: beyond gradients and Jacobians.
- Derivatives of functions with matrix inputs and/or outputs (e.g. matrix inverses and determinants). Kronecker products and matrix "vectorization."
- Derivatives of matrix factorizations (e.g. eigenvalues/SVD) and derivatives with constraints (e.g. orthogonal matrices).
- Multidimensional chain rules, and the signifance of right-to-left ("forward") vs. left-to-right ("reverse") composition. Chain rules on computational graphs (e.g. neural networks).
- Forward- and reverse-mode manual and automatic multivariate differentiation.
- Adjoint methods (vJp/pullback rules) for derivatives of solutions of linear, nonlinear, and differential equations.
- Application to nonlinear root-finding and optimization. Multidimensional Newton and steepest–descent methods.
- Applications in engineering/scientific optimization and machine learning.
- Second derivatives, Hessian matrices, quadratic approximations, and quasi-Newton methods.

## Calendar

{{< tableopen >}}{{< theadopen >}}{{< tropen >}}{{< thopen >}}
Lecture # and Topics
{{< thclose >}}{{< thopen >}}
Key Dates
{{< thclose >}}{{< trclose >}}{{< theadclose >}}{{< tbodyopen >}}{{< tropen >}}{{< tdopen >}}
Lecture 1 Part 1: Overview, Applications, and Motivation                
Lecture 1 Part 2: Derivatives as Linear Operators
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 2 Part 0: Examples of Linear and Nonlinear Transformations of ℝ² via Images   
Lecture 2 Part 1: Derivatives as Linear Operators (cont.)               
Lecture 2 Part 2: Two by Two Matrix Jacobians
{{< tdclose >}}{{< tdopen >}}
Problem Set 1 out
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 3 Part 1: Two by Two Matrix Jacobians  (cont.)            
Lecture 3 Part 2: Finite Difference
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 4 Part 1: Generalized Gradients and Inner Products             
Lecture 4 Part 2: Nonlinear Root-Finding, Optimization, and Adjoint-Method Differentiation
{{< tdclose >}}{{< tdopen >}}
Problem Set 1 due               
Problem Set 2 out
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 5 Part 0: Norms and Derivatives: Why a Norm of the Input and Output are Needed to Define a Derivative?  
Lecture 5 Part 1: Derivative of Matrix Determinant and Inverse  
Lecture 5 Part 2: Forward-Mode Automatic Differentiation via Dual Numbers  
Lecture 5 Part 3: Forward and Reverse-Mode Automatic Differentiation on Computational Graphs
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 6 Part 1: An Introduction to (Local) Sensitivity Analysis for (Ordinary) Differential Equations             
Lecture 6 Part 2: Calculus of Variations
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 7 Part 1: Derivatives of Random Functions              
Lecture 7 Part 2: Backpropagation through Back Substitution with a Backslash
{{< tdclose >}}{{< tdopen >}}
Problem Set 2 due
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Lecture 8 Part 1: Hessian Matrices (cont.)             
Lecture 8 Part 2: Differentiable Programming and Neural Differential Equations
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}