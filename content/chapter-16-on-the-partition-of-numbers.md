# Chapter 16 — On the Partition of Numbers

**Summary**: §297–§331. Euler founds the theory of integer partitions: counting the number of ways a positive integer $n$ can be expressed as a sum of prescribed parts. The central technique is the **generating function** — a product $\prod_i(1 + x^{\alpha_i}z)$ enumerates partitions into *distinct* parts drawn from $\{\alpha_i\}$ via the coefficient of $z^m x^n$, while the reciprocal $1/\prod_i(1 - x^{\alpha_i}z)$ enumerates partitions with *repetition* allowed (§297–§305). Setting $\alpha_i = i$ and $z = 1$ gives the partition function $p(n)$ (§305) and the distinct-part counterpart $q(n)$ (§301). The chapter then derives closed-form recurrent series for the column generating functions (§307–§315), states the column-by-column **Pascal-like recurrence** $p_m(n) = p_{m-1}(n) + p_m(n-m)$ (§318), proves the **pentagonal number theorem** $\prod(1 - x^k) = \sum(-1)^n x^{n(3n-1)/2}$ (§323), the **distinct = odd** identity $\prod(1+x^k) = \prod 1/(1-x^{2k-1})$ (§326), and the **uniqueness of binary** and **balanced-ternary** representations (§329, §331). A 70×11 partition table closes the chapter.

**Sources**: chapter16.pdf

**Last updated**: 2026-05-11

---

## Movement 1 — Products as partition generating functions (§297–§301)

For any sequence of positive integers $\alpha, \beta, \gamma, \ldots$ and the product

$$(1 + x^\alpha z)(1 + x^\beta z)(1 + x^\gamma z)\cdots = 1 + Pz + Qz^2 + Rz^3 + \cdots,$$

each coefficient $P, Q, R, \ldots$ is itself a series in $x$. The coefficient of $z^m$ collects products of $m$ *distinct* powers $x^{\alpha_{i_1}}\cdots x^{\alpha_{i_m}}$, so the coefficient of $x^n z^m$ is precisely the **number of ways $n$ can be written as a sum of $m$ distinct terms** of the sequence (source: chapter16.pdf, §297–§299). Setting $\alpha_i = i$ (§300) and reading the coefficient $15x^{35}$ off $z^7$ records that $35$ can be written as a sum of $7$ distinct positive integers in $15$ ways. Setting $z = 1$ (§301) collapses to

$$\prod_{k\geq 1}(1 + x^k) = 1 + x + x^2 + 2x^3 + 2x^4 + 3x^5 + 4x^6 + 5x^7 + 6x^8 + \cdots,$$

the generating function for **partitions into distinct parts** without restriction on their number.

See [[partition-generating-functions]], [[partitions-into-distinct-parts]].

## Movement 2 — Reciprocal products and unrestricted partitions (§302–§305)

Moving the product to the denominator gives the **unrestricted** counterpart:

$$\frac{1}{(1 - x^\alpha z)(1 - x^\beta z)\cdots} = 1 + Pz + Qz^2 + \cdots,$$

where each factor's geometric expansion $1/(1 - x^{\alpha_i}z) = 1 + x^{\alpha_i}z + x^{2\alpha_i}z^2 + \cdots$ permits a factor to be reused. The coefficient of $x^n z^m$ now counts partitions of $n$ into $m$ parts from $\{\alpha_i\}$ **with repetition allowed** (§302–§303). At $z = 1$:

$$\frac{1}{(1-x)(1-x^2)(1-x^3)\cdots} = 1 + x + 2x^2 + 3x^3 + 5x^4 + 7x^5 + 11x^6 + 15x^7 + 22x^8 + 30x^9 + \cdots,$$

the celebrated **partition function** $p(n)$ (§305). Euler enumerates the eleven partitions of $6$ to confirm the coefficient.

## Movement 3 — Closed-form recurrent series for $P_m$ (§306–§315)

To extract each $P_m$ explicitly, Euler uses a single functional-equation trick. For $Z = \prod_{k\geq 1}(1 + x^k z)$, substituting $xz$ for $z$ shifts the indexing and drops one factor:

$$Z(x, xz) = \frac{Z(x, z)}{1 + xz}.$$

Equating coefficients of $z^m$ yields $P_m\cdot(1 - x^m) = x^m P_{m-1}$, hence (§307)

$$P_1 = \frac{x}{1-x},\quad P_2 = \frac{x^3}{(1-x)(1-x^2)},\quad P_3 = \frac{x^6}{(1-x)(1-x^2)(1-x^3)},\quad P_4 = \frac{x^{10}}{(1-x)(1-x^2)(1-x^3)(1-x^4)},\ldots$$

The numerator exponent is the **triangular number** $m(m+1)/2$. Applied to the reciprocal product (§313–§314) the same machinery gives

$$P_m^{\text{unrestricted}} = \frac{x^m}{(1-x)(1-x^2)\cdots(1-x^m)}.$$

Comparing the two leads to the four bijection theorems of §314–§315 — the **staircase trick** $q_m(n) = p_m(n - m(m-1)/2)$ (subtract $0+1+\cdots+(m-1)$ from a distinct partition to flatten it into an arbitrary one). See [[partitions-into-distinct-parts]].

## Movement 4 — The Pascal-like recurrence (§316–§318)

Euler states the **central computational identity**. Let $N = p_m(n)$, $M = p_m(n - m)$, $L = p_{m-1}(n)$. Then

$$N = L + M,$$

because every partition of $n$ with parts $\leq m$ either omits $m$ (counted by $L$) or includes at least one $m$ (counted by $M$, after removing one $m$). This is $p_m(n) = p_{m-1}(n) + p_m(n - m)$, the recurrence by which Euler's partition table is built up column by column. See [[partition-recurrence]].

## Movement 5 — Figurate-number structure of the columns (§319–§322)

The column for partitions into parts $\leq m$ is the coefficient of $x^n$ in $1/\prod_{k=1}^m(1-x^k)$. By writing $1/(1-x^k) = (1 + x + \cdots + x^{k-1})/(1-x)^k$ Euler shows that column II's entries arise from the **natural numbers** by an averaging step, column III's from the **triangular numbers**, column IV's from the **tetrahedral numbers**, and so on (§320–§322). The figurate numbers — already studied in §64–§67 as [[higher-order-arithmetic-progressions]] — supply the leading term of each column.

## Movement 6 — The pentagonal number theorem (§323–§324)

Multiplying out $\prod_{k\geq 1}(1 - x^k)$ Euler observes that nearly all coefficients vanish:

$$\prod_{k\geq 1}(1 - x^k) = 1 - x - x^2 + x^5 + x^7 - x^{12} - x^{15} + x^{22} + x^{26} - x^{35} - x^{40} + \cdots.$$

The surviving exponents are the **generalized pentagonal numbers** $(3n^2 \pm n)/2$, with sign $(-1)^n$ (§323). Inverted, this is the **scale of the relation** for the partition function:

$$p(n) = p(n-1) + p(n-2) - p(n-5) - p(n-7) + p(n-12) + p(n-15) - \cdots,$$

with only $O(\sqrt n)$ non-zero terms — the fastest classical recurrence for $p(n)$, and the one used to compute the chapter's table. See [[eulers-pentagonal-number-theorem]].

## Movement 7 — Distinct parts equals odd parts (§325–§327)

Letting $P = \prod(1 - x^k)$ and $Q = \prod(1 + x^k)$, the pairing $PQ = \prod(1 - x^{2k})$ gives

$$\frac{1}{Q} = \frac{P}{PQ} = \prod_{k\geq 1}(1 - x^{2k - 1})\quad\Longleftrightarrow\quad \prod_{k\geq 1}(1 + x^k) = \prod_{k\geq 1}\frac{1}{1 - x^{2k - 1}}.$$

The left side counts partitions of $n$ into **distinct** parts; the right side counts partitions of $n$ into **odd** parts (with repetition). They are equal — the **distinct = odd theorem** (§326). §327 then derives the series for $q(n)$ from the pentagonal-number expansion of $1/P$. See [[distinct-parts-equals-odd-parts]].

## Movement 8 — Binary and balanced-ternary uniqueness (§328–§331)

Setting $P = \prod_{k\geq 0}(1 + x^{2^k})$, the substitution $x \mapsto x^2$ drops the first factor, giving the fixed-point equation $(1 + x)P(x^2) = P$. Matching coefficients shows all of them equal $1$:

$$\prod_{k\geq 0}(1 + x^{2^k}) = \sum_{n\geq 0} x^n = \frac{1}{1 - x}.$$

Every non-negative integer has a **unique binary representation** (§329). Application: weighing with $1, 2, 4, 8, \ldots$-pound weights on a one-pan scale.

§330–§331 repeat the argument for the formal Laurent product $\prod_{k\geq 0}(x^{-3^k} + 1 + x^{3^k})$. The same fixed-point trick yields

$$\prod_{k\geq 0}(x^{-3^k} + 1 + x^{3^k}) = \sum_{n\in\mathbb Z} x^n,$$

so every integer has a **unique balanced-ternary representation** with digits in $\{-1, 0, +1\}$. Application: weighing with $1, 3, 9, 27, \ldots$-pound weights on a two-pan balance. See [[binary-representation-theorem]], [[balanced-ternary-representation]].

## Movement 9 — The partition table (pages 280–283)

Euler closes with a table whose entry at row $n$, column $m$ is $p_m(n) = $ number of partitions of $n$ into parts $\leq m$ (equivalently, into at most $m$ parts). The table runs to $n \approx 70$ and $m = 11$. Combined with the staircase bijection (§315), it answers queries about partitions into distinct or unrestricted parts of any size. Worked examples (§318): partitions of $50$ into $7$ unequal numbers $=$ row $22$, column VII $= 522$; partitions of $50$ into $7$ numbers (equal or unequal) $=$ row $43$, column VII $= 8946$.

## Significance

Chapter 16 introduces:

- The **generating-function method** for partitions — the bivariate enumerator in part-count and integer-size that remains the foundational technique a quarter of a millennium later.
- The **pentagonal number theorem** (§323), Euler's signature additive identity and the first nontrivial theta-function vanishing pattern.
- The **distinct = odd** identity (§326), the model for bijective partition combinatorics.
- The **uniqueness of binary** and **balanced-ternary** representations (§329, §331), with the link to weighing problems.
- The **Pascal-like recurrence** (§318), the algorithm by which all partition tables since have been computed.

This is the additive-number-theory pivot of the *Introductio*, parallel to the multiplicative pivot of [[chapter-15-on-series-which-arise-from-products|Chapter 15]].

## Related pages

- [[partition-of-numbers]]
- [[partition-generating-functions]]
- [[partitions-into-distinct-parts]]
- [[partition-recurrence]]
- [[eulers-pentagonal-number-theorem]]
- [[distinct-parts-equals-odd-parts]]
- [[binary-representation-theorem]]
- [[balanced-ternary-representation]]
- [[recurrent-series]]
- [[scale-of-the-relation]]
- [[higher-order-arithmetic-progressions]]
- [[geometric-series]]
- [[chapter-15-on-series-which-arise-from-products]]
