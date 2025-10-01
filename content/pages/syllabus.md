---
content_type: page
description: This page includes course meeting times, prerequisites, course description,
  and topics.
draft: false
title: Syllabus
uid: c649638c-8d02-4221-ba19-ebc202192803
---
## Course Meeting Times

Lectures: 3 sessions / week, 2 hours / session

## Prerequisites

Courses in linear algebra (such as {{% resource_link "d628efb8-bcba-4219-b28b-466d5e34b4cc" "*18.06 Linear Algebra*" %}}) and multivariate calculus (such as {{% resource_link "03cb8060-ce30-41b4-a501-1d8957951bc5" "*18.02 Multivariable Calculus*" %}})

## Course Description

We all know that calculus courses such as {{% resource_link "ccb954a1-d1b5-4cdd-9161-759872047def" "*18.01 Single Variable Calculus*" %}} and {{% resource_link "03cb8060-ce30-41b4-a501-1d8957951bc5" "*18.02 Multivariable Calculus*" %}} cover univariate and vector calculus, respectively. Modern applications such as machine learning and large-scale optimization require the next big step, "matrix calculus" and calculus on arbitrary vector spaces.

This class covers a coherent approach to matrix calculus showing techniques that allow you to think of a matrix holistically (not just as an array of scalars), generalize and compute derivatives of important matrix factorizations and many other complicated-looking operations, and understand how differentiation formulas must be reimagined in large-scale computing. We will discuss reverse/adjoint/backpropagation differentiation, custom vector-Jacobian products, and how modern automatic differentiation is more computer science than calculus (it is neither symbolic formulas nor finite differences).

## Lecture Notes

There is no required textbook for this course, but a {{% resource_link "b67b8d11-1918-467a-bb76-1cfdb8289174" "complete set of lecture notes" %}} is provided. The lecture notes were prepared by Paige Bright under the guidance of Professors Edelman and Johnson. The notes are also available on {{% resource_link "d1dad955-1ef3-4cd9-92e5-043bb9d7d234" "arXiv.org" %}}, along with any updates and citing information.

## Topics

Here are some of the topics covered:

- Derivatives as linear operators and linear approximation on arbitrary vector spaces: beyond gradients and Jacobians.
- Derivatives of functions with matrix inputs and/or outputs (e.g. matrix inverses and determinants). Kronecker products and matrix "vectorization."
- Derivatives of matrix factorizations (e.g. eigenvalues/SVD) and derivatives with constraints (e.g. orthogonal matrices).
- Multidimensional chain rules, and the significance of right-to-left ("forward") vs. left-to-right ("reverse") composition. Chain rules on computational graphs (e.g. neural networks).
- Forward- and reverse-mode manual and automatic multivariate differentiation.
- Adjoint methods (vJp/pullback rules) for derivatives of solutions of linear, nonlinear, and differential equations.
- Application to nonlinear root-finding and optimization. Multidimensional Newton and steepest–descent methods.
- Applications in engineering/scientific optimization and machine learning.
- Second derivatives, Hessian matrices, quadratic approximations, and quasi-Newton methods.

## Grading

The course grade is based on performance on the two homework assignments.