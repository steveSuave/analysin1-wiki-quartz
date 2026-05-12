# Chapter 10: On the Use of the Discovered Factors to Sum Infinite Series

**Summary**: Euler harvests the [[chapter-9-on-trinomial-factors|Chapter 9 infinite products]]. The mechanism: an infinite product expansion provides the elementary symmetric polynomials of the function's reciprocal zeros via its power-series coefficients; [[newtons-identities|Newton's identities]] then convert them into power sums. This single technique solves the [[basel-problem|Basel problem]], evaluates [[zeta-at-even-integers|every $\zeta(2k)$]], generates Leibniz's $\pi/4$ series and a vast family of [[circular-arc-series|character-style sums]], and produces the [[cotangent-partial-fraction|partial-fraction expansions of cot, csc, coth, csch]].

**Sources**: chapter10.pdf

**Last updated**: 2026-04-30

---

## Overview

Chapter 9 built infinite products. Chapter 10 extracts numerical content from them. The recipe is one slide:

1. Take an infinite-product expansion $1 + Az + Bz^2 + \cdots = \prod(1 + \alpha_k z)$, where the $\alpha_k$ are the reciprocal zeros of the function.
2. The series-side coefficients $A, B, C, \ldots$ are the elementary symmetric polynomials of the $\alpha_k$.
3. [[newtons-identities|Newton's identities]] convert these into the power sums $P = \sum\alpha_k$, $Q = \sum\alpha_k^2$, $R = \sum\alpha_k^3$, $\ldots$
4. The power sums are the *interesting* numbers.

The chapter has four movements:

1. **§165–§166 — the engine.** [[newtons-identities|Newton's identities]] for converting elementary symmetrics to power sums, given as a recurrence: $P = A$, $Q = AP - 2B$, $R = AQ - BP + 3C$, etc.
2. **§167–§170 — even-zeta values.** Apply the engine to the [[exponential-infinite-product|sinh product]] for $\zeta(2)$ ([[basel-problem|the Basel problem]]) and through the [[zeta-at-even-integers|table $\zeta(2k)$]] for $k \le 13$. The [[cosine-infinite-product|cosh product]] gives sums over odd squares; the §170 [[odd-and-alternating-zeta-decomposition|even/odd/alternating decomposition]] connects all variants.
3. **§171–§180 — character-style sums.** Apply the engine to the [[chapter-9-on-trinomial-factors|§164 arc-form products]] and obtain the [[circular-arc-series|family of series]] indexed by arithmetic progressions. Special cases: Leibniz's $\pi/4$, $\pi^2/8$, $\pi^3/32$; $n = 3$ gives $\sqrt 3$ series; $n = 4, 8$ gives $\sqrt 2$ series.
4. **§181–§183 — partial fractions.** Combine pairs of series and substitute $a = m^2/n^2$ to obtain the [[cotangent-partial-fraction|partial-fraction expansions]] $\pi\cot(\pi\sqrt a) = \cdots$, $\pi/\sin(\pi\sqrt a) = \cdots$. The hyperbolic version (negative $a$) follows by [[eulers-formula|imaginary substitution]].

## Structure of the chapter

### §165–§166 — Newton's identities

If $1 + Az + Bz^2 + Cz^3 + \cdots = (1 + \alpha z)(1 + \beta z)(1 + \gamma z)\cdots$, then $A, B, C, \ldots$ are the elementary symmetric polynomials of $\alpha, \beta, \gamma, \ldots$. Defining the power sums $P = \sum\alpha_k^1$, $Q = \sum\alpha_k^2$, $R = \sum\alpha_k^3$, $\ldots$, Euler states the recurrence

$$P = A,\quad Q = AP - 2B,\quad R = AQ - BP + 3C,\quad S = AR - BQ + CP - 4D,\quad\ldots$$

(source: chapter10.pdf, §166). The truth "is intuitively clear, but a rigorous proof will be given in the differential calculus." See [[newtons-identities]].

### §167 — The Basel problem

Apply the engine to the [[exponential-infinite-product|sinh product]] $(e^x - e^{-x})/(2x) = \prod(1 + x^2/k^2\pi^2)$. Substituting $x^2 = \pi^2 z$ identifies the elementary symmetrics from the power-series coefficients:

$$A = \frac{\pi^2}{6},\ B = \frac{\pi^4}{120},\ C = \frac{\pi^6}{5040},\ \ldots$$

and the roots are $\alpha_k = 1/k^2$. Newton's identities deliver

$$P = \sum_{k=1}^{\infty}\frac{1}{k^2} = \frac{\pi^2}{6},$$

$$Q = \sum_{k=1}^{\infty}\frac{1}{k^4} = \frac{\pi^4}{90},\quad R = \sum_{k=1}^{\infty}\frac{1}{k^6} = \frac{\pi^6}{945},\quad S = \sum_{k=1}^{\infty}\frac{1}{k^8} = \frac{\pi^8}{9450},\quad\ldots$$

See [[basel-problem]] and [[zeta-at-even-integers]].

### §168 — Tabulation through $\zeta(26)$

Euler tabulates the rational coefficients of $\zeta(2k)/\pi^{2k}$ for $k = 1, \ldots, 13$. The "irregular" sequence $1, 1/3, 1/3, 3/5, 5/3, 691/105, 35/1, \ldots$ is, in modern terms, $|B_{2k}|$ (Bernoulli numbers) rescaled. Euler does not have the Bernoulli connection in front of him here, but he notes the sequence's "extraordinary usefulness." See [[zeta-at-even-integers]].

### §169 — Sums over odd squares

The same mechanism applied to the [[cosine-infinite-product|cosh product]] $(e^x + e^{-x})/2 = \prod(1 + 4x^2/(2k+1)^2\pi^2)$ gives

$$\sum_{k=0}^{\infty}\frac{1}{(2k+1)^2} = \frac{\pi^2}{8},\quad \sum_{k=0}^{\infty}\frac{1}{(2k+1)^4} = \frac{\pi^4}{96},\quad \sum_{k=0}^{\infty}\frac{1}{(2k+1)^6} = \frac{\pi^6}{960},\quad\ldots$$

See [[zeta-at-even-integers]].

### §170 — Even/odd/alternating decomposition

For any $n$ and $M = \zeta(n) = \sum 1/k^n$:

$$\frac{M}{2^n} = \sum\frac{1}{(2k)^n},\quad M - \frac{M}{2^n} = \frac{2^n - 1}{2^n}M = \sum\frac{1}{(2k+1)^n},\quad M - \frac{2M}{2^n} = \frac{2^{n-1}-1}{2^{n-1}}M = \sum_{k\ge 1}\frac{(-1)^{k+1}}{k^n}.$$

A linear-algebra observation that cleanly converts any closed form for $\zeta(n)$ into closed forms for the even, odd, and alternating restrictions. See [[odd-and-alternating-zeta-decomposition]].

### §171–§174 — The arc-form expansion

Substitute $v = \pi x/n$, $g = m\pi/n$ in the [[chapter-9-on-trinomial-factors|§164 product]]

$$\cos(v/2) + \tan(g/2)\sin(v/2) = \prod\left(1 \pm \frac{v}{(2j+1)\pi - g}\right)\left(1 \mp \frac{v}{(2j+1)\pi + g}\right)$$

to obtain

$$\left(1 + \frac{x}{n-m}\right)\left(1 - \frac{x}{n+m}\right)\left(1 + \frac{x}{3n-m}\right)\cdots = \cos\frac{\pi x}{2n} + \tan\frac{m\pi}{2n}\sin\frac{\pi x}{2n}.$$

The right side, expanded in $x$, gives elementary symmetric coefficients $A, B, C, \ldots$ involving $\tan(m\pi/2n)$ and $\pi^k/n^k$. Newton's identities convert them into power sums $P, Q, R, S, T, V$ of the roots $1/(n-m), -1/(n+m), 1/(3n-m), \ldots$. See [[circular-arc-series]].

### §175–§180 — Special values

Euler walks through $m = 1, n = 2$ (Leibniz's $\pi/4$ and friends), $m = 1, n = 3$ ($\sqrt 3$ series), $m = 1, n = 4$ and $n = 8$ ($\sqrt 2$ series), and combinations. Each produces a different "character pattern" on the integers. See [[circular-arc-series]] for the catalog.

### §181–§182 — Pairing two-by-two: $\pi\cot$ and $\pi/\sin$

Adding/subtracting adjacent-term combinations of §172 and §174 collapses to

$$\sum_{k=1}^{\infty}\frac{1}{k^2 - a} = \frac{1}{2a} - \frac{\pi}{2\sqrt a\tan(\pi\sqrt a)},\quad \sum_{k=1}^{\infty}\frac{(-1)^{k+1}}{k^2 - a} = \frac{\pi}{2\sqrt a\sin(\pi\sqrt a)} - \frac{1}{2a}.$$

These are the partial-fraction expansions of $\pi\cot(\pi\sqrt a)$ and $\pi/\sin(\pi\sqrt a)$. See [[cotangent-partial-fraction]].

### §183 — Hyperbolic version via Euler's formula

For $a = -b$, [[eulers-formula]] $\cos(yi) = (e^y + e^{-y})/2$, $\sin(yi) = (e^y - e^{-y})/(2i)$ converts the §182 formulas into

$$\sum_{k=1}^{\infty}\frac{1}{k^2 + b} = \frac{\pi\sqrt b\coth(\pi\sqrt b)}{2b} - \frac{1}{2b},\quad \sum_{k=1}^{\infty}\frac{(-1)^{k+1}}{k^2 + b} = \frac{1}{2b} - \frac{\pi\sqrt b}{2b\sinh(\pi\sqrt b)}.$$

These are the partial fractions of $\coth$ and $\text{csch}$. Euler chooses this route over an independent §162 derivation "since it is a nice illustration of the reduction of sines and cosines of complex arcs to real exponentials" (source: chapter10.pdf, §183). See [[cotangent-partial-fraction]].

## Notable points

- **Newton's identities are the only computational engine.** The whole chapter is one technique applied to many products. This is unusual for Euler, who normally varies methods; here the technique's range is the point.
- **Even-zeta values come for free from Chapter 9.** The Basel problem — open for a century, the showpiece of the *Introductio* — falls out of $A = \pi^2/6$ in the [[exponential-infinite-product|sinh product]]. No further work.
- **Odd-zeta values are absent.** The chapter never produces $\zeta(2k+1) = \sum 1/n^{2k+1}$ in closed form. This is not a gap in Euler's exposition; it is a structural limit of the method, and the limit persists in 2026.
- **Character sums emerge from arc parameters.** The §171–§180 family — $1 - 1/3 + 1/5 - 1/7 + \cdots$, $1 - 1/2 + 1/4 - 1/5 + \cdots$, and many more — are the values of [[circular-arc-series|Dirichlet $L$-functions]] at integer arguments, computed *before* Dirichlet introduced the concept. Euler's parametrization $(m, n)$ corresponds to a real quadratic character mod $4n$.
- **Partial fractions arise from product manipulation.** The §181–§183 derivation of $\pi\cot$ and $\pi/\sin$ partial fractions is the first appearance of what would become Mittag-Leffler theory. Euler reaches the formulas without complex analysis as a discipline; they are correct and survived unaltered into modern texts.
- **Euler uses real and imaginary forms interchangeably.** §183 transitions between trigonometric and hyperbolic series by setting $a = -b$, with [[eulers-formula]] as the dictionary. This freedom — rotating across the imaginary axis to swap circular for hyperbolic — is one of the [[chapter-7-on-exponentials-and-logarithms-expressed-through-series|*Introductio*'s]] characteristic moves.

## Why this chapter matters

Chapter 10 closes a chord struck across the entire first volume:

- [[chapter-2-on-the-transformation-of-functions|Chapter 2]]: every polynomial factors over $\mathbb R$.
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series|Chapter 7]] / [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle|Chapter 8]]: the elementary transcendentals $e^z$, $\sin z$, $\cos z$ are limits of polynomials.
- [[chapter-9-on-trinomial-factors|Chapter 9]]: factoring those polynomials through the limit produces infinite products.
- **Chapter 10**: comparing the products to the power series produces every numerical result of importance — $\pi^2/6$, $\pi^4/90$, $\pi/4$, $\pi\cot(\pi z)$, $\pi/\sin(\pi z)$.

Each step uses only the previous one. The whole edifice rests on real algebra, [[infinitesimal-and-infinite-numbers|infinitesimals]], and [[eulers-formula|the imaginary substitution]] — Euler's three persistent tools.

After Chapter 10, the *Introductio*'s analytic-function project is complete. Chapters 11–18 specialize to recurring topics (continued fractions, partition identities, Diophantine equations) that complement but do not extend the synthesis.

## Related pages

- [[newtons-identities]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[odd-and-alternating-zeta-decomposition]]
- [[circular-arc-series]]
- [[cotangent-partial-fraction]]
- [[exponential-infinite-product]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[eulers-formula]]
- [[arctangent-series]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
