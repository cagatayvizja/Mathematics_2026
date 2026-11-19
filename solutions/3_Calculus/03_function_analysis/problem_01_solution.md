# Function Analysis

## Problem 1. Cubic Graph Sketch with Critical Points and Monotonicity

## Question

Analyze the cubic function

$$f(x) = x^3 - 3x^2 + 2$$

by finding its derivative, determining the sign of the derivative and the intervals of increase and decrease, identifying its local extrema, and sketching the graph with the critical points $(0, 2)$ and $(2, -2)$ and the increasing/decreasing intervals clearly labelled.

## Solution

**Step 1: Derivative, critical points, and monotonicity**

Differentiating $f(x) = x^3 - 3x^2 + 2$ with respect to $x$ gives:

$$f'(x) = 3x^2 - 6x = 3x(x - 2).$$

Setting $f'(x) = 0$ yields the critical numbers $x = 0$ and $x = 2$. Evaluating $f(x)$ at these points gives the critical points:

$$f(0) = 0^3 - 3(0)^2 + 2 = 2 \implies (0, 2), \qquad f(2) = 2^3 - 3(2)^2 + 2 = -2 \implies (2, -2).$$

Examining the sign of $f'(x) = 3x(x - 2)$ across the intervals determined by $x = 0$ and $x = 2$:
- For $x \in (-\infty, 0)$, both $3x < 0$ and $x - 2 < 0$, so $f'(x) > 0$ and $f$ is **increasing** on $(-\infty, 0)$.
- For $x \in (0, 2)$, $3x > 0$ and $x - 2 < 0$, so $f'(x) < 0$ and $f$ is **decreasing** on $(0, 2)$.
- For $x \in (2, \infty)$, both $3x > 0$ and $x - 2 > 0$, so $f'(x) > 0$ and $f$ is **increasing** on $(2, \infty)$.

**Step 2: Local extrema**

Because $f'(x)$ changes sign from positive to negative at $x = 0$, $(0, 2)$ is a **local maximum**. Because $f'(x)$ changes sign from negative to positive at $x = 2$, $(2, -2)$ is a **local minimum**.

**Step 3: Labelled sketch of the cubic graph**

```text
   y
   ^
   |        [INC: (-inf, 0)]
   |            \
   |             * (0, 2)  <-- Local Maximum
   |              \
   |               \  [DEC: (0, 2)]
   |                \
---+-----------------\-----------------> x
   |                  \
   |                   \
   |                    * (2, -2) <-- Local Minimum
   |                     \
   |                      \  [INC: (2, +inf)]
   |                       \
```

**Explanation:** The sign of the first derivative $f'(x)$ governs where the tangent slope is positive (increasing) or negative (decreasing), turning points occur at $(0, 2)$ and $(2, -2)$, and the labelled sketch ties the algebraic derivative analysis directly to the shape of the cubic curve.
