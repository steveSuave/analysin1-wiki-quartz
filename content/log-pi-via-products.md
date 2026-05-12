# Computing log π via Infinite Products

**Summary**: §188–§190: starting from the [[wallis-product|Wallis product]] re-paired as $\pi = 4\prod_{k\ge 1}(1 - 1/(2k+1)^2)$, taking the logarithm, expanding each $\log(1 - 1/(2k+1)^2)$ via the [[logarithmic-series|§118 power series]], and transposing the resulting double sum, Euler reduces $\log\pi$ to the linear combination $\log\pi = \log 4 - (A - 1) - \tfrac12(B - 1) - \tfrac13(C - 1) - \cdots$ of the [[zeta-at-even-integers|§169 odd-square sums]] $A, B, C, \ldots$. Tabulating these to twenty digits gives $\log_e\pi = 1.144729885849400174\ldots$ and $\log_{10}\pi = 0.497149872694133854\ldots$.

**Sources**: chapter11.pdf

**Last updated**: 2026-05-01

---

## The starting product

The [[wallis-product|Wallis product]] re-paired by adjacent factors reads

$$\frac{\pi}{2} = 2\!\left(1 - \frac{1}{9}\right)\!\left(1 - \frac{1}{25}\right)\!\left(1 - \frac{1}{49}\right)\!\left(1 - \frac{1}{81}\right)\cdots$$

(source: chapter11.pdf, §188), equivalently

$$\pi = 4\prod_{k\ge 1}\!\left(1 - \frac{1}{(2k+1)^2}\right).$$

Each factor is $1 - $ small, so the logarithm is well-behaved.

## Take the log

$$\log\pi = \log 4 + \sum_{k\ge 1}\log\!\left(1 - \frac{1}{(2k+1)^2}\right) = \log 2 - \sum_{k\ge 1}\log\!\left(1 - \frac{1}{(2k)^2}\right)$$

(source: chapter11.pdf, §189; the second form rewrites Wallis with denominator $(2k)^2$ instead of $(2k+1)^2$). Both versions hold whether logarithms are common or natural; for what follows, *natural* logarithms are essential because they are the ones whose power series has no extra constant.

## Expand each log

The [[logarithmic-series|§118 series]]:

$$\log_e(1 - x) = -x - \frac{x^2}{2} - \frac{x^3}{3} - \frac{x^4}{4} - \cdots$$

Apply to $x = 1/(2k+1)^2$:

$$\log_e\!\left(1 - \frac{1}{(2k+1)^2}\right) = -\frac{1}{(2k+1)^2} - \frac{1}{2(2k+1)^4} - \frac{1}{3(2k+1)^6} - \frac{1}{4(2k+1)^8} - \cdots$$

Substituting into $\log\pi = \log 4 + \sum_k \log(\cdots)$ produces a *double sum* over $(j, k)$ where $j$ indexes the power and $k$ indexes the original product factor (source: chapter11.pdf, §190):

$$\log\pi = \log 4 + \left(-\sum_{k\ge 1}\frac{1}{(2k+1)^2}\right) + \left(-\frac{1}{2}\sum_{k\ge 1}\frac{1}{(2k+1)^4}\right) + \left(-\frac{1}{3}\sum_{k\ge 1}\frac{1}{(2k+1)^6}\right) + \cdots$$

## Transpose: the columns are odd-square sums

Reading the double sum *column by column*, each column is

$$\sum_{k\ge 1}\frac{1}{(2k+1)^{2j}} = A_j - 1$$

where

$$A_j = \sum_{k\ge 0}\frac{1}{(2k+1)^{2j}} = 1 + \frac{1}{3^{2j}} + \frac{1}{5^{2j}} + \frac{1}{7^{2j}} + \cdots$$

These are exactly the [[zeta-at-even-integers|§169 odd-square sums]], whose closed forms are known: $A_1 = \pi^2/8$, $A_2 = \pi^4/96$, $A_3 = \pi^6/960$, etc. Euler labels them $A, B, C, D, \ldots$:

$$A = 1 + \frac{1}{3^2} + \frac{1}{5^2} + \cdots,\quad B = 1 + \frac{1}{3^4} + \frac{1}{5^4} + \cdots,\quad C = 1 + \frac{1}{3^6} + \frac{1}{5^6} + \cdots,\quad\ldots$$

The transposed sum becomes

$$\boxed{\;\log\pi = \log 4 - (A - 1) - \frac{1}{2}(B - 1) - \frac{1}{3}(C - 1) - \frac{1}{4}(D - 1) - \cdots\;}$$

(source: chapter11.pdf, §190).

## Why this is fast

Each column sum $(A_j - 1)$ is dominated by the leading term $1/3^{2j}$, which decays *geometrically* in $1/9^j$. So the $j$-th term of the outer sum is bounded by $\tfrac{1}{j}\cdot\tfrac{1}{9^j}\cdot O(1)$, and twenty terms suffice for ~20 correct digits. By contrast, the original Wallis product needs ~$10^{20}$ factors for the same precision.

The trick — *take logs, expand, transpose* — converts an $O(1/N^2)$-convergent product into a doubly-summed series whose outer sum is $O(9^{-j})$. This is Chapter 11's key innovation.

## The numerical result

Euler tabulates the column sums to 18+ digits (source: chapter11.pdf, §190):

| Symbol | Value |
| --- | --- |
| $A$ | $1.2337005501369820\ldots$ |
| $B$ | $1.0146780316041921\ldots$ |
| $C$ | $1.0014470766409421\ldots$ |
| $D$ | $1.0001551790252961\ldots$ |
| $E$ | $1.0000170413630448\ldots$ |
| $F$ | $1.0000018858484583\ldots$ |
| $\vdots$ | $\vdots$ |
| $X$ | $1.0000000000000001\ldots$ |

(Symbols continue through the alphabet to where the entries flatten to $1.0\ldots$ and contribute negligibly.) Plugging into the boxed formula yields

$$\log_e\pi = 1.144729885849400174\,14342\ldots$$

(source: chapter11.pdf, §190). Multiplying by $\log_{10}e = 0.4342944819\ldots$ converts to the common log:

$$\log_{10}\pi = 0.497149872694133854\,35126\ldots$$

(source: chapter11.pdf, §190).

## Why bother with a separate $\log\pi$ table?

In Euler's day, every transcendental computation began by reaching for a table. The constant $\pi$ appears as a multiplier in countless integrals, in the law of cosines, in any series involving sines/cosines — and computing $\pi$ to 20 digits and then *taking its logarithm* by long division would be far slower than computing $\log\pi$ directly.

Euler's reasoning: the ingredients $A, B, C, \ldots$ are exactly the same odd-square sums he tabulated in [[zeta-at-even-integers|§168–§169]], and the rest of Chapter 11 (§191–§196) reuses them again for $\log\sin$ and $\log\cos$. One small table of column sums supports computations of $\log\pi$, $\log\sin(m\pi/2n)$, $\log\cos(m\pi/2n)$, $\log\tan(m\pi/2n)$, $\log\cot(m\pi/2n)$ for *every* rational angle — a major simplification of trig log table production.

## A modern reading

The transposition

$$\sum_{k\ge 1}\sum_{j\ge 1}\frac{1}{j(2k+1)^{2j}} = \sum_{j\ge 1}\frac{1}{j}\sum_{k\ge 1}\frac{1}{(2k+1)^{2j}}$$

is justified by absolute convergence (Fubini for double series) — Euler does it without comment, but the rearrangement is in fact valid here because every term is positive and the double series converges. The boxed identity is essentially the Taylor expansion of $\log\Gamma$ at $1/2$ in disguise; modern derivations use the Hurwitz zeta function.

## Related pages

- [[wallis-product]]
- [[linear-factors-of-sine-cosine]]
- [[logarithmic-series]]
- [[zeta-at-even-integers]]
- [[basel-problem]]
- [[log-sine-via-products]]
- [[pi]]
- [[characteristic-and-mantissa]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
