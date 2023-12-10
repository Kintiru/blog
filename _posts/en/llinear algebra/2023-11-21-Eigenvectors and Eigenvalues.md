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

## Definition
Eigenvector of a matrix is a nonzero vector after the transformation by a square matrix is scalar times of the original vector.

$$
\tag{1} A\vec x = \lambda \vec x
$$

Where $A$ is a square matrix in $\mathbb{R}^{n \times n}$ and $\lambda$ is a scalar.

There are exactly $n$ eigenvectors and associated eigenvalues in a $n$ by $n$ matrix, including duplicate values.

$A$, $\lambda$, and the eigenvector $\vec x$ can include complex numbers.

## Finding Eigenvectors and Eigenvalues

By rearranging the equation (1) above, we can get

$$
 A\vec x - \lambda \vec x = 0
$$

Using the identity matrix, we can rewrite the equation.

$$
 A\vec x - \lambda I \vec x = 0
$$

And finally, we can factor out $\vec x$.

$$
(A - \lambda I)\vec x = 0
$$

Since $\vec x$ should be nonzero, it means $(A - \lambda I)$ should be singular, and thus the determinant should be zero.

$$
\det(A-\lambda I) = 0
$$

By solving the determeinant, we get $n$ th degree polynomial, and this is why $n \times n$ matrix has exactly $n$ roots including multiplicity by the fundamental threorem of algebra.

<details>

<summary>Example of finding eigenvalues using determinant</summary>

Let $A$ be 2 by 2 matrix.

$$
A = \begin{bmatrix}1&2 \\ -1&4\end{bmatrix}
$$

Solving the determinant $\det(A - \lambda I) = 0$

$$
\begin{vmatrix}1-\lambda &2 \\ -1&4-\lambda \end{vmatrix} = 0
$$
$$
(1-\lambda )(4-\lambda ) + 2 = 0
$$

$$
\lambda^2 - 5\lambda + 6 = 0\\
$$

Finally, we can get two eigenvalues of

$$
\lambda = 2, \lambda = 3
$$

</details>

<details>

<summary>Example of finding associated eigenvalues</summary>

Using the example above with

$$
A = \begin{bmatrix}1&2 \\ -1&4\end{bmatrix}, \lambda_1 = 2, \lambda_2 = 3
$$

We can find associated eigenvectors with each $\lambda_1$ and $\lambda_2$ using Gauss Elimination with augemented matrix.

Starting with $\lambda_1$,

$$
(A - \lambda I)\vec x = \vec 0
$$

$$
\left(\begin{bmatrix}1&2 \\ -1&4\end{bmatrix} - 2\begin{bmatrix}1&0\\0&1\end{bmatrix}\right)\vec x  = \vec 0\\
\begin{bmatrix}1-2&2 \\ -1&4-2\end{bmatrix}\vec x = \vec 0
$$

Now we can make it augmented and apply Gauss Elimination

$$
\begin{bmatrix}-1&2&|&0\\-1&2&|&0\end{bmatrix} \to \begin{bmatrix}-1&2&|&0\\0&0&|&0\end{bmatrix}
$$

$$
-1x_1 +2x_2 = 0\\
x_1 = 2x_2
$$

Therefore, we can solve for $\vec x$

$$
\vec x = \begin{bmatrix}x_1\\x_2\end{bmatrix} = \begin{bmatrix}x_1\\x_1/2\end{bmatrix} = \begin{bmatrix}1\\1/2\end{bmatrix}x_1
$$

Therefore the eigenvector associated with $\lambda = 2$ is $\begin{bmatrix}1\\1/2\end{bmatrix}$

</details>

# Relation to Trace

trace is sum of diagonal entries of a matirix, and it is equal to the sum of eigenvalues of the matrix.

$$
\text{trace}(A) = \sum_{i=1}^n \lambda_i
$$

# Complex Eigenvectors/Eigenvalues

If a matrix is a real matrix, $A\in \mathbb{R}^{n\times n}$, then the complex conjugate of its eigenvectors and eigenvalues are also the eigenvector and eigenvalues of the matrix $A$.

Which implies that if there a matrix have odd number of eigenvalues, at least one of the eigenvalues and associated eigenvector is real.

## Having only complex numbers in eigenvalues/eigenvectors

If a matrix has only complex eigenvectors and eigenvaues, it means any real vectors will be rotated by the matrix.

# Eigenvalues of bipartite graph

Eigenvalues of bipartite graph are plus minus pairs.

It means the sum of eigenvalues are zero, thus trace of matrix is zero.