# Single-valued and Multi-valued Functions

**Summary**: A function is single-valued if each input determines one output, and $n$-valued if it determines $n$ outputs. Euler introduces multi-valued functions as those defined by degree-$n$ polynomial equations with single-valued coefficients, and states Vieta's relations for them.

**Sources**: chapter1

**Last updated**: 2026-04-23

---

## Definitions

> A single-valued function is one for which, no matter what value is assigned to the variable $z$, a single value of the function is determined. ... A multiple-valued function is one such that, for some value substituted for the variable $z$, the function determines several values. (source: chapter1, §10)

Euler uses capital letters $P, Q, R, S, T$ for generic single-valued functions of $z$ throughout what follows.

## What is single- vs. multi-valued

- All non-irrational functions (polynomial, rational) are single-valued (source: chapter1, §10).
- All irrational functions are multi-valued, because radicals are ambiguous ($\sqrt{\dots}$ carries a $\pm$ sign).
- Transcendental functions can be single-valued, multi-valued, or even infinite-valued. Euler's example of an infinite-valued function is the arcsine, since "there are infinitely many circular arcs with the same sine" (source: chapter1, §10).

## n-valued functions by polynomial equations

The central construction (§§11-14): if $P, Q, R, S, \dots$ are single-valued functions of $z$, then the equation

$$
Z^n - P Z^{n-1} + Q Z^{n-2} - R Z^{n-3} + S Z^{n-4} - \dots = 0
$$

defines $Z$ as an $n$-valued function of $z$. Each choice of $z$ gives $n$ values of $Z$ — the roots of the equation.

### Low-degree cases

**Two-valued (§11)**: $Z^2 - P Z + Q = 0$ gives $Z = \frac{1}{2} P \pm \sqrt{\frac{1}{4} P^2 - Q}$. Both values are real or both are complex. Their sum is $P$, their product is $Q$.

**Three-valued (§12)**: $Z^3 - P Z^2 + Q Z - R = 0$. The three values are either all real, or one real and two complex. Sum = $P$, sum of pairwise products = $Q$, product = $R$.

**Four-valued (§13)**: $Z^4 - P Z^3 + Q Z^2 - R Z + S = 0$. The four values are all real, two real and two complex, or all complex. Sum = $P$, sum of pairwise products = $Q$, sum of triple products = $R$, product = $S$.

These are [[vietas-formulas|Vieta's formulas]] stated for coefficients that are themselves functions of $z$.

## Rules for reducing to rationality and counting values

To determine how many values $Z$ has as a function of $z$, the defining equation must first be "reduced to rationality"; then the largest power of $Z$ is the count (source: chapter1, §14). If any of $P, Q, R, S, \dots$ is itself multi-valued, the total number of values of $Z$ is larger than the apparent degree.

Parity of complex roots: complex roots come in conjugate pairs. Consequences (source: chapter1, §14):

- If $n$ is odd, at least one value of $Z$ is real.
- If $n$ is even, it is possible that no value of $Z$ is real.

## Multi-valued functions that "imitate" single-valued ones (§15)

If a multi-valued function always has exactly one real value among its $n$ values, it can often be treated as single-valued. Fractional powers $P^{m/n}$:

- $n$ odd, any $m$: one real value, others complex $\to$ may be treated as single-valued.
- $n$ even, $m/n$ in lowest terms: either no real value or two $\to$ two-valued.

## Reciprocity and valuedness

If $y$ is a function of $z$, then $z$ is a function of $y$, but the two counts of values may differ (source: chapter1, §16). Example: $y^3 = ayz - bz^2$ makes $y$ three-valued in $z$ and $z$ two-valued in $y$.

## Related pages

- [[function]]
- [[classification-of-functions]]
- [[even-and-odd-functions]]
- [[vietas-formulas]]
- [[chapter-1-on-functions-in-general]]
