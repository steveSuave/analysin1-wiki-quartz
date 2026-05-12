# Chapter 4: On the Development of Functions in Infinite Series

**Summary**: Euler argues that any function can be represented as an infinite series $A + Bz + Cz^2 + Dz^3 + \cdots$ (with real exponents allowed), and shows how to obtain such expansions for rational functions (geometric and recurrent series) and for irrational functions (Newton's binomial series).

**Sources**: chapter4.pdf

**Last updated**: 2026-04-23

---

## Overview

Chapters 2–3 taught how to rewrite functions as simple pieces — linear/quadratic factors, partial fractions, rational parametrizations. Chapter 4 begins the move from finite rewriting to *infinite* representation. Euler's thesis (§59) is that polynomial form $A + Bz + Cz^2 + \cdots$ is the form in which "the mind grasps the nature" of a function, and that any function — rational, irrational, or transcendental — can be put in this form if infinite many terms are allowed, with real-number exponents $Az^\alpha + Bz^\beta + \cdots$ when necessary (source: chapter4.pdf, §59).

The chapter splits into two halves:

1. **Series for rational functions** (§60–§70). Any rational function expands into a [[recurrent-series]] whose coefficient law is read off the denominator. See [[geometric-series]], [[method-of-undetermined-coefficients]], [[recurrent-series]], [[higher-order-arithmetic-progressions]].
2. **Series for irrational functions** (§71–§76). Newton's "universal theorem" $(P + Q)^{m/n}$ gives a series expansion; when specialized to $(1 + Z)^m$ with $Z$ a polynomial in $z$, the resulting series is again recurrent. See [[binomial-series]].

Euler defers a proof of the general binomial law to "the principles of differential calculus" and is content here to make its truth "reasonable by the application to examples of so many different kinds" (source: chapter4.pdf, §76).

## Structure of the chapter

### §59 — Motivation: functions as infinite polynomials

Polynomial functions $A + Bz + Cz^2 + \cdots$ (finite) are "well understood." Every other function — rational, irrational, transcendental — is to be *expressed* in this form if at all possible, allowing the number of terms to be infinite and the exponents to be any real numbers (source: chapter4.pdf, §59). This framing sets the program for the entire *Introductio*.

### §60 — Geometric series by division and by undetermined coefficients

For $\dfrac{a}{\alpha + \beta z}$, long division yields

$$ \frac{a}{\alpha + \beta z} = \frac{a}{\alpha} - \frac{a \beta z}{\alpha^2} + \frac{a \beta^2 z^2}{\alpha^3} - \frac{a \beta^3 z^3}{\alpha^4} + \cdots, $$

the ratio of successive terms being $-\beta z / \alpha$ (source: chapter4.pdf, §60). The same series is recovered by the [[method-of-undetermined-coefficients]]: setting $a/(\alpha + \beta z) = A + B z + C z^2 + \cdots$, multiplying out, and matching powers of $z$ gives $A = a/\alpha$ and $\alpha Q + \beta P = 0$ for any two consecutive coefficients $P, Q$. See [[geometric-series]].

### §61 — Quadratic denominator

For $\dfrac{a + b z}{\alpha + \beta z + \gamma z^2}$, the same match gives $A = a/\alpha$, $B = b/\alpha - a\beta/\alpha^2$, and the three-term recurrence $\alpha R + \beta Q + \gamma P = 0$ connecting any three consecutive coefficients (source: chapter4.pdf, §61). Example: $\dfrac{1 + 2z}{1 - z - z^2} = 1 + 3z + 4z^2 + 7z^3 + 11z^4 + 18z^5 + \cdots$ (Lucas numbers), where $R = P + Q$.

### §62 — Recurrent series

A series whose coefficients satisfy a fixed linear recurrence is called *recurrent*, a name due to De Moivre — because to compute a term one must "run back" to earlier terms (source: chapter4.pdf, §62). The order of the recurrence equals the degree of the denominator. See [[recurrent-series]].

### §63 — Proper rational functions and the general law

For a proper rational function $\dfrac{a + b z + c z^2 + \cdots}{1 - \alpha z - \beta z^2 - \gamma z^3 - \cdots}$ (constant term of the denominator normalized to 1, remaining terms written with minus signs), the coefficient recurrence reads

$$ A = a, \quad B = \alpha A + b, \quad C = \alpha B + \beta A + c, \quad D = \alpha C + \beta B + \gamma A + d, \ldots $$

Once the numerator's terms run out, coefficients are determined entirely by the fixed recurrence (source: chapter4.pdf, §63). If the rational function is improper, the polynomial part disturbs early terms — Euler illustrates with $\dfrac{1 + 2z - z^3}{1 - z - z^2}$, whose fourth coefficient $6z^3$ breaks the Fibonacci-like law.

### §64–§67 — Powers of $(1 - \alpha z)$ and progressions of higher order

If the denominator is $(1 - \alpha z)^n$, the coefficient law still exists (expand the denominator as a polynomial) and the series is recurrent. The bridge to classical material: setting $\alpha = z = 1$ converts the series into a *progression of order $n-1$* — one whose $(n-1)$-st differences are constant. See [[higher-order-arithmetic-progressions]].

Specifically:

- §64. $\dfrac{a + bz}{(1 - \alpha z)^2}$ has coefficient $(n+1)\alpha^n a + n \alpha^{n-1} b$. With $\alpha = z = 1$, one gets the arithmetic progression $a, 2a+b, 3a+2b, \ldots$ (first differences constant).
- §65. $\dfrac{a + bz + cz^2}{(1 - \alpha z)^3}$ has coefficient $\tfrac{(n+1)(n+2)}{2}\alpha^n a + \tfrac{n(n+1)}{2}\alpha^{n-1}b + \tfrac{(n-1)n}{2}\alpha^{n-2}c$. With $\alpha = z = 1$, this is a second-order progression (second differences constant) with recurrence $D = 3C - 3B + A$.
- §66. Analogous formula for $(1 - \alpha z)^4$; third-order progression, recurrence $E = 4D - 6C + 4B - A$ — the coefficients of $(1 - z)^4$ with alternating signs.
- §67. General pattern: the $(m-1)$-th order progression $a^m + (a+b)^m + (a+2b)^m + \cdots$ is recurrent with denominator $(1 - z)^{m+1}$ (source: chapter4.pdf, §67).

### §68 — Powers of a multinomial denominator

If the denominator is $(1 - \alpha z - \beta z^2 - \gamma z^3 - \cdots)^{m+1}$, the coefficient law still computes each term from a fixed number of predecessors, but the coefficients in the recurrence now depend on the *power of $z$* (source: chapter4.pdf, §68). Writing the series as $1 + Az + Bz^2 + \cdots + Kz^{n-3} + Lz^{n-2} + Mz^{n-1} + Nz^n + \cdots$:

$$ N = \tfrac{m + n}{n} \alpha M + \tfrac{2m + n}{n} \beta L + \tfrac{3m + n}{n} \gamma K + \cdots $$

This "non-constant law" is Euler's first encounter with a recurrence whose coefficients vary with index. It applies only when the numerator is a constant; a general numerator complicates matters, and Euler defers it (§68).

### §69 — Zero constant term in the denominator

If the denominator vanishes at $z = 0$ — say it has the form $z^m (1 - \alpha z - \beta z^2 - \cdots)$ — the expansion acquires negative powers of $z$:

$$ \frac{a + b z + c z^2 + \cdots}{z^m (1 - \alpha z - \beta z^2 - \cdots)} = \frac{A}{z^m} + \frac{B}{z^{m-1}} + \cdots + \frac{C}{z^{m-2}} + \cdots $$

with $A, B, C, \ldots$ the same coefficients as in the $m = 0$ case (source: chapter4.pdf, §69). Modern reading: this is a Laurent expansion at $z = 0$.

### §70 — Same function, infinitely many recurrent representations

Because a rational function $y(z)$ can be *reparametrized* (see [[chapter-3-on-the-transformation-of-functions-by-substitution]]), the same $y$ admits infinitely many distinct recurrent-series expansions in different variables. Euler illustrates with $y = (1 + z)/(1 - z - z^2)$: the substitutions $z = 1/x$ and $z = (1-x)/(1+x)$ both produce entirely different-looking recurrent series for the same $y$ (source: chapter4.pdf, §70).

### §71–§72 — Newton's "universal theorem" for $(P + Q)^{m/n}$

Irrational functions expand via

$$ (P + Q)^{m/n} = P^{m/n} + \tfrac{m}{n} P^{(m-n)/n} Q + \tfrac{m(m-n)}{n \cdot 2n} P^{(m-2n)/n} Q^2 + \tfrac{m(m-n)(m-2n)}{n \cdot 2n \cdot 3n} P^{(m-3n)/n} Q^3 + \cdots $$

with finitely many terms iff $m/n$ is a positive integer (source: chapter4.pdf, §71). Euler tabulates the cases $m/n = 1/2, -1/2, 1/3, -1/3, 2/3$ explicitly. Section §72 notes the term-to-term recurrence and rewrites the formula in modern form

$$ (1 + Z)^m = 1 + \tfrac{m}{1} Z + \tfrac{m(m-1)}{1 \cdot 2} Z^2 + \tfrac{m(m-1)(m-2)}{1 \cdot 2 \cdot 3} Z^3 + \cdots $$

valid for any real $m$ (source: chapter4.pdf, §72). See [[binomial-series]].

### §73–§76 — Binomial series with polynomial $Z$

Specializing $Z$ to $\alpha z$, $\alpha z + \beta z^2$, $\alpha z + \beta z^2 + \gamma z^3$, …, Euler expands $(1 + \alpha z + \beta z^2 + \cdots)^{m-1}$ and collects terms by powers of $z$. The resulting series is recurrent with a non-constant law that matches §68 exactly — under the substitution $m \mapsto -m$ with negated inner coefficients (source: chapter4.pdf, §76). A rigorous proof is deferred to differential calculus; Euler is satisfied by the empirical consistency with §68.

## Notable points

- Euler's framing in §59 — "any function = $A + Bz^\alpha + Cz^\beta + \cdots$" — anticipates the modern definition of a power series while still being liberal about real exponents. The commitment to infinite series as the universal representation shapes the entire *Introductio*.
- The "law from the denominator" (§62–§63) is the first systematic statement of a fact that is obvious in hindsight: a rational generating function encodes a linear recurrence, and vice versa. De Moivre had the idea; Euler lays it out as a procedure.
- The identification in §64–§67 of arithmetic and higher-order progressions with recurrent series generated by $(1-z)^n$ prefigures the modern finite-difference calculus, and gives the binomial coefficients $\binom{n}{k}(-1)^k$ as the recurrence kernel.
- §68 and §76 together show Euler noticing — without yet proving — that $(1 - \alpha z - \beta z^2 - \cdots)^{-(m+1)}$ obeys the same non-constant law as $(1 + \alpha z + \beta z^2 + \cdots)^{m-1}$ with sign flips. This equivalence under $m \mapsto -m$ is the shadow of a single theorem, to be made precise once derivatives are available.
- §70 is a notable observation: a rational function has no canonical power-series representation; every substitution gives a different one. The *choice of variable* is part of the data.
- The §71 binomial series is stated without proof and without a convergence discussion; Euler's stance, explicit in §76, is that the accumulated agreement with computed examples is persuasive enough for now.

## Why this chapter matters

Chapter 4 is the pivot from finite algebra to analysis. Every later chapter of Book I — logarithms, exponentials, trigonometric functions, $e$, factorizations of $\sin$ and $\cos$ — rests on the ability to write a function as an infinite series and manipulate it term by term. The two tools introduced here, the recurrent-series machinery for rational functions and the binomial series for radicals, are the foundation on which the rest of the *Introductio* is built.

## Related pages

- [[geometric-series]]
- [[method-of-undetermined-coefficients]]
- [[recurrent-series]]
- [[higher-order-arithmetic-progressions]]
- [[binomial-series]]
- [[improper-rational-function]]
- [[partial-fraction-decomposition]]
- [[chapter-3-on-the-transformation-of-functions-by-substitution]]
