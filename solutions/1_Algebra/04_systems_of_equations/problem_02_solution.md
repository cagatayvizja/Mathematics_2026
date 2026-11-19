# Systems of Linear Equations

## Exercise 1. From a System to a Matrix

## Question

Write the system

$$
\begin{cases}
2x - y + z = 4, \\
x + 3y - 2z = 1, \\
3x + y + z = 7.
\end{cases}
$$

in the matrix form $Ax = b$. Identify the coefficient matrix $A$, the variable vector $x$, and the right-hand side vector $b$, and explain how each row of the matrix equation corresponds to one equation of the system.

## Solution

**Step 1: Identify the coefficient matrix $A$, variable vector $x$, and right-hand side vector $b$**

Collecting the coefficients of the unknowns $x$, $y$, and $z$ from the left-hand side of each equation forms the $3 \times 3$ coefficient matrix $A$:

$$
A = \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}.
$$

Ordering the unknowns into a column vector gives the variable vector $x$:

$$
x = \begin{pmatrix} x \\ y \\ z \end{pmatrix}.
$$

Collecting the constants on the right-hand side of each equation gives the right-hand side vector $b$:

$$
b = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.
$$

Combining these components yields the matrix equation $Ax = b$:

$$
\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.
$$

**Step 2: Explain how each row represents one equation**

By the definition of matrix-vector multiplication, each entry of the product $Ax$ is the dot product of a row of $A$ with the column vector $x$, which is set equal to the corresponding entry of $b$:

- **First row:** Multiplying the first row $(2, -1, 1)$ by $x = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$ produces $2x - y + z$, matching the first entry $4$ of $b$:

$$
2x - y + z = 4.
$$

- **Second row:** Multiplying the second row $(1, 3, -2)$ by $x = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$ produces $x + 3y - 2z$, matching the second entry $1$ of $b$:

$$
x + 3y - 2z = 1.
$$

- **Third row:** Multiplying the third row $(3, 1, 1)$ by $x = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$ produces $3x + y + z$, matching the third entry $7$ of $b$:

$$
3x + y + z = 7.
$$

**Explanation:** Representing the system as $Ax = b$ separates the numerical structure of the equations (stored in $A$ and $b$) from the unknowns (stored in $x$), so each row of $A$ encodes the linear combination of variables for a single scalar equation.
