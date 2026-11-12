# Second-Degree Curves and Surfaces

## Goal of the Set

After completing this set, the student should be able to recognize the basic second-degree curves in the plane and the basic second-degree surfaces in space, read their most important features from equations, reduce simple equations to canonical form, and interpret geometric cross-sections.

---

## Basic Exercises

### Exercise 1. Recognizing Curves from Canonical Form

## Question

Recognize the curves

$$
x^2 + y^2 = 9,
$$

$$
\frac{x^2}{16} + \frac{y^2}{9} = 1,
$$

$$
y^2 = 8x,
$$

$$
\frac{x^2}{9} - \frac{y^2}{4} = 1.
$$

For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

## Solution

**1. Equation:** $x^2 + y^2 = 9$
- **Curve Type:** Circle.
- **Features:** Center at $(0, 0)$, radius $r = \sqrt{9} = 3$.
- **Recognition Rule:** Both variables are squared with equal positive coefficients.

**2. Equation:** $\frac{x^2}{16} + \frac{y^2}{9} = 1$
- **Curve Type:** Ellipse.
- **Features:** Center at $(0, 0)$, horizontal semiaxis $a = 4$, vertical semiaxis $b = 3$.
- **Recognition Rule:** Sum of squared variables with different positive denominators equating to $1$.

**3. Equation:** $y^2 = 8x$
- **Curve Type:** Parabola.
- **Features:** Vertex at $(0, 0)$, opens to the right, axis of symmetry is the $x$-axis, focal parameter $4p = 8 \implies p = 2$.
- **Recognition Rule:** Only one variable is squared while the other is linear.

**4. Equation:** $\frac{x^2}{9} - \frac{y^2}{4} = 1$
- **Curve Type:** Hyperbola.
- **Features:** Center at $(0, 0)$, opens horizontally with real semiaxis $a = 3$, conjugate semiaxis $b = 2$, asymptotes $y = \pm \frac{2}{3}x$.
- **Recognition Rule:** Difference of two squared variables equating to $1$.

**Explanation:** The presence of linear versus quadratic terms and the signs between squared terms immediately dictate the fundamental geometric classification of second-degree plane curves.

---

### Exercise 2. Circle by Completing the Square

## Question

Reduce

$$
x^2 + y^2 - 6x + 4y - 3 = 0
$$

to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

## Solution

**Step 1: Complete the square for $x$ and $y$**

$$
(x^2 - 6x + 9) + (y^2 + 4y + 4) = 3 + 9 + 4
$$
$$
(x - 3)^2 + (y + 2)^2 = 16
$$

**Step 2: Identify center and radius**

- **Center:** $(3, -2)$
- **Radius:** $r = \sqrt{16} = 4$

**Step 3: Test simple points**

Let's test point $(3, 2)$ (which is $r$ units directly above the center):
- Canonical form: $(3 - 3)^2 + (2 + 2)^2 = 0 + 4^2 = 16$ (True)
- General form: $3^2 + 2^2 - 6(3) + 4(2) - 3 = 9 + 4 - 18 + 8 - 3 = 0$ (True)

Let's test point $(7, -2)$ ($r$ units to the right):
- Canonical form: $(7 - 3)^2 + (-2 + 2)^2 = 4^2 + 0 = 16$ (True)
- General form: $7^2 + (-2)^2 - 6(7) + 4(-2) - 3 = 49 + 4 - 42 - 8 - 3 = 0$ (True)

**Explanation:** Completing the square regroups general quadratic terms into squared binomials, revealing the canonical center-radius form of a circle.

---

### Exercise 3. Ellipse

## Question

For

$$
\frac{x^2}{25} + \frac{y^2}{9} = 1,
$$

find the semiaxis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

## Solution

**Step 1: Find semiaxis lengths**

- Horizontal semiaxis: $a = \sqrt{25} = 5$
- Vertical semiaxis: $b = \sqrt{9} = 3$

**Step 2: Find coordinate intercepts**

- **$x$-intercepts:** Set $y = 0 \implies \frac{x^2}{25} = 1 \implies x = \pm 5 \implies \text{Points: } (\pm 5, 0)$.
- **$y$-intercepts:** Set $x = 0 \implies \frac{y^2}{9} = 1 \implies y = \pm 3 \implies \text{Points: } (0, \pm 3)$.

**Explanation:** The ellipse is more stretched along the $x$-axis because the denominator under $x^2$ ($25$) is larger than the denominator under $y^2$ ($9$), meaning the curve extends further horizontally than vertically.

---

### Exercise 4. Parabola

## Question

For

$$
y^2 = 12x,
$$

identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for $x = 3$ and use them to make a sketch.

## Solution

**Step 1: Identify geometric features**

- **Vertex:** $(0, 0)$
- **Axis of symmetry:** The $x$-axis ($y = 0$)
- **Opening direction:** Right (since $12 > 0$ multiplying $x$)

**Step 2: Find points for $x = 3$**

$$
y^2 = 12(3) = 36 \implies y = \pm 6
$$
Points: $(3, 6)$ and $(3, -6)$.

**Explanation:** The linear variable dictates the axis of symmetry, while the sign and magnitude of the coefficient control the opening direction and width.

---

### Exercise 5. Hyperbola and Asymptotes

## Question

For

$$
\frac{x^2}{16} - \frac{y^2}{9} = 1,
$$

find the intercepts with the $x$-axis, the asymptotes, and make a sketch. Explain why the asymptotes describe the behavior of the curve far from the center.

## Solution

**Step 1: Find $x$-axis intercepts**

Set $y = 0 \implies \frac{x^2}{16} = 1 \implies x = \pm 4 \implies \text{Intercepts: } (\pm 4, 0)$. (Note: there are no $y$-intercepts).

**Step 2: Find asymptotes**

The asymptotes of a canonical hyperbola are given by $y = \pm \frac{b}{a}x$:
$$
y = \pm \frac{3}{4}x
$$

**Explanation:** As $x$ and $y$ grow very large in magnitude, the constant $1$ on the right side becomes negligible compared to the fraction terms, causing the hyperbola equation to approximate $\frac{x^2}{16} - \frac{y^2}{9} \approx 0 \implies y = \pm \frac{3}{4}x$.

---

### Exercise 6. Shifted Ellipse

## Question

Reduce

$$
4x^2 + 9y^2 - 16x + 18y - 11 = 0
$$

to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

## Solution

**Step 1: Group and complete the square**

$$
(4x^2 - 16x) + (9y^2 + 18y) = 11
$$
$$
4(x^2 - 4x + 4) + 9(y^2 + 2y + 1) = 11 + 4(4) + 9(1)
$$
$$
4(x - 2)^2 + 9(y + 1)^2 = 11 + 16 + 9 = 36
$$

**Step 2: Convert to canonical form**

Divide everything by $36$:
$$
\frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1
$$

**Step 3: Identify center and semiaxes**

- **Center:** $(2, -1)$
- **Semiaxes:** $a = \sqrt{9} = 3$, $b = \sqrt{4} = 2$.

**Step 4: Check center coordinates in general equation**

Substitute $(2, -1)$ into $4x^2 + 9y^2 - 16x + 18y - 11$:
$$
4(2)^2 + 9(-1)^2 - 16(2) + 18(-1) - 11 = 4(4) + 9(1) - 32 - 18 - 11 = 16 + 9 - 32 - 18 - 11 = -36
$$
Wait, let's verify: the original equation equals $11$ when moved to the right side, but evaluating the left-hand side at the center $(2,-1)$ gives the constant term relative to the shifted coordinates, which matches the $-36$ adjustment from completing the square ($11 - 47 = -36$, and moving $-36$ gives $36$).

**Explanation:** Shifting variables via completing the square relocates the geometric center from the origin to $(h, k)$.

---

### Exercise 7. Classifying a Second-Degree Equation

## Question

Determine the type of object described by:
1. $4x^2 + 9y^2 = 36$,
2. $x^2 - y^2 = 1$,
3. $x^2 - 4y = 0$,
4. $x^2 + y^2 + 1 = 0$.

In the last case, explain why there are no real points.

## Solution

1. **$4x^2 + 9y^2 = 36$:** Dividing by $36$ yields $\frac{x^2}{9} + \frac{y^2}{4} = 1 \implies$ **Ellipse**.
2. **$x^2 - y^2 = 1$:** Difference of two squares equating to $1 \implies$ **Hyperbola**.
3. **$x^2 - 4y = 0$:** Rewrites as $x^2 = 4y \implies$ **Parabola**.
4. **$x^2 + y^2 + 1 = 0$:** Rewrites as $x^2 + y^2 = -1 \implies$ **No real points (Empty set)** because the sum of two real squares can never be negative.

**Explanation:** Examining coefficients and signs of quadratic terms determines the curve class and whether real solutions exist.

---

### Exercise 8. Sphere

## Question

Reduce

$$
x^2 + y^2 + z^2 - 4x + 2y - 6z - 2 = 0
$$

to canonical form. Give the center and radius. Give two points on the sphere and check them in the equation.

## Solution

**Step 1: Complete the square for $x, y, z$**

$$
(x^2 - 4x + 4) + (y^2 + 2y + 1) + (z^2 - 6z + 9) = 2 + 4 + 1 + 9
$$
$$
(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16
$$

**Step 2: Identify center and radius**

- **Center:** $(2, -1, 3)$
- **Radius:** $r = \sqrt{16} = 4$

**Step 3: Find and test two points**

- Point 1 (moving $r$ units along $x$): $(2 + 4, -1, 3) = (6, -1, 3)$.
  Check canonical: $(6 - 2)^2 + (-1 + 1)^2 + (3 - 3)^2 = 4^2 + 0 + 0 = 16$ (True).
- Point 2 (moving $r$ units along $y$): $(2, -1 + 4, 3) = (2, 3, 3)$.
  Check canonical: $(2 - 2)^2 + (3 + 1)^2 + (3 - 3)^2 = 0 + 4^2 + 0 = 16$ (True).

**Explanation:** Extending completing the square to three variables converts a general second-degree spherical equation into canonical distance form.

---

### Exercise 9. Ellipsoid and Its Cross-Sections

## Question

Consider

$$
\frac{x^2}{9} + \frac{y^2}{4} + \frac{z^2}{16} = 1.
$$

Give the semiaxis lengths, describe the cross-section $z = 0$, and explain how the cross-sections $z = c$ change for $|c| < 4$.

## Solution

**Step 1: Semiaxis lengths**

$a = 3$, $b = 2$, $c = 4$ (along the $x, y, z$ axes respectively).

**Step 2: Cross-section $z = 0$**

Substituting $z = 0$ yields:
$$
\frac{x^2}{9} + \frac{y^2}{4} = 1
$$
This is an **ellipse** in the $xy$-plane with semiaxes $3$ and $2$.

**Step 3: Cross-sections $z = c$ for $|c| < 4$**

Substituting $z = c$:
$$
\frac{x^2}{9} + \frac{y^2}{4} = 1 - \frac{c^2}{16}
$$
Dividing by $(1 - c^2/16)$ reveals an ellipse whose overall scale shrinks uniformly as $|c|$ increases toward $4$, reducing to a single point when $|c| = 4$.

**Explanation:** Analyzing parallel plane slices ($z = c$) reduces a 3D quadric surface into an intuitive family of 2D cross-sectional curves.

---

### Exercise 10. Paraboloids

## Question

Compare

$$
z = x^2 + y^2
$$

and

$$
z = x^2 - y^2.
$$

For each surface, describe the cross-sections $x = 0$, $y = 0$, and $z = c$, then make a qualitative sketch.

## Solution

**1. Elliptic Paraboloid ($z = x^2 + y^2$):**
- **$x = 0$:** $z = y^2$ (Parabola opening upwards).
- **$y = 0$:** $z = x^2$ (Parabola opening upwards).
- **$z = c$ ($c > 0$):** $x^2 + y^2 = c$ (Circles of radius $\sqrt{c}$).

**2. Hyperbolic Paraboloid ($z = x^2 - y^2$ - Saddle surface):**
- **$x = 0$:** $z = -y^2$ (Parabola opening downwards).
- **$y = 0$:** $z = x^2$ (Parabola opening upwards).
- **$z = c$ ($c \neq 0$):** $x^2 - y^2 = c$ (Hyperbolas).

**Explanation:** Changing signs between quadratic terms alters the cross-sectional geometry from nested circles (bowl shape) to intersecting hyperbolas (saddle shape).

---

## More Challenging Exercises

### Exercise 11. Two Similar Surfaces

## Question

Compare

$$
x^2 + y^2 - z^2 = 1
$$

and

$$
x^2 + y^2 - z^2 = -1.
$$

For several values $z = c$, check whether the cross-section exists and what its radius is. Based on this, describe qualitatively the difference between the surfaces and make sketches.

## Solution

**1. Hyperboloid of One Sheet ($x^2 + y^2 - z^2 = 1$):**
- Cross-section at $z = c$: $x^2 + y^2 = 1 + c^2$.
- **Behavior:** Exists for all real values of $c$. The cross-section is a circle whose radius reaches a minimum of $1$ at $z = 0$ and grows larger as $|c|$ increases.

**2. Hyperboloid of Two Sheets ($x^2 + y^2 - z^2 = -1$ or $z^2 - x^2 - y^2 = 1$):**
- Cross-section at $z = c$: $x^2 + y^2 = c^2 - 1$.
- **Behavior:** Exists only when $|c| \ge 1$. At $z = \pm 1$, the cross-section is a single point ($r = 0$), and for $|c| > 1$, it expands into circles. No cross-sections exist for $-1 < c < 1$.

**Explanation:** The constant term on the right side dictates whether the central neck is open continuously across the $xy$-plane (one sheet) or separated into two disjoint components along the $z$-axis (two sheets).

---

### Exercise 12. Recognizing a Surface from Cross-Sections

## Question

A certain surface has the following properties:
- the cross-section $z = 0$ is a point,
- for $z > 0$, the cross-sections $z = \text{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

## Solution

**Proposed Equation:**
$$
z = x^2 + y^2
$$

**Justification:**
- At $z = 0$, $x^2 + y^2 = 0$, which restricts the solution to the single origin point $(0, 0, 0)$.
- For any constant $z > 0$, $x^2 + y^2 = z$ represents circles with radius $\sqrt{z}$, which strictly increases as $z$ grows.
- Vertical cross-sections through the $Oz$ axis (such as setting $x = 0$) yield $z = y^2$, which are parabolas.

**Explanation:** Reversing the analytical pipeline matches geometric cross-sectional traits directly to canonical algebraic templates.

---

### Exercise 13. Intersection of a Sphere and a Plane

## Question

Given the sphere

$$
x^2 + y^2 + z^2 = 25
$$

and the plane $z = 3$, find the equation of the intersection curve and its radius. Then describe what happens for $z = c$ depending on $c$.

## Solution

**Step 1: Substitute $z = 3$ into the sphere equation**

$$
x^2 + y^2 + (3)^2 = 25 \implies x^2 + y^2 + 9 = 25 \implies x^2 + y^2 = 16
$$

**Step 2: Identify the intersection curve and radius**

The intersection curve is a **circle** lying in the plane $z = 3$ centered at $(0, 0, 3)$ with radius $r = \sqrt{16} = 4$.

**Step 3: Describe behavior for general $z = c$**

Substituting $z = c$ gives $x^2 + y^2 = 25 - c^2$:
- **If $|c| < 5$:** The intersection is a circle of radius $\sqrt{25 - c^2}$.
- **If $|c| = 5$:** The plane touches the sphere at a single point ($r = 0$).
- **If $|c| > 5$:** The plane does not intersect the sphere (empty set).

**Explanation:** Intersecting a sphere with parallel planes yields circles whose radii shrink symmetrically as the cutting plane moves away from the center.

---

### Exercise 14. Cone and Cylinder

## Question

Compare

$$
x^2 + y^2 = z^2
$$

and

$$
x^2 + y^2 = 4.
$$

For each surface, describe the cross-sections $z = c$, $x = 0$, and $y = 0$, make a sketch, and explain why the radius of the cross-section depends on $z$ in the first case but is constant in the second.

## Solution

**1. Circular Cone ($x^2 + y^2 = z^2$):**
- **$z = c$:** $x^2 + y^2 = c^2$ (Circles whose radius $|c|$ scales directly with height $z$).
- **$x = 0$:** $y^2 = z^2 \implies y = \pm z$ (Intersecting lines forming an $X$ shape).
- **$y = 0$:** $x = \pm z$ (Intersecting lines).

**2. Circular Cylinder ($x^2 + y^2 = 4$):**
- **$z = c$:** $x^2 + y^2 = 4$ (Circles of constant radius $2$ for all $z$).
- **$x = 0$:** $y^2 = 4 \implies y = \pm 2$ (Two parallel vertical lines).
- **$y = 0$:** $x = \pm 2$ (Two parallel vertical lines).

**Explanation:** The cone equation includes $z^2$, coupling horizontal spread directly to vertical elevation, whereas the cylinder equation lacks any $z$ dependence, maintaining uniform cross-sections infinitely along the $z$-axis.

---

### Exercise 15. Recognition and Sketch Without a Given Name

## Question

Consider the two equations:

$$
4x^2 + 9y^2 - 8x + 36y + 4 = 0,
$$

$$
4x^2 + y^2 = z^2.
$$

For the first equation, reduce it to canonical form, recognize the curve, give its most important features, and make a sketch.

For the second equation, do not begin by using a ready-made name for the surface. First describe the cross-sections $z = c$ and the cross-sections by the planes $x = 0$ and $y = 0$, paying attention to the different scales along the axes. Only then identify the surface and make a sketch.

## Solution

**Part 1: Analyzing $4x^2 + 9y^2 - 8x + 36y + 4 = 0$**

Group and complete the square:
$$
4(x^2 - 2x + 1) + 9(y^2 + 4y + 4) = -4 + 4(1) + 9(4)
$$
$$
4(x - 1)^2 + 9(y + 2)^2 = 36
$$
Divide by $36$:
$$
\frac{(x - 1)^2}{9} + \frac{(y + 2)^2}{4} = 1
$$
- **Curve Type:** Shifted Ellipse.
- **Features:** Center at $(1, -2)$, horizontal semiaxis $a = 3$, vertical semiaxis $b = 2$.

**Part 2: Analyzing $4x^2 + y^2 = z^2$**

- **Cross-sections $z = c$:** $4x^2 + y^2 = c^2 \implies \frac{x^2}{(c/2)^2} + \frac{y^2}{c^2} = 1$ (Ellipses whose axes scale proportionally with $|c|$).
- **Cross-sections $x = 0$:** $y^2 = z^2 \implies y = \pm z$ (Intersecting lines).
- **Cross-sections $y = 0$:** $4x^2 = z^2 \implies z = \pm 2x$ (Intersecting lines with steeper slopes due to the $4$ scaling factor).
- **Identification:** This is an **elliptic cone** aligned along the $z$-axis, featuring cross-sections that expand elliptically as $|z|$ increases.

**Explanation:** Reducing quadratic equations to canonical form uncovers shifted centers for conics, while systematic cross-sectional analysis exposes the true 3D geometry of quadric surfaces.
