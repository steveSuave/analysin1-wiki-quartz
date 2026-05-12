# Divergence of Prime Reciprocals

**Summary**: §278–§280. Euler's proof that $\sum_p 1/p = \infty$ — the sum of reciprocals of the primes diverges. Taking the natural logarithm of the [[euler-product-formula|Euler product]] at $n = 1$ and expanding by the [[logarithmic-series|§118 series]] gives a double sum in which all but the first inner series are finite, forcing the prime-reciprocal series itself to be infinite. This is the first quantitative refinement of Euclid's theorem.

**Sources**: chapter15.pdf

**Last updated**: 2026-05-11

---

## The setup (§278)

Starting from the [[euler-product-formula|Euler product]]

$$M = \sum_{k=1}^{\infty}\frac{1}{k^n} = \prod_{p\text{ prime}}\frac{1}{1-1/p^n},$$

take natural logs and apply the §118 [[logarithmic-series|expansion]] $-\log(1-x) = x + x^2/2 + x^3/3 + \cdots$ to each factor:

$$\log M = \sum_{p}\left(\frac{1}{p^n} + \frac{1}{2 p^{2n}} + \frac{1}{3 p^{3n}} + \frac{1}{4 p^{4n}} + \cdots\right).$$

Rearranging by the power of $p$ in the denominator (Euler **transposes the double sum** the way he does in [[log-pi-via-products|§188]] and [[log-sine-via-products|§191]]):

$$\log M = \sum_{k=1}^{\infty}\frac{1}{k}\sum_{p}\frac{1}{p^{kn}} = \sum_{k=1}^{\infty}\frac{S(kn)}{k},$$

where $S(m) := \sum_p 1/p^m$ is the **prime zeta** sum. Explicitly,

$$\log M = 1\cdot S(n) + \tfrac{1}{2}\,S(2n) + \tfrac{1}{3}\,S(3n) + \tfrac{1}{4}\,S(4n) + \cdots$$

## The divergence proof at $n = 1$ (§279)

At $n = 1$: $M = 1 + 1/2 + 1/3 + 1/4 + \cdots = \log\infty$ (the harmonic series, divergent), and Euler had earlier identified $\zeta(2) = M(n=2) = \pi^2/6$. With $n = 1$ the transposed identity becomes (after first separating the $k=1$ piece from the $k \geq 2$ pieces, and using the $n = 2$ Euler product to relate $S(2)$ to $\pi^2/6$ via $\log N = \log(\pi^2/6) = S(2) + S(4)/2 + S(6)/3 + \cdots$ which is therefore finite, hence $S(2k) < \infty$ for every $k$):

$$\log\log\infty - \tfrac12\log\tfrac{\pi^2}{6} = S(1) + \tfrac{1}{3}S(3) + \tfrac{1}{5}S(5) + \tfrac{1}{7}S(7) + \cdots$$

(see §279 for the precise grouping). Every inner sum $S(3), S(5), S(7), \ldots$ is finite (bounded above by the corresponding $\zeta(k)$, hence by $\sum 1/k^3 < 2$, etc., and Euler tabulates them at [[prime-zeta-values|§282]]). So the right side equals

$$S(1) + (\text{a finite real number}).$$

The left side is $\log\log\infty - \frac{1}{2}\log(\pi^2/6)$, which is $\log\log\infty - 0.249\ldots$, i.e. **infinite**. Therefore

$$\boxed{S(1) = \frac{1}{2} + \frac{1}{3} + \frac{1}{5} + \frac{1}{7} + \frac{1}{11} + \frac{1}{13} + \cdots = \infty.}$$

Euler's exact phrasing (source: chapter15.pdf, §279):

> "But these series, except for the first ones, not only have finite sums, but the sum of all of them taken together is still finite, and reasonably small. It follows that the first series $\tfrac12 + \tfrac13 + \tfrac15 + \tfrac17 + \cdots$ has an infinite sum."

## Comparison with Euclid

Euclid proved (Elements IX.20) that the number of primes is infinite. Euler's result is strictly stronger: not only are there infinitely many primes, but **they are dense enough that the sum of their reciprocals diverges**.

To contextualise the density:

| Series | Sum |
|---|---|
| $\sum 1/k$ | $\infty$ (logarithmic) |
| $\sum 1/p$ | $\infty$ (loglog, by Mertens) |
| $\sum 1/k^2$ | $\pi^2/6$ (finite) |
| $\sum 1/p^2$ | $0.4522\ldots$ (finite, see [[prime-zeta-values]]) |

So $\{p\}$ has density strictly between $\{k^2\}$ and $\{k\}$. The growth rate of $\sum_{p\le x} 1/p$ is $\log\log x + M + o(1)$ where $M = 0.2614\ldots$ is the **Mertens constant** — a result of Mertens (1874) that quantifies Euler's qualitative divergence.

## At $n = 2$: a closed expression for $\sum 1/p^2 + \cdots$ (§280)

The same identity at $n = 2$ gives the convergent statement

$$2\log\pi - \log 6 = S(2) + \tfrac{1}{2}\,S(4) + \tfrac{1}{3}\,S(6) + \cdots$$

(since $\log M = \log(\pi^2/6) = 2\log\pi - \log 6$). At $n = 4$ similarly

$$4\log\pi - \log 90 = S(4) + \tfrac{1}{2}\,S(8) + \tfrac{1}{3}\,S(12) + \cdots$$

Euler also displays the combination $\log M - \tfrac{1}{2}\log N$ that isolates **odd** prime-power contributions:

$$\log M - \tfrac12\log N = S(n) + \tfrac{1}{3}S(3n) + \tfrac{1}{5}S(5n) + \cdots,$$

useful because the right side has all $S$ at odd multiples of $n$ only — exactly the inputs needed for the closed-form $\zeta(2k)$ machinery of [[basel-problem|Chapter 10]]. Specialised at $n = 2$, this is $\tfrac12\log(5/2)$ in §280; at $n = 1$ it gives the divergence statement.

## A second look at the proof structure

Euler's argument has the following four ingredients:

1. **Euler product**: $\zeta(n) = \prod (1-1/p^n)^{-1}$. (§274; see [[euler-product-formula]])
2. **Logarithmic series**: $-\log(1-x) = x + x^2/2 + \cdots$. (§118; see [[logarithmic-series]])
3. **Transposition** of the double sum $\sum_p\sum_k$ to $\sum_k\sum_p$.
4. **Boundedness of inner sums**: $S(kn) < \zeta(kn) < \infty$ for $kn \geq 2$.

The last ingredient is the part that "lets divergence escape" — if $\zeta(n)$ is finite for $n \geq 2$ but infinite at $n = 1$, the only inner sum free to absorb the infinity is $S(n) = S(1)$.

## Significance

Together with the [[basel-problem|Basel problem]], this is the *Introductio*'s most striking number-theoretic result. It marks the birth of **analytic number theory**: an analytic identity (logarithm of a product) is used to deduce a combinatorial fact (density of primes). The pattern — relate a Dirichlet series to a product over primes, then take logs and pull out information — drives:

- Dirichlet's theorem (1837) on primes in arithmetic progressions, via $L(1, \chi) \neq 0$.
- Mertens' theorems (1874) on the asymptotics of $\sum_{p \le x} 1/p$.
- The Prime Number Theorem (Hadamard, de la Vallée Poussin, 1896), via $\zeta(1 + it) \neq 0$.
- The Riemann Hypothesis, which would sharpen all of the above.

Euler's quantitative phrase "reasonably small" (the finite tail in §279) anticipates the modern Mertens constant.

## Related pages

- [[chapter-15-on-series-which-arise-from-products]]
- [[euler-product-formula]]
- [[prime-zeta-values]]
- [[squarefree-and-mobius-series]]
- [[logarithmic-series]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[log-pi-via-products]]
- [[log-sine-via-products]]
