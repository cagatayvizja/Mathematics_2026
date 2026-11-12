# Lines and Planes

## Goal of the Set

After completing this set, the student should be able to describe lines and planes using points, direction vectors, and normal vectors; move between the most important forms of equations; analyze the relative position of geometric objects; and compute intersections, angles, distances, and projections.

---

## Basic Exercises

### Exercise 1. Line Through Two Points

## Question

Find the equation of the line through $A = (1, 2)$ and $B = (4, -1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## Solution

**Step 1: Find a direction vector**

$$v = B - A = \begin{pmatrix} 4 - 1 \\ -1 - 2 \end{pmatrix} = \begin{pmatrix} 3 \\ -3 \end{pmatrix}$$

**Step 2: Write the parametric form**

Using point $A$ and direction $v$:
$$(x, y) = (1, 2) + t(3, -3), \quad t \in \mathbb{R}$$

**Step 3: Find the general form ($Ax + By = C$)**

The slope is $m = \frac{-3 - 2}{4 - 1} = \frac{-5}{3} = -1$. Using the point-slope form with normal vector coefficients:
A direction vector is $v = (3, -3)$, so an orthogonal normal vector is $n = (3, 3)$ (or simplified to $(1, 1)$).
Equation: $1(x - 1) + 1(y - 2) = 0 \implies x + y = 3$.

**Step 4: Check both points**
- For $A = (1, 2)$: $1 + 2 = 3$ (True)
- For $B = (4, -1)$: $4 + (-1) = 3$ (True)

**Explanation:** The parametric form uses a point and a direction vector, whereas the general form uses a normal vector perpendicular to the line's direction.

---

### Exercise 2. A Line in Space

## Question

Given

$$L: (x, y, z) = (2, -1, 3) + t(1, 2, -2).$$

State a point on the line and its direction vector, check whether $P = (4, 3, -1)$ lies on $L$, and find the point corresponding to $t = -1$.

## Solution

**Step 1: Identify point and direction vector**
- Point on line: $p_0 = (2, -1, 3)$
- Direction vector: $v = (1, 2, -2)$

**Step 2: Check whether $P = (4, 3, -1)$ lies on $L$**

Set $(4, 3, -1) = (2 + t, -1 + 2t, 3 - 2t)$ to solve for $t$:
1. $2 + t = 4 \implies t = 2$
2. $-1 + 2t = 3 \implies 2t = 4 \implies t = 2$
3. $3 - 2t = -1 \implies -2t = -4 \implies t = 2$

Since $t = 2$ satisfies all three coordinate equations simultaneously, **$P$ lies on the line**.

**Step 3: Find the point corresponding to $t = -1$**

$$(x, y, z) = (2, -1, 3) + (-1)(1, 2, -2) = (2 - 1, -1 - 2, 3 + (-1)(-2)) = (1, -3, 5)$$

**Explanation:** A parametric line equation generates a unique point for every real number $t$. Compatibility across all coordinates indicates a point belongs to the line.

---

### Exercise 3. Plane Through a Point with a Given Normal Vector

## Question

Find the equation of the plane through $P = (1, -2, 3)$ and perpendicular to $n = (2, 1, -1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

## Solution

**Step 1: Construct the plane equation**

The general equation of a plane with normal $n = (A, B, C)$ passing through $P = (x_0, y_0, z_0)$ is:
$$A(x - x_0) + B(y - y_0) + C(z - z_0) = 0$$
$$2(x - 1) + 1(y - (-2)) + (-1)(z - 3) = 0$$
$$2x - 2 + y + 2 - z + 3 = 0 \implies 2x + y - z + 3 = 0$$

**Step 2: Check by substituting point $P$**

$$2(1) + (-2) - (3) + 3 = 2 - 2 - 3 + 3 = 0 \text{ (True)}$$

**Explanation:** The normal vector supplies the constant coefficients $(A, B, C)$ for the planar equation, defining the orientation of the plane in space.

---

### Exercise 4. Plane Through Three Points

## Question

Find the equation of the plane through

$$A = (1, 0, 0), \quad B = (0, 1, 0), \quad C = (0, 0, 1).$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

## Solution

**Step 1: Construct two vectors in the plane**

$$\overrightarrow{AB} = B - A = \begin{pmatrix} -1 \\ 1 \\ 0 \end{pmatrix}, \qquad \overrightarrow{AC} = C - A = \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix}$$

**Step 2: Compute the normal vector via cross product**

$$n = \overrightarrow{AB} \times \overrightarrow{AC} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ -1 & 1 & 0 \\ -1 & 0 & 1 \end{vmatrix} = \begin{pmatrix} (1)(1) - (0)(0) \\ (0)(-1) - (-1)(1) \\ (-1)(0) - (1)(-1) \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$$

**Step 3: Formulate the plane equation**

Using point $A(1, 0, 0)$ and $n = (1, 1, 1)$:
$$1(x - 1) + 1(y - 0) + 1(z - 0) = 0 \implies x + y + z = 1$$

**Step 4: Verify on all points**
- $A(1, 0, 0) \implies 1 + 0 + 0 = 1$ (True)
- $B(0, 1, 0) \implies 0 + 1 + 0 = 1$ (True)
- $C(0, 0, 1) \implies 0 + 0 + 1 = 1$ (True)

**Explanation:** The cross product of two non-collinear vectors lying in a plane yields an orthogonal normal vector, establishing the plane's orientation.

---

### Exercise 5. Relative Position of Two Lines

## Question

Analyze the position of

$$L_1: (x, y, z) = (1, 1, 0) + t(1, 2, 1),$$

$$L_2: (x, y, z) = (2, 0, 1) + s(0, 1, -1).$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

## Solution

**Step 1: Check if direction vectors are parallel**

$v_1 = (1, 2, 1)$ and $v_2 = (0, 1, -1)$ are not scalar multiples of each other, so the lines are **not parallel**.

**Step 2: Set up equations to check for intersection**

$$\begin{cases} 1 + t = 2 \\ 1 + 2t = s \\ t = 1 - s \end{cases}$$

From equation 1, $t = 1$.
