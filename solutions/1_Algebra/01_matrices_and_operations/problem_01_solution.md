# Matrices and Operations

## Exercise 1. Matrix Dimensions, Entries, Rows, and Columns

## Question

Consider the two matrices

$$
A = \begin{pmatrix} 2 & -1 & 4 \\ 0 & 5 & -3 \end{pmatrix} \quad \text{and} \quad B = \begin{pmatrix} 1 & 3 \\ -2 & 4 \\ 6 & 0 \end{pmatrix}.
$$

Determine the size (dimensions) of each matrix, find the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$, and write out the second row of $A$ and the second column of $B$.

## Solution

**Step 1: Determine the size of each matrix**

The size of a matrix is written as $m \times n$, where $m$ is the number of rows and $n$ is the number of columns:

- Matrix $A$ has $2$ horizontal rows and $3$ vertical columns, so its size is

$$
\text{size}(A) = 2 \times 3.
$$

- Matrix $B$ has $3$ horizontal rows and $2$ vertical columns, so its size is

$$
\text{size}(B) = 3 \times 2.
$$

**Step 2: Identify the four requested entries**

Using the standard index notation $m_{ij}$, where $i$ denotes the row index and $j$ denotes the column index:

- The entry $a_{12}$ lies in row $1$, column $2$ of $A$:

$$
a_{12} = -1.
$$

- The entry $a_{23}$ lies in row $2$, column $3$ of $A$:

$$
a_{23} = -3.
$$

- The entry $b_{21}$ lies in row $2$, column $1$ of $B$:

$$
b_{21} = -2.
$$

- The entry $b_{32}$ lies in row $3$, column $2$ of $B$:

$$
b_{32} = 0.
$$

**Step 3: Extract the requested row and column vectors**

Reading across the second horizontal row of $A$ produces the $1 \times 3$ row vector:

$$
\mathbf{r}_2(A) = \begin{pmatrix} 0 & 5 & -3 \end{pmatrix}.
$$

Reading down the second vertical column of $B$ produces the $3 \times 1$ column vector:

$$
\mathbf{c}_2(B) = \begin{pmatrix} 3 \\ 4 \\ 0 \end{pmatrix}.
$$

**Explanation:** Matrix dimensions specify the grid layout ($m \times n$), while double-subscript indexing $m_{ij}$ uniquely locates each entry by intersecting its horizontal row $i$ with its vertical column $j$.
