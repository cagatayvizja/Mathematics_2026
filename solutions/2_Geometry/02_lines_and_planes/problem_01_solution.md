# Lines and Planes

## Exercise 1. Line Through Two Points

## Question

Consider the line in the $xy$-plane passing through the two points $P(1, 2)$ and $Q(4, -1)$. Find the slope of the line, a direction vector, a normal vector, and the general equation of the line, and verify that both given points satisfy the resulting equation.

## Solution

**Step 1: Compute the slope of the line**

The slope $m$ of a non-vertical line passing through $P(x_1, y_1) = (1, 2)$ and $Q(x_2, y_2) = (4, -1)$ is the ratio of the vertical change to the horizontal change:

$$
m = \frac{y_2 - y_1}{x_2 - x_1} = \frac{-1 - 2}{4 - 1} = \frac{-3}{3} = -1.
$$

**Step 2: Determine a direction vector and a normal vector**

Subtracting the coordinates of $P$ from $Q$ produces a direction vector $\mathbf{v}$ parallel to the line:

$$
\mathbf{v} = \overrightarrow{PQ} = \begin{pmatrix} 4 - 1 \\ -1 - 2 \end{pmatrix} = \begin{pmatrix} 3 \\ -3 \end{pmatrix}.
$$

Dividing by $3$ gives the simplified direction vector $\mathbf{d} = (1, -1)$. In two dimensions, rotating a direction vector $(d_x, d_y)$ by $90^\circ$ produces a perpendicular normal vector $\mathbf{n} = (-d_y, d_x)$:

$$
\mathbf{n} = (1, 1).
$$

We verify orthogonality via the dot product:

$$
\mathbf{n} \cdot \mathbf{d} = 1(1) + 1(-1) = 1 - 1 = 0.
$$

**Step 3: Write the general equation of the line**

Using the normal vector $\mathbf{n} = (1, 1)$ and the point $P(1, 2)$ in the point-normal form $n_x(x - x_1) + n_y(y - y_1) = 0$ yields:

$$
1(x - 1) + 1(y - 2) = 0 \implies x + y - 3 = 0,
$$

or equivalently in standard form:

$$
x + y = 3.
$$

**Step 4: Verify that both given points lie on the line**

Substituting $P(1, 2)$ and $Q(4, -1)$ into the equation $x + y = 3$ confirms that both points satisfy the line:

$$
\text{For } P(1, 2): \quad 1 + 2 = 3,
$$

$$
\text{For } Q(4, -1): \quad 4 + (-1) = 3.
$$

**Explanation:** Because the vertical drop of $-3$ matches the horizontal run of $3$, the slope is $-1$, which corresponds to the simplified direction vector $(1, -1)$ and normal vector $(1, 1)$; substituting either point fixes the constant term so that $x + y = 3$ uniquely represents the line through $P$ and $Q$.
