# Partition Recurrence

**Summary**: Euler's central computational identity for partitions (§316–§318): if $p_m(n)$ is the number of partitions of $n$ into parts $\leq m$, then $p_m(n) = p_{m-1}(n) + p_m(n - m)$. This Pascal-triangle-like recurrence builds the partition table column by column and is the workhorse of all partition computation.

**Sources**: chapter16.pdf

**Last updated**: 2026-05-11

---

## Statement

Let $p_m(n)$ be the number of partitions of $n$ into positive parts all at most $m$. Equivalently (Euler's §315 bijection), the number of partitions of $n$ into at most $m$ parts. Then for $m, n \geq 1$:

$$p_m(n) = p_{m-1}(n) + p_m(n - m),$$

with conventions $p_0(0) = 1$, $p_0(n) = 0$ for $n \geq 1$, and $p_m(n) = 0$ for $n < 0$ (source: chapter16.pdf, §318).

## Combinatorial derivation (§316–§318)

Every partition of $n$ with parts $\leq m$ falls into one of two disjoint cases:

- **No part equals $m$**: all parts are $\leq m - 1$, so there are $p_{m-1}(n)$ such partitions (Euler writes $L$).
- **At least one part equals $m$**: subtract one $m$, leaving a partition of $n - m$ with parts still $\leq m$. There are $p_m(n - m)$ such (Euler writes $M$).

Summing: $N = L + M$, where $N = p_m(n)$.

## Algebraic derivation

The same identity falls out of generating functions. The column-$m$ generating series is

$$\sum_n p_m(n)\,x^n = \frac{1}{(1-x)(1-x^2)\cdots(1-x^m)}.$$

Peeling off the last factor:

$$\frac{1}{\prod_{k=1}^m(1-x^k)} = \frac{1}{1 - x^m}\cdot\frac{1}{\prod_{k=1}^{m-1}(1-x^k)},$$

i.e. $(1 - x^m)\sum_n p_m(n) x^n = \sum_n p_{m-1}(n) x^n$. Matching the coefficient of $x^n$: $p_m(n) - p_m(n - m) = p_{m-1}(n)$.

## Using the recurrence: Euler's partition table

Euler tabulates $p_m(n)$ for $n = 1, \ldots, 69$ and $m = 1, \ldots, 11$ on pages 280–283 of the chapter. Each column is filled in from the previous one by the recurrence, starting from $p_1(n) = 1$ for all $n$ (only one partition with parts $\leq 1$ — all ones). Filling in by the recurrence:

- Column II: $p_2(n) = \lfloor n/2 \rfloor + 1$, giving $1, 1, 2, 2, 3, 3, 4, 4, 5, 5, 6, \ldots$.
- Column III: $1, 1, 2, 3, 4, 5, 7, 8, 10, 12, 14, 16, 19, 21, 24, 27, \ldots$
- Column IV: $1, 1, 2, 3, 5, 6, 9, 11, 15, 18, 23, 27, 34, 39, 47, 54, \ldots$
- Column XI starts to approach $p(n)$ for moderate $n$, since $p_{11}(n) = p(n)$ as long as $n \leq 11\cdot 12/2 = 66$ does not force a part exceeding $11$ — for $n \leq 11$ the column XI entry is the full $p(n)$.

Euler's two worked examples (§318):

- **Partitions of $50$ into $7$ unequal numbers**: by the [[partitions-into-distinct-parts|staircase bijection]] $q_7(50) = p_{\leq 7}(50 - 7\cdot 8/2) = p_{\leq 7}(22)$, read off the table at row $22$, column VII — value $522$.
- **Partitions of $50$ into $7$ numbers (equal or unequal)**: $p_{=7}(50) = p_{\leq 7}(50 - 7) = p_{\leq 7}(43)$, read at row $43$, column VII — value $8946$.

## Connection to figurate numbers (§319–§322)

The columns interact richly with the figurate numbers — already studied as [[higher-order-arithmetic-progressions]]. Using $1 - x^k = (1 - x)(1 + x + \cdots + x^{k-1})$,

$$\prod_{k=1}^m(1 - x^k) = (1 - x)^m\cdot\prod_{k=2}^m(1 + x + \cdots + x^{k-1}),$$

so the column-$m$ series factors as

$$\frac{1}{\prod_{k=1}^m(1-x^k)} = \frac{1}{(1-x)^m}\cdot\frac{1}{\prod_{k=2}^m(1 + x + \cdots + x^{k-1})}.$$

The first factor is the generating function for the **figurate numbers** $\binom{n+m-1}{m-1}$ (an order-$(m-1)$ arithmetic progression — column III's leading term is the triangular numbers $\binom{n+2}{2}$, column IV's the tetrahedral numbers $\binom{n+3}{3}$, etc.); the second factor is a polynomial correction in low-degree symmetric series. The §320–§322 schemes write each column as an iterated addition starting from the corresponding figurate-number sequence.

## Faster recurrence via the pentagonal number theorem

For the full partition function $p(n) = p_\infty(n)$, the [[eulers-pentagonal-number-theorem|pentagonal number theorem]] gives a recurrence with only $O(\sqrt n)$ terms:

$$p(n) = p(n-1) + p(n-2) - p(n-5) - p(n-7) + p(n-12) + p(n-15) - p(n-22) - p(n-26) + \cdots.$$

The recurrence above (Pascal-like, in $m$ and $n$) is the slower but column-by-column workhorse; the pentagonal-number recurrence collapses to the unrestricted partition function in a single step.

## The N = L + M rule across the table

Read horizontally: every entry equals the entry to its left plus the entry $m$ rows up in the same column. This is Euler's explicit rule (§318) and the way every printed partition table since has been computed.

## Related pages

- [[chapter-16-on-the-partition-of-numbers]]
- [[partition-of-numbers]]
- [[partition-generating-functions]]
- [[partitions-into-distinct-parts]]
- [[eulers-pentagonal-number-theorem]]
- [[recurrent-series]]
- [[higher-order-arithmetic-progressions]]
