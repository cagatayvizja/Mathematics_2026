# Limits of Sequences and Functions

## Goal of the Set

After completing this set, the student should understand the common idea of a limit: studying the behavior of an object as its argument approaches a specified value or grows without bound. We first practice limits of sequences and then move to limits of functions, one-sided limits, and continuity.

---

## Basic Exercises

### Exercise 1. Dominant Terms in a Sequence

## Question

Compute

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.
$$

Explain why the highest-degree terms determine the result.

## Solution

**Step 1: Divide numerator and denominator by the highest power of $n$ ($n^2$)**

$$
\lim_{n\to\infty}\frac{\frac{4n^2}{n^2} - \frac{3n}{n^2} + \frac{1}{n^2}}{\frac{2n^2}{n^2} + \frac{5n}{n^2} - \frac{7}{n^2}} = \lim_{n\to\infty}\frac{4 - \frac{3}{n} + \frac{1}{n^2}}{2 + \frac{5}{n} - \frac{7}{n^2}}
$$

**Step 2: Evaluate the limit as $n \to \infty$**

As $n$ grows without bound, terms containing $n$ in the denominator approach zero:
- $\lim_{n\to\infty}\frac{3}{n} = 0$, $\lim_{n\to\infty}\frac{1}{n^2} = 0$
- $\lim_{n\to\infty}\frac{5}{n} = 0$, $\lim_{n\to\infty}\frac{7}{n^2} = 0$

$$
\lim_{n\to\infty}\frac{4 - 0 + 0}{2 + 0 - 0} = \frac{4}{2} = 2
$$

**Explanation:** For very large values of $n$, the quadratic terms ($4n^2$ and $2n^2$) grow much faster than the linear and constant terms, dominating the overall value of the quotient.

---

### Exercise 2. Different Growth Rates

## Question

Compute

$$
\lim_{n\to\infty}\frac{3n+1}{n^2+4},\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}.
$$

Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

## Solution

**Step 1: First limit (Numerator degree < Denominator degree)**

Divide all terms by $n^2$:
$$
\lim_{n\to\infty}\frac{\frac{3}{n} + \frac{1}{n^2}}{1 + \frac{4}{n^2}} = \frac{0 + 1}{1 + 0} = 0
$$

**Step 2: Second limit (Numerator degree > Denominator degree)**

Divide all terms by $n^2$:
$$
\lim_{n\to\infty}\frac{2n - \frac{1}{n}}{5 + \frac{1}{n^2}} = \frac{\infty - 0}{5 + 0} = \infty
$$

**Explanation:** 
- When the degree of the denominator is higher, the fraction approaches $0$.
- When the degree of the numerator is higher, the expression grows without bound ($\infty$).

---

### Exercise 3. A Square Root and Removing an Indeterminate Form

## Question

Compute

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right).
$$

Use the conjugate expression and explain why this transformation removes the difficulty.

## Solution

**Step 1: Multiply and divide by the conjugate expression**

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right) \cdot \frac{\sqrt{n^2+5n}+n}{\sqrt{n^2+5n}+n} = \lim_{n\to\infty}\frac{(n^2+5n) - n^2}{\sqrt{n^2+5n}+n} = \lim_{n\to\infty}\frac{5n}{\sqrt{n^2+5n}+n}
$$

**Step 2: Divide numerator and denominator by $n$**

$$
\lim_{n\to\infty}\frac{5}{\sqrt{1 + \frac{5}{n}} + 1} = \frac{5}{\sqrt{1 + 0} + 1} = \frac{5}{1 + 1} = \frac{5}{2}
$$

**Explanation:** Conjugation transforms the indeterminate $\infty - \infty$ form into a rational fraction where dominant-term analysis can be successfully applied.

---

### Exercise 4. Powers and Oscillation

## Question

Analyze

$$
\left(\frac{2}{3}\right)^n,\qquad \left(\frac{3}{2}\right)^n,\qquad (-1)^n,\qquad \frac{(-1)^n}{n}.
$$

For each sequence, describe the type of behavior and justify your answer.

## Solution

1. **$\left(\frac{2}{3}\right)^n$:** Converges to $0$ because the base is strictly between $-1$ and $1$.
2. **$\left(\frac{3}{2}\right)^n$:** Diverges to $\infty$ because the base is greater than $1$, causing exponential growth.
3. **$(-1)^n$:** Oscillates between $-1$ and $1$ indefinitely and does not converge.
4. **$\frac{(-1)^n}{n}$:** Converges to $0$ by the Squeeze Theorem, since $-\frac{1}{n} \le \frac{(-1)^n}{n} \le \frac{1}{n}$ and both bounds approach $0$.

**Explanation:** Exponential bases determine long-term growth or decay, while alternating signs introduce oscillation whose convergence depends on whether magnitude diminishes to zero.

---

### Exercise 5. The Classical Limit Leading to the Number $e$

## Question

Compute

$$
\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n.
$$

Calculate several values for increasing $n$ and compare the observed behavior with the value of the limit. Explain why a few values do not constitute a proof.

## Solution

**Step 1: Evaluate for increasing values of $n$**
- For $n = 1$: $(1 + 1)^1 = 2$
- For $n = 10$: $(1 + 0.1)^{10} \approx 2.5937$
- For $n = 100$: $(1 + 0.01)^{100} \approx 2.7048$
- For $n = 1000$: $(1 + 0.001)^{1000} \approx 2.7169$

**Step 2: State the limit**

$$
\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n = e \approx 2.71828
$$

**Explanation:** While numerical calculations show terms stabilizing near $2.718$, computing a finite set of values cannot substitute for a rigorous analytical proof showing convergence for all arbitrary $n \to \infty$.

---

### Exercise 6. From a Sequence to a Function — Limit at Infinity

## Question

Compute

$$
\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}.
$$

Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

## Solution

**Step 1: Divide numerator and denominator by $x^2$**

$$
\lim_{x\to\infty}\frac{3 - \frac{1}{x} + \frac{1}{x^2}}{5 + \frac{4}{x} - \frac{2}{x^2}}
$$

**Step 2: Evaluate as $x \to \infty$**

$$
\frac{3 - 0 + 0}{5 + 0 - 0} = \frac{3}{5}
$$

**Explanation:** The algebraic steps mirror Exercise 1. The primary difference is that $x$ is a continuous real variable approaching infinity rather than a discrete integer index $n$, though the limit evaluation mechanism remains identical.

---

### Exercise 7. Limit at a Point and Canceling a Factor

## Question

Compute

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3}.
$$

Explain why the value of the function at $x=3$ is not needed to compute the limit.

## Solution

**Step 1: Factor the numerator**

$$
x^2 - 4x + 3 = (x - 3)(x - 1)
$$

**Step 2: Simplify and evaluate**

$$
\lim_{x\to3}\frac{(x-3)(x-1)}{x-3} = \lim_{x\to3}(x - 1) = 3 - 1 = 2
$$

**Explanation:** The function is undefined at $x = 3$ (yielding $0/0$). Limits evaluate behavior *near* a point rather than *at* the point, allowing us to cancel the common factor $(x-3)$.

---

### Exercise 8. A Square Root in a Function Limit

## Question

Compute

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}
$$

by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

## Solution

**Step 1: Multiply by the conjugate numerator**

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4} \cdot \frac{\sqrt{x}+2}{\sqrt{x}+2} = \lim_{x\to4}\frac{x - 4}{(x-4)(\sqrt{x}+2)}
$$

**Step 2: Simplify and evaluate**

$$
\lim_{x\to4}\frac{1}{\sqrt{x}+2} = \frac{1}{\sqrt{4}+2} = \frac{1}{2 + 2} = \frac{1}{4}
$$

**Explanation:** Just like rationalizing sequences with square roots, multiplying by the conjugate expression eliminates square roots from the numerator, clearing the indeterminate $0/0$ form.

---

### Exercise 9. One-Sided Limits and an Asymptote

## Question

Analyze the left-hand and right-hand limits of

$$
f(x)=\frac{1}{x-2}
$$

as $x\to2$. Does the two-sided limit exist? Interpret the result on a sketch of the graph and identify the vertical asymptote.

## Solution

**Step 1: One-sided limits**
- **Left-hand limit:** $\lim_{x\to2^-}\frac{1}{x-2} = -\infty$ (as $x$ approaches $2$ from values slightly less than $2$, the denominator is small and negative).
- **Right-hand limit:** $\lim_{x\to2^+}\frac{1}{x-2} = +\infty$ (denominator is small and positive).

**Step 2: Two-sided limit & Asymptote**
- Since left-hand and right-hand limits diverge ($\neq$), the **two-sided limit does not exist**.
- **Vertical asymptote:** $x = 2$.

**Explanation:** Discrepancies between one-sided limits indicate a vertical asymptote where function values grow unboundedly in opposite directions.

---

### Exercise 10. Continuity of a Piecewise Function

## Question

Find $a$ so that

$$
f(x)=
\begin{cases}
ax+1,&x<2, \\
x^2-1,&x\ge2
\end{cases}
$$

is continuous at $x=2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

## Solution

**Step 1: Compute function value and right-hand limit at $x = 2$**

$$
f(2) = 2^2 - 1 = 3
$$
$$\lim_{x\to2^+}(x^2 - 1) = 3$$

**Step 2: Compute left-hand limit**

$$
\lim_{x\to2^-}(ax + 1) = 2a + 1
$$

**Step 3: Equate limits for continuity**

$$
2a + 1 = 3 \implies 2a = 2 \implies a = 1
$$

**Explanation:** A function is continuous at a point if and only if its left-hand limit, right-hand limit, and direct function value all match.

---

## More Challenging Exercises

### Exercise 11. An n-th Root

## Question

Compute

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n}.
$$

Explain which term dominates and why the transformation looks different from the case of a quotient of polynomials.

## Solution

**Step 1: Factor out the dominant term inside the root ($5^n$)**

$$
\lim_{n\to\infty}\sqrt[n]{5^n \left(1 + \left(\frac{2}{5}\right)^n\right)} = \lim_{n\to\infty} 5 \cdot \left(1 + \left(\frac{2}{5}\right)^n\right)^{1/n}
$$

**Step 2: Evaluate the limit**

As $n \to \infty$, $\left(\frac{2}{5}\right)^n \to 0$ and $\left(1 + 0\right)^{1/n} \to 1$:
$$
5 \cdot 1 = 5
$$

**Explanation:** The term $5^n$ dominates exponentially over $2^n$. Factoring it out isolates the dominant growth factor from the root.

---

### Exercise 12. Exponential Function Limit

## Question

Compute

$$
\lim_{x\to0}(1+3x)^{1/x}.
$$

Connect the result with the limit from Exercise 5 and show the appropriate transformation.

## Solution

**Step 1: Use substitution to match the $e$-limit pattern**

Let $n = \frac{1}{3x}$, which means $3x = \frac{1}{n}$. As $x \to 0$, $n \to \infty$.

**Step 2: Rewrite the expression**

$$
\lim_{n\to\infty}\left(1 + \frac{1}{n}\right)^{3n} = \lim_{n\to\infty}\left[\left(1 + \frac{1}{n}\right)^n\right]^3 = e^3
$$

**Explanation:** Through substitution, this transforms directly into the classical limit definition of $e$ raised to the power of $3$.

---

### Exercise 13. Fundamental Trigonometric Limit

## Question

Using

$$
\lim_{x\to0}\frac{\sin x}{x}=1,
$$

compute

$$
\lim_{x\to0}\frac{\sin5x}{x},\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}.
$$

In each case, show how you reduce the expression to the fundamental limit.

## Solution

**1. First limit:**
$$
\lim_{x\to0}\frac{\sin5x}{x} = \lim_{x\to0} 5 \cdot \frac{\sin5x}{5x} = 5 \cdot 1 = 5
$$

**2. Second limit:**
$$
\lim_{x\to0}\frac{\sin2x}{\sin3x} = \lim_{x\to0} \frac{\frac{\sin2x}{x}}{\frac{\sin3x}{x}} = \lim_{x\to0} \frac{2 \cdot \frac{\sin2x}{2x}}{3 \cdot \frac{\sin3x}{3x}} = \frac{2 \cdot 1}{3 \cdot 1} = \frac{2}{3}
$$

**Explanation:** Multiplying and dividing by matching scale factors reduces composite trigonometric expressions to the fundamental limit $\lim \frac{\sin u}{u} = 1$.

---

### Exercise 14. A $0/0$ Limit with Trigonometry

## Question

Compute

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}.
$$

Justify the result without using l'Hôpital's rule, using a trigonometric identity and the fundamental limit.

## Solution

**Step 1: Multiply numerator and denominator by the conjugate $(1 + \cos x)$**

$$
\lim_{x\to0}\frac{(1-\cos x)(1+\cos x)}{x^2(1+\cos x)} = \lim_{x\to0}\frac{1 - \cos^2 x}{x^2(1+\cos x)}
$$

**Step 2: Apply Pythagorean identity ($1 - \cos^2 x = \sin^2 x$)**

$$
\lim_{x\to0}\left(\frac{\sin x}{x}\right)^2 \cdot \frac{1}{1+\cos x}
$$

**Step 3: Evaluate using the fundamental limit**

$$
(1)^2 \cdot \frac{1}{1 + \cos(0)} = 1 \cdot \frac{1}{1 + 1} = \frac{1}{2}
$$

**Explanation:** Trigonometric identities transform the expression into a product containing the square of the fundamental limit $\frac{\sin x}{x}$.

---

### Exercise 15. Observation Versus Proof

## Question

Choose one sequence and one function from this set. For the sequence, compute several values for increasingly large $n$. For the function, prepare a table of values with arguments approaching the limit point from the left and right. Sketch the behavior of both objects.

Compare the observation with the analytical result and explain why a finite number of calculations or a sketch does not constitute a proof that the limit exists.

## Solution

**Analysis & Observation:**
- **Sequence Example:** $a_n = \frac{4n^2-3n+1}{2n^2+5n-7}$ (Exercise 1). Calculating values for $n = 10, 100, 1000$ yields terms progressively closer to $2$.
- **Function Example:** $f(x) = \frac{\sqrt{x}-2}{x-4}$ (Exercise 8) near $x = 4$. Evaluating points at $x = 3.9, 3.99$ and $4.1, 4.01$ shows values clustering near $0.25$.

**Explanation:** Numerical observations and sketches reveal strong empirical trends, but they remain incomplete because they only test a finite subset of points, whereas rigorous mathematical proofs must account for an infinite domain approaching the limit boundary.
