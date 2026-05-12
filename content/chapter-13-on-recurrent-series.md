# Chapter 13: On Recurrent Series

**Summary**: Euler completes the theory of [[recurrent-series|recurrent series]] introduced in [[chapter-4-on-the-development-of-functions-in-infinite-series|Chapter 4]]. Three movements: (i) closed-form *general term* of any recurrent series, obtained by [[real-partial-fraction-decomposition|real partial fractions]] of the generating rational function plus explicit formulas for each fraction type; (ii) the inverse problem — extracting the generating rational function from the recurrence law — and De Moivre's "*scale of the relation*"; (iii) the *sum* of a recurrent series, finite or infinite, expressed in closed form.

**Sources**: chapter13, chapter17

**Last updated**: 2026-05-11

---

## Overview

[[chapter-4-on-the-development-of-functions-in-infinite-series|Chapter 4]] introduced [[recurrent-series|recurrent series]] — power series whose coefficients obey a fixed linear recurrence — and showed that every proper rational function expands into one. The *coefficient law* was read directly off the denominator. But the recurrence by itself does not give the $n$-th coefficient as a closed-form function of $n$. Chapter 13 supplies that closed form, by combining three pieces:

- [[partial-fraction-decomposition|Chapter 2]]'s decomposition into simple linear-factor fractions,
- [[real-partial-fraction-decomposition|Chapter 12]]'s extension to real quadratic factors,
- explicit power-series expansions of each fraction type, then summed.

The chapter also reverses the question (given the series, recover the rational function — the *scale of the relation*) and computes both finite and infinite sums.

## Structure of the chapter

### §211–§214 — Decompose, expand, sum

Any proper rational function decomposes by [[real-partial-fraction-decomposition|Chapters 2 and 12]] into a sum of simple fractions. Each simple fraction expands into its own recurrent series. The general term of the original series is the *sum* of the general terms of the partial-fraction series (source: chapter13, §212–§213). Equality of two power series is justified by setting $z = 0$, subtracting the constant, dividing by $z$, repeating (source: chapter13, §214).

### §215–§216 — General term for $A/(1-pz)^k$

The fundamental linear-factor brick is

$$\frac{A}{(1 - pz)^k} \;=\; A + kApz + \frac{k(k+1)}{2!}A p^2 z^2 + \cdots,$$

with general term

$$\binom{n + k - 1}{k - 1}\, A p^n z^n \;=\; \frac{(n+1)(n+2)\cdots(n+k-1)}{(k-1)!}\, A p^n z^n.$$

(source: chapter13, §215). Once this is in hand, the partial-fraction tower for *any* repeated linear factor gives the general term term-by-term (§216). See [[general-term-of-recurrent-series]].

### Examples I–V (§216, p. 183–186)

Five worked examples illustrate the method for distinct or repeated *real* linear factors:

- **I.** $\dfrac{1-z}{1-z-2z^2}$ has partial fractions $\dfrac{2/3}{1+z} + \dfrac{1/3}{1-2z}$; general term $\dfrac{2^n \pm 2}{3}z^n$ (sign by parity of $n$).
- **II.** $\dfrac{1-z}{1-5z+6z^2} = \dfrac{-1}{1-2z} + \dfrac{2}{1-3z}$; general term $(2\cdot 3^n - 2^n) z^n$.
- **III.** $\dfrac{1+2z}{1-z-z^2}$ has roots $(1\pm\sqrt 5)/2$; general term is the sum of $((1+\sqrt 5)/2)^{n+1} + ((1-\sqrt 5)/2)^{n+1}$ — the Lucas-numbers Binet formula.
- **IV.** Symbolic: $\dfrac{a + bz}{1 - \alpha z - \beta z^2}$ — the closed form for *any* two-term linear recurrence ([[closed-form-two-term-recurrence|Binet-type formula]]).
- **V.** $\dfrac{1}{1-z-z^2+z^3} = \dfrac{1}{(1-z)^2(1+z)}$, with repeated factor; partial fractions $\tfrac{1/2}{(1-z)^2} + \tfrac{1/4}{1-z} + \tfrac{1/4}{1+z}$ give general term $\dfrac{2n + 3 \pm 1}{4}z^n$.

### §217–§222 — General term for the quadratic-factor brick

When the denominator has the [[trinomial-factor|trinomial factor]] $1 - 2pz\cos\phi + p^2 z^2$, complex partial fractions expose a closed form involving sines and cosines of multiples of $\phi$. The base case $k=1$ comes from the [[trigonometric-recurrent-progression|§129 sin/cos recurrent progression]]: the series for $A/(1 - 2pz\cos\phi + p^2 z^2)$ has general term $\dfrac{A\sin(n+1)\phi}{\sin\phi}p^n z^n$ (source: chapter13, §218). For $A + Bpz$ in the numerator, this becomes $\dfrac{A\sin(n+1)\phi + B\sin n\phi}{\sin\phi}\,p^n z^n$.

For $k = 2$ (§220) and $k = 3$ (§221) Euler derives explicit, increasingly complicated formulas; the §219 derivation passes through a complex factorization $(1 - (\cos\phi+i\sin\phi)pz)(1 - (\cos\phi-i\sin\phi)pz)$ and converts back to real form via the identities $16\sin^5\phi = 10\sin\phi - 5\sin 3\phi + \sin 5\phi$ and similar (§222) — the same odd-power table that Chapter 14 [[powers-of-sine-and-cosine|derives systematically]] in §262. See [[general-term-of-recurrent-series]].

### §223 — Two big mixed examples

The two examples sweep up everything in the chapter:

- $\dfrac{1}{(1-z)(1-z^2)(1-z^3)} = \dfrac{1}{(1-z)^3(1+z)(1+z+z^2)}$ — repeated linear, simple linear, and quadratic factor (with $\phi = \pi/3$). The general term takes a *different* closed form on each residue class $n \pmod 6$ (source: chapter13, §223 Example I).
- $\dfrac{1+z+z^2}{1-z-z^4+z^5} = \dfrac{1+z+z^2}{(1-z)^2(1+z)(1+z^2)}$ — produces a four-case formula, one per residue class mod $4$.

### §224–§230 — The inverse problem: scale of the relation

Reading the rational function back off the recurrence law: given $D = \alpha C + \beta B + \gamma A$ etc., the denominator is $1 - \alpha z - \beta z^2 - \gamma z^3$. The list $\alpha, \beta, \gamma, \ldots$ is De Moivre's [[scale-of-the-relation|*scale of the relation*]] (source: chapter13, §224).

For a *two-member* scale (each term determined by the two preceding), §226–§229 give the [[closed-form-two-term-recurrence|Binet-type closed form]] $A_n = (Up^n + Vq^n)$ where $p, q$ are the roots of the denominator. A striking identity follows: $UV = \dfrac{B^2 - \alpha AB + \beta A^2}{4\beta - \alpha^2}$ (source: chapter13, §227). Hence each term can be obtained from a *single* predecessor by

$$Q = \tfrac{1}{2}\alpha P + \sqrt{\bigl((1/4)\alpha^2 - \beta\bigr)P^2 + (B^2 - \alpha AB + \beta A^2)\,\beta^n}$$

— an apparent irrationality that is always rational. Worked Lucas example (§229 Example): $Q = \tfrac{1}{2}(P + \sqrt{5P^2 + 20})$, sign by parity. Section §230 sketches the analogous cubic relation for a three-member scale.

### §231–§233 — Sum of a recurrent series

The sum of the *infinite* series equals the generating rational function (source: chapter13, §231). The sum of the *first* $n+1$ terms is the rational function minus the tail, which is itself a rational function with shifted numerator (source: chapter13, §232). For a two-member scale this collapses to a clean closed form

$$\sum_{k=0}^{n} A_k z^k \;=\; \frac{A + (B - \alpha A)z - Q z^{n+1} - R z^{n+2}}{1 - \alpha z - \beta z^2}.$$

Lucas example at $z = 1$: $1 + 3 + 4 + 7 + 11 + \cdots + P = P + Q - 3 = \dfrac{3P - 6 + \sqrt{5P^2 + 20}}{2}$ — the partial sum is determined by the *last term alone* (source: chapter13, §233 Example). See [[sum-of-recurrent-series]].

## Notable points

- **The chapter is the closed-form complement to Chapter 4.** Chapter 4 gave the *recurrence*; Chapter 13 gives the *closed form*. The bridge between them is the [[partial-fraction-decomposition|partial-fraction decomposition]] of the generating rational function.
- **Real-partial-fraction machinery powers the trigonometric formulas.** §218's clean $\sin(n+1)\phi/\sin\phi$ is the "$k=1$" case of the iterative tower in §219–§222, which extends to repeated quadratic factors. The [[real-partial-fraction-decomposition|Chapter 12]] tower is exactly what makes the extension possible.
- **De Moivre's name appears twice.** Once for naming the [[recurrent-series|recurrent series]] themselves (§211, restating §62), once for naming the [[scale-of-the-relation|scale of the relation]] (§224). De Moivre's *Miscellanea Analytica* (1730) is the proximate source.
- **The $UV$ identity is the discriminant-like invariant.** §227's $UV = (B^2 - \alpha AB + \beta A^2)/(4\beta - \alpha^2)$ is the "irrational core" of the closed-form: it isolates exactly the quantity that appears under the square root in the term-from-predecessor formula. Modulo the substitution $\beta \mapsto -\beta$ this is a standard Fibonacci-like invariant.
- **Why apparent irrationality stays rational.** The series coefficients are rational by construction; the square root in §227 must therefore always evaluate to a rational. Euler does not prove this — he just notes it (source: chapter13, §227).

## Why this chapter matters

Closed-form general terms make recurrent series a tractable computational tool: any coefficient can be evaluated directly without iterating the recurrence. The trigonometric formulas of §217–§222 anticipate the discrete Fourier-type structure of solutions to linear recurrences with complex roots (modern: oscillatory solutions $r^n \cos n\phi$, $r^n \sin n\phi$). The "scale of the relation" framework is essentially the modern theory of constant-coefficient linear difference equations, written half a century before Lagrange formalized the analogous theory for differential equations.

Combined with [[chapter-12-on-the-development-of-real-rational-functions|Chapter 12]]'s real partial fractions and [[chapter-4-on-the-development-of-functions-in-infinite-series|Chapter 4]]'s expansion machinery, the *Introductio* now has a complete, real, closed-form theory of rational generating functions — the prerequisite for both the integration of rational functions and the formal manipulation of generating series in combinatorics.

## Inverse application in Chapter 17

[[chapter-17-using-recurrent-series-to-find-roots-of-equations|Chapter 17]] runs the chapter-13 closed-form machinery in reverse. There, the equation's coefficients are known but the roots are not; the dominant term $U p^n$ of the §215 expansion controls the ratio $Q/P \to p$ of consecutive recurrent-series coefficients, giving [[bernoullis-method-for-roots|Daniel Bernoulli's method]] for the largest root. The §217–§222 trigonometric formulas play the same role for a dominant [[trinomial-factor|trinomial factor]] — Euler eliminates $A, B,$ and $n$ from the §218 closed form to extract the modulus $p$ and argument $\phi$ of a dominant complex pair from four consecutive coefficients ([[trinomial-factor-from-recurrent-series]]).

## Related pages

- [[recurrent-series]]
- [[general-term-of-recurrent-series]]
- [[scale-of-the-relation]]
- [[closed-form-two-term-recurrence]]
- [[sum-of-recurrent-series]]
- [[partial-fraction-decomposition]]
- [[real-partial-fraction-decomposition]]
- [[trinomial-factor]]
- [[trigonometric-recurrent-progression]]
- [[de-moivre-formula]]
- [[powers-of-sine-and-cosine]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
- [[chapter-12-on-the-development-of-real-rational-functions]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
- [[bernoullis-method-for-roots]]
- [[trinomial-factor-from-recurrent-series]]
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]]
