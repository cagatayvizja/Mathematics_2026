# Matrices and Basic Operations

## Goal of the Set

After completing this set, the student should understand what a matrix is, when basic operations can be performed, how matrix multiplication and matrix-vector multiplication work, and how matrices describe simple linear transformations.

The goal is not to perform many similar calculations. Each exercise presents a different aspect of working with matrices.

## How to Work Through the Exercises

For each exercise, prepare a solution containing at least:

- the result,
- the main steps,
- a brief explanation of the property or method used,
- a mathematical verification of the result, when possible.

---

## Basic Exercises

### Exercise 1. Matrix Size and Entries

## Question

Given

$$A = \begin{pmatrix} 2 & -1 & 3 \\ 0 & 4 & 5 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\ -2 & 3 \\ 4 & 1 \end{pmatrix}.$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## Solution

**Step 1: Determine the matrix sizes**

Matrix size is given by $(\text{number of rows}) \times (\text{number of columns})$.
- Matrix $A$ has $2$ rows and $3$ columns, so its size is $2 \times 3$.
- Matrix $B$ has $3$ rows and $2$ columns, so its size is $3 \times 2$.

**Step 2: Identify the specific entries**

Using the index notation $m_{ij}$ (row $i$, column $j$):
- $a_{12} = -1$ (row 1, column 2 of $A$)
- $a_{23} = 5$ (row 2, column 3 of $A$)
- $b_{21} = -2$ (row 2, column 1 of $B$)
- $b_{32} = 1$ (row 3, column 2 of $B$)

**Step 3: Write the specified row and column as vectors**

Second row of $A$:

$$r_2 = \begin{pmatrix} 0 & 4 & 5 \end{pmatrix}$$

First column of $B$:

$$c_1 = \begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$$

**Explanation & Verification:** The first subscript always denotes the vertical row position from top to bottom, and the second denotes the horizontal column position from left to right.

---

### Exercise 2. Addition and Scalar Multiplication

## Question

For

$$A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}$$

compute

$$A+B, \qquad A-B, \qquad 3A-2B.$$

Explain why matrix addition is possible only for matrices of the same size.

## Solution

**Step 1: Compute $A + B$**

Add corresponding entries:

$$A + B = \begin{pmatrix} 1 + 4 & 2 + (-2) \\ -1 + 0 & 3 + 5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$$

**Step 2: Compute $A - B$**

Subtract corresponding entries:

$$A - B = \begin{pmatrix} 1 - 4 & 2 - (-2) \\ -1 - 0 & 3 - 5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$$

**Step 3: Compute $3A - 2B$**

First, multiply each matrix by its respective scalar:

$$3A = \begin{pmatrix} 3(1) & 3(2) \\ 3(-1) & 3(3) \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}$$

$$2B = \begin{pmatrix} 2(4) & 2(-2) \\ 2(0) & 2(5) \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}$$

Now subtract $2B$ from $3A$:

$$3A - 2B = \begin{pmatrix} 3 - 8 & 6 - (-4) \\ -3 - 0 & 9 - 10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$$

**Explanation & Verification:** Matrix addition is defined entry-by-entry ($c_{ij} = a_{ij} + b_{ij}$). If two matrices have different dimensions, there is no one-to-one correspondence between their entries, making the sum undefined. Verification: $(A + B) - B = \begin{pmatrix} 5-4 & 0-(-2) \\ -1-0 & 8-5 \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = A$.

---

### Exercise 3. When Can Matrices Be Multiplied?

## Question

The matrix sizes are

$$A_{2\times3}, \qquad B_{3\times4}, \qquad C_{4\times2}, \qquad D_{2\times2}.$$

For the products

$$AB, \ BA, \ BC, \ CB, \ AC, \ CA, \ AD, \ DA$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Solution

**Step 1: State the dimension compatibility rule**

A product $P_{m \times n} Q_{r \times p}$ is defined if and only if $n = r$. When defined, the resulting matrix has size $m \times p$.

**Step 2: Evaluate each product**

1. **$AB$ ($2\times3$ and $3\times4$):** Defined, because inner dimensions match ($3 = 3$). Size: $2 \times 4$.
2. **$BA$ ($3\times4$ and $2\times3$):** Undefined, because inner dimensions differ ($4 \neq 2$).
3. **$BC$ ($3\times4$ and $4\times2$):** Defined, because inner dimensions match ($4 = 4$). Size: $3 \times 2$.
4. **$CB$ ($4\times2$ and $3\times4$):** Undefined, because inner dimensions differ ($2 \neq 3$).
5. **$AC$ ($2\times3$ and $4\times2$):** Undefined, because inner dimensions differ ($3 \neq 4$).
6. **$CA$ ($4\times2$ and $2\times3$):** Defined, because inner dimensions match ($2 = 2$). Size: $4 \times 3$.
7. **$AD$ ($2\times3$ and $2\times2$):** Undefined, because inner dimensions differ ($3 \neq 2$).
8. **$DA$ ($2\times2$ and $2\times3$):** Defined, because inner dimensions match ($2 = 2$). Size: $2 \times 3$.

**Explanation:** Each entry in a matrix product is the dot product of a row from the first matrix and a column from the second. For this dot product to exist, the number of elements in a row of the first matrix (its columns) must equal the number of elements in a column of the second matrix (its rows).

---

### Exercise 4. Matrix Multiplication and Noncommutativity

## Question

For

$$A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Solution

**Step 1: Compute $AB$**

$$AB = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix} = \begin{pmatrix} (1)(2) + (2)(3) & (1)(0) + (2)(1) \\ (0)(2) + (1)(3) & (0)(0) + (1)(1) \end{pmatrix} = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}$$

**Step 2: Compute $BA$**

$$BA = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (2)(1) + (0)(0) & (2)(2) + (0)(1) \\ (3)(1) + (1)(0) & (3)(2) + (1)(1) \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$$

**Step 3: Compare $AB$ and $BA$**

$$AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \neq \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix} = BA$$

**Explanation:** No, $AB \neq BA$. Noncommutativity means that changing the order of factors in matrix multiplication generally yields a different result, because the rows of the left matrix interact with the columns of the right matrix asymmetrically.

---

### Exercise 5. Matrix Times Vector

## Question

Let

$$A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \qquad x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}.$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## Solution

**Step 1: Compute $Ax$ via row-by-column multiplication**

$$
Ax = \begin
