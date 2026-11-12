# Systems of Linear Equations

## Goal of the Set

After completing this set, the student should be able to write a system in the form $Ax=b$, solve it using Gaussian elimination, and recognize the three basic cases: exactly one solution, infinitely many solutions, and no solution.

---

## Basic Exercises

### Exercise 1. From a System to a Matrix

## Question

Write the system

$$\begin{cases} 2x - y + z = 4, \\ x + 3y - 2z = 1, \\ 3x + y + z = 7. \end{cases}$$

in the form $Ax = b$. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Solution

**Step 1: Write in matrix form $Ax = b$**

$$\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}$$

**Step 2: Identify components**

- **Coefficient matrix ($A$):** $\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}$
- **Vector of unknowns ($x$):** $\begin{pmatrix} x \\ y \\ z \end{pmatrix}$
- **Right-hand side vector ($b$):** $\begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}$

**Explanation:** Each row of the matrix $A$ contains the coefficients of the variables for a single equation. Multiplying row $i$ by the vector of unknowns reconstructs the left-hand side of equation $i$, which is equated to the corresponding entry of $b$.

---

### Exercise 2. Gaussian Elimination — One Solution

## Question

Solve using Gaussian elimination:

$$\begin{cases} x + y + z = 6, \\ 2x - y + z = 3, \\ x + 2y - z = 2. \end{cases}$$

After solving, substitute the result into all equations and check consistency.

## Solution

**Step 1: Set up the augmented matrix $[A \mid b]$**

$$\left(\begin{array}{ccc\|c} 1 & 1 & 1 & 6 \\ 2 & -1 & 1 & 3 \\ 1 & 2 & -1 & 2 \end{array}\right)$$

**Step 2: Apply row operations**

- $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:
  $$\left(\begin{array}{ccc\|c} 1 & 1 & 1 & 6 \\ 0 & -3 & -1 & -9 \\ 0 & 1 & -2 & -4 \end{array}\right)$$
- Swap $R_2$ and $R_3$ for convenience:
  $$\left(\begin{array}{ccc\|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & -3 & -1 & -9 \end{array}\right)$$
- $R_3 \leftarrow R_3 + 3R_2$:
  $$\left(\begin{array}{ccc\|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & 0 & -7 & -21 \end{array}\right)$$
- $R_3 \leftarrow -\frac{1}{7}R_3$:
  $$\left(\begin{array}{ccc\|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & 0 & 1 & 3 \end{array}\right)$$

**Step 3: Back-substitution**

- From $z = 3$:
- $y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2$
- $x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1$

Solution: $x = 1, y = 2, z = 3$.

**Step 4: Verification check**
- Eq 1: $1 + 2 + 3 = 6$ (True)
- Eq 2: $2(1) - 2 + 3 = 3$ (True)
- Eq 3: $1 + 2(2) - 3 = 2$ (True)

**Explanation:** Gaussian elimination transforms the system into row echelon form, allowing easy back-substitution to find the unique solution.

---

### Exercise 3. Inconsistent System

## Question

Solve or show that the system is inconsistent:

$$\begin{cases} x + 2y = 3, \\ 2x + 4y = 7. \end{cases}$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Solution

**Step 1: Set up the augmented matrix**

$$\left(\begin{array}{cc\|c} 1 & 2 & 3 \\ 2 & 4 & 7 \end{array}\right)$$

**Step 2: Apply elimination ($R_2 \leftarrow R_2 - 2R_1$)**

$$\left(\begin{array}{cc\|c} 1 & 2 & 3 \\ 0 & 0 & 1 \end{array}\right)$$

**Step 3: Interpretation**

The second row translates to the equation $0x + 0y = 1$, which simplifies to $0 = 1$. This contradiction proves the system is inconsistent and has **no solution**.

**Explanation:** An inconsistent system contains parallel or conflicting lines that never intersect, resulting in a false statement like $0 = 1$ during elimination.

---

### Exercise 4. Infinitely Many Solutions

## Question

Solve

$$\begin{cases} x + y + z = 2, \\ 2x + 2y + 2z = 4, \\ x - y + z = 0. \end{cases}$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## Solution

**Step 1: Set up the augmented matrix
