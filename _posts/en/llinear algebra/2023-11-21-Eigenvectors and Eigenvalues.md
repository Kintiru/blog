---
title: 'Eigenvectors and Eigenvalues'
date: 2023-11-21 16:00:00 +0900
author: kintiru
categories: [English, Linear Algebra]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English, Linear Algebra, Math]     # TAG names should always be lowercase
math: true
mermaid: true
#img_path: 
#image: #preview image
    #path:
    #alt:
    #lqpq:
#pin: true
---

# Eigenvector
Eigenvector of a matrix means the vector after the transformation by matrix is scalar times of the original vector.

$$
A\vec x = \lambda x
$$

Where A is an arbitrary matrix and 

# Complex Eigenvectors/Eigenvalues

If a matrix is a real matrix, $A\in \mathbb{R}^{m\times n}$, then the complex conjugate of its eigenvectors and eigenvalues are also the eigenvector and eigenvalues of the matrix $A$.

This implies that if there a matrix have odd number of eigenvalues, at least one of the eigenvalues and associated eigenvector is real.

## Having only complex numbers in eigenvalues/eigenvectors

If a matrix has only complex eigenvectors and eigenvaues, it means any real vectors will be rotated by the matrix.

## Eigenvalues of bipartite graph

Eigenvalues of bipartite graph are plus minus pairs.

It means the sum of eigenvalues are zero, thus trace of matrix is zero.