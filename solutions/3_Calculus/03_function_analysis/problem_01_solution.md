# Function Analysis

## Problem 1. Cubic Graph Sketch with Critical Points and Monotonicity

## Question

Consider the cubic function defined by

$$f(x) = x^3 - 3x^2 + 2.$$

Determine the first derivative $f'(x)$, analyze its sign to find the intervals where $f$ is increasing and decreasing, identify all critical points and local extrema, and provide a labelled sketch of the graph showing the critical points $(0, 2)$ and $(2, -2)$ along with the increasing and decreasing intervals.

## Solution

**Step 1: Compute the first derivative and find the critical points**

To study the monotonicity and turning points of $f(x)$, we differentiate the polynomial term by term with respect to $x$:

$$f'(x) = \frac{d}{dx}(x^3 - 3x^2 + 2) = 3x^2 - 6x.$$

Factoring out $3x$ reveals the roots of the derivative immediately:

$$f'(x) = 3x(x - 2).$$

Setting $f'(x) = 0$ gives the critical numbers $x = 0$ and $x = 2$. Substituting these values back into the original function $f(x) = x^3 - 3x^2 + 2$ yields the coordinates of the two critical points:

$$f(0) = 0^3 - 3(0)^2 + 2 = 2 \implies (0, 2),$$

$$f(2) = 2^3 - 3(2)^2 + 2 = 8 - 12 + 2 = -2 \implies (2, -2).$$

**Step 2: Analyze the sign of $f'(x)$ and determine monotonicity and extrema**

The critical numbers $x = 0$ and $x = 2$ partition the real line into three open intervals: $(-\infty, 0)$, $(0, 2)$, and $(2, \infty)$. Testing the sign of $f'(x) = 3x(x - 2)$ on each interval determines where the function rises or falls:

- On $(-\infty, 0)$, both $3x < 0$ and $x - 2 < 0$, so their product is positive:

$$f'(x) > 0 \quad \text{for } x \in (-\infty, 0) \implies f \text{ is increasing on } (-\infty, 0).$$

- On $(0, 2)$, we have $3x > 0$ and $x - 2 < 0$, so their product is negative:

$$f'(x) < 0 \quad \text{for } x \in (0, 2) \implies f \text{ is decreasing on } (0, 2).$$

- On $(2, \infty)$, both $3x > 0$ and $x - 2 > 0$, so their product is positive:

$$f'(x) > 0 \quad \text{for } x \in (2, \infty) \implies f \text{ is increasing on } (2, \infty).$$

By the First Derivative Test, $f'(x)$ changes sign from positive to negative at $x = 0$, so $(0, 2)$ is a **local maximum**. Conversely, $f'(x)$ changes sign from negative to positive at $x = 2$, so $(2, -2)$ is a **local minimum**.

**Step 3: Labelled sketch of the cubic graph**

Combining the behavior as $x \to -\infty$ ($f(x) \to -\infty$), the local maximum at $(0, 2)$, the local minimum at $(2, -2)$, and the behavior as $x \to +\infty$ ($f(x) \to +\infty$) produces the following labelled sketch:

```text
      y
      ^
      |               * (0, 2)  [Local Maximum]
      |              / \
      |             /   \
      |  Increasing/     \ Decreasing
      |  (-inf,
