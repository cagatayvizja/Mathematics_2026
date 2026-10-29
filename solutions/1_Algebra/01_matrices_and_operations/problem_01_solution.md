Sistem kurallarım gereği yanıtlarımı Türkçe olarak vermem gerekiyor, ancak GitHub'daki `.md` (Markdown) ödev dosyana doğrudan kopyalayıp yapıştırabilmen için tüm matematiksel LaTeX kodlarını ve çözümleri uluslararası standartlarda aşağıda hazırladım.

Bu blokları doğrudan GitHub README veya `.md` dosyalarına ekleyebilirsin:

```markdown
### Exercise 1. Matrix Size and Entries

Given
$$A = \begin{pmatrix} 2 & -1 & 3 \\ 0 & 4 & 5 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\ -2 & 3 \\ 4 & 1 \end{pmatrix}$$

1. **Sizes:** $A$ is of size $2 \times 3$, and $B$ is of size $3 \times 2$.
2. **Entries:** 
   * $a_{12} = -1$
   * $a_{23} = 5$
   * $b_{21} = -2$
   * $b_{32} = 1$
3. **Vectors:** The second row of $A$ is $\begin{pmatrix} 0 & 4 & 5 \end{pmatrix}$ and the first column of $B$ is $\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$.

---

### Exercise 2. Addition and Scalar Multiplication

For
$$A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}$$

* **Addition ($A+B$):**
  $$A + B = \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$$
* **Subtraction ($A-B$):**
  $$A - B = \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$$
* **Linear Combination ($3A-2B$):**
  $$3A - 2B = 3\begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} - 2\begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix} - \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$$

---

### Exercise 3. When Can Matrices Be Multiplied?

Given sizes: $A_{2 \times 3}, \ B_{3 \times 4}, \ C_{4 \times 2}, \ D_{2 \times 2}$.

* $AB$: $2 \times \mathbf{3}$ and $\mathbf{3} \times 4 \implies$ **Defined**, size **$2 \times 4$**.
* $BA$: $3 \times \mathbf{4}$ and $\mathbf{2} \times 3 \implies$ **Undefined** ($4 \neq 2$).
* $BC$: $3 \times \mathbf{4}$ and $\mathbf{4} \times 2 \implies$ **Defined**, size **$3 \times 2$**.
* $CB$: $4 \times \mathbf{2}$ and $\mathbf{3} \times 4 \implies$ **Undefined** ($2 \neq 3$).
* $AC$: $2 \times \mathbf{3}$ and $\mathbf{4} \times 2 \implies$ **Undefined** ($3 \neq 4$).
* $CA$: $4 \times \mathbf{2}$ and $\mathbf{2} \times 3 \implies$ **Defined**, size **$4 \times 3$**.
* $AD$: $2 \times \mathbf{3}$ and $\mathbf{2} \times 2 \implies$ **Undefined** ($3 \neq 2$).
* $DA$: $2 \times \mathbf{2}$ and $\mathbf{2} \times 3 \implies$ **Defined**, size **$2 \times 3$**.

---

### Exercise 4. Matrix Multiplication and Noncommutativity

For
$$A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}$$

* **Product $AB$:**
  $$AB = \begin{pmatrix} 1(2)+2(3) & 1(0)+2(1) \\ 0(2)+1(3) & 0(0)+1(1) \end{pmatrix} = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}$$
* **Product $BA$:**
  $$BA = \begin{pmatrix} 2(1)+0(0) & 2(2)+0(1) \\ 3(1)+1(0) & 3(2)+1(1) \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$$
* **Conclusion:** Since $AB \neq B A$, matrix multiplication is noncommutative.

---

### Exercise 5. Matrix Times Vector

Let
$$A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \qquad x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$$

* **Multiplication ($Ax$):**
  $$Ax = \begin{pmatrix} 2(4) + (-1)(2) \\ 1(4) + 3(2) \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$$
* **Linear Combination:**
  $$Ax = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$$

---

### Exercise 6. Transpose

For
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}$$

* **Transposes:**
  $$A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}, \qquad B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}$$
* **Verification of $(AB)^T = B^TA^T$:**
  $$AB = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix} \implies (AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$$
  $$B^TA^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix} = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$$

---

### Exercise 7. Identity Matrix, Zero Matrix, and Powers

For
$$A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$$

* **Neutral Elements:** $AI = IA = A$ and $A + 0 = A$.
* **Powers:**
  $$A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}, \qquad A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$$
* **Pattern:** $A^n = \begin{pmatrix} 2^n & n 2^{n-1} \\ 0 & 2^n \end{pmatrix}$.

---

### Exercise 8. Row Operations and Their Reversibility

For
$$A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}$$

1. **Step 1 ($R_2 \leftarrow R_2 - 2R_1$):** $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}$ (Reversed by $R_2 \leftarrow R_2 + 2R_1$).
2. **Step 2 ($R_3 \leftarrow R_3 + R_1$):** $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}$ (Reversed by $R_3 \leftarrow R_3 - R_1$).
3. **Step 3 ($R_2 \leftrightarrow R_3$):** $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}$ (Reversed by swapping $R_2$ and $R_3$ back).

---

### Exercise 9. Composing Transformations

Let
$$S = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}, \quad R = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}, \quad x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$$

* **$RSx$:**
  $$Sx = \begin{pmatrix} 2 \\ 2 \end{pmatrix} \implies RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$$
* **$SRx$:**
  $$Rx = \begin{pmatrix} -2 \\ 1 \end{pmatrix} \implies SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$$

---

### Exercise 10. Columns of a Matrix Product

Given
$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}$$

* **Column Multiplications:**
  $$Ab_1 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}, \quad Ab_2 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$$
* **Product:**
  $$AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}$$

---

### Exercise 11. When Do Matrices Commute?

Given
$$A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$$

* **Condition for $AB = BA$:** $c = 0$ and $d = a$.
* **General Form:** $B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$.

---

### Exercise 12. Formula for a Matrix Power

Let
$$A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$$

* **Powers:** $A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \ A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$.
* **Conjecture:** $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$.

---

### Exercise 13. A Recurrence Written in Matrix Form

Let
$$F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$$

* **Powers & Sequence:** Powers of $F$ generate the Fibonacci sequence ($0, 1, 1, 2, 3, 5, \dots$).
* **Recurrence Step:** $F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} a+b \\ a \end{pmatrix}$.

---

### Exercise 14. Rotation Matrices

For
$$R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$$

* **Multiplication:** Using angle-sum identities:
  $$R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha+\beta)$$

---

### Exercise 15. Associativity of Multiplication

Given matrices $A, B, C$, computing $(AB)C$ and $A(BC)$ yields identical final matrices due to the associativity property of matrix multiplication.

```
