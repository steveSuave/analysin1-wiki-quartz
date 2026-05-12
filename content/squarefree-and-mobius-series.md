# Squarefree and Möbius Series

**Summary**: §267–§269. With primes (or reciprocals of prime powers) used as the factors in $\prod(1\pm\alpha_i)$, the multiplied-out series characterises **squarefree numbers**: each squarefree natural number appears exactly once, every number divisible by a square is missing, and the negative-factor variant attaches **Möbius-style signs** to each term by the parity of its prime-factor count.

**Sources**: chapter15.pdf

**Last updated**: 2026-05-11

---

## The squarefree characterisation (§267)

Substituting the primes $\alpha = 2, \beta = 3, \gamma = 5, \delta = 7, \ldots$ into the product

$$P = (1+2)(1+3)(1+5)(1+7)(1+11)(1+13)\cdots$$

and expanding gives, by [[chapter-15-on-series-which-arise-from-products|§264]],

$$P = 1 + 2 + 3 + 5 + 6 + 7 + 10 + 11 + 13 + 14 + 15 + \cdots,$$

the sum over $1$ and all distinct **products of distinct primes**. Equivalently, $P$ contains every **squarefree** natural number and excludes every integer divisible by the square of a prime. Euler notes (source: chapter15.pdf, §267):

> "The series lacks the numbers 4, 8, 9, 12, 16, 18 since they are either powers, as 4, 8, 9, 16, or divisible by powers, as 12, 18."

The product diverges to $\infty$, but the bookkeeping is exact term-by-term.

## Reciprocal-prime-power version (§268)

With $\alpha_i = 1/p_i^n$ the analogous identity is

$$\prod_{p\text{ prime}}\Bigl(1+\frac{1}{p^n}\Bigr) = 1 + \frac{1}{2^n} + \frac{1}{3^n} + \frac{1}{5^n} + \frac{1}{6^n} + \frac{1}{7^n} + \frac{1}{10^n} + \frac{1}{11^n} + \cdots,$$

where the sum runs over **squarefree** $k$ in the denominators. For $n \geq 2$ both sides converge; the missing terms are exactly the indices divisible by a square. In modern notation,

$$\prod_p\Bigl(1+\frac{1}{p^n}\Bigr) = \sum_{k\text{ squarefree}}\frac{1}{k^n} = \frac{\zeta(n)}{\zeta(2n)}.$$

## Möbius signs (§269)

Switching to negative factors,

$$\prod_p\Bigl(1-\frac{1}{p^n}\Bigr) = 1 - \frac{1}{2^n} - \frac{1}{3^n} - \frac{1}{5^n} + \frac{1}{6^n} - \frac{1}{7^n} + \frac{1}{10^n} - \frac{1}{11^n} + \frac{1}{15^n} - \cdots$$

The sign rule is purely combinatorial (source: chapter15.pdf, §269):

> "Terms with primes, or products of three different primes, or any product of an odd number of different primes, appear with a negative sign. Those terms in which the product of two, four, six, or any even number of different primes, appear with a positive sign."

This is the **Möbius function** $\mu(k)$ in disguise:

$$\prod_p\Bigl(1-\frac{1}{p^n}\Bigr) = \sum_{k=1}^{\infty}\frac{\mu(k)}{k^n}.$$

Euler's example: $1/30^n$ has sign $-$ since $30 = 2\cdot 3\cdot 5$ is the product of three different primes. The term $1/4^n$ does not appear at all since 4 is divisible by $2^2$ (only **squarefree** denominators occur).

## The reciprocal relation (§275)

By [[euler-product-formula|§274's]] reciprocal product expansion,

$$\frac{1}{\prod_p(1-1/p^n)} = \sum_{k=1}^{\infty}\frac{1}{k^n} = \zeta(n).$$

Multiplying the two products gives $P\cdot Q = 1$ where

- $P = \prod(1-1/p^n) = \sum \mu(k)/k^n$,
- $Q = \prod(1-1/p^n)^{-1} = \sum 1/k^n = \zeta(n)$.

Hence $\zeta(n)\cdot\sum\mu(k)/k^n = 1$, i.e. $\sum \mu(k)/k^n = 1/\zeta(n)$.

Worked numerically (§277, "Example I"–"Example III") at $n = 2, 4$:

$$\sum_{k=1}^{\infty}\frac{\mu(k)}{k^2} = \frac{6}{\pi^2},\qquad \sum_{k=1}^{\infty}\frac{\mu(k)}{k^4} = \frac{90}{\pi^4}.$$

The §276 version with $+$ factors gives the parallel pair $\sum \mu(k)/k^n$ over squarefree $k$ (which is the same as the §269 series since $\mu(k) = 0$ on non-squarefree $k$).

## The qualitative picture

The three products

| Product | Series | Meaning |
|---|---|---|
| $\prod(1+\tfrac{1}{p^n})$ | $\sum_{k\text{ squarefree}}\tfrac{1}{k^n}$ (all $+$) | sum over squarefree integers |
| $\prod(1-\tfrac{1}{p^n})$ | $\sum_{k}\tfrac{\mu(k)}{k^n}$ (signed) | Möbius-signed sum |
| $\prod(1-\tfrac{1}{p^n})^{-1}$ | $\sum_{k\ge 1}\tfrac{1}{k^n} = \zeta(n)$ | sum over all integers |

express the three basic identities of multiplicative number theory at the level of formal series. The first two come from the §264 finite-product expansion; the third — the Euler product — from the §270 reciprocal expansion that allows repeated factors.

## Related pages

- [[chapter-15-on-series-which-arise-from-products]]
- [[euler-product-formula]]
- [[divergence-of-prime-reciprocals]]
- [[prime-zeta-values]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
