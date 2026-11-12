# Applications of Differential and Integral Calculus

## Goal of the Problem Set

This problem set is cross-sectional in nature and is intentionally shorter than the others. The student should be able to choose variables from a problem description, build a model, decide whether a derivative, an integral, or both tools are needed, and then interpret the result in the context of the problem.

---

## Basic Problems

### Problem 1. Motion — from Position to Velocity

## Question

The position of a point is described by

$$s(t) = t^3 - 6t^2 + 9t + 2, \qquad t \ge 0.$$

1. Determine the velocity and acceleration.
2. Find the times at which the point stops.
3. Determine on which intervals the point moves in the positive direction of the axis and on which intervals it moves in the negative direction.

## Solution

**Step 1: Determine velocity $v(t)$ and acceleration $a(t)$**

- Velocity is the first derivative of position with respect to time:
  $$v(t) = s'(t) = \frac{d}{dt}\left(t^3 - 6t^2 + 9t + 2\right) = 3t^2 - 12t + 9$$
- Acceleration is the second derivative of position (or first derivative of velocity):
  $$a(t) = v'(t) = \frac{d}{dt}\left(3t^2 - 12t + 9\right) = 6t - 12$$

**Step 2: Find the times at which the point stops**

The point stops when its velocity is zero ($v(t) = 0$):
$$3t^2 - 12t + 9 = 0 \implies t^2 - 4t + 3 = 0 \implies (t - 1)(t - 3) = 0$$
Thus, the point stops at **$t = 1$** and **$t = 3$**.

**Step 3: Determine movement intervals**

- **Positive direction ($v(t) > 0$):** $3(t - 1)(t - 3) > 0 \implies t \in [0, 1) \cup (3, \infty)$.
- **Negative direction ($v(t) < 0$):** $3(t - 1)(t - 3) < 0 \implies t \in (1, 3)$.

**Explanation:** The sign of the velocity derivative directly indicates the directional heading along the coordinate axis, while zeros mark instantaneous resting points.

---

### Problem 2. Maximum Area of a Rectangle

## Question

A rectangle has perimeter $40$.
1. Write its area as a function of the length of one side.
2. Determine the domain of this function resulting from the geometry of the problem.
3. Find the dimensions that give the maximum area.
4. Justify that the point found actually gives a maximum.

## Solution

**Step 1: Express area as a function of one side**

Let the sides be $x$ and $y$. The perimeter is $2x + 2y = 40 \implies x + y = 20 \implies y = 20 - x$.
Area function:
$$A(x) = x(20 - x) = 20x - x^2$$

**Step 2: Determine the domain**

Sides must be strictly positive:
- $x > 0$
- $20 - x > 0 \implies x < 20$
- **Domain:** $(0, 20)$.

**Step 3: Find dimensions for maximum area**

Compute the first derivative and set it to zero:
$$A'(x) = 20 - 2x = 0 \implies x = 10$$
When $x = 10$, $y = 20 - 10 = 10$. The dimensions are $10 \times 10$ (a square).

**Step 4: Justify the maximum**

The second derivative is $A''(x) = -2 < 0$, which confirms by the second derivative test that the critical point at $x = 10$ is a **global maximum**.

**Explanation:** Optimization models combine geometric constraints with derivative tests to isolate extreme performance points.

---

### Problem 3. A Box Made from Cardboard

## Question

From a $30\,\mathrm{cm} \times 40\,\mathrm{cm}$ sheet, squares of side length $x$ are cut from the corners and the edges are folded up to form an open box. Write the volume as a function of $x$, determine the physically meaningful domain, and find the value of $x$ for which the volume is greatest.

## Solution

**Step 1: Write volume as a function of $x$**

After cutting squares of side $x$ from each corner, the dimensions of the open box are:
- Height = $x$
- Width = $30 - 2x$
- Length = $40 - 2x$

Volume function:
$$V(x) = x(30 - 2x)(40 - 2x) = x(1200 - 60x - 80x + 4x^2) = 4x^3 - 140x^2 + 1200x$$

**Step 2: Determine the domain**

All dimensions must be positive:
- $x > 0$
- $30 - 2x > 0 \implies x < 15$
- $40 - 2x > 0 \implies x < 20$
- **Domain:** $(0, 15)$.

**Step 3: Find maximum volume**

Compute derivative:
$$V'(x) = 12x^2 - 280x + 1200$$
Set $V'(x) = 0$ and simplify by $4$:
$$3x^2 - 70x + 300 = 0$$
Using the quadratic formula:
$$x = \frac{70 \pm \sqrt{(-70)^2 - 4(3)(300)}}{2(3)} = \frac{70 \pm \sqrt{4900 - 3600}}{6} = \frac{70 \pm \sqrt{1300}}{6} = \frac{70 \pm 10\sqrt{13}}{6} \approx \frac{70 \pm 36.055}{6}$$
- $x_1 \approx \frac{106.055}{6} \approx 17.67$ (outside domain)
- $x_2 \approx \frac{33.945}{6} \approx 5.66\,\mathrm{cm}$ (valid)

**Explanation:** Cutting corners of optimal size $x \approx 5.66\,\mathrm{cm}$ maximizes internal folding capacity.

---

### Problem 4. Area Between Curves

## Question

Find the area of the region bounded by the graphs $y = x$ and $y = x^2$. First find the intersection points and justify which function is greater on the relevant interval.

## Solution

**Step 1: Find intersection points**

Set $x = x^2 \implies x^2 - x = 0 \implies x(x - 1) = 0$.
Intersections occur at $x = 0$ and $x = 1$.

**Step 2: Justify upper and lower functions**

On the interval $[0, 1]$, testing $x = 0.5$:
- Line value: $0.5$
- Parabola value: $(0.5)^2 = 0.25$
Since $0.5 > 0.25$, the linear function $y = x$ is greater than $y = x^2$ throughout $(0, 1)$.

**Step 3: Compute the area via integration**

$$\text{Area} = \int_{0}^{1} (x - x^2) \, dx = \left[ \frac{x^2}{2} - \frac{x^3}{3} \right]_{0}^{1} = \left(\frac{1}{2} - \frac{1}{3}\right) - 0 = \frac{1}{6}$$

**Explanation:** Integrating the difference between upper and lower bounding curves yields the enclosed geometric area.

---

### Problem 5. Distance from Velocity

## Question

The velocity of a car during the first five seconds is described by the function $v(t) = 4t + 2\,[\mathrm{m/s}]$. Compute the distance traveled and explain why the integral of velocity gives the change in position. Then answer what would have to be changed in the reasoning if the velocity also took negative values.

## Solution

**Step 1: Compute distance traveled**

Since $v(t) > 0$ for all $t \in [0, 5]$, the displacement equals the total distance traveled:
$$\text{Distance} = \int_{0}^{5} (4t + 2) \, dt = \left[ 2t^2 + 2t \right]_{0}^{5} = (2(25) + 2(5)) - 0 = 50 + 10 = 60\,\mathrm{meters}$$

**Explanation:** The integral of velocity yields position change because integration accumulates instantaneous rates of change over time. If velocity became negative, we would need to integrate the absolute value of velocity ($\vert{}v(t)\vert{}$) to capture total physical distance traveled rather than net displacement.

---

### Problem 6. Average Value of a Function

## Question

Compute the average value of the function $f(x) = x^2$ on the interval $[0, 3]$. Find a point $c \in [0, 3]$ for which $f(c)$ is equal to this average value, and interpret the result geometrically.

## Solution

**Step 1: Compute the average value**

$$f_{\text{avg}} = \frac{1}{3 - 0} \int_{0}^{3} x^2 \, dx = \frac{1}{3} \left[ \frac{x^3}{3} \right]_{0}^{3} = \frac{1}{3} \left( \frac{27}{3} - 0 \right) = \frac{9}{3} = 3$$

**Step 2: Find point $c$**

Set $f(c) = 3 \implies c^2 = 3 \implies c = \sqrt{3}$ (since $\sqrt{3} \in [0, 3]$).

**Explanation:** Geometrically, the rectangle formed by the interval length and the average height ($3 \times 3 = 9$) has an area exactly matching the integral accumulation under the parabola $y = x^2$ from $0$ to $3$.

---

### Problem 7. Exponential Growth

## Question

Assume the model $N(t) = N_0 e^{kt}$, ($k > 0$).
1. Verify by differentiation that the model satisfies the relation $N'(t) = kN(t)$.
2. Find the population doubling time.
3. Explain why the doubling time does not depend on $N_0$.

## Solution

**Step 1: Verify differential relation**

$$N'(t) = \frac{d}{dt}\left[N_0 e^{kt}\right] = N_0 \cdot k e^{kt} = k(N_0 e^{kt}) = kN(t) \quad (\text{Verified})$$

**Step 2: Find doubling time $T$**

Set $N(T) = 2N_0$:
$$N_0 e^{kT} = 2N_0 \implies e^{kT} = 2 \implies kT = \ln 2 \implies T = \frac{\ln 2}{k}$$

**Explanation:** $N_0$ cancels out algebraically during the exponential equation reduction, proving that doubling time depends strictly on the relative growth rate $k$.

---

### Problem 8. Number of Requests Handled by a Server

## Question

The rate at which requests arrive at a server during the first 5 minutes is described by the function $r(t) = 100 + 20t\,[\mathrm{requests/min}]$, ($0 \le t \le 5$).
1. Compute the total number of requests that arrived during this time.
2. Compute the average rate of incoming requests over this interval.
3. Compare the average rate with the values $r(0)$ and $r(5)$.

## Solution

**Step 1: Compute total requests**

$$\text{Total} = \int_{0}^{5} (100 + 20t) \, dt = \left[ 100t + 10t^2 \right]_{0}^{5} = (100(5) + 10(25)) - 0 = 500 + 250 = 750\,\mathrm{requests}$$

**Step 2: Compute average rate**

$$\text{Average Rate} = \frac{750}{5 - 0} = 150\,\mathrm{requests/min}$$

**Step 3: Comparison**
- Initial rate $r(0) = 100$- Final rate$r(5) = 100 + 20(5) =
