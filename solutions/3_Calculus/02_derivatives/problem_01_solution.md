# Derivatives

## Goal of the Problem Set

The student should understand the derivative as a rate of change and the slope of a tangent line, and should be able to apply the basic differentiation rules: the sum rule, product rule, quotient rule, chain rule, and derivatives of trigonometric, exponential, and logarithmic functions.

---

## Basic Problems

### Problem 1. Derivative of a Polynomial and the Slope of a Tangent Line

## Question

For

$$f(x) = 3x^5 - 2x^3 + 7x - 4$$

find $f'(x)$. Then compute $f'(0)$ and $f'(1)$, determine the signs of the obtained values, and explain what they say about the slope of the tangent line to the graph at these two points.

## Solution

**Step 1: Compute $f'(x)$ using the power and sum rules**

$$f'(x) = 3(5x^4) - 2(3x^2) + 7(1) - 0 = 15x^4 - 6x^2 + 7$$

**Step 2: Evaluate at $x = 0$ and $x = 1$**

- For $x = 0$:
  $$f'(0) = 15(0)^4 - 6(0)^2 + 7 = 7$$
- For $x = 1$:
  $$f'(1) = 15(1)^4 - 6(1)^2 + 7 = 15 - 6 + 7 = 16$$

**Step 3: Analyze the signs and geometric meaning**

- Both $f'(0) = 7$ and $f'(1) = 16$ are **positive**.
- This indicates that the tangent lines to the graph at $x = 0$ and $x = 1$ are upward sloping (the function is strictly increasing at both points, rising faster at $x = 1$).

**Explanation:** The derivative evaluates the instantaneous rate of change and the exact geometric slope of the tangent line at any given point on the curve.

---

### Problem 2. Powers, Roots, and the Domain

## Question

For

$$f(x) = 2\sqrt{x} - \frac{3}{x^2} + x^{3/2}$$

1. rewrite the function using powers,
2. determine the domain,
3. compute the derivative,
4. compare the domain of the function with the domain of its derivative.

## Solution

**Step 1: Rewrite using rational and negative powers**

$$f(x) = 2x^{1/2} - 3x^{-2} + x^{3/2}$$

**Step 2: Determine the domain of $f(x)$**

Because of the square root term $x^{1/2}$ ($\sqrt{x}$), $x$ must be non-negative. Furthermore, the term $\frac{3}{x^2}$ implies $x \neq 0$. 
- **Domain of $f(x)$:** $(0, \infty)$ or $x > 0$.

**Step 3: Compute the derivative**

$$f'(x) = 2\left(\frac{1}{2}x^{-1/2}\right) - 3(-2x^{-3}) + \frac{3}{2}x^{1/2}$$
$$f'(x) = x^{-1/2} + 6x^{-3} + \frac{3}{2}x^{1/2} = \frac{1}{\sqrt{x}} + \frac{6}{x^3} + \frac{3}{2}\sqrt{x}$$

**Step 4: Compare domains**

- **Domain of $f'(x)$:** $x > 0$ (due to the presence of $\sqrt{x}$ in the denominator and numerator).
- **Comparison:** Both the original function and its derivative share the exact same domain $(0, \infty)$.

**Explanation:** Rewriting radical and rational terms into fractional and negative exponents allows direct application of the power rule while preserving strict domain boundaries.

---

### Problem 3. The Product Rule — Why Is It Needed?

## Question

For

$$f(x) = (x^2 + 1)e^x$$

compute the derivative. Then compare the correct result with the incorrect idea

$$f'(x) \stackrel{?}{=} (2x)e^x$$

and explain which term is missing.

## Solution

**Step 1: Apply the product rule $[u(x)v(x)]' = u'(x)v(x) + u(x)v'(x)$**

Let $u(x) = x^2 + 1$ and $v(x) = e^x$:
- $u'(x) = 2x$
- $v'(x) = e^x$

$$f'(x) = (2x)(e^x) + (x^2 + 1)(e^x) = (x^2 + 2x + 1)e^x = (x + 1)^2 e^x$$

**Step 2: Analyze the common mistake**

The incorrect expression $(2x)e^x$ only accounts for the derivative of the first factor times the second factor ($u'v$). The missing term is $uv'$, which accounts for the first factor times the derivative of the
