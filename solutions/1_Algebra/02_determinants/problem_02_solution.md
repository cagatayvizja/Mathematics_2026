# Determinants

## Goal of the Set

After completing this set, the student should be able to compute determinants of small matrices, understand their connection with invertibility, know how row operations affect the determinant, and recognize situations in which the determinant gives quick information about a matrix or a system of equations.

---

## Basic Exercises

### Exercise 1. Determinant of a 2×2 Matrix

## Question

Compute

$$\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}, \qquad \det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}.$$

Which matrix is invertible? Justify your answer.

## Solution

**Step 1: Compute the determinant of the first matrix**

For a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is given by $ad - bc$:

$$\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix} = (3)(4) - (-2)(5) = 12 - (-10) = 22$$

**Step 2: Compute the determinant of the second matrix**

$$\det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix} = (1)(14) - (7)(2) = 14 - 14 = 0$$

**Step 3: Determine invertibility**

- The first matrix ($\det = 22 \neq 0$) **is invertible** because its determinant is non-zero.
- The second matrix ($\det = 0$) **is not invertible** (it is singular) because its determinant is zero.

**Explanation:** A square matrix is invertible if and only if its determinant is non-zero. Geometrically, a zero determinant in a $2 \times 2$ matrix indicates that the columns are linearly dependent and collapse the 2D area to zero.

---

### Exercise 2. Determinant of a 3×3 Matrix

## Question

For

$$A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## Solution

**Step 1: Compute $\det A$ using Sarrus' rule**

Append the first two columns to the right of the matrix:

$$\begin{vmatrix} 1 & 2 & -1 & 1 & 2 \\ 0 & 3 & 4 & 0 & 3 \\ 2 & 1 & 5 & 2 & 1 \end{vmatrix}$$

Sum the products of the downward diagonals and subtract the products of the upward diagonals:

- Downward products: $(1)(3)(5) + (2)(4)(2) + (-1)(0)(1) = 15 + 16 + 0 = 31$
- Upward products: $(2)(3)(-1) + (1)(4)(1) + (5)(0)(2) = -6 + 4 + 0 = -2$

$$\det A = 31 - (-2) = 33$$

**Step 2: Verification check**

We can verify by computing the determinant via cofactor expansion along the first column (which has a zero, making it efficient):

$$\det A = 1 \cdot \begin{vmatrix} 3 & 4 \\ 1 & 5 \end{vmatrix} - 0 \cdot \begin{vmatrix} 2 & -1 \\ 1 & 5 \end{vmatrix} + 2 \cdot \begin{vmatrix} 2 & -1 \\ 3 & 4 \end{vmatrix}$$

$$\det A = 1 \cdot (15 - 4) - 0 + 2 \cdot (8 - (-3)) = 11 + 2(11) = 11 + 22 = 33$$

**Explanation:** Sarrus' rule provides a rapid computational shortcut for $3 \times 3$ matrices by repeating columns, while cofactor expansion provides an alternative method to verify consistency across different calculation paths.

---

### Exercise 3. Swapping Two Rows

## Question

For

$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$. First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

## Solution

**Step 1: Compute $\det A$**

Using cofactor expansion along the first row:

$$\det A = 1 \cdot \begin{vmatrix} 3 & 1 \\ 1 & 1 \end{vmatrix} - 2 \cdot \begin{vmatrix} 0 & 1 \\ 2 & 1 \end{vmatrix} + 0 \cdot \begin{vmatrix} 0 & 3 \\ 2 & 1 \end{vmatrix}$$

$$\det A = 1(3 - 1) - 2(0 - 2) + 0 = 1(2) - 2(-2) = 2 + 4 = 6$$

**Step 2: Predict $\det B$**

Matrix $B$ is formed by swapping $R_1$ and $R_2$ of $A$. A fundamental property of determinants states that swapping any two rows multiplies the determinant by $-1$. Therefore, we predict:

$$\det B = -\det A = -6$$

**Step 3: Verify by direct computation of $\det B$**

$$B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}$$

Expanding along the first row:

$$\det B = 0 \cdot \begin{vmatrix} 2 & 0 \\ 1 & 1 \end{vmatrix} - 3 \cdot \begin{vmatrix} 1 & 0 \\ 2 & 1 \end{vmatrix} + 1 \cdot \begin{vmatrix} 1 & 2 \\ 2 & 1 \end{vmatrix}$$

$$\det B = 0 - 3(1 - 0) + 1(1 - 4) = -3 + (-3) = -6$$

**Explanation:** Swapping two rows of a matrix reverses the orientation of the underlying geometric transformation, which flips the sign of the determinant.

---

### Exercise 4. Triangular Matrix

## Question

Without expanding the determinant, compute

$$\det \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}.$$

State the rule for an arbitrary triangular matrix and explain it using this example.

## Solution

**Step 1: Compute the determinant**

Since the matrix is upper triangular (all entries below the main diagonal are zero), the determinant is simply the product of the entries along its main diagonal:

$$\det = (2)(-3)(7) = -42$$

**Rule for Triangular Matrices:** The determinant of any triangular matrix (upper or lower) is equal to the product of its diagonal entries.

**Explanation:** In cofactor expansion along the first column of an upper triangular matrix, the only non-zero term is the top-left entry multiplied by the determinant of the remaining upper-triangular submatrix. Iterating this process leaves only the product of the diagonal elements.

---

### Exercise 5. Row Operations

## Question

For

$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Solution

**Step 1: Apply row operations to reach row echelon form**

Initial matrix:
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}$$

Operation 1: $R_2 \leftarrow R_2 - 2R_1$
$$\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{pmatrix}$$
*(Note: Replacement operations do not change the value of the determinant).*

Operation 2: $R_3 \leftarrow R_3 + R_1$
$$\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}$$
*(Note: Replacement operations preserve the determinant).*

Operation 3: $R_3 \leftarrow R_3 + 2R_2$
$$\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}$$
*(Note: Replacement operation; determinant remains unchanged).*

**Step 2: Calculate the final triangular determinant**

The resulting matrix is upper triangular, so its determinant is the product of its diagonal entries:

$$\det A = (1)(-3)(-7) = 21$$

**Explanation:** Row replacement operations add a multiple of one row to another, which leaves the determinant completely unchanged, allowing us to reduce the matrix to triangular form safely.

---

### Exercise 6. Parameter and Invertibility

## Question

For

$$A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## Solution

**Step 1: Compute the determinant in terms of $t$**

$$\det A(t) = (t)(t) - (1)(2) = t^2 - 2$$

**Step 2: Find values where the matrix is not invertible**

A matrix is not invertible when its determinant equals zero:
$$t^2 - 2 = 0 \implies t^2 = 2 \implies t = \pm\sqrt{2}$$

**Explanation:** The matrix fails to be invertible at $t = \sqrt{2}$ and $t = -\sqrt{2}$ because the determinant vanishes at these points, meaning the columns become linearly dependent and the matrix maps 2D space onto a line or point.

---

### Exercise 7. Using Properties Instead of Recomputing

## Question

Suppose that for a $3 \times 3$ matrix, $\det A = -4$. Compute

$$\det(2A), \qquad \det(A^T), \qquad \det(A^2), \qquad \det(-A).$$

Justify each answer using the appropriate property.

## Solution

**Step 1: Compute $\det(2A)$**

For an $n \times n$ matrix, scaling the entire matrix by a scalar $c$ multiplies the determinant by $c^n$. Here $n = 3$ and $c = 2$:
$$\det(2A) = 2^3 \det(A) = 8 \cdot (-4) = -32$$

**Step 2: Compute $\det(A^T)$**

The determinant of a transpose is equal to the determinant of the original matrix:
$$\det(A^T) = \det(A) = -4$$

**Step 3: Compute $\det(A^2)$**

The determinant of a product is the product of the determinants ($\det(A^2) = \det(A \cdot A) = \det(A)\det(A)$):
$$\det(A^2) = (-4)^2 = 16$$

**Step 4: Compute $\det(-A)$**

Multiplying by $-1$ is equivalent to scalar multiplication by $-1$ for a $3 \times 3$ matrix:
$$\det(-A) = (-1)^3 \det(A) = -1 \cdot (-4) = 4$$

**Explanation:** Matrix properties allow us to evaluate scalar multiples, powers, and transposes algebraically without knowing the individual entry values of $A$.

---

### Exercise 8. Determinant of a Product

## Question

Let $A, B$ be square matrices such that $\det A = 3$ and $\det B = -5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB \neq B A$.

## Solution

**Step 1: Compute $\det(AB)$**

Using the multiplicative property $\det(AB) = \det(A)\det(B)$:
$$\det(AB) = (3)(-5) = -15$$

**Step 2: Compute $\det(BA)$**

Similarly, $\det(BA) = \det(B)\det(A) = (-5)(3) = -15$:
$$\det(BA) = -15$$

**Step 3: Compute $\det(A^{-1}B)$**

Using $\det(A^{-1}) = \frac{1}{\det(A)}$:
$$\det(A^{-1}B) = \det(A^{-1})\det(B) = \frac{1}{3} \cdot (-5) = -\frac{5}{3}$$

**Explanation:** $\det(AB) = \det(BA)$ because scalar multiplication of real numbers is commutative, even though matrix multiplication itself is non-commutative.

---

### Exercise 9. Area and the Determinant

## Question

The vectors

$$u = \begin{pmatrix} 3 \\ 1 \end{pmatrix}, \qquad v = \begin{pmatrix} 1 \\ 4 \end{pmatrix}$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does
