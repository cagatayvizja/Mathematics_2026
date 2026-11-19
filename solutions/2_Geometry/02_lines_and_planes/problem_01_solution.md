# Lines and Planes

## Goal of the Set

After completing this set, the student should be able to describe lines and planes using points, direction vectors, and normal vectors; move between the most important forms of equations; analyze the relative position of geometric objects; and compute intersections, angles, distances, and projections.

---

## Basic Exercises

### Exercise 1. Line Through Two Points

## Question

Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## Solution

**Step 1: Compute the slope and direction vector**

Using the slope formula between $A=(1,2)$ and $B=(4,-1)$, we compute:

$$
m = \frac{-1 - 2}{4 - 1} = \frac{-3}{3} = -1.
$$

Subtracting coordinates from $A$ to $B$ gives the displacement vector $\vec{u} = (4-1, -1-2) = (3, -3)$, which simplifies to the direction vector:

$$
\vec{d} = (1, -1).
$$

**Step 2: Find a normal vector**

A normal vector $\vec{n}$ is perpendicular to the direction vector $\vec{d}$, so their dot product must vanish. Choosing $\vec{n} = (1, 1)$ gives:

$$
\vec{n} \cdot \vec{d} = (1)(1) + (1)(-1) = 0,
$$

confirming $\vec{n} = (1, 1)$ is a valid normal vector.

**Step 3: Write parametric and general forms**

Starting at point $A=(1,2)$ with direction vector $\vec{d}=(1,-1)$ and parameter $t \in \mathbb{R}$, the parametric equation is:

$$
(x, y) = (1, 2) + t(1, -1), \qquad \text{i.e.,} \qquad x = 1 + t, \quad y = 2 - t.
$$

Using the point-slope relation with slope $m = -1$ through $(1,2)$:

$$
y - 2 = -1(x - 1) \implies x + y = 3,
$$

which is the general (standard) form of the line.

**Step 4: Verify both points**

Substituting $A=(1,2)$ into $x + y = 3$ gives $1 + 2 = 3$. Substituting $B=(4,-1)$ into $x + y = 3$ gives $4 + (-1) = 3$. Both points satisfy the equation.

---

### Exercise 2. A Line in Space

## Question

Given

$$
L:(x,y,z)=(2,-1,3)+t(1,2,-2),
$$

state a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

## Solution

**Step 1: Point and direction vector**

From the parametric representation $(x,y,z) = p_0 + t\vec{v}$, a point on $L$ (at $t=0$) is $P_0 = (2, -1, 3)$, and a direction vector is:

$$
\vec{v} = (1, 2, -2).
$$

**Step 2: Check whether $P=(4,3,-1)$ lies on $L$**

We solve $(2+t, -1+2t, 3-2t) = (4, 3, -1)$:

$$
2 + t = 4 \implies t = 2, \qquad -1 + 2t = 3 \implies t = 2, \qquad 3 - 2t = -1 \implies t = 2.
$$

Because the same parameter $t = 2$ satisfies all three coordinates, $P=(4,3,-1)$ lies on $L$.

**Step 3: Point for $t=-1$**

Substituting $t = -1$ into the parametric equation:

$$
(x, y, z) = (2, -1, 3) + (-1)(1, 2, -2) = (1, -3, 5).
$$

---

### Exercise 3. Plane Through a Point with a Given Normal Vector

## Question

Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

## Solution

**Step 1: Construct the plane equation**

A plane passing through $P=(x_0, y_0, z_0)$ with normal vector $\vec{n}=(a,b,c)$ consists of all points $X=(x,y,z)$ such that $\vec{n} \cdot (X - P) = 0$:

$$
2(x - 1) + 1(y + 2) - 1(z - 3) = 0.
$$

Expanding and simplifying gives:

$$
2x + y - z - 2 + 2 + 3 = 0 \implies 2x + y - z + 3 = 0.
$$

**Step 2: Check point $P$ and role of the normal vector**

Substituting $P=(1,-2,3)$ gives $2(1) + (-2) - (3) + 3 = 0$, verifying $P$ lies on the plane. The normal vector $\vec{n}$ fixes the orientation of the plane in space because every vector lying inside the plane is orthogonal to $\vec{n}$.

---

### Exercise 4. Plane Through Three Points

## Question

Find the equation of the plane through

$$
A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

## Solution

**Step 1: Construct two in-plane vectors and take their cross product**

Subtracting coordinates gives two vectors in the plane:

$$
\overrightarrow{AB} = (-1, 1, 0), \qquad \overrightarrow{AC} = (-1, 0, 1).
$$

Their cross product yields a normal vector orthogonal to both directions:

$$
\vec{n} = \overrightarrow{AB} \times \overrightarrow{AC} = \det \begin{pmatrix} \vec{i} & \vec{j} & \vec{k} \\ -1 & 1 & 0 \\ -1 & 0 & 1 \end{pmatrix} = (1, 1, 1).
$$

**Step 2: Write and check the plane equation**

Using normal $\vec{n}=(1,1,1)$ and point $A=(1,0,0)$:

$$
1(x - 1) + 1(y - 0) + 1(z - 0) = 0 \implies x + y + z = 1.
$$

Checking all three points:
- For $A(1,0,0)$: $1 + 0 + 0 = 1$.
- For $B(0,1,0)$: $0 + 1 + 0 = 1$.
- For $C(0,0,1)$: $0 + 0 + 1 = 1$.

---

### Exercise 5. Relative Position of Two Lines

## Question

Analyze the position of

$$
L_1:(x,y,z)=(1,1,0)+t(1,2,1),
$$

$$
L_2:(x,y,z)=(2,0,1)+s(0,1,-1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

## Solution

**Step 1: Check parallelism**

The direction vectors are $\vec{v}_1 = (1,2,1)$ and $\vec{v}_2 = (0,1,-1)$. Since $\vec{v}_1$ is not a scalar multiple of $\vec{v}_2$, the lines are not parallel.

**Step 2: Test for intersection**

Equating coordinates for $L_1$ and $L_2$:

$$
1 + t = 2 \implies t = 1.
$$

Substituting $t = 1$ into the remaining coordinates:

$$
1 + 2(1) = 0 + s \implies 3 = s, \qquad 0 + 1(1) = 1 - s \implies 1 = 1 - 3 = -2,
$$

which is a contradiction ($1 \neq -2$). Because the lines are neither parallel nor intersecting, they are **skew**.

---

### Exercise 6. Angle Between Planes

## Question

Given

$$
\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

## Solution

**Step 1: Check parallelism via normal vectors**

The normal vectors are $\vec{n}_1 = (1,1,1)$ and $\vec{n}_2 = (1,-1,0)$. Since $\vec{n}_1$ is not proportional to $\vec{n}_2$, the planes are not parallel.

**Step 2: Compute the angle and justify using normals**

The angle $\theta$ between two planes equals the angle between their normal vectors:

$$
\cos\theta = \frac{|\vec{n}_1 \cdot \vec{n}_2|}{\|\vec{n}_1\|\|\vec{n}_2\|} = \frac{|(1)(1) + (1)(-1) + (1)(0)|}{\sqrt{1^2+1^2+1^2}\sqrt{1^2+(-1)^2+0^2}} = \frac{0}{\sqrt{3}\sqrt{2}} = 0.
$$

Thus $\theta = \frac{\pi}{2}$ ($90^\circ$), meaning the planes are orthogonal. Normal vectors suffice because rotating a plane rigidly rotates its normal vector by the exact same angle.

---

### Exercise 7. A Line Relative to a Plane

## Question

For

$$
L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,
$$

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

## Solution

**Step 1: Dot product of direction and normal vectors**

Here $\vec{v} = (1,-1,0)$ and $\vec{n} = (1,1,1)$. Computing the dot product:

$$
\vec{v} \cdot \vec{n} = (1)(1) + (-1)(1) + (0)(1) = 0.
$$

A zero dot product means $\vec{v} \perp \vec{n}$, so the line is either parallel to $\Pi$ or contained in $\Pi$.

**Step 2: Check a point on the line**

For $t = 0$, the point $P_0 = (1,1,0)$ lies on $L$. Substituting into $\Pi$:

$$
1 + 1 + 0 = 2.
$$

Since $P_0$ satisfies the plane equation and $\vec{v} \cdot \vec{n} = 0$, the entire line **lies in the plane** $\Pi$.

---

### Exercise 8. Intersection Point of a Line and a Plane

## Question

Find the intersection point of

$$
(x,y,z)=(1,0,2)+t(1,2,-1)
$$

with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

## Solution

**Step 1: Substitute parametric coordinates into the plane**

With $x = 1 + t$, $y = 2t$, and $z = 2 - t$:

$$
(1 + t) + 2t + (2 - t) = 4 \implies 3 + 2t = 4 \implies t = \frac{1}{2}.
$$

**Step 2: Find and verify the intersection point**

Substituting $t = \frac{1}{2}$ into the line equation gives:

$$
(x, y, z) = \left(1 + \frac{1}{2},\; 2\left(\frac{1}{2}\right),\; 2 - \frac{1}{2}\right) = \left(\frac{3}{2}, 1, \frac{3}{2}\right).
$$

Checking in the plane: $\frac{3}{2} + 1 + \frac{3}{2} = 4$. Checking in the line: $(1,0,2) + \frac{1}{2}(1,2,-1) = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$.

---

### Exercise 9. Distances

## Question

Compute:

1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

## Solution

**1. Distance from $P=(2,3)$ to $3x+4y-10=0$**

Using the point-to-line distance formula:

$$
d(P, L) = \frac{|3(2) + 4(3) - 10|}{\sqrt{3^2 + 4^2}} = \frac{|6 + 12 - 10|}{5} = \frac{8}{5}.
$$

**2. Distance from $Q=(2,-1,3)$ to $2x-2y+z-4=0$**

Using the point-to-plane distance formula:

$$
d(Q, \Pi) = \frac{|2(2) - 2(-1) + 1(3) - 4|}{\sqrt{2^2 + (-2)^2 + 1^2}} = \frac{|4 + 2 + 3 - 4|}{3} = \frac{5}{3}.
$$

**Comparison:** Both formulas project the displacement from a given point to the geometric object onto the unit normal vector $\frac{\vec{n}}{\|\vec{n}\|}$, measuring shortest perpendicular separation along the normal direction.

---

### Exercise 10. Projection of a Point onto a Plane

## Question

Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

## Solution

**Step 1: Orthogonal projection $P'$**

The normal to $x+y+z=3$ is $\vec{n}=(1,1,1)$. The perpendicular line through $P=(2,1,3)$ is $(2+t, 1+t, 3+t)$. Substituting into the plane:

$$
(2+t) + (1+t) + (3+t) = 3 \implies 6 + 3t = 3 \implies t = -1.
$$

Thus the orthogonal projection is:

$$
P' = (2 - 1, 1 - 1, 3 - 1) = (1, 0, 2).
$$

**Step 2: Reflection $P^*$ and midpoint check**

Since $P'$ is the midpoint of $P$ and $P^*$:

$$
P^* = 2P' - P = 2(1, 0, 2) - (2, 1, 3) = (0, -1, 1).
$$

The midpoint of $P(2,1,3)$ and $P^*(0,-1,1)$ is $\left(\frac{2+0}{2}, \frac{1-1}{2}, \frac{3+1}{2}\right) = (1, 0, 2)$, which satisfies $1 + 0 + 2 = 3$ and lies on the plane.

---

## More Challenging Exercises

### Exercise 11. Plane Containing a Line and a Point

## Question

Find the equation of the plane containing

$$
(x,y,z)=(1,0,2)+t(1,1,-1)
$$

and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

## Solution

**Step 1: Build two direction vectors and normal vector**

A point on the line is $A = (1,0,2)$ with line direction $\vec{v}_1 = (1,1,-1)$. Another direction in the plane connects $A$ to $P=(0,2,1)$:

$$
\vec{v}_2 = P - A = (-1, 2, -1).
$$

Taking the cross product gives a normal vector:

$$
\vec{n} = \vec{v}_1 \times \vec{v}_2 = (1,1,-1) \times (-1,2,-1) = (1, 2, 3).
$$

**Step 2: Write and verify the plane equation**

Using $\vec{n}=(1,2,3)$ and $A=(1,0,2)$:

$$
1(x - 1) + 2(y - 0) + 3(z - 2) = 0 \implies x + 2y + 3z = 7.
$$

Checking $P(0,2,1)$: $0 + 2(2) + 3(1) = 7$. Checking the line $(1+t, t, 2-t)$: $(1+t) + 2t + 3(2-t) = 7$ for all $t \in \mathbb{R}$.

---

### Exercise 12. Intersection Line of Two Planes

## Question

Find a parametric equation of the line that is the intersection of

$$
x+y+z=3,\qquad x-y+z=1.
$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

## Solution

**Step 1: Direction vector from cross product of normals**

The normal vectors are $\vec{n}_1 = (1,1,1)$ and $\vec{n}_2 = (1,-1,1)$. Their cross product is:

$$
\vec{d} = \vec{n}_1 \times \vec{n}_2 = (1,1,1) \times (1,-1,1) = (2, 0, -2),
$$

which can be scaled to $\vec{v} = (1, 0, -1)$.

**Step 2: Solve the system for parametric form**

Subtracting the second equation from the first:

$$
(x+y+z) - (x-y+z) = 3 - 1 \implies 2y = 2 \implies y = 1.
$$

Substituting $y = 1$ gives $x + z = 2$. Setting $x = 2 + t$ gives $z = -t$, so a parametric form is:

$$
(x, y, z) = (2, 1, 0) + t(1, 0, -1).
$$

Both methods yield the exact same direction $(1, 0, -1)$ (up to nonzero scalar scaling).

---

### Exercise 13. Closest Point on a Plane

## Question

Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

## Solution

**Step 1: Find the closest point (orthogonal projection)**

The normal vector to $x+2y+2z=4$ is $\vec{n}=(1,2,2)$. Parameterizing the perpendicular line through $P=(3,0,0)$ gives $(3+t, 2t, 2t)$. Substituting into the plane:

$$
(3+t) + 2(2t) + 2(2t) = 4 \implies 3 + 9t = 4 \implies t = \frac{1}{9}.
$$

Thus the closest point is:

$$
Q = \left(3 + \frac{1}{9},\; \frac{2}{9},\; \frac{2}{9}\right) = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right).
$$

**Step 2: Distance and perpendicularity check**

The distance is:

$$
\|Q - P\| = \left\|\left(\frac{1}{9}, \frac{2}{9}, \frac{2}{9}\right)\right\| = \frac{\sqrt{1^2 + 2^2 + 2^2}}{9} = \frac{3}{9} = \frac{1}{3}.
$$

Since $Q - P = \frac{1}{9}(1,2,2) = \frac{1}{9}\vec{n}$, the segment $PQ$ is parallel to $\vec{n}$ and therefore perpendicular to the plane.

---

### Exercise 14. Contrast: Intersection and Parallelism

## Question

From the point $P=(0,0,1)$, two lines are drawn with direction vectors

$$
v_1=(2,1,-1),\qquad v_2=(2,1,0).
$$

For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

## Solution

**1. Line $L_1$ with direction $\vec{v}_1=(2,1,-1)$**

Its parameterization is $(2t, t, 1-t)$. Setting $z = 0$ gives $1 - t = 0 \implies t = 1$, so $L_1$ **intersects** the plane $z=0$ at:

$$
(2, 1, 0).
$$

**2. Line $L_2$ with direction $\vec{v}_2=(2,1,0)$**

The plane $z=0$ has normal vector $\vec{n} = (0,0,1)$. Because the $z$-component of $\vec{v}_2$ is $0$, $\vec{v}_2 \cdot \vec{n} = 0$, meaning $L_2$ is parallel to $z=0$. Since $P=(0,0,1)$ has $z = 1 \neq 0$, $L_2$ does not lie on the plane and is strictly **parallel** to it.

---

### Exercise 15. Complete Classification of a Line Relative to a Plane

## Question

Let

$$
L:p+tv,\qquad \Pi:n\cdot x=d.
$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

## Solution

**General Classification Criteria**

Substituting $x = p + tv$ into $\vec{n} \cdot x = d$ gives $(\vec{n} \cdot \vec{v})t = d - \vec{n} \cdot p$:

1. **One intersection point:** $\vec{n} \cdot \vec{v} \neq 0$. A unique parameter $t = \frac{d - \vec{n} \cdot p}{\vec{n} \cdot \vec{v}}$ exists.
2. **Parallel with no common points:** $\vec{n} \cdot \vec{v} = 0$ and $\vec{n} \cdot p \neq d$.
3. **Line contained in the plane:** $\vec{n} \cdot \vec{v} = 0$ and $\vec{n} \cdot p = d$.

**Numerical Examples (for plane $z = 0$, so $\vec{n}=(0,0,1)$ and $d=0$)**

- **One intersection:** $p=(0,0,1)$, $\vec{v}=(0,0,1)$ gives $\vec{n}\cdot\vec{v} = 1 \neq 0$ (intersects at $(0,0,0)$).
- **Strictly parallel:** $p=(0,0,1)$, $\vec{v}=(1,0,0)$ gives $\vec{n}\cdot\vec{v} = 0$ and $\vec{n}\cdot p = 1 \neq 0$.
- **Contained in plane:** $p=(0,0,0)$, $\vec{v}=(1,0,0)$ gives $\vec{n}\cdot\vec{v} = 0$ and $\vec{n}\cdot p = 0$.
