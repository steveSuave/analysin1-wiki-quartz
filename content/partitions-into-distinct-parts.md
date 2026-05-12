# Partitions Into Distinct Parts

**Summary**: A partition of $n$ into **distinct** (unequal) parts uses each positive integer at most once. The generating function is $\prod_{k\geq 1}(1 + x^k z)$, with $z$ tracking the number of parts. Chapter 16 derives closed-form recurrent series for the number of partitions with exactly $m$ distinct parts (numerator $x^{m(m+1)/2}$, denominator $\prod_{k=1}^m(1 - x^k)$) and proves the **staircase bijection** $q_m(n) = p_m(n - m(m-1)/2)$ between distinct and unrestricted partitions.

**Sources**: chapter16.pdf

**Last updated**: 2026-05-11

---

## Definition

A partition of $n$ into distinct parts is an unordered tuple $a_1 > a_2 > \cdots > a_m \geq 1$ with $\sum a_i = n$. Write $q_m(n)$ for the number of such partitions with exactly $m$ parts and $q(n) = \sum_m q_m(n)$ for the total.

## Enumerations (Chapter 16)

For $n = 8$ (source: chapter16.pdf, §301), $q(8) = 6$:

$$8 = 8 = 7+1 = 6+2 = 5+3 = 5+2+1 = 4+3+1.$$

For $n = 9$ (§325), $q(9) = 8$:

$$9 = 9 = 6+2+1 = 8+1 = 5+4 = 7+2 = 5+3+1 = 6+3 = 4+3+2.$$

For $n = 35$ with exactly $m = 7$ distinct parts (§300), $q_7(35) = 15$.

## Generating function (§297, §301)

$$\prod_{k\geq 1}(1 + x^k z) = \sum_{n,m\geq 0} q_m(n)\,x^n z^m.$$

At $z = 1$:

$$\prod_{k\geq 1}(1 + x^k) = \sum_n q(n)\,x^n = 1 + x + x^2 + 2x^3 + 2x^4 + 3x^5 + 4x^6 + 5x^7 + 6x^8 + 8x^9 + 10x^{10} + 12x^{11} + \cdots.$$

## Closed-form recurrent series for each $q_m$ (§307–§312)

Let $Z = \prod_{k\geq 1}(1 + x^k z) = 1 + Pz + Qz^2 + Rz^3 + Sz^4 + Tz^5 + \cdots$. Substituting $xz$ for $z$ removes the $k = 1$ factor:

$$Z(x, xz) = \frac{Z(x, z)}{1 + xz}.$$

Expanding and matching coefficients of $z^m$ yields the recursion $P_m(1 - x^m) = x^m P_{m-1}$, hence

$$P = \frac{x}{1-x},\qquad Q = \frac{x^3}{(1-x)(1-x^2)},\qquad R = \frac{x^6}{(1-x)(1-x^2)(1-x^3)},$$

$$S = \frac{x^{10}}{(1-x)(1-x^2)(1-x^3)(1-x^4)},\qquad T = \frac{x^{15}}{(1-x)(1-x^2)(1-x^3)(1-x^4)(1-x^5)}.$$

The numerator exponents $1, 3, 6, 10, 15, 21, \ldots$ are the **triangular numbers** $m(m+1)/2$ (§312). In general

$$P_m = \frac{x^{m(m+1)/2}}{\prod_{k=1}^m(1 - x^k)}.$$

Each is a [[recurrent-series|recurrent series]] with [[scale-of-the-relation|scale]] given by $\prod_{k=1}^m(1 - x^k)$.

## The staircase bijection (§312, §315)

Two equivalent forms appear:

**Form A** (Euler §312, by inspection of the recurrent series): The denominator $1/\prod_{k=1}^m(1-x^k)$ is the generating function for partitions of any integer into parts $\leq m$. The numerator $x^{m(m+1)/2}$ shifts the indexing, so

$$q_m(N) = \#\{\text{partitions of } N - m(m+1)/2 \text{ into parts} \leq m\}.$$

Equivalently: $q_m(n + m(m+1)/2) = p_m(n)$.

**Form B** (Euler §315, derived from the unrestricted closed form): rephrased in terms of partitions of $n$ into exactly $m$ parts,

$$q_m(n) = p_m\!\left(n - \frac{m(m-1)}{2}\right).$$

**Bijective interpretation**: from a distinct partition $a_1 > a_2 > \cdots > a_m \geq 1$, subtract the staircase $0, 1, 2, \ldots, (m-1)$ to obtain $b_i = a_i - (m - i)$:

$$b_1 \geq b_2 \geq \cdots \geq b_m \geq 1,\quad \sum b_i = n - \binom{m}{2}.$$

The map is invertible (add the staircase back), so it is a bijection between $m$-distinct partitions of $n$ and $m$-unrestricted partitions of $n - m(m-1)/2$. Euler does not give the bijection — he proves the identity algebraically — but the algebraic identity is the modern bijection in disguise.

## Worked numerical examples (§318)

- $q_7(50)$ = number of partitions of $50$ into $7$ unequal numbers = (using the table) $p_7(50 - 28) = p_7(22) = 522$.
- Equivalently, by Form A: $q_7(50) = p_{\leq 7}(50 - 28) = p_{\leq 7}(22) = 522$.

## Connection to $q(n)$ via the pentagonal theorem (§327)

Summing $q_m$ over all $m$ gives $q(n) = \sum_m q_m(n)$. Euler computes the values of $q(n)$ directly from

$$Q = \prod(1 + x^k) = \frac{\prod(1 - x^{2k})}{\prod(1 - x^k)} = \frac{1}{P}\cdot\prod_{k\geq 1}(1 - x^{2k}),$$

where $1/P = \sum p(n) x^n$ and the second factor is the pentagonal-number expansion at $x^2$: $\prod(1 - x^{2k}) = 1 - x^2 - x^4 + x^{10} + x^{14} - x^{24} - x^{30} + \cdots$. The product of these two known series gives

$$Q = 1 + x + x^2 + 2x^3 + 2x^4 + 3x^5 + 4x^6 + 5x^7 + 6x^8 + 8x^9 + \cdots.$$

See [[eulers-pentagonal-number-theorem]] for the expansion of $\prod(1 - x^k)$ used here.

## Related pages

- [[partition-of-numbers]]
- [[partition-generating-functions]]
- [[partition-recurrence]]
- [[eulers-pentagonal-number-theorem]]
- [[distinct-parts-equals-odd-parts]]
- [[recurrent-series]]
- [[scale-of-the-relation]]
- [[chapter-16-on-the-partition-of-numbers]]
