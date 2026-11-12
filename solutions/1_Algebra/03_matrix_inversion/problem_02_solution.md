# Inverse Matrix

## Goal of the Set

After completing this set, the student should understand what an inverse matrix is, when it exists, be able to find it using basic methods, check the result, and use the inverse to solve simple problems.

---

## Basic Exercises

### Exercise 1. Definition of the Inverse

## Question

For

$$A = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}$$

check, without using a formula, whether $B = A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## Solution

**Step 1: Compute the product $AB$**

$$AB = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix} = \begin{pmatrix} (2)(1) + (1)(-1) & (2)(-1) + (1)(2) \\ (1)(1) + (1)(-1) & (1)(-1) + (1)(2) \end{pmatrix} = \begin{pmatrix} 2 - 1 & -2 + 2 \\ 1 - 1 & -1 + 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

**Step 2: Compute the product $BA$**

$$BA = \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} (1)(2) + (-1)(1) & (1)(1) + (-1)(1) \\ (-1)(2) + (2)(1) & (-1)(1) + (2)(1) \end{pmatrix} = \begin{pmatrix} 2 - 1 & 1 - 1 \\ -2 + 2 & -1 + 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

**Step 3: Conclusion**

Since $AB = I$ and $BA = I$, matrix $B$ is indeed the inverse of $A$ ($B = A^{-1}$).

**Explanation:** By definition, a matrix $B$ is the inverse of $A$ if multiplying them in either order yields the identity matrix $I$.

---

### Exercise 2. Formula for a 2×2 Matrix

## Question

Find the inverse of

$$A = \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix}$$

using the formula for a $2 \times 2$ matrix. At the end, check the result by computing one product with $A$.

## Solution

**Step 1: Compute the determinant of $A$**

$$\det(A) = (3)(4) - (2)(5) = 12 - 10 = 2$$

**Step 2: Apply the $2 \times 2$ inverse formula**

For $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the inverse is $A^{-1} = \frac{1}{ad-bc} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$:

$$A^{-1} = \frac{1}{2} \begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix} = \begin{pmatrix} 2 & -1 \\ -5/2 & 3/2 \end{pmatrix}$$

**Step 3: Verify the result by multiplication**

$$A A^{-1} = \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ -5/2 & 3/2 \end{pmatrix} = \begin{pmatrix} 3(2) + 2(-5/2) & 3(-1) + 2(3/2) \\ 5(2) + 4(-5/2) & 5(-1) + 4(3/2) \end{pmatrix} = \begin{pmatrix} 6 - 5 & -3 + 3 \\ 10 - 10 & -5 + 6 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

**Explanation:** The explicit formula for $2 \times 2$ matrices swaps the main diagonal elements, negates the off-diagonal elements, and scales by the reciprocal of the determinant.

---

### Exercise 3. When Does the Inverse Not Exist?

## Question

For

$$A = \begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix}$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## Solution

**Way 1: Using the Determinant**

$$\det(A) = (2)(2) - (4)(1) = 4 - 4 = 0$$

Since the determinant is zero, the inverse formula $\frac{1}{\det(A)}\text{adj}(A)$ involves division by zero, meaning $A^{-1}$ does not exist.

**Way 2: Using Row Dependence**

Notice that the second row is half of the first row ($R_2 = \frac{1}{2}R_1$). Because the rows are linearly dependent, the matrix cannot span full 2D space, making it singular (non-invertible).

**Explanation:** Non-invertibility is characterized simultaneously by a zero determinant and linearly dependent rows or columns.

---

### Exercise 4. Gauss–Jordan

## Question

Find $A^{-1}$ using the Gauss–Jordan method for

$$A = \begin{pmatrix} 1 & 2 \\ 3 & 5 \end{pmatrix}.$$

Show the augmented matrix $[A \mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## Solution

**Step 1: Set up the augmented matrix $[A \mid I]$**

$$\left(\begin{array}{cc\|cc} 1 & 2 & 1 & 0 \\ 3 & 5 & 0 & 1 \end{array}\right)$$

**Step 2: Perform row operations**

Operation $R_2 \leftarrow R_2 - 3R_1$:
$$\left(\begin{array}{cc\|cc} 1 & 2 & 1 & 0 \\ 0 & -1 & -3 & 1 \end{array}\right)$$

Operation $R_2 \leftarrow -R_2$:
$$\left(\begin{array}{cc\|cc} 1 & 2 & 1 & 0 \\ 0 & 1 & 3 & -1 \end{array}\right)$$

Operation $R_1 \leftarrow R_1 - 2R_2$:
$$\left(\begin{array}{cc\|cc} 1 & 0 & -5 & 2 \\ 0 & 1 & 3 & -1 \end{array}\right)$$

**Step 3: Extract the inverse**

$$A^{-1} = \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}$$

**Explanation:** Gauss–Jordan elimination applies a sequence of elementary row operations equivalent to multiplying $A$ by elementary matrices until the left side becomes $I$. Since these operations transform $A$ into $I$, they simultaneously transform $I$ into $A^{-1}$ (because $A^{-1}A = I$).

---

### Exercise 5. A 3×3 Matrix

## Question

Use Gauss–Jordan elimination to find the inverse of

$$A = \begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \end{pmatrix}.$$

Check the result by multiplication.

## Solution

**Step 1: Set up the augmented matrix**

$$\left(\begin{array}{ccc\|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 1 & 0 & 1 & 0 & 0 & 1 \end{array}\right)$$

**Step 2: Row operations**

Operation $R_3 \leftarrow R_3 - R_1$:
$$\left(\begin{array}{ccc\|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & -1 & 1 & -1 & 0 & 1 \end{array}\right)$$

Operation $R_3 \leftarrow R_3 + R_2$:
$$\left(\begin{array}{ccc\|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 2 & -1 & 1 & 1 \end{array}\right)$$

Operation $R_3 \leftarrow \frac{1}{2}R_3$:
$$\left(\begin{array}{ccc\|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right)$$

Operation $R_2 \leftarrow R_2 - R_3$:
$$\left(\begin{array}{ccc\|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & 1/2 & 1/2 & -1/2 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right)$$

Operation $R_1 \leftarrow R_1 - R_2$:
$$\left(\begin{array}{ccc\|ccc} 1 & 0 & 0 & 1/2 & -1/2 & 1/2 \\ 0 & 1 & 0 & 1/2 & 1/2 & -1/2 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right)$$

**Step 3: Resulting Inverse**

$$A^{-1} = \begin{pmatrix} 1/2 & -1/2 & 1/2 \\ 1/2 & 1/2 & -1/2 \\ -1/2 & 1/2 & 1/2 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix}$$

**Step 4: Verification**

$$A A^{-1} = \begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \end{pmatrix} \cdot \frac{1}{2}\begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}$$

**Explanation:** Gauss–Jordan elimination systematically clears out lower and upper triangular components until the identity matrix is isolated on the left.

---

### Exercise 6. Solving a System Using the Inverse

## Question

Solve $Ax = b$, where

$$A = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix}, \qquad b = \begin{pmatrix} 5 \\ 7 \end{pmatrix},$$

using $x = A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

## Solution

**Step 1: Find $A^{-1}$**

Using the $2 \times 2$ formula ($\det(A) = (2)(3) - (1)(1) = 5$):
$$A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}$$

**Step 2: Compute $x = A^{-1}b$**

$$x = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 5 \\ 7 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 3(5) + (-1)(7) \\ -1(5) + 2(7) \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 15 - 7 \\ -5 + 14 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 8 \\ 9 \end{pmatrix} = \begin{pmatrix} 8/5 \\ 9/5 \end{pmatrix}$$

**Step 3: Check by substitution into $Ax$**

$$A x = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} 8/5 \\ 9/5 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 2(8) + 1(9) \\ 1(8) + 3(9) \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 16 + 9 \\ 8 + 27 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 25 \\ 35 \end{pmatrix} = \begin{pmatrix} 5 \\ 7 \end{pmatrix} = b$$

**Explanation:** Multiplying both sides of $Ax = b$ by $A^{-1}$ isolates $x$ directly as $x = A^{-1}b$.

---

### Exercise 7. Inverse of a Product

## Question

For

$$A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix}$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

## Solution

**Step 1
