# Function Analysis

## Goal of the Problem Set

The student should be able to combine the domain, zeros, limits, derivatives, monotonicity, extrema, convexity, and asymptotes into one coherent description of a function and, on this basis, sketch its graph.

---

## Basic Problems

### Problem 1. A Cubic Polynomial

## Question

Analyze the monotonicity and extrema of

$$f(x) = x^3 - 3x^2 + 2.$$

Sketch the graph based on the results and mark the critical points.

## Solution

**Step 1: Compute the first derivative**

$$f'(x) = 3x^2 - 6x = 3x(x - 2)$$

**Step 2: Find critical points**

Set $f'(x) = 0$:
$$3x(x - 2) = 0 \implies x = 0 \text{ or } x = 2$$

**Step 3: Analyze monotonicity and extrema**

- **For $x < 0$:** Test $x = -1 \implies f'(-1) = 3(-1)(-1 - 2) = 9 > 0$ (Increasing).
- **For $0 < x < 2$:** Test $x = 1 \implies f'(1) = 3(1)(1 - 2) = -3 < 0$ (Decreasing).
- **For $x > 2$:** Test $x = 3 \implies f'(3) = 3(3)(3 - 2) = 9 > 0$ (Increasing).

**Extrema:**
- Local maximum at $x = 0$: $f(0) = 0^3 - 3(0)^2 + 2 = 2 \implies \text{Point: } (0, 2)$.
- Local minimum at $x = 2$: $f(2) = 2^3 - 3(2)^2 + 2 = 8 - 12 + 2 = -2 \implies \text{Point: } (2, -2)$.

**Explanation:** The first derivative test determines where the slope of the curve is positive (increasing) or negative (zero-crossings indicate local peaks and troughs).

---

### Problem 2. A Parabola from the Perspective of the Derivative

## Question

For $f(x) = x^2 - 4x + 1$, find the minimum using the derivative. Compare the result with the vertex form and explain why both approaches lead to the same point.

## Solution

**Step 1: Find the minimum using the derivative**

$$f'(x) = 2x - 4$$
Set $f'(x) = 0 \implies 2x - 4 = 0 \implies x = 2$.
Since $f''(x) = 2 > 0$, $x = 2$ is a global minimum.
Evaluate $f(2) = (2)^2 - 4(2) + 1 = 4 - 8 + 1 = -3$. Minimum point: $(2, -3)$.

**Step 2: Convert to vertex form by completing the square**

$$f(x) = (x^2 - 4x + 4) - 4 + 1 = (x - 2)^2 - 3$$
The vertex from this form is directly read as $(2, -3)$.

**Explanation:** Both approaches find the exact same point because setting the derivative to zero locates the horizontal tangent line at the vertex of the parabola.

---

### Problem 3. A Rational Function

## Question

Analyze the domain, zeros, asymptotes, and monotonicity of

$$f(x) = \frac{x + 1}{x - 2}.$$

Finally, sketch a graph consistent with all the information obtained.

## Solution

**Step 1: Domain and Zeros**
- **Domain:** Denominator cannot be zero $\implies x \neq 2$, so $(-\infty, 2) \cup (2, \infty)$.
- **Zeros:** Set numerator to zero $\implies x + 1 = 0 \implies x = -1$.

**Step 2: Asymptotes**
- **Vertical Asymptote:** $\lim_{x\to2^\pm} \frac{x+1}{x-2} = \pm\infty \implies x = 2$.
- **Horizontal Asymptote:** $\lim_{x\to\pm\infty} \frac{x+1}{x-2} = 1 \implies y = 1$.
