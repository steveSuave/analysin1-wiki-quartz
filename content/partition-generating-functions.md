# Partition Generating Functions

**Summary**: Bivariate generating functions enumerate partitions by both the integer being partitioned (the exponent of $x$) and the number of parts (the exponent of $z$). Chapter 16 develops two parallel families: the product $\prod_i(1 + x^{\alpha_i}z)$ for partitions into *distinct* parts drawn from $\{\alpha_i\}$, and the reciprocal product $1/\prod_i(1 - x^{\alpha_i}z)$ for *unrestricted* (repetition-allowed) partitions. Closed-form recurrent series for each $z^m$ coefficient follow from a single functional-equation trick.

**Sources**: chapter16

**Last updated**: 2026-05-11

---

## The distinct-parts product (§297)

For any sequence of positive integers $\alpha, \beta, \gamma, \ldots$,

$$\prod_{i\geq 1}(1 + x^{\alpha_i} z) = 1 + Pz + Qz^2 + Rz^3 + Sz^4 + \cdots,$$

where each $P, Q, R, \ldots$ is itself a series in $x$. The coefficient $P$ is the sum $\sum x^{\alpha_i}$; the coefficient $Q$ is the sum of $x^{\alpha_i + \alpha_j}$ over pairs $i < j$; the coefficient $R$ over triples; and so on (source: chapter16, §297). These are the **elementary symmetric polynomials** in $\{x^{\alpha_i}\}$. The combinatorial reading is

$$[x^n z^m]\text{-coefficient} = \#\{(i_1 < i_2 < \cdots < i_m) : \alpha_{i_1} + \cdots + \alpha_{i_m} = n\}.$$

If a sum can be formed in $N$ ways, the coefficient is $N$ (§298–§299).

**Example (§300):** with $\alpha_i = i$,

$$\prod_{k\geq 1}(1 + x^k z) = 1 + z(x + x^2 + x^3 + \cdots) + z^2(x^3 + x^4 + 2x^5 + 2x^6 + 3x^7 + 3x^8 + 4x^9 + 4x^{10} + 5x^{11} + \cdots) + z^3(\cdots) + \cdots.$$

Reading $z^7$ at $x^{35}$ gives the coefficient $15$: thirty-five can be written as a sum of seven distinct positive integers in fifteen ways.

**At $z = 1$ (§301):**

$$\prod_{k\geq 1}(1 + x^k) = 1 + x + x^2 + 2x^3 + 2x^4 + 3x^5 + 4x^6 + 5x^7 + 6x^8 + 8x^9 + 10x^{10} + \cdots,$$

the generating function for partitions of $n$ into **distinct** positive integers, no count constraint.

## The unrestricted-parts product (§302)

Moving the product to the denominator gives the unrestricted counterpart:

$$\frac{1}{\prod_{i\geq 1}(1 - x^{\alpha_i} z)} = 1 + Pz + Qz^2 + Rz^3 + \cdots.$$

Each factor's geometric series $1/(1 - x^{\alpha_i} z) = \sum_{j\geq 0}(x^{\alpha_i})^j z^j$ permits the factor to be reused, so

$$[x^n z^m]\text{-coefficient} = \#\{(i_1 \leq i_2 \leq \cdots \leq i_m) : \alpha_{i_1} + \cdots + \alpha_{i_m} = n\}$$

(§302–§303).

**Example (§304):** $\alpha_i = i$ gives

$$\frac{1}{\prod_{k\geq 1}(1 - x^k z)} = 1 + z(x + x^2 + x^3 + \cdots) + z^2(x^2 + x^3 + 2x^4 + 2x^5 + 3x^6 + 3x^7 + 4x^8 + \cdots) + \cdots,$$

with $x^{13} z^5$ having coefficient $18$ — thirteen has $18$ partitions into five parts (equal or unequal).

**At $z = 1$ (§305):**

$$\frac{1}{\prod_{k\geq 1}(1 - x^k)} = 1 + x + 2x^2 + 3x^3 + 5x^4 + 7x^5 + 11x^6 + 15x^7 + 22x^8 + 30x^9 + \cdots,$$

the celebrated **partition function** $p(n)$.

## The functional-equation trick (§306–§307)

Let $Z = \prod_{k\geq 1}(1 + x^k z) = 1 + Pz + Qz^2 + Rz^3 + \cdots$. Substituting $xz$ for $z$ shifts the indexing by one step and removes the $k = 1$ factor:

$$\prod_{k\geq 1}(1 + x^{k+1}z) = \frac{Z(x, z)}{1 + xz}.$$

Expanding both sides and matching the coefficient of $z^m$:

$$x^m P_m + Qx^{2m}\cdot(\ldots) + \cdots\quad\Longrightarrow\quad P_m\cdot(1 - x^m) = x^m\cdot P_{m-1},$$

hence

$$P_m = \frac{x^m\cdot P_{m-1}}{1 - x^m}.$$

Iterating from $P_0 = 1$ produces the closed forms

$$P_1 = \frac{x}{1-x},\quad P_2 = \frac{x^{1+2}}{(1-x)(1-x^2)},\quad P_3 = \frac{x^{1+2+3}}{(1-x)(1-x^2)(1-x^3)},\quad\ldots\quad P_m = \frac{x^{m(m+1)/2}}{\prod_{k=1}^m(1 - x^k)}.$$

The numerator exponents are the **triangular numbers**.

The unrestricted case (§313) uses the analogous identity $Z(x, xz)\cdot(1 - xz) = Z(x, z)$ to give

$$P_m^{\text{unrestricted}} = \frac{x^m}{\prod_{k=1}^m(1 - x^k)}.$$

Each is a [[recurrent-series|recurrent series]] in $x$ whose [[scale-of-the-relation|scale of the relation]] is the expansion of $\prod_{k=1}^m(1 - x^k)$.

## Bijection theorems (§314–§315)

Comparing the rational expressions for distinct and unrestricted $P_m$ yields four equivalent forms of the **staircase bijection**:

- $q_m(n + m(m+1)/2) = \#\{\text{partitions of } n \text{ into parts} \leq m\}$ (§311–§312).
- $q_m(n) = p_m(n - m(m-1)/2)$ (§315) — number of partitions of $n$ into $m$ distinct parts equals number of partitions of $n - m(m-1)/2$ into $m$ unrestricted parts.

**Bijective interpretation**: subtract $0, 1, 2, \ldots, (m-1)$ from the parts of a distinct partition $a_1 > a_2 > \cdots > a_m$ to flatten it into $a_1 - (m-1) \geq a_2 - (m-2) \geq \cdots \geq a_m \geq 1$.

## Numerical worked example

Number of partitions of $50$ into $7$ distinct parts (§318): consult the table at row $50 - 7\cdot 8/2 = 22$, column VII — gives $522$. Number of partitions of $50$ into $7$ parts (equal or unequal): row $50 - 7 = 43$, column VII — gives $8946$.

## Related pages

- [[partition-of-numbers]]
- [[partitions-into-distinct-parts]]
- [[partition-recurrence]]
- [[eulers-pentagonal-number-theorem]]
- [[distinct-parts-equals-odd-parts]]
- [[recurrent-series]]
- [[scale-of-the-relation]]
- [[chapter-16-on-the-partition-of-numbers]]
