# Computing log sin and log cos via Infinite Products

**Summary**: §191–§198: applying the same "take logs, expand, transpose" recipe of [[log-pi-via-products|§188–§190]] to the [[linear-factors-of-sine-cosine|§184 sine and cosine products]] yields rapidly convergent series for $\log\sin(m\pi/2n)$ and $\log\cos(m\pi/2n)$. The columns of the transposed double sum are the [[zeta-at-even-integers|§169 odd-square sums]] $A, B, C, \ldots$ and the analogous sums $\alpha, \beta, \gamma, \ldots$ over even integers. With these tabulated once, the natural and common logarithms of every trig function at every rational angle become a few additions away. §197–§198 give a faster alternative for $\tan, \cot$ via the [[cotangent-partial-fraction|§181 partial fractions]].

**Sources**: chapter11

**Last updated**: 2026-05-01

---

## The setup

The [[linear-factors-of-sine-cosine|§184 products]] applied to $z = m\pi/(2n)$ in the original §158 quadratic-factor form (not yet linearized) read

$$\sin\frac{m\pi}{2n} = \frac{m\pi}{2n}\!\left(1 - \frac{m^2}{4n^2}\right)\!\left(1 - \frac{m^2}{16n^2}\right)\!\left(1 - \frac{m^2}{36n^2}\right)\cdots$$

$$\cos\frac{m\pi}{2n} = \!\left(1 - \frac{m^2}{n^2}\right)\!\left(1 - \frac{m^2}{9n^2}\right)\!\left(1 - \frac{m^2}{25n^2}\right)\cdots$$

— the §158 forms restricted to rational angles. (One could also start from the linearized §184 forms; Euler uses the quadratic forms here because they keep the bookkeeping symmetric.)

## Take the log

For the sine — replacing the awkward $m\pi/2n$ leading factor by $\log m + \log(2n - m) + \log(2n + m) - 3\log n + \log\pi - \log 8$ via the linear factors, then logarithming the rest:

$$\log\sin\frac{m\pi}{2n} = \log m + \log(2n - m) + \log(2n + m) - 3\log n + \log\pi - \log 8 + \sum_{k\ge 1}\log\!\left(1 - \frac{m^2}{(2k+1)^2 n^2}\right) - \sum_{k\ge 1}\frac{m^2/4n^2 + \cdots}{}\ldots$$

(source: chapter11, §191; the algebra of the lead term is finicky but not deep). Similarly for cosine:

$$\log\cos\frac{m\pi}{2n} = \log(n - m) + \log(n + m) - 2\log n - \frac{m^2}{9n^2}\big[\cdots\big] - \cdots$$

## Expand each log via the §118 series

$$\log\!\left(1 - \frac{m^2}{(kn)^2}\right) = -\frac{m^2}{k^2 n^2} - \frac{m^4}{2k^4 n^4} - \frac{m^6}{3k^6 n^6} - \cdots$$

Substituting and summing over $k$ produces a double sum in which $j$ indexes the power and $k$ the original product factor. Transposing — sum first over $k$, holding $j$ fixed — the columns become reciprocal-power sums.

## The two tables of column sums

Two distinct sets of columns appear, depending on whether the denominator runs over odd integers or all positive integers:

**Odd integers** (from the cosine product factors at odd denominators $(2k+1)n$, *and* from the linear-factor cosine):

$$A = \sum_{k\ge 0}\frac{1}{(2k+1)^2} = \frac{\pi^2}{8},\quad B = \sum_{k\ge 0}\frac{1}{(2k+1)^4} = \frac{\pi^4}{96},\quad C = \sum_{k\ge 0}\frac{1}{(2k+1)^6} = \frac{\pi^6}{960},\quad\ldots$$

**Even integers** (from the sine product factors at even denominators $2kn$):

$$\alpha = \sum_{k\ge 1}\frac{1}{(2k)^2} = \frac{\pi^2}{24},\quad \beta = \sum_{k\ge 1}\frac{1}{(2k)^4} = \frac{\pi^4}{1440},\quad \gamma = \sum_{k\ge 1}\frac{1}{(2k)^6} = \frac{\pi^6}{60480},\quad\ldots$$

Both sets are [[zeta-at-even-integers|§169 sums]], differing by the factors $(1 - 2^{-2j})\zeta(2j)$ vs $2^{-2j}\zeta(2j)$. Euler tabulates both to 16+ digits (source: chapter11, §193). Note that $A_j + 2^{-2j}\zeta(2j) = \zeta(2j)$ provides an internal consistency check.

## The boxed result for sine

$$\boxed{\;\log\sin\frac{m\pi}{2n} = \log m + \log(2n - m) + \log(2n + m) - 3\log n + \log\pi - \log 8 - \frac{m^2}{n^2}\!\left(\alpha - \frac{1}{2^2}\right) - \frac{m^4}{2 n^4}\!\left(\beta - \frac{1}{2^4}\right) - \frac{m^6}{3 n^6}\!\left(\gamma - \frac{1}{2^6}\right) - \cdots\;}$$

(source: chapter11, §192–§194). The "$- 1/4^j$" subtraction inside each $\alpha, \beta, \ldots$ accounts for the $k = 1$ term of the all-integer even-power sum being absent (it is folded into the closed-form lead $\log m + \log(2n - m) + \log(2n + m) - 3\log n + \log\pi - \log 8$).

## The boxed result for cosine

$$\boxed{\;\log\cos\frac{m\pi}{2n} = \log(n - m) + \log(n + m) - 2\log n - \frac{m^2}{n^2}(A - 1) - \frac{m^4}{2n^4}(B - 1) - \frac{m^6}{3n^6}(C - 1) - \cdots\;}$$

(source: chapter11, §192–§194). Same recipe: lead term absorbs the $k = 0$ slot, and each $(A_j - 1) = A_j - 1/1^{2j}$ is the *odd*-integer reciprocal-power sum minus its first entry.

## Convergence

Each $\alpha_j - 1/2^{2j}$ and each $A_j - 1$ is dominated by $1/4^j$. The $j$-th term of the outer sum is therefore bounded by $\tfrac{1}{j}\cdot(m/n)^{2j}\cdot 4^{-j}\cdot O(1)$. Provided $m/n \le 1/2$ — which is always achievable, since trig functions of angles in $(\pi/4, \pi/2)$ reduce to those in $(0, \pi/4)$ via the [[trigonometric-addition-formulas|co-function identity]] — the outer sum converges as $16^{-j}$. Ten terms give 30+ digits.

Euler is explicit: "the fraction $m/n$ need never be greater than $1/2$, and for this reason the terms converge much more quickly" (source: chapter11, §196). Convergence is so good that Euler tabulates the coefficients to 18 digits (in §194 for natural logs, §195 for tabular common logs with the $+10$ convention) and treats the formulas as the *practical* engine of trig log tables.

## Numerical example

For $m = 1, n = 2$ — i.e. $\sin(\pi/4) = 1/\sqrt 2$ — the sine formula gives

$$\log\sin\frac{\pi}{4} = \log 1 + \log 3 + \log 5 - 3\log 2 + \log\pi - \log 8 - \frac{1}{16^2}\!\left(\alpha - \frac{1}{4}\right)\cdot 2 \cdots$$

which evaluates (via the tabulated $\alpha, \beta, \ldots$) to $-\tfrac{1}{2}\log 2$, the exact value. Each term is small and the formula re-derives the closed form to twenty digits in a few operations.

## Tangent and cotangent — the §197 trick

Naïvely, $\log\tan = \log\sin - \log\cos$ doubles the work and gives a difference of two close numbers, losing precision. Euler's better route (§197–§198) starts from the [[cotangent-partial-fraction|§181 partial-fraction expansion]] specialized to rational angle:

$$\tan\frac{m\pi}{2n} = \frac{4mn}{\pi}\!\left(\frac{1}{n^2 - m^2} + \frac{1}{9n^2 - m^2} + \frac{1}{25n^2 - m^2} + \cdots\right).$$

Each fraction $1/((2k+1)^2 n^2 - m^2)$ expands as a geometric series in $m^2/((2k+1)^2 n^2)$:

$$\frac{1}{(2k+1)^2 n^2 - m^2} = \frac{1}{(2k+1)^2 n^2}\cdot\frac{1}{1 - m^2/(2k+1)^2 n^2} = \frac{1}{(2k+1)^2 n^2} + \frac{m^2}{(2k+1)^4 n^4} + \cdots$$

Transposing the resulting double sum, the columns are again $A, B, C, \ldots$. Result (source: chapter11, §198):

$$\boxed{\;\tan\frac{m\pi}{2n} = \frac{mn}{n^2 - m^2}\cdot\frac{4}{\pi} + \frac{m}{n}\cdot\frac{4}{\pi}(A - 1) + \frac{m^3}{n^3}\cdot\frac{4}{\pi}(B - 1) + \frac{m^5}{n^5}\cdot\frac{4}{\pi}(C - 1) + \cdots\;}$$

with the cofactor $1/\pi = 0.318309886183790671\,53776\,79267\,45028\,72\ldots$ already known. The cotangent has the analogous formula

$$\cot\frac{m\pi}{2n} = \frac{n}{m}\cdot\frac{2}{\pi} - \frac{4mn}{4n^2 - m^2}\cdot\frac{1}{\pi} - \frac{m}{n}\cdot\frac{4}{\pi}\!\left(\alpha - \frac{1}{2^2}\right) - \frac{m^3}{n^3}\cdot\frac{4}{\pi}\!\left(\beta - \frac{1}{2^4}\right) - \cdots$$

(source: chapter11, §198). $\sec$ and $\csc$ then follow by simple addition/subtraction of $\tan$ and $\cot$ using the §137 identities.

## Why this matters

These five formulas — $\log\pi$, $\log\sin$, $\log\cos$, $\tan$, $\cot$ — share *one* table of constants $A, B, C, \ldots, \alpha, \beta, \gamma, \ldots$. Euler computes that table once (chapter11, §190 and §193) and reuses it for every trig log computation thereafter. The combined effect is to make a thirty-digit *Tabula Sinuum, Tangentium et Secantium logarithmica* feasible to compute by hand.

The same architectural move — "decompose the function into operations on a small precomputed table" — is the ancestor of every method by which special functions are evaluated in modern numerical libraries.

## A modern reading

The Euler recipe for $\log\sin(\pi z)$ is, after rearrangement, the Taylor expansion

$$\log\frac{\sin\pi z}{\pi z} = -\sum_{j\ge 1}\frac{\zeta(2j)}{j}z^{2j},\qquad |z| < 1.$$

This is a special case of the *Hurwitz zeta function* power series. Euler does not have $\zeta(s)$ as a function of complex $s$ in the *Introductio*, but he is computing exactly its values at positive even integers and using them as expansion coefficients. The computational pipeline of this chapter is the same one used in 2026 to evaluate $\log\Gamma$, $\log\sin$, and related functions in arbitrary-precision libraries.

## Related pages

- [[linear-factors-of-sine-cosine]]
- [[log-pi-via-products]]
- [[logarithmic-series]]
- [[zeta-at-even-integers]]
- [[cotangent-partial-fraction]]
- [[wallis-product]]
- [[trig-infinite-products]]
- [[characteristic-and-mantissa]]
- [[trigonometric-addition-formulas]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
