# Vectors

## Goal of the Set

After completing this set, the student should be comfortable performing vector operations in $\mathbb R^2$ and $\mathbb R^3$, understand length, angle, dot product, cross product, projection, and linear dependence. Vectors should be treated both computationally and geometrically.

---

## Basic Exercises

### Exercise 1. Vector Operations and Their Meaning

## Question

For $u = (2, -1, 3)$ and $v = (-1, 4, 2)$ compute

$$u + v, \qquad u - v, \qquad 3u - 2v.$$

Then verify that $(u + v) - v = u$, and explain geometrically what adding two vectors means.

## Solution

**Step 1: Compute $u + v$**

$$u + v = \begin{pmatrix} 2 + (-1) \\ -1 + 4 \\ 3 + 2 \end{pmatrix} = \begin{pmatrix} 1 \\ 3 \\ 5 \end{pmatrix}$$

**Step 2: Compute $u - v$**

$$u - v = \begin{pmatrix} 2 - (-1) \\ -1 - 4 \\ 3 - 2 \end{pmatrix} = \begin{pmatrix} 3 \\ -5 \\ 1 \end{pmatrix}$$

**Step 3: Compute $3u - 2v$**

$$3u = \begin{pmatrix} 6 \\ -3 \\ 9 \end{pmatrix}, \qquad 2v = \begin{pmatrix} -2 \\ 8 \\ 4 \end{pmatrix}$$

$$3u - 2v = \begin{pmatrix} 6 - (-2) \\ -3 - 8 \\ 9 - 4 \end{pmatrix} = \begin{pmatrix} 8 \\ -11 \\ 5 \end{pmatrix}$$

**Step 4: Verify $(u + v) - v = u$**

$$(u + v) - v = \begin{pmatrix} 1 \\ 3 \\ 5 \end{pmatrix} - \begin{pmatrix} -1 \\ 4 \\ 2 \end{pmatrix} = \begin{pmatrix} 1 - (-1) \\ 3 - 4 \\ 5 - 2 \end{pmatrix} = \begin{pmatrix} 2 \\ -1 \\ 3 \end{pmatrix} = u$$

**Explanation:** Geometrically, adding two vectors corresponds to placing them head-to-tail (the parallelogram or triangle law), where the resulting vector represents the net displacement from the start of the first vector to the end of the second.

---

### Exercise 2. Distance as the Length of a Vector

## Question

The points are $A = (1, 2, 3)$ and $B = (4, -2, 6)$.
1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

## Solution

**Step 1: Construct $\overrightarrow{AB}$**

$$\overrightarrow{AB} = B - A = \begin{pmatrix} 4 - 1 \\ -2 - 2 \\ 6 - 3 \end{pmatrix} = \begin{pmatrix} 3 \\ -4 \\ 3 \end{pmatrix}$$

**Step 2: Compute its length $\|\overrightarrow{AB}\|**

$$\Vert{}\overrightarrow{AB}\Vert{} = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}$$

**Step 3: Compute distance via coordinate formula**

$$d(A, B) = \sqrt{(4 - 1)^2 + (-2 - 2)^2 + (6 - 3)^2} = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}$$

**Explanation:** Both calculations yield the exact same result because the distance formula between two points is mathematically identical to computing the Euclidean norm (length) of their difference vector $\overrightarrow{AB} = B - A$.

---

### Exercise 3. Vector Normalization

## Question

For $v = (3, 4)$ find a unit vector $e$ with the same direction and orientation. Check that $\Vert{}e\Vert{} = 1$, reconstruct $v$ in the form $v = \Vert{}v\Vert{}e$, and explain what changes during normalization and what remains unchanged.

## Solution

**Step 1: Compute the length of $v$**

$$\Vert{}v\Vert{} = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5$$

**Step 2: Find the unit vector $e$**

$$e = \frac{v}{\Vert{}v\Vert{}} = \frac{1}{5} \begin{pmatrix} 3 \\ 4 \end{pmatrix} = \begin{pmatrix} 3/5 \\ 4/5 \end{pmatrix}$$

**Step 3: Check that $\Vert{}e\Vert{} = 1$**

$$\Vert{}e\Vert{} = \sqrt{(3/5)^2 + (4/5)^2} = \sqrt{9/25 + 16/25} = \sqrt{25/25} = 1$$

**Step 4: Reconstruct $v$**

$$\Vert{}v\Vert{}e = 5 \begin{pmatrix} 3/5 \\ 4/5 \end{pmatrix} = \begin{pmatrix} 3 \\ 4 \end{pmatrix} = v$$

**Explanation:** During normalization, the vector's length is scaled to $1$, changing its magnitude, while its orientation and line of direction remain completely unchanged.

---

### Exercise 4. Dot Product and Perpendicularity

## Question

For $u = (1, 2, -1)$ and $v = (2, -1, 3)$ compute $u \cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w = (2, -1, a)$ is perpendicular to $u$, and check the result.

## Solution

**Step 1: Compute $u \cdot v$**

$$u \cdot v = (1)(2) + (2)(-1) + (-1)(3) = 2 - 2 - 3 = -3$$

**Step 2: Determine perpendicularity**

Since $u \cdot v = -3 \neq 0$, the vectors $u$ and $v$ are **not perpendicular**.

**Step 3: Find $a$ such that $w \perp u$ ($u \cdot w = 0$)**

$$u \cdot w = (1)(2) + (2)(-1) + (-1)(a) = 2 - 2 - a = -a$$

Setting $-a = 0 \implies a = 0$.

**Step 4: Check the result**

For $w = (2, -1, 0)$:
$$u \cdot w = (1)(2) + (2)(-1) + (-1)(0) = 2 - 2 + 0 = 0 \implies \text{Perpendicular verified.}$$

**Explanation:** The dot product equals zero if and only if two vectors are orthogonal (perpendicular). We use this condition as an algebraic equation to solve for unknown vector coordinates.

---

### Exercise 5. Angle Between Vectors

## Question

Given $u = (1, 1, 0)$ and $v = (1, 0, 1)$:
1. Use the sign of $u \cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

## Solution

**Step 1: Predict angle type using $u \cdot v$**

$$u \cdot v = (1)(1) + (1)(0) + (0)(1) = 1$$

Since $u \cdot v > 0$, the cosine is positive, predicting an **acute angle** ($\theta < 90^\circ$).

**Step 2: Compute the angle**

- Lengths:
  $$\Vert{}u\Vert{} = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{2}, \qquad \Vert{}v\Vert{} = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}$$
- Using the dot product formula $\cos\theta = \frac{u \cdot v}{\Vert{}u\Vert{} \Vert{}v\Vert{}}$:
  $$\cos\theta = \frac{1}{\sqrt{2} \cdot \sqrt{2}} = \frac{1}{2}$$
- Angle: $\theta = \arccos(1/2) = 60^\circ$ (or $\pi/3$ radians).

**Step 3: Comparison**

The computed angle ($60^\circ$) matches our qualitative prediction that the angle would be acute.

**Explanation:** The sign of the dot product gives immediate qualitative insight into the geometric angle before evaluating trigonometric functions.

---

### Exercise 6. Projection and Perpendicular Component

## Question

Find the projection of $u = (4, 2)$ onto the direction $v = (1, 1)$. Then compute

$$r = u - \operatorname{proj}_v u$$

and verify that $r \cdot v = 0$. Explain this result geometrically.

## Solution

**Step 1: Compute components for projection**

$$u \cdot v = (4)(1) + (2)(1) = 6, \qquad v \cdot v = 1^2 + 1^2 = 2$$

**Step 2: Compute $\operatorname{proj}_v u$**

$$\operatorname{proj}_v u = \frac{u \cdot v}{v \cdot v} v = \frac{6}{2} \begin{pmatrix} 1 \\ 1 \end{pmatrix} = 3 \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \begin{pmatrix} 3 \\ 3 \end{pmatrix}$$

**Step 3: Compute orthogonal component $r$**

$$r = u - \operatorname{proj}_v u = \begin{pmatrix} 4 \\ 2 \end{pmatrix} - \begin{pmatrix} 3 \\ 3 \end{pmatrix} = \begin{pmatrix} 1 \\ -1 \end{pmatrix}$$

**Step 4: Verify $r \cdot v = 0$**

$$r \cdot v = (1)(1) + (-1)(1) = 1 - 1 = 0$$

**Explanation:** Decomposing $u$ splits it into a parallel vector lying along $v$ and a perpendicular remainder vector $r$, which forms a right triangle with $u$ and its projection.

---

### Exercise 7. Linear Dependence Without Heavy Computation

## Question

Given

$$u = (1, 2, 3), \qquad v = (2, 4, 6), \qquad w = (0, 1, 1).$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

## Solution

**Step 1: Identify relation between $u$ and $v$**

Notice that $v = 2u$, because:
$$\begin{pmatrix} 2 \\ 4 \\ 6 \end{pmatrix} = 2 \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$$

**Step 2: Determine linear independence**

Since $v$ is a direct scalar multiple of $u$, the set of vectors $\{u, v, w\}$ is **linearly dependent**.

**Explanation:** No heavy calculation (such as computing a full $3 \times 3$ determinant or reducing a matrix) is required because spotting that one vector is a scalar multiple of another immediately guarantees linear dependence for any collection containing them.

---

### Exercise 8. Linear Combination and Checking the Result

## Question

Check whether $w = (5, 1)$ can be written as

$$w = au + bv,$$

where $u = (1, 1)$ and $v = (2, -1)$. If so, find $a, b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

## Solution

**Step 1: Set up the system of linear equations**

$$a \begin{pmatrix} 1 \\ 1 \end{pmatrix} + b \begin{pmatrix} 2 \\ -1 \end{pmatrix} = \begin{pmatrix} 5 \\ 1 \end{pmatrix} \implies \begin{cases} a + 2b = 5 \\ a - b = 1 \end{cases}$$

**Step 2: Solve for $a$ and $b$**

Subtract the second equation from the first:
$$(a + 2b) - (a - b) = 5 - 1 \implies 3b = 4 \implies b = 4/3$$
Substitute $b = 4/3$ into $a - b = 1$:
$$a - 4/3 = 1 \implies a = 7/3$$

**Step 3: Reconstruct $w$**

$$\frac{7}{3} \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \frac{4}{3} \begin{pmatrix} 2 \\ -1 \end{pmatrix} = \begin{pmatrix} 7/3 + 8/3 \\ 7/3 - 4/3 \end{pmatrix} = \begin{pmatrix} 15/3 \\ 3/3 \end{pmatrix} = \begin{pmatrix} 5 \\ 1 \end{pmatrix} = w$$

**Explanation:** The existence of such coefficients means $w$ lies in the span of $u$ and $v$ (in this case, forming a linear combination that spans the 2D plane).

---

### Exercise 9. Cross Product as a Perpendicular Direction

## Question

For $u = (1, 2, 0)$ and $v = (0, 1, 3)$ compute $u \times v$. Use dot products to check perpendicularity to both vectors, compute $v \times u$, and compare the results.

## Solution

**Step 1: Compute $u \times v$**

$$u \times v = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ 1 & 2 & 0 \\ 0 & 1 & 3 \end{vmatrix} = \hat{i}((2)(3) - (0)(1)) - \hat{j}((1)(3) - (0)(0)) + \hat{k}((1)(1) - (2)(0)) = \begin{pmatrix} 6 \\ -3 \\ 1 \end{pmatrix}$$

**
