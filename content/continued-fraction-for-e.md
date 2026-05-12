# Continued Fraction for $e$

**Summary**: Euler runs the Euclidean algorithm on the decimal expansion of $(e - 1)/2 = 0.8591409142295\ldots$ and finds that its partial quotients form an arithmetic progression $1, 6, 10, 14, 18, 22, 26, 30, 34, \ldots$ with common difference $4$. This is the first appearance of the celebrated *simple* continued fraction for $e$, whose pattern reveals $e$'s irrationality and (with later work) its transcendence — Euler asserts it can be "confirmed by infinitesimal calculus."

**Sources**: `raw/chapter18.pdf` (§381 Example III).

**Last updated**: 2026-05-11

---

## The identity

Euler starts from $e = 2.718281828459\ldots$, so $(e - 1)/2 = 0.8591409142295\ldots$. Applying the [[euclidean-algorithm-continued-fraction|Euclidean-algorithm-based]] decimal-to-CF method (§381) to $\;0.8591409142295 = 8591409142295/10000000000000$:

$$\begin{aligned}
10000000000000/\,8591409142295 &= 1 + 1408590857704/8591409142295 \\
8591409142295/1408590857704 &= 6 + 139863996071/1408590857704 \\
1408590857704/\,139863996071 &= 10 + 9950896994/139863996071 \\
139863996071/\,9950896994 &= 14 + 551438155/9950896994 \\
9950896994/\,551438155 &= 18 + 25010204/551438155 \\
551438155/\,25010204 &= 22 + 1213667/25010204\quad\text{etc.}
\end{aligned}$$

The partial quotients are $1, 6, 10, 14, 18, 22, \ldots$. Euler observes that if the starting decimal had been more accurate the next quotients would be $26, 30, 34, \ldots$ — an *arithmetic progression* with first term $1$ and common difference $4$ (after the initial $0$ from the integer part of $(e-1)/2$). So

$$\boxed{\ \frac{e - 1}{2} = \cfrac{1}{1 + \cfrac{1}{6 + \cfrac{1}{10 + \cfrac{1}{14 + \cfrac{1}{18 + \cfrac{1}{22 + \cdots}}}}}}\ }$$

with partial quotients $1, 6, 10, 14, 18, 22, 26, 30, 34, \ldots$.

## Equivalent forms

The same pattern (proven rigorously by Euler in 1737 via the Riccati equation, and asserted here as "this result can be confirmed by infinitesimal calculus") generates the more familiar modern form

$$e = [2;\, 1, 2, 1,\, 1, 4, 1,\, 1, 6, 1,\, 1, 8, 1, \ldots]$$

— partial quotients $2$ followed by the pattern $1, 2k, 1$ for $k = 1, 2, 3, \ldots$. The $(e-1)/2$ form Euler gives in the *Introductio* is the "cleaner" one because its quotients form a single arithmetic progression rather than an interleaved one.

## Significance

1. **Irrationality**. An infinite simple continued fraction whose partial quotients are unbounded represents an irrational number. The AP pattern proves $e \notin \mathbb{Q}$ immediately. (Lambert in 1761 used a similar CF for $\tan x$ to prove $\pi \notin \mathbb{Q}$.)
2. **First non-trivial transcendental constant with explicit CF pattern**. The discovery that an analytic constant born from limits ($e = \lim(1 + 1/j)^j$, [[eulers-number|§122]]) has such a tightly structured arithmetic continued-fraction expansion was a strong hint that $e$ is not merely irrational but transcendental — proved by Hermite in 1873.
3. **Euler's empirical → analytic style**. Euler discovers the AP pattern by *running the Euclidean algorithm on a 13-digit decimal expansion* and noticing the quotients are $1, 6, 10, 14, 18, 22$ — then extrapolates. This is the same empirical-then-prove pattern as the [[eulers-pentagonal-number-theorem|pentagonal number theorem]] (§323) and the [[basel-problem|Basel problem]] (§167).

## Related pages

- [[eulers-number]] — the constant $e = 2.71828\ldots$, first appearance in §122
- [[euclidean-algorithm-continued-fraction]] — the decimal-to-CF method that produced the AP pattern
- [[exponential-series]] — alternating series for $1/e$ used in the §370 (different) CF derivation of $1/(e-1)$
- [[continued-fraction-series-equivalence]] — the §370 template gives a different (numerator $\neq 1$) CF for $1/(e-1)$
- [[chapter-18-on-continued-fractions]]
