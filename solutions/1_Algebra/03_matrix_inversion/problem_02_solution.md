# Matrix Inversion

## Exercise 1. Verifying an Inverse Matrix

## Question

Given the matrices

$$
A = \begin{pmatrix} 2 & 1 \\ 5 & 3 \end{pmatrix} \quad \text{and} \quad B = \begin{pmatrix} 3 & -1 \\ -5 & 2 \end{pmatrix},
$$

determine whether $B$ is the inverse of $A$ by computing both products $AB$ and $BA$ and comparing each result with the $2 \times 2$ identity matrix $I$.

## Solution

**Step 1: Compute the product $AB$**

Using standard row-by-column matrix multiplication, we multiply each row of $A$ by each column of $B$:

$$
AB = \begin{pmatrix} 2 & 1 \\ 5 & 3 \end{pmatrix} \begin{pmatrix} 3 & -1 \\ -5 & 2 \end{pmatrix} = \begin{pmatrix} 2(3) + 1(-5) & 2(-1) + 1(2) \\ 5(3) + 3(-5) & 5(-1) + 3(2) \end{pmatrix}.
$$

Simplifying each entry gives:

$$
AB = \begin{pmatrix} 6 - 5 & -2 + 2 \\ 15 - 15 & -5 + 6 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.
$$

**Step 2: Compute the product $BA$**

Now we reverse the multiplication order and multiply each row of $B$ by each column of $A$:

$$
BA = \begin{pmatrix} 3 & -1 \\ -5 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 5 & 3 \end{pmatrix} = \begin{pmatrix} 3(2) + (-1)(5) & 3(1) + (-1)(3) \\ (-5)(2) + 2(5) & (-5)(1) + 2(3) \end{pmatrix}.
$$

Simplifying each entry gives:

$$
BA = \begin{pmatrix} 6 - 5 & 3 - 3 \\ -10 + 10 & -5 + 6 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.
$$

**Step 3: Compare with the identity matrix**

Since both $AB = I$ and $BA = I$, where

$$
I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix},
$$

matrix $B$ is indeed the inverse of $A$ (that is, $B = A^{-1}$).

**Explanation:** Matrix multiplication is not commutative in general, so verifying that a candidate matrix is the two-sided inverse of an invertible square matrix requires checking both $AB = I$ and $BA = I$; obtaining the identity matrix in both orders confirms that applying $A$ and $B$ in either sequence leaves vectors unchanged.
