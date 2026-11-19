# Systems of Equations

## Exercise 1. Writing a Linear System in Matrix Form

## Question

Write the following system of linear equations in the matrix form $Ax = b$:

$$
\begin{cases}
2x_1 + 3x_2 = 7, \\
-x_1 + 4x_2 = -2.
\end{cases}
$$

State the coefficient matrix $A$, the variable vector $x$, and the right-hand side vector $b$, and explain how each row of the matrix multiplication represents one equation of the system.

## Solution

**Step 1: Identify the coefficient matrix $A$, variable vector $x$, and right-hand side vector $b$**

From the coefficients of $x_1$ and $x_2$ on the left-hand side of each equation, we form the $2 \times 2$ coefficient matrix $A$:

$$
A = \begin{pmatrix} 2 & 3 \\ -1 & 4 \end{pmatrix}.
$$

Collecting the unknowns into a column vector gives the variable vector $x$:

$$
x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}.
$$

Collecting the constants on the right-hand side of each equation gives the right-hand side vector $b$:

$$
b = \begin{pmatrix} 7 \\ -2 \end{pmatrix}.
$$

Thus, the linear system in matrix form is:

$$
\begin{pmatrix} 2 & 3 \\ -1 & 4 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} 7 \\ -2 \end{pmatrix}.
$$

**Step 2: Row-by-row explanation of the matrix equation**

In matrix-vector multiplication, each entry of the resulting product $Ax$ is the dot product of a row of $A$ with the column vector $x$:

- **First row:** Taking the first row $(2, 3)$ of $A$ and multiplying it by $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ gives $2x_1 + 3x_2$, which equals the first entry $7$ of $b$:

$$
2x_1 + 3x_2 = 7.
$$

- **Second row:** Taking the second row $(-1, 4)$ of $A$ and multiplying it by $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ gives $-x_1 + 4x_2$, which equals the second entry $-2$ of $b$:

$$
-x_1 + 4x_2 = -2.
$$

**Explanation:** Writing a linear system as $Ax = b$ organizes the coefficients into a single transformation acting on the unknown vector $x$, where each row of $A$ encodes the weights of the variables in one scalar equation matching the corresponding entry of $b$.
