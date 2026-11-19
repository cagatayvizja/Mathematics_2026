# Second-Degree Curves and Surfaces

## Goal of the Set

After completing this set, the student should be able to recognize the basic second-degree curves in the plane and the basic second-degree surfaces in space, read their most important features from equations, reduce simple equations to canonical form, and interpret geometric cross-sections.

---

## Basic Exercises

### Exercise 1. Recognizing Curves from Canonical Form

## Question

Recognize the curves

$$x^2+y^2=9,$$

$$\frac{x^2}{16}+\frac{y^2}{9}=1,$$

$$y^2=8x,$$

$$\frac{x^2}{9}-\frac{y^2}{4}=1.$$

For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

## Solution

**1. Circle:**

$$x^2 + y^2 = 9$$

- **Recognition Rule:** Both variables

$$x \quad \text{and} \quad y$$

are squared with equal positive coefficients

$$1$$

and equal a positive constant

$$r^2 = 9$$

- **Key Features:** Center

$$(0, 0)$$

radius

$$r = \sqrt{9} = 3$$

intercepts

$$(\pm 3, 0) \quad \text{and} \quad (0, \pm 3)$$

**Labelled Sketch:**

```text
          y ^
            |
         (0,3)
         . - * - .
      .      |      .
(-3,0)*------+------*(3,0) ---> x
      .    (0,0)    .
         . - * - .
         (0,-3)
```

**2. Ellipse:**

$$\frac{x^2}{16} + \frac{y^2}{9} = 1$$

- **Recognition Rule:** Sum of two squared terms with unequal positive denominators

$$a^2 = 16, \quad b^2 = 9$$

equal to

$$1$$

- **Key Features:** Center

$$(0, 0)$$

horizontal semiaxis

$$a = 4$$

vertical semiaxis

$$b = 3$$

vertices

$$(\pm 4, 0)$$

co-vertices

$$(0, \pm 3)$$

**Labelled Sketch:**

```text
            y ^
              |
           (0,3)
        .  -  *  -  .
     .        |        .
(-4,0)*-------+-------*(4,0) ---> x
     .      (0,0)      .
        .  -  *  -  .
           (0,-3)
```

**3. Parabola:**

$$y^2 = 8x$$

- **Recognition Rule:** Only one variable

$$y$$

is squared while the other

$$x$$

is linear.
- **Key Features:** Vertex

$$(0, 0)$$

axis of symmetry

$$y = 0$$

opens to the right since

$$4p = 8 \implies p = 2 > 0$$

focus

$$(2, 0)$$

reference points

$$(2, \pm 4)$$

**Labelled Sketch:**

```text
          y ^
            |       . (2,4)
            |    .
            |  .
  ----------+*(0,0)---*(2,0)---> x
            |  .     Focus
            |    .
            |       . (2,-4)
```

**4. Hyperbola:**

$$\frac{x^2}{9} - \frac{y^2}{4} = 1$$

- **Recognition Rule:** Difference of two squared terms equal to

$$1$$

with positive

$$x^2$$

term and negative

$$y^2$$

term.
- **Key Features:** Center

$$(0, 0)$$

opens horizontally, semiaxes

$$a = 3, \quad b = 2$$

vertices

$$(\pm 3, 0)$$

asymptotes

$$y = \pm \frac{2}{3}x$$

**Labelled Sketch:**

```text
       \        y ^        /  y = (2/3)x
        \         |       /
      .  \        |      /  .
       .  \       |     /  .
  ------*--+------+----+--*-------> x
    (-3,0) /    (0,0)   \ (3,0)
       .  /       |      \  .
      .  /        |       \  .
        /         |        \  y = -(2/3)x
```

**Explanation:** The powers of the variables, the signs connecting the squared terms, and the denominators uniquely determine the conic family, orientation, and scale.

---

### Exercise 2. Circle by Completing the Square

## Question

Reduce

$$x^2+y^2-6x+4y-3=0$$

to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

## Solution

**Step 1: Group terms and complete the square**

$$(x^2 - 6x) + (y^2 + 4y) = 3$$

Add

$$\left(\frac{-6}{2}\right)^2 = 9 \quad \text{and} \quad \left(\frac{4}{2}\right)^2 = 4$$

to both sides:

$$(x^2 - 6x + 9) + (y^2 + 4y + 4) = 3 + 9 + 4$$

$$(x - 3)^2 + (y + 2)^2 = 16$$

**Step 2: Identify center and radius**

- **Center:**

$$C = (3, -2)$$

- **Radius:**

$$r = \sqrt{16} = 4$$

**Step 3: Verify two points on the circle**

Choose two points at distance

$$r = 4$$

horizontally from the center:

$$P_1 = (7, -2) \quad \text{and} \quad P_2 = (-1, -2)$$

- **For**

$$P_1(7, -2)$$

Canonical form:

$$(7 - 3)^2 + (-2 + 2)^2 = 4^2 + 0 = 16$$

General form:

$$7^2 + (-2)^2 - 6(7) + 4(-2) - 3 = 49 + 4 - 42 - 8 - 3 = 0$$

- **For**

$$P_2(-1, -2)$$

Canonical form:

$$(-1 - 3)^2 + (-2 + 2)^2 = (-4)^2 + 0 = 16$$

General form:

$$(-1)^2 + (-2)^2 - 6(-1) + 4(-2) - 3 = 1 + 4 + 6 - 8 - 3 = 0$$

**Explanation:** Completing the square converts general expanded quadratic polynomials into shifted geometric coordinates, directly exposing the center and radius.

---

### Exercise 3. Ellipse

## Question

For

$$\frac{x^2}{25}+\frac{y^2}{9}=1,$$

find the semiaxis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

## Solution

**Step 1: Find semiaxis lengths**

- Horizontal semiaxis:

$$a = \sqrt{25} = 5$$

- Vertical semiaxis:

$$b = \sqrt{9} = 3$$

**Step 2: Find coordinate intercepts**

- Horizontal intercepts: Set

$$y = 0$$

$$\frac{x^2}{25} = 1 \implies x = \pm 5 \implies (\pm 5, 0)$$

- Vertical intercepts: Set

$$x = 0$$

$$\frac{y^2}{9} = 1 \implies y = \pm 3 \implies (0, \pm 3)$$

**Step 3: Labelled Sketch**

```text
             y ^
               |
            (0,3)
         .  -  *  -  .
      .        |        .
(-5,0)*--------+--------*(5,0) ---> x
      .      (0,0)      .
         .  -  *  -  .
            (0,-3)
```

**Explanation:** The ellipse is stretched more along the horizontal axis because the denominator under

$$x^2$$

which is

$$25$$

is larger than the denominator under

$$y^2$$

which is

$$9$$

giving a horizontal semiaxis of

$$5$$

versus a vertical semiaxis of

$$3$$

---

### Exercise 4. Parabola

## Question

For

$$y^2=12x,$$

identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for

$$x=3$$

and use them to make a sketch.

## Solution

**Step 1: Identify geometric features**

Comparing

$$y^2 = 12x$$

with the canonical form

$$y^2 = 4px$$

- **Vertex:**

$$(0, 0)$$

- **Axis of symmetry:**

$$y = 0$$

- **Opening direction:** Right, since

$$4p = 12 \implies p = 3 > 0$$

with focus at

$$(3, 0)$$

**Step 2: Find points for**

$$x = 3$$

$$y^2 = 12(3) = 36 \implies y = \pm 6$$

Reference points:

$$(3, 6) \quad \text{and} \quad (3, -6)$$

**Step 3: Labelled Sketch**

```text
          y ^
            |        * (3,6)
            |      .
            |    .
            |  .
  ----------+*(0,0)----
