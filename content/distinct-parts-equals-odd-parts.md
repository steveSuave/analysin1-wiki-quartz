# Distinct Parts Equals Odd Parts

**Summary**: Euler's theorem (§326): the number of partitions of $n$ into distinct (unequal) parts equals the number of partitions of $n$ into odd parts (with repetition allowed). The generating-function proof is one line: $\prod_{k\geq 1}(1 + x^k) = \prod_{k\geq 1}1/(1 - x^{2k - 1})$.

**Sources**: chapter16.pdf

**Last updated**: 2026-05-11

---

## Statement

For every positive integer $n$,

$$q(n) = q_{\text{odd}}(n),$$

where $q(n)$ is the number of partitions of $n$ into **distinct** positive parts and $q_{\text{odd}}(n)$ is the number of partitions of $n$ into **odd** parts (with repetition allowed). (Source: chapter16.pdf, §326.)

## Generating-function proof (§325–§326)

Let

$$P = \prod_{k\geq 1}(1 - x^k),\qquad Q = \prod_{k\geq 1}(1 + x^k).$$

Pairing $(1 - x^k)(1 + x^k) = 1 - x^{2k}$:

$$PQ = \prod_{k\geq 1}(1 - x^{2k}).$$

Dividing,

$$\frac{1}{Q} = \frac{P}{PQ} = \frac{\prod_{k\geq 1}(1 - x^k)}{\prod_{k\geq 1}(1 - x^{2k})}.$$

The numerator includes one factor for each $k \geq 1$; the denominator only for even $k$. Cancellation leaves only the odd factors in the numerator:

$$\frac{1}{Q} = \prod_{k\geq 1}(1 - x^{2k - 1}),\qquad\text{so}\qquad Q = \prod_{k\geq 1}\frac{1}{1 - x^{2k-1}}.$$

The left side $Q = \prod(1 + x^k) = \sum_n q(n) x^n$ enumerates partitions into **distinct** parts.

The right side $\prod 1/(1 - x^{2k-1})$ expands as

$$\prod_{k\geq 1}(1 + x^{2k-1} + x^{2(2k-1)} + x^{3(2k-1)} + \cdots),$$

so the coefficient of $x^n$ is the number of ways to write $n$ as $\sum_k m_k(2k-1)$ with $m_k \geq 0$ — i.e. as a sum of odd parts with repetition allowed.

Equating coefficients of $x^n$ proves the theorem.

## Worked example for $n = 9$ (§325)

**Distinct partitions** (eight, from §325):

$$9 = 8+1 = 7+2 = 6+3 = 6+2+1 = 5+4 = 5+3+1 = 4+3+2.$$

**Odd partitions** of $9$ (eight):

$$9 = 7+1+1 = 5+3+1 = 5+1+1+1+1 = 3+3+3 = 3+3+1+1+1 = 3+1+1+1+1+1+1 = 1+1+1+1+1+1+1+1+1.$$

Both counts are $8 = q(9)$.

## Application to computing $q(n)$ via the pentagonal theorem (§327)

Combining with [[eulers-pentagonal-number-theorem|Euler's pentagonal theorem]] one can compute $q(n)$ from $p(n)$:

$$Q = \frac{\prod_{k\geq 1}(1 - x^{2k})}{\prod_{k\geq 1}(1 - x^k)} = \bigl(\sum_n p(n) x^n\bigr)\cdot\bigl(1 - x^2 - x^4 + x^{10} + x^{14} - x^{24} - x^{30} + \cdots\bigr),$$

where the second factor is the pentagonal-number expansion of $P$ evaluated at $x^2$, so the surviving exponents are $2\cdot(3n^2 \pm n)/2 = 3n^2 \pm n$.

Multiplying the two series term by term gives §327's listing:

$$Q = 1 + x + x^2 + 2x^3 + 2x^4 + 3x^5 + 4x^6 + 5x^7 + 6x^8 + 8x^9 + 10x^{10} + 12x^{11} + \cdots.$$

## Bijective proof (anachronistic — Glaisher 1883)

Euler proved the theorem only as an algebraic identity. The classical bijection (Glaisher) makes the equality combinatorially explicit:

- **Odd → distinct**: group equal parts of an odd partition by powers of $2$. If an odd part $a$ appears $m$ times, write $m$ in binary $m = 2^{i_1} + 2^{i_2} + \cdots$ and replace the $m$ copies of $a$ by the distinct parts $a\cdot 2^{i_1}, a\cdot 2^{i_2}, \ldots$. (These are distinct because of the uniqueness of binary representation — see [[binary-representation-theorem]].)

- **Distinct → odd**: write each distinct part as $a = a_{\text{odd}}\cdot 2^k$ and split into $2^k$ copies of the odd factor $a_{\text{odd}}$.

The two maps are inverse, giving an explicit bijection.

## Modern reading

This is the simplest case of a **partition identity**: a statement that the number of partitions of $n$ from one class equals the number from another. The pattern has spawned a vast subject (Rogers–Ramanujan identities, Schur identities, Andrews's theory), all anchored on Euler's distinct-vs-odd prototype.

## Related pages

- [[chapter-16-on-the-partition-of-numbers]]
- [[partition-of-numbers]]
- [[partition-generating-functions]]
- [[partitions-into-distinct-parts]]
- [[eulers-pentagonal-number-theorem]]
- [[partition-recurrence]]
- [[binary-representation-theorem]]
