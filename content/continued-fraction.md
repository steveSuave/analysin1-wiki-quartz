# Continued Fraction

**Summary**: A continued fraction is an infinite expression in which the denominator at each level is itself the sum of an integer (or polynomial expression) and another fraction of the same kind. Euler treats two forms: the *simple* form with all numerators equal to $1$, and the *generalised* form with arbitrary numerators.

**Sources**: `chapter18` (§357).

**Last updated**: 2026-05-11

---

## Definition

Euler (§357): "By a continued fraction I mean a fraction of such a kind that the denominator consists of the sum of an integer and a fraction whose denominator again is the sum of an integer and a fraction of the same kind."

### Simple form (numerators all $1$)

$$a + \cfrac{1}{b + \cfrac{1}{c + \cfrac{1}{d + \cfrac{1}{e + \cfrac{1}{f + \cdots}}}}}$$

This is the form Euler considers first; the partial denominators $a, b, c, d, \ldots$ are typically positive integers when the continued fraction is meant to represent a real number.

### Generalised form (arbitrary numerators)

$$a + \cfrac{\alpha}{b + \cfrac{\beta}{c + \cfrac{\gamma}{d + \cfrac{\delta}{e + \cdots}}}}$$

The partial numerators $\alpha, \beta, \gamma, \ldots$ may be arbitrary expressions. This form is the natural target of [[continued-fraction-series-equivalence|series-to-continued-fraction conversion]] (Movements 2–3 of [[chapter-18-on-continued-fractions|chapter 18]]), since requiring numerators to be $1$ would over-constrain the matching.

### Termination

A continued fraction may stop after a finite number of levels (a *terminating* continued fraction) or continue indefinitely. Terminating simple-form CFs represent exactly the rational numbers ([[euclidean-algorithm-continued-fraction|§381]]); periodic simple-form CFs represent exactly the [[periodic-continued-fractions|quadratic irrationals]].

## Role in the *Introductio*

Euler positions continued fractions as the third kind of infinite expression in Book I, alongside infinite series (chapters 4, 7, 8, 13, 14, 15, 17) and infinite products (chapters 9, 10, 11). The book closes with this chapter — Euler considered continued fractions essential machinery for the analysis of the infinite, but underdeveloped, and predicted in §356 that they "will be much more widely used in the times to come." That prediction was correct: Lagrange (1770), Gauss (1813), and the 19th-century number theorists made continued fractions central to Diophantine approximation, transcendence theory, and Pell-equation solutions.

## Related pages

- [[chapter-18-on-continued-fractions]]
- [[convergents-of-a-continued-fraction]] — three-term recurrence for numerators and denominators of truncated CFs
- [[continued-fraction-series-equivalence]] — bidirectional dictionary between continued fractions and alternating series
- [[periodic-continued-fractions]] — when partial denominators repeat
- [[euclidean-algorithm-continued-fraction]] — how every rational number gives a finite CF
