# Odd and Alternating Zeta Decomposition

**Summary**: §170: from the full sum $M = 1 + 1/2^n + 1/3^n + \cdots$, the four basic variants — even-only, odd-only, alternating — fall out by elementary algebra. The mechanism that converts any closed form for $\zeta(n)$ into closed forms for $\sum 1/(2k)^n$, $\sum 1/(2k+1)^n$, and $\sum (-1)^{k+1}/k^n$.

**Sources**: chapter10

**Last updated**: 2026-04-30

---

## The decomposition

Let

$$M = 1 + \frac{1}{2^n} + \frac{1}{3^n} + \frac{1}{4^n} + \frac{1}{5^n} + \cdots = \zeta(n).$$

Multiplying through by $1/2^n$:

$$\frac{M}{2^n} = \frac{1}{2^n} + \frac{1}{4^n} + \frac{1}{6^n} + \frac{1}{8^n} + \cdots\quad\text{(even terms only)}.$$

Subtracting:

$$M - \frac{M}{2^n} = \frac{2^n - 1}{2^n}\,M = 1 + \frac{1}{3^n} + \frac{1}{5^n} + \frac{1}{7^n} + \cdots\quad\text{(odd terms only)}.$$

Subtracting twice over:

$$M - \frac{2M}{2^n} = \frac{2^{n-1} - 1}{2^{n-1}}\,M = 1 - \frac{1}{2^n} + \frac{1}{3^n} - \frac{1}{4^n} + \frac{1}{5^n} - \cdots\quad\text{(alternating)}.$$

(source: chapter10, §170). Euler's comment: "If $n$ is an even number and the sum is $A\pi^n$, then $A$ will be a rational number" — i.e. the rationality result of [[zeta-at-even-integers]] propagates through all four variants.

## Worked tabulation

For $n = 2$, with $M = \pi^2/6$ ([[basel-problem|Basel]]):

| series | sum |
|---|---|
| all $1/k^2$  | $\pi^2/6$ |
| even $1/(2k)^2$ | $\pi^2/24$ |
| odd $1/(2k+1)^2$ | $\pi^2/8$ |
| alternating $\sum(-1)^{k+1}/k^2$ | $\pi^2/12$ |

The odd-terms-only result $\pi^2/8$ recovers the value computed independently in §169 from the [[cosine-infinite-product|cosh product]] — an internal consistency check.

For $n = 4$, with $M = \pi^4/90$:

| series | sum |
|---|---|
| all $1/k^4$  | $\pi^4/90$ |
| even $1/(2k)^4$ | $\pi^4/1440$ |
| odd $1/(2k+1)^4$ | $\pi^4/96$ |
| alternating $\sum(-1)^{k+1}/k^4$ | $7\pi^4/720$ |

## Why this matters

The decomposition is purely formal: it does not depend on the closed form of $M$. Whatever methods evaluate $M$ — Newton's identities on the [[sine-infinite-product|sine product]], coefficient comparison, or anything else — the same closed form propagates to the even, odd, and alternating restrictions by linear algebra.

A consequence Euler exploits later: every zeta-style series can be split into "divisible by $p$" and "not divisible by $p$" parts using the same trick with $1/p^n$ in place of $1/2^n$. §177 splits by $1/3$, e.g.

$$\sum_{k\,\text{not divisible by }3}\frac{1}{k^2} = \frac{\pi^2}{6} - \sum_{k\ge 1}\frac{1}{(3k)^2} = \frac{\pi^2}{6} - \frac{\pi^2}{54} = \frac{8\pi^2}{54} = \frac{4\pi^2}{27}.$$

This is the seed of an important tool: writing the zeta function as an Euler product over primes.

## Modern footnote: Dirichlet $L$-functions and the Euler product

The four decompositions are the simplest case of a general principle. For any **Dirichlet character** $\chi$ mod $m$, the series $\sum_{n\ge 1}\chi(n)/n^s$ defines a Dirichlet $L$-function. The $\chi = $ trivial character recovers $\zeta(s)$; the principal character mod $2$ recovers Euler's odd-only sum; the non-trivial character mod $4$ recovers the Leibniz-style alternating series. The decomposition

$$\zeta(s) = \prod_p\frac{1}{1 - p^{-s}}$$

(the Euler product) is the systematic version of the §170 "subtract the multiples of $p$" trick. Euler's manipulations in §170 and §177 are early instances of the prime-factorization viewpoint that became foundational under Dirichlet (1837) and Riemann (1859).

## Related pages

- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[newtons-identities]]
- [[circular-arc-series]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
