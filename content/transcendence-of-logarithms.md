# Transcendence of Logarithms

**Summary**: Euler's §105 argument: if $a$ and $b$ are rational and $b$ is not a rational power of $a$, then $\log_a b$ is neither rational nor irrational — i.e. not algebraic. Such quantities Euler calls *transcendental*. This is the chapter's first extension of the algebraic/transcendental distinction from *functions* (Chapter 1) to *numbers*.

**Sources**: chapter6.pdf (§105)

**Last updated**: 2026-04-26

---

## The dichotomy

Suppose $\log b = r$ for some real $r$, where $a, b$ are rational and $a > 1$ is the base. Euler argues by cases on what kind of number $r$ could be (source: chapter6.pdf, §105):

- **$r$ rational, $r = m/n$.** Then $a^{m/n} = b$, i.e. $a^m = b^n$. With both $a$ and $b$ rational, this forces $b$ to be exactly the $(m/n)$-th power of $a$ — a rational power.
- **$r$ irrational, $r = \sqrt{n}$.** Then $a^{\sqrt n} = b$. Euler asserts this is impossible for rational $a, b$ — a power of a rational number with an irrational exponent cannot be rational.

So if $b$ is *not* a rational power of $a$, then $r = \log b$ falls into neither category. By exclusion, $r$ is "neither rational nor irrational" in Euler's sense — i.e. not algebraic. He coins the term *transcendental* for such quantities, and concludes:

> Logarithms (in general) are transcendental.

## What Euler is and is not proving

Euler's argument is informal by modern standards. The second case — that $a^{\sqrt n}$ cannot be rational for rational $a, b$ — requires the full Gelfond–Schneider theorem (1934) for a rigorous proof. Euler treats the impossibility as evident.

What Euler *does* establish cleanly is the dichotomy: *either* $b$ is a rational power of $a$ (in which case $\log b$ is rational) *or* $\log b$ is not rational. The "not rational" case he then calls transcendental, importing the language he had used for transcendental functions (see [[classification-of-functions]]) and applying it for the first time to a single quantity.

## Why this matters

- It is the conceptual jump from *transcendental functions* (defined as not algebraic, in Chapter 1) to *transcendental numbers* (a number not satisfying any polynomial equation with rational coefficients).
- It justifies all the *approximate* methods that follow: §106 (geometric-mean iteration), §109 (tables of primes), §112 (decimal approximations via [[characteristic-and-mantissa]]).
- It explains why logarithm tables are *useful*: most logarithms cannot be written down exactly, so a table of decimal approximations is the only practical interface to them.

## A working consequence

Almost every logarithm one encounters is transcendental — $\log 2$, $\log 3$, $\log 5$, $\log 7$, etc. — since these are only rational powers of 10 in the trivial cases (powers of 10 itself). Hence the entire table of common logarithms (Chapter 6, Briggs/Vlacq) consists of decimal approximations to transcendental numbers.

## Related pages

- [[logarithm]]
- [[exponential-function]]
- [[classification-of-functions]]
- [[geometric-mean-method-for-logarithms]]
- [[chapter-6-on-exponentials-and-logarithms]]
