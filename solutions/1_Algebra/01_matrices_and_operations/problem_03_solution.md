# Matrices and Operations

## Exercise 1. Matrix Dimensions, Entries, Rows, and Columns

## Question

Consider the matrices

$$
A = \begin{pmatrix} 2 & -1 & 4 \\ 0 & 3 & 5 \end{pmatrix} \quad \text{and} \quad B = \begin{pmatrix} 1 & 2 \\ -3 & 0 \\ 4 & 6 \end{pmatrix}.
$$

State the sizes (dimensions) of both matrices, identify four specific entries (one from each row/column position), and extract a row vector and a column vector.

## Solution

**Step 1: Determine the sizes of both matrices**

A matrix with $m$ rows and $n$ columns has size $m \times n$. Counting rows and columns directly gives:

$$
\text{size}(A) = 2 \times 3, \qquad \text{size}(B) = 3 \times 2.
$$

Matrix $A$ has $2$ horizontal rows and $3$ vertical columns, whereas matrix $B$ has $3$ horizontal rows and $2$ vertical columns.

**Step 2: Identify four entries**

Using standard row-column indexing $a_{ij}$ (row $i$, column $j$) and $b_{ij}$ (row $i$, column $j$), we locate four entries across the two matrices:

$$
a_{11} = 2, \qquad a_{13} = 4, \qquad b_{21} = -3, \qquad b_{32} = 6.
$$

Each entry is read by moving down to row $i$ and across to column $j$ in the corresponding matrix.

**Step 3: Extract a row vector and a column vector**

Taking the second row of $A$ gives the horizontal row vector:

$$
r_2 = \begin{pmatrix} 0 & 3 & 5 \end{pmatrix}.
$$

Taking the first column of $B$ gives the vertical column vector:

$$
c_1 = \begin{pmatrix} 1 \\ -3 \\ 4 \end{pmatrix}.
$$

**Explanation:** Matrix dimensions specify the domain and codomain shapes of linear transformations, individual entries isolate local coefficients by row-column coordinates, and row or column vectors extract one-dimensional slices along a single index direction.
