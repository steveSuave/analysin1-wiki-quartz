# Euler's Pentagonal Number Theorem

**Summary**: The infinite product $\prod_{k\geq 1}(1 - x^k)$ has nearly all coefficients zero. The surviving exponents are the **generalized pentagonal numbers** $(3n^2 \pm n)/2$, and the corresponding coefficient is $(-1)^n$. Compactly, $\prod_{k\geq 1}(1 - x^k) = \sum_{n\in\mathbb Z}(-1)^n x^{n(3n-1)/2}$. The identity gives an $O(\sqrt n)$-term recurrence for the [[partition-of-numbers|partition function]] $p(n)$.

**Sources**: chapter16

**Last updated**: 2026-05-11

---

## Statement (§323)

$$\prod_{k\geq 1}(1 - x^k) = 1 - x - x^2 + x^5 + x^7 - x^{12} - x^{15} + x^{22} + x^{26} - x^{35} - x^{40} + x^{51} + x^{57} - \cdots.$$

The exponents form the sequence $1, 2, 5, 7, 12, 15, 22, 26, 35, 40, 51, 57, \ldots$ — the **generalized pentagonal numbers** $g_n = n(3n-1)/2$ for $n = \pm 1, \pm 2, \pm 3, \ldots$, i.e. the numbers $(3n^2 \pm n)/2$ for $n \geq 1$ (source: chapter16, §323).

The sign of $x^{(3n^2 \pm n)/2}$ is $(-1)^n$: positive when $n$ is even, negative when $n$ is odd. Compactly,

$$\prod_{k\geq 1}(1 - x^k) = \sum_{n\in\mathbb Z}(-1)^n x^{n(3n-1)/2}.$$

## Euler's discovery (§323)

Euler arrived at the identity **empirically**: he expanded the product and noticed that the surviving exponents fit the pattern $(3n^2 \pm n)/2$. His statement (§323):

> "the only exponents which appear are of the form $3n^2 \pm n)/2$ and the sign of the corresponding term is negative when $n$ is odd, and the sign is positive when $n$ is even."

He gives **no proof** here. The first proof would come twenty years later in his 1750 paper *Découverte d'une loi tout extraordinaire des nombres par rapport à la somme de leurs diviseurs* and in a 1751 letter to Goldbach. The classical proof uses telescoping arguments on partial products; modern proofs (Sylvester, Franklin) give an explicit bijection on partitions.

## The induced recurrence for $p(n)$ (§324)

The product $\prod(1 - x^k)$ is the **reciprocal** of the partition generating function:

$$\sum_{n\geq 0} p(n)\,x^n = \frac{1}{\prod_{k\geq 1}(1 - x^k)}.$$

So multiplying both sides of $\bigl(\sum p(n) x^n\bigr)\cdot\bigl(\prod(1 - x^k)\bigr) = 1$ and matching the coefficient of $x^n$ for $n \geq 1$:

$$p(n) - p(n-1) - p(n-2) + p(n-5) + p(n-7) - p(n-12) - p(n-15) + \cdots = 0,$$

or equivalently

$$p(n) = \sum_{k \geq 1}(-1)^{k+1}\bigl[p\!\bigl(n - \tfrac{k(3k-1)}{2}\bigr) + p\!\bigl(n - \tfrac{k(3k+1)}{2}\bigr)\bigr].$$

The number of non-zero terms is $O(\sqrt n)$ — only those $k$ with $k(3k-1)/2 \leq n$. Worked examples:

- $p(7) = p(6) + p(5) - p(2) - p(0) = 11 + 7 - 2 - 1 = 15$. The fifteen partitions of $7$ are listed in §324: $7, 6+1, 5+2, 5+1+1, 4+3, 4+2+1, 4+1+1+1, 3+3+1, 3+2+2, 3+2+1+1, 3+1+1+1+1, 2+2+2+1, 2+2+1+1+1, 2+1+1+1+1+1, 1+1+1+1+1+1+1$.
- $p(10) = p(9) + p(8) - p(5) - p(3) = 30 + 22 - 7 - 3 = 42$.
- $p(15) = p(14) + p(13) - p(10) - p(8) + p(3) + p(0) = 135 + 101 - 42 - 22 + 3 + 1 = 176$.

This is the **fastest classical recurrence** for the partition function, and the one Euler implicitly uses to extend the table beyond what column-by-column computation provides.

## The scale of the relation

Viewed as a [[recurrent-series|recurrent series]], $\sum p(n) x^n$ has [[scale-of-the-relation|scale of the relation]]

$$(+1, +1, 0, 0, -1, 0, -1, 0, 0, 0, 0, +1, 0, 0, +1, 0, 0, 0, 0, 0, 0, -1, 0, 0, 0, -1, 0, 0, 0, 0, 0, 0, 0, 0, +1, \ldots),$$

with non-zero entries at positions $(3k^2 \pm k)/2$. Although the scale is infinite, only $O(\sqrt n)$ entries are consulted to compute any given term — a unique feature among classical recurrences.

## Why "pentagonal"

The classical **pentagonal numbers** $P_n = n(3n - 1)/2$ for $n \geq 1$ are $1, 5, 12, 22, 35, 51, \ldots$ — they count dots in nested pentagons, analogous to triangular numbers counting dots in nested triangles. The "**generalized pentagonal numbers**" extend the formula to $n = -1, -2, \ldots$, giving the intermediate values $P_{-1} = 2, P_{-2} = 7, P_{-3} = 15, P_{-4} = 26, \ldots$.

## Connection to theta functions (anachronistic)

The identity $\prod(1 - x^k) = \sum(-1)^n x^{n(3n-1)/2}$ is the first nontrivial **theta function identity**. The right-hand side is essentially the **Dedekind eta function** $\eta(\tau)$: setting $x = e^{2\pi i\tau}$,

$$\eta(\tau) = x^{1/24}\prod_{k\geq 1}(1 - x^k).$$

The pentagonal-number vanishing pattern is the first hint of $\eta$'s modular structure, which was eventually elucidated by Jacobi a century later. Euler had no such language; he reports a beautiful empirical pattern.

## Use in the chapter

§325–§327 use the pentagonal expansion of $P = \prod(1 - x^k)$ together with $PQ = \prod(1 - x^{2k})$ — which is just $P$ evaluated at $x^2$ — to **derive the series for $q(n)$ (partitions into distinct parts)** from $p(n)$. See [[distinct-parts-equals-odd-parts]].

## Related pages

- [[chapter-16-on-the-partition-of-numbers]]
- [[partition-of-numbers]]
- [[partition-generating-functions]]
- [[partition-recurrence]]
- [[distinct-parts-equals-odd-parts]]
- [[recurrent-series]]
- [[scale-of-the-relation]]
