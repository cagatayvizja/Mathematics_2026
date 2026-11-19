# Determinants

## Exercise 1. Computing Determinants and Checking Invertibility

## Question

Consider the two $2 \times 2$ matrices

$$
A = \begin{pmatrix} 3 & 2 \\ 1 & 4 \end{pmatrix} \quad \text{and} \quad B = \begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix}.
$$

Calculate the determinant of each matrix and explain which matrix is invertible.

## Solution

**Step 1: Calculate the determinant of matrix $A$**

For a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is given by the product of the main diagonal minus the product of the off-diagonal, $\det = ad - bc$. Applying this rule to $A$:

$$
\det(A) = (3)(4) - (2)(1) = 12 - 2 = 10.
$$

**Step 2: Calculate the determinant of matrix $B$**

Applying the same $2 \times 2$ determinant formula to matrix $B$:

$$
\det(B) = (2)(2) - (4)(1) = 4 - 4 = 0.
$$

**Step 3: Determine invertibility**

A square matrix is invertible (nonsingular) if and only if its determinant is nonzero:

$$
\det(A) = 10 \neq 0 \implies A \text{ is invertible}, \qquad \det(B) = 0 \implies B \text{ is not invertible (singular)}.
$$

**Explanation:** Because $\det(A) = 10 \neq 0$, the rows and columns of $A$ are linearly independent and the associated linear transformation is reversible. In contrast, the second row of $B$ is half of its first row, causing $\det(B) = 0$ and collapsing the area scale factor to zero so no inverse matrix $B^{-1}$ exists.
