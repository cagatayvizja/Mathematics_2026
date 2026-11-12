# Integrals

## Goal of the Problem Set

The student should understand the indefinite integral as a family of antiderivatives, the definite integral as a tool for summation and area, and should be able to apply the basic techniques: direct integration, simple substitution, and integration by parts.

---

## Basic Problems

### Problem 1. Antiderivative and Verification

## Question

For

$$
f(x) = 3x^2 - 4x + 5
$$

find one antiderivative $F(x)$. Write the entire family of antiderivatives, verify the result by differentiation, and explain the meaning of the constant $C$.

## Solution

**Step 1: Find one antiderivative $F(x)$**

Using the reverse power rule on each term:
$$
F(x) = 3\left(\frac{x^3}{3}\right) - 4\left(\frac{x^2}{2}\right) + 5x = x^3 - 2x^2 + 5x
$$

**Step 2: Write the entire family of antiderivatives**

$$
\int (3x^2 - 4x + 5) \, dx = x^3 - 2x^2 + 5x + C, \quad C \in \mathbb{R}
$$

**Step 3: Verify by differentiation**

$$
\frac{d}{dx}\left[x^3 - 2x^2 + 5x + C\right] = 3x^2 - 4x + 5 + 0 = 3x^2 - 4x + 5 = f(x)
$$

**Explanation:** The constant $C$ represents the vertical shift ambiguity of antiderivatives; because the derivative of any constant is zero, infinitely many valid antiderivatives exist, all sharing identical slopes at any given $x$.

---

### Problem 2. Powers, Roots, and the Domain

## Question

Compute

$$
\int \left(2\sqrt{x} + \frac{3}{x^2} - x^{1/3}\right) \, dx.
$$

First rewrite the terms as powers, determine the domain of the original expression, and verify the result by differentiation.

## Solution

**Step 1: Rewrite terms as powers**

$$
\int \left(2x^{1/2} + 3x^{-2} - x^{1/3}\right) \, dx
$$

**Step 2: Determine the domain**

Due to the square root term ($\sqrt{x}$), $x$ must be non-negative, and the term $\frac{3}{x^2}$ implies $x \neq 0$. 
- **Domain:** $(0, \infty)$ or $x > 0$.

**Step 3: Compute the antiderivative**

$$
= 2\left(\frac{x^{3/2}}{3/2}\right) + 3\left(\frac{x^{-1}}{-1}\right) - \left(\frac{x^{4/3}}{4/3}\right) + C = \frac{4}{3}x^{3/2} - 3x^{-1} - \frac{3}{4}x^{4/3} + C
$$
$$
= \frac{4}{3}x\sqrt{x} - \frac{3}{x} - \frac{3}{4}\sqrt[3]{x^4} + C
$$

**Step 4: Verify by differentiation**

$$
\frac{d}{dx}\left[\frac{4}{3}x^{3/2} - 3x^{-1} - \frac{3}{4}x^{4/3} + C\right] = \frac{4}{3}\left(\frac{3}{2}x^{1/2}\right) - 3(-x^{-2}) - \frac{3}{4}\left(\frac{4}{3}x^{1/3}\right) = 2x^{1/2} + 3x^{-2} - x^{1/3}
$$

**Explanation:** Rewriting radical and rational fractions into exponential power form allows direct integration via the power rule.

---

### Problem 3. Recognizing Basic Antiderivatives

## Question

Compute

$$
\int \left(2e^x + 3\cos x - 4\sin x\right) \, dx.
$$

Match each term with a known derivative and verify the entire result with one differentiation.

## Solution

**Step 1: Integrate term-by-term**
- $\int 2e^x \, dx = 2e^x$ (since $\frac{d}{dx}[e^x] = e^x$)
- $\int 3\cos x \, dx = 3\sin x$ (since $\frac{d}{dx}[\sin x] = \cos x$)
- $\int -4\sin x \, dx = 4\cos x$ (since $\frac{d}{dx}[\cos x] = -\sin x$)

Combined result:
$$
2e^x + 3\sin x + 4\cos x + C
$$

**Step 2: Verify by differentiation**

$$
\frac{d}{dx}\left[2e^x + 3\sin x + 4\cos x + C\right] = 2e^x + 3\cos x - 4\sin x
$$

**Explanation:** Basic antiderivatives are found directly by reversing standard differentiation formulas for exponential and trigonometric functions.

---

### Problem 4. Substitution as Reversing the Chain Rule

## Question

Compute

$$
\int 2x(x^2 + 1)^4 \, dx.
$$

Before calculating, identify a candidate for the new variable $u$ and show that its derivative appears in the integral. Finally, verify the result by differentiation.

## Solution

**Step 1: Identify substitution candidate**

Let $u = x^2 + 1$. Its derivative is $du = 2x \, dx$, which matches the external factor in the integrand.

**Step 2: Rewrite and integrate**

$$
\int (x^2 + 1)^4 \cdot (2x \, dx) = \int u^4 \, du = \frac{u^5}{5} + C
$$

**Step 3: Substitute back in terms of $x$**

$$
\frac{1}{5}(x^2 + 1)^5 + C
$$

**Step 4: Verify by differentiation (using chain rule)**

$$
\frac{d}{dx}\left[\frac{1}{5}(x^2 + 1)^5 + C\right] = \frac{1}{5} \cdot 5(x^2 + 1)^4 \cdot (2x) = 2x(x^2 + 1)^4
$$

**Explanation:** Substitution systematically undoes the chain rule by replacing a composite inner function with a single variable $u$ when its derivative factor is present.

---

### Problem 5. The Same Substitution in a Different Context

## Question

Compute

$$
\int x e^{x^2} \, dx.
$$

First compare the structure with Problem 4 and explain what is common despite the different appearance of the function.

## Solution

**Step 1: Apply substitution**

Let $u = x^2 \implies du = 2x \, dx \implies x \, dx = \frac{1}{2} \, du$.

**Step 2: Integrate**

$$
\int e^{x^2} \cdot (x \, dx) = \int e^u \cdot \frac{1}{2} \, du = \frac{1}{2} \int e^u \, du = \frac{1}{2}e^u + C = \frac{1}{2}e^{x^2} + C
$$

**Explanation:** Structurally, both integrals contain an inner composite function ($x^2 + 1$ and $x^2$) paired alongside a constant multiple of its derivative ($2x$ and $x$), proving that substitution relies on structural alignment rather than function type.

---

### Problem 6. When Does a Logarithm Appear from an Integral?

## Question

Compute

$$
\int \frac{2x}{x^2 + 5} \, dx.
$$

Identify the denominator as a candidate for substitution, compare the numerator with its derivative, and explain the source of the logarithm in the result.

## Solution

**Step 1: Choose substitution**

Let $u = x^2 + 5 \implies du = 2x \, dx$.

**Step 2: Rewrite and integrate**

$$
\int \frac{1}{x^2 + 5} \cdot (2x \, dx) = \int \frac{1}{u} \, du = \ln|u| + C = \ln|x^2 + 5| + C
$$

**Explanation:** A natural logarithm arises whenever the numerator of a rational expression yields the exact derivative of the denominator, matching the standard rule $\int \frac{u'}{u} \, du = \ln|u| + C$.

---

### Problem 7. Integration by Parts as Reversing the Product Rule

## Question

Compute

$$
\int x e^x \, dx.
$$

First write the product differentiation rule and, on that basis, explain the meaning of the integration-by-parts formula. Verify the result by differentiation.

## Solution

**Step 1: Set up integration by parts**

Using the formula $\int u \, dv = uv - \int v \, du$:
- Let $u = x \implies du = dx$
- Let $dv = e^x \, dx \implies v = e^x$

$$
\int x e^x \, dx = x e^x - \int e^x \, dx = x e^x - e^x + C = (x - 1)e^x + C
$$

**Step 2: Verify by differentiation (product rule)**

$$
\frac{d}{dx}\left[(x - 1)e^x + C\right] = (1)e^x + (x - 1)(e^x) = e^x + xe^x - e^x = xe^x
$$

**Explanation:** Integration by parts directly reverses the product differentiation rule, transforming a difficult integral into a simpler one by shifting derivatives.

---

### Problem 8. Choosing the Factors in Integration by Parts

## Question

Compute

$$
\int x \cos x \, dx.
$$

Before calculating, justify why it is convenient to differentiate $x$ and integrate $\cos x$, rather than the other way around.

## Solution

**Step 1: Choose factors**

- Let $u = x \implies du = dx$ (differentiating $x$ simplifies it to a constant $1$).
- Let $dv = \cos x \, dx \implies v = \sin x$.

**Step 2: Apply integration by parts formula**

$$
\int x \cos x \, dx = x \sin x - \int \sin x \, dx = x \sin x - (-\cos x) + C = x \sin x + \cos x + C
$$

**Explanation:** Choosing $u = x$ simplifies the resulting integral because its derivative is $1$, eliminating the linear term $x$. Reversing this choice would escalate $x$ into $x^2/2$, complicating the integral further.

---

### Problem 9. Definite Integral and Geometric Area

## Question

Compute

$$
\int_{-1}^{2} x \, dx.
$$

Then separately compute the areas of the parts of the graph below and above the $x$-axis and explain the difference between the definite integral and geometric area.

## Solution

**Step 1: Compute definite integral**

$$
\int_{-1}^{2} x \, dx = \left[ \frac{x^2}{2} \right]_{-1}^{2} = \frac{2^2}{2} - \frac{(-1)^2}{2} = 2 - \frac{1}{2} = \frac{3}{2}
$$

**Step 2: Geometric area analysis**
- Below $x$-axis (interval $[-1, 0]$): Forms a triangle with base $1$ and height $1$. Area = $\frac{1}{2}(1)(1) = 0.5$, counted as **negative** ($\text{Area}_1 = -0.5$).
- Above $x$-axis (interval $[0, 2]$): Forms a triangle with base $2$ and height $2$. Area = $\frac{1}{2}(2)(2) = 2$, counted as **positive** ($\text{Area}_2 = 2$).
- Net definite integral = $-0.5 + 2 = 1.5$ ($3/2$).

**Explanation:** Definite integrals calculate **signed accumulation** (areas above the axis minus areas below), whereas geometric area represents total physical space and is always non-negative.

---

### Problem 10. Definite Integral and Checking the Result

## Question

Before carrying out the exact calculation, estimate the possible range of values of the integral

$$
\int_0^2 (x^2 + 1) \, dx,
$$

using $1 \le x^2 + 1 \le 5$ on $[0, 2]$. Only then compute the integral exactly, compare the result with the earlier estimate, and explain what type of computational error such a check can detect.

## Solution

**Step 1: Estimate bounds using bounding inequality**

The interval length is $2 - 0 = 2$.
- Minimum estimate: $\text{Min value} \times \text{length} = 1 \cdot 2 = 2$
- Maximum estimate: $\text{Max value} \times \text{length} = 5 \cdot 2 = 10$
- Estimated range: $2 \le \int_0^2 (x^2 + 1) \, dx \le 10$.

**Step 2: Compute the exact integral**

$$
\int_0^2 (x^2 + 1) \, dx = \left[ \frac{x^3}{3} + x \right]_0^2 = \left(\frac{8}{3} + 2\right) - (0 + 0) = \frac{14}{3} \approx 4.67
$$

**Step 3: Comparison**

The exact value ($4.67$) falls cleanly inside the estimated bounds $[2, 10]$.

**Explanation:** Bounding checks help detect gross arithmetic errors, misplaced decimal points, or incorrect sign reversals that push answers outside logical geometric bounds.

---

## More Difficult Problems

### Problem 11. Choose the Method First

## Question

For each integral, first write which method you choose and how you recognize it, and then compute:
1. $\int \sin(3x) \, dx$,
2. $\int x \ln x \, dx$,
3. $\int \frac{x}{\sqrt{x^2 + 1}} \, dx$.

## Solution

**1. First integral: $\int \sin(3x) \, dx$**
- **Method:** Direct integration with linear substitution. Recognized by a linear inner function inside a standard trigonometric template.
- **Computation:** $-\frac{1}{3}\cos(3x) + C$.

**2. Second integral: $\int x \ln x \, dx$**
- **Method:** Integration by parts. Recognized by a product of dissimilar functions where logarithmic terms simplify upon differentiation.
- **Computation:** Let $u = \ln x \implies du = \frac{1}{x} \, dx$ and $dv = x \, dx \implies v = \frac{x^2}{2}$.
  $$
  \frac{x^2}{2}\ln x - \int \frac{x^2}{2} \cdot \frac{1}{x} \, dx = \frac{x^2}{2}\ln x - \frac{x^2}{4} + C
  $$

**3. Third integral: $\int \frac{x}{\sqrt{x^2 + 1}} \, dx$**
- **Method:** Substitution. Recognized because the numerator ($x$) is a constant multiple of the derivative of the inner radicand expression ($x^2 + 1$).
- **Computation:** Let $u = x^2 + 1 \implies du = 2x \, dx$.
  $$
  \frac{1}{2}\int u^{-1/2} \, du = \frac{1}{2}\left(2u^{1/2}\right) + C = \sqrt{x^2 + 1} + C
  $$

---

### Problem 12. Symmetry, Sign, and Absolute Value

## Question

Compare

$$
\int_{-2}^{2} x \, dx \quad \text{and} \quad \int_{-2}^{2} |x| \, dx.
$$

Before calculating, predict the results from symmetry and a sketch, then carry out the calculation and explain the difference.

## Solution

**Step 1: Predictions via symmetry**
- For $\int_{-2}^{2} x \, dx$: The integrand $f(x) = x$ is an **odd function** ($f(-x) = -f(x)$) integrated over a symmetric interval $[-2, 2]$, predicting a net result of **$0$**.
- For $\int_{-2}^{2} |x| \, dx$: The integrand $f(x) = |x|$ is an **even function** ($f(-x) = f(x)$) representing two identical triangular areas above the axis, predicting a positive doubled value.

**Step 2: Calculations**
- Integral 1: $\left[ \frac{x^2}{2} \right]_{-2}^{2} = \frac{4}{2} - \frac{4}{2} = 0$.
- Integral 2: Split at $x = 0$:
  $$
  \int_{-2}^{0} (-x) \, dx + \int_{0}^{2} x \, dx = \left[ -\frac{x^2}{2} \right]_{-2}^{0} + \left[ \frac{x^2}{2} \right]_{0}^{2} = (0 - (-2)) + (2 - 0) = 2 + 2 = 4
  $$

**Explanation:** Odd integrands cancel out symmetrically across zero, whereas absolute value functions convert negative lobes into positive contributions, accumulating total area.

---

### Problem 13. An Integral Depending on the Upper Limit

## Question

Let

$$
F(x) = \int_0^x (t^2 + 1) \, dt.
$$

Determine $F(x)$, compute $F'(x)$, and compare the result with the integrand. Explain in your own words why the height of the function describes the local rate of increase of the accumulated area.

## Solution

**Step 1: Determine $F(x)$**

$$
F(x) = \left[ \frac{t^3}{3} + t \right]_0^x = \frac{x^3}{3} + x
$$

**Step 2: Compute $F'(x)$**

$$
F'(x) = \frac{d}{dx}\left[\frac{x^3}{3} + x\right] = x^2 + 1
$$

**Step 3: Comparison**

$F'(x)$ matches the original integrand $t^2 + 1$ (with $t$ replaced by $x$), demonstrating the Fundamental Theorem of Calculus.

**Explanation:** The local rate of area accumulation depends directly on the current height ($t^2 + 1$) of the bounding curve at the moving boundary $x$.

---

### Problem 14. A Piecewise-Defined Function

## Question

Let

$$
f(x) = \begin{cases} x + 1, & -1 \le x < 1, \\ 2, & 1 \le x \le 3. \end{cases}
$$

Sketch the graph, decide where to split the integral, compute

$$
\int_{-1}^{3} f(x) \, dx
$$

and verify the result geometrically.

## Solution

**Step 1: Split the integral at the boundary $x = 1$**

$$
\int_{-1}^{3} f(x) \, dx = \int_{-1}^{1} (x + 1) \, dx + \int_{1}^{3} 2 \, dx
$$

**Step 2: Evaluate each part**
- First part:
  $$
  \int_{-1}^{1} (x + 1) \, dx = \left[ \frac{x^2}{2} + x \right]_{-1}^{1} = \left(\frac{1}{2} + 1\right) - \left(\frac{1}{2} - 1\right) = \frac{3}{2} - \left(-\frac{1}{2}\right) = 2
  $$
- Second part:
  $$
  \int_{1}^{3} 2 \, dx = \left[ 2x \right]_{1}^{3} = 6 - 2 = 4
  $$
- Total integral = $2 + 4 = 6$.

**Step 3: Geometric verification**
- From $x = -1$ to $1$, the shape is a trapezoid with base lengths $0$ and $2$, height $2$. Area = $\frac{0+2}{2} \cdot 2 = 2$.
- From $x = 1$ to $3$, the shape is a rectangle with width $2$ and height $2$. Area = $2 \cdot 2 = 4$.
- Total geometric area = $2 + 4 = 6$ (Verified).

**Explanation:** Piecewise functions require splitting the domain of integration into sub-intervals where individual algebraic definitions apply continuously.

---

### Problem 15. Recovering a Function from Its Derivative and a Condition

## Question

The function $F$ satisfies

$$
F'(x) = 2x e^{x^2}
$$

and

$$
F(0) = 3.
$$

1. Recognize the method needed to find the function $F$.
2. Determine the entire family of functions with the given derivative.
3. Use the condition $F(0) = 3$ to determine the correct constant.
4. Verify the final result by differentiation and substitution of $x = 0$.

## Solution

**Step 1: Recognize method**

Recognized as reversing the chain rule via **substitution**, matching Problem 5.

**Step 2: Determine the family of antiderivatives**

$$
F(x) = \int 2x e^{x^2} \, dx = e^{x^2} + C
$$

**Step 3: Use initial condition $F(0) = 3$ to solve for $C$**

$$
F(0) = e^{0^2} + C = 3 \implies 1 + C = 3 \implies C = 2
$$
Unique function: $F(x) = e^{x^2} + 2$.

**Step 4: Verify result**
- **Differentiation:** $\frac{d}{dx}[e^{x^2} + 2] = e^{x^2}(2x) + 0 = 2x e^{x^2}$ (Matches $F'(x)$).
- **Initial condition substitution:** $F(0) = e^{0} + 2 = 1 + 2 = 3$ (Matches condition).

**Explanation:** Initial conditions provide the specific anchor value required to resolve the integration constant $C$ from a general family of antiderivatives.
