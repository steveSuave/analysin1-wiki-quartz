# Chapter 12: On the Development of Real Rational Functions

**Summary**: Euler extends [[partial-fraction-decomposition|Chapter 2's partial-fraction algorithm]] from real linear factors to real *quadratic* factors of the form $p^2 - 2pqz\cos\phi + q^2z^2$ (the [[trinomial-factor]] of [[chapter-9-on-trinomial-factors|Chapter 9]]). The result keeps the decomposition entirely real even when the denominator has complex roots, and an iterative variant handles repeated quadratic factors.

**Sources**: chapter12.pdf

**Last updated**: 2026-05-04

---

## Overview

[[partial-fraction-decomposition|Chapter 2]] decomposed a proper rational function $M/N$ into one simple fraction per linear factor of $N$. When $N$ has complex linear factors the resulting partial fractions are also complex — useless if the goal is a *real* decomposition. Chapter 9 supplied the cure: every real polynomial factors into real linear factors and real quadratic [[trinomial-factor|trinomial factors]] $p^2 - 2pqz\cos\phi + q^2z^2$. Chapter 12 makes this cure operational: it gives an algorithm for the partial fraction with denominator equal to a quadratic trinomial, and then extends the algorithm to the case where that trinomial is repeated (source: chapter12.pdf, §199).

The chapter has two movements:

1. **§199–§205 — distinct quadratic factors.** For a single trinomial factor $p^2 - 2pqz\cos\phi + q^2z^2$ in $N$, the corresponding partial fraction is $(P + Qz)/(p^2 - 2pqz\cos\phi + q^2z^2)$ with two unknown coefficients $P$ and $Q$. Substituting the complex roots $z = (p/q)(\cos\phi \pm i\sin\phi)$ via [[de-moivre-formula|De Moivre]] turns the divisibility condition into two real equations, solvable for $P$ and $Q$ in closed form. §204–§205 streamline the formula so only one substitution is needed instead of two. See [[real-partial-fraction-decomposition]].
2. **§206–§210 — repeated quadratic factors.** When $(p^2 - 2pqz\cos\phi + q^2z^2)^k$ divides $N$, the contribution is a tower of $k$ partial fractions with quadratic denominators of decreasing power. Each numerator is determined by an iterative procedure that mirrors [[partial-fraction-decomposition|§42–§45]]: extract the top numerator, divide out one factor of the trinomial, repeat. The last "remainder" polynomial is the numerator of the complementary fraction with denominator $Z$ (the cofactor of the trinomial tower in $N$). See [[real-partial-fraction-decomposition]].

## Structure of the chapter

### §199 — Why real quadratic denominators

If the linear factors of the denominator are complex, the partial fractions of [[partial-fraction-decomposition|Chapter 2]] are also complex — "of little use to express a real rational function in terms of complex fractions" (source: chapter12.pdf, §199). Since every real polynomial admits real factorization into linear and quadratic pieces ([[fundamental-theorem-of-algebra]], constructively given by [[chapter-9-on-trinomial-factors|Chapter 9]]), a *real* rational function decomposes into partial fractions whose denominators are real linear or real quadratic factors.

### §200 — The form of the partial fraction

For one [[trinomial-factor|trinomial factor]] $p^2 - 2pqz\cos\phi + q^2z^2$ of $N$, the corresponding partial fraction has the form

$$\frac{P + Qz}{p^2 - 2pqz\cos\phi + q^2z^2},$$

with a *first*-degree numerator. The numerator must be exactly first degree: a higher degree would leave behind a polynomial part (which should already have been removed; see [[improper-rational-function]]) (source: chapter12.pdf, §200).

### §201 — The divisibility condition

Write $N = (p^2 - 2pqz\cos\phi + q^2z^2) Z$ and let $M$ be the numerator. Subtracting the $(P + Qz)/(\cdots)$ piece leaves $Y/Z$ where

$$Y = \frac{M - PZ - QZz}{p^2 - 2pqz\cos\phi + q^2z^2}.$$

For $Y$ to be a polynomial, $M - PZ - QZz$ must vanish at the two roots of the trinomial — namely $z = (p/q)(\cos\phi \pm i\sin\phi)$. Setting $f = p/q$, [[de-moivre-formula|De Moivre]] gives $z^n = f^n(\cos n\phi \pm i\sin n\phi)$ at each root (source: chapter12.pdf, §201).

### §202–§203 — Two real equations, closed-form solution

Substituting both roots into $M = PZ + QZz$ and separating real and imaginary parts yields two real equations $R = PS + QT$ and $r = Ps + Qt$, where (for $M = A + Bz + Cz^2 + \cdots$ and $Z = \alpha + \beta z + \gamma z^2 + \cdots$)

$$R = A + Bf\cos\phi + Cf^2\cos 2\phi + \cdots,\qquad r = Bf\sin\phi + Cf^2\sin 2\phi + \cdots,$$
$$S = \alpha + \beta f\cos\phi + \gamma f^2\cos 2\phi + \cdots,\qquad s = \beta f\sin\phi + \gamma f^2\sin 2\phi + \cdots,$$
$$T = \alpha f\cos\phi + \beta f^2\cos 2\phi + \cdots,\qquad t = \alpha f\sin\phi + \beta f^2\sin 2\phi + \cdots.$$

(That is: $R, r$ come from $M$; $S, s$ come from $Z$; $T, t$ come from $Zz$.) Solving the linear system,

$$P = \frac{Rt - rT}{St - sT},\qquad Q = \frac{Rs - rS}{sT - St}.$$

(source: chapter12.pdf, §203). See [[real-partial-fraction-decomposition]] for derivation and worked examples.

### §204–§205 — Streamlined formula

A direct calculation shows $T = f(S\cos\phi - s\sin\phi)$ and $t = f(S\sin\phi + s\cos\phi)$, so $T$ and $t$ are determined by $S, s, \cos\phi, \sin\phi$ alone. Substituting into the §203 expressions collapses to

$$\frac{P + Qz}{p^2 - 2pqz\cos\phi + q^2z^2} = \frac{(RS + rs)p\sin\phi + (Rs - rS)(p\cos\phi - qz)}{(p^2 - 2pqz\cos\phi + q^2z^2)(S^2 + s^2)\,p\sin\phi}.$$

Only the four scalars $R, r, S, s$ are needed — half the computation of §203 (source: chapter12.pdf, §205).

### §206 — Why repeated factors need a different rule

If the denominator contains $(p^2 - 2pqz\cos\phi + q^2z^2)^2$ or higher, then after substituting $z = f(\cos\phi \pm i\sin\phi)$ both $M - PZ - QZz$ *and* $Z$ vanish, so the §203 system degenerates and $P, Q$ cannot be solved (source: chapter12.pdf, §206). A new procedure is needed.

### §207–§209 — Iterative algorithm for $(p^2 - 2pqz\cos\phi + q^2z^2)^k$

The repeated-quadratic factor contributes the tower

$$\frac{U + uz}{(p^2 - 2pqz\cos\phi + q^2z^2)^k} + \frac{V + vz}{(p^2 - 2pqz\cos\phi + q^2z^2)^{k-1}} + \cdots + \frac{X + xz}{p^2 - 2pqz\cos\phi + q^2z^2}.$$

Each numerator is determined by a one-step substitution analogous to [[partial-fraction-decomposition|§45]]: substitute $z = f(\cos\phi \pm i\sin\phi)$ into a numerator expression and divide by the trinomial to expose the next numerator. Concretely (writing $N$ for the value of $Z$ at the root and $n$ for its imaginary part):

$$U = \frac{YN + yn}{N^2 + n^2} + \frac{Yn - yN}{N^2 + n^2}\cdot\frac{\cos\phi}{\sin\phi},\qquad u = -\frac{Yn - yN}{N^2 + n^2}\cdot\frac{q}{p\sin\phi},$$

with $Y, y$ the values of $M$ at the roots. Then $F = (M - (U + uz)Z)/(p^2 - 2pqz\cos\phi + q^2z^2)$ is the next polynomial; the same formula on $F$ produces $V, v$; and so on through $G, H, I, K, \ldots$ (source: chapter12.pdf, §207–§209). See [[real-partial-fraction-decomposition]] for the full derivation and worked example.

### §210 — The complementary fraction falls out for free

The sequence of polynomials $F, G, H, I, K, \ldots$ used to extract numerators is automatically the right object for the *complementary* fraction with denominator $Z$ (the cofactor of the trinomial tower in $N$). For $k = 1$, $F/Z$ is the complement; for $k = 2$, $G/Z$; and so on. The complement, having denominator $Z$ which contains *no* further power of this trinomial, can itself be expressed in partial fractions by the rules above (source: chapter12.pdf, §210).

## Worked examples in the chapter

Three examples in §203 plus one in §209 illustrate the procedure.

- **Example I (§203):** $\dfrac{z^2}{(1 - z + z^2)(1 + z^4)}$. The factor $1 - z + z^2$ has $p = q = 1$, $\cos\phi = 1/2$, $\phi = \pi/3$. Computation gives $P = -1$, $Q = 0$, so the partial fraction is $-1/(1 - z + z^2)$ and the complement is $(1 + z + z^2)/(1 + z^4)$.
- **Example II (§203):** Continues by decomposing the complement $(1 + z + z^2)/((1 + \sqrt 2 z + z^2)(1 - \sqrt 2 z + z^2))$. Both factors have $\phi = \pi/4$, with $f = -1$ and $f = +1$ respectively. The two partial fractions are $(\sqrt 2 - 1)\sqrt 2/(2(1 + \sqrt 2 z + z^2))$ and $(\sqrt 2 + 1)\sqrt 2/(2(1 - \sqrt 2 z + z^2))$.
- **Example III (§203):** $\dfrac{1 + 2z + z^2}{(1 - \tfrac{8}{5}z + z^2)(1 + 2z + 3z^2)}$. The first factor has $\cos\phi = 4/5$ — *not* a fractional part of a right angle, so the multiples $\cos n\phi, \sin n\phi$ must be computed by [[trigonometric-addition-formulas|the addition formulas]]. The result is $\dfrac{9(17 - 5z)/178}{1 - \tfrac{8}{5}z + z^2} + \dfrac{5(5 + 27z)/178}{1 + 2z + 3z^2}$.
- **Example (§209):** $\dfrac{z - z^3}{(1 + z^2)^4(1 + z^4)}$. The factor $(1 + z^2)^4$ has $\cos\phi = 0$, $\phi = \pi/2$. Iterating §207 gives the four partial fractions $\dfrac{z}{(1 + z^2)^4} + \dfrac{z}{2(1 + z^2)^3} + 0\cdot\dfrac{1}{(1 + z^2)^2} - \dfrac{z}{4(1 + z^2)}$. The complement, with denominator $1 + z^4$, is $(-z + z^3)/(4(1 + z^4))$.

## Notable points

- **The chapter is the missing complement to Chapter 2.** Chapter 2 promised a partial-fraction decomposition algorithm and gave one for linear factors. Chapter 12 finishes the job by handling the quadratic-factor case that arises whenever the polynomial has complex roots. After this chapter, *every* real rational function admits a fully real partial-fraction decomposition.
- **The §201 device is the same one as Chapter 9.** Substituting $z = f(\cos\phi \pm i\sin\phi)$ and separating real/imaginary parts is exactly the [[trinomial-factor|§148 trick]] for finding trinomial factors. Chapter 9 used the trick to *find* the factor; Chapter 12 uses it to find the *coefficient* of the partial fraction whose denominator is that factor. The unified mechanism explains why the [[de-moivre-formula]] is the workhorse of both chapters.
- **§204 is a small but real economy.** Without §204, one needs three substitutions (for $R/r$, $S/s$, $T/t$) — each a separate calculation of trigonometric multiples. §204 cuts the work by a third. Euler does not state a corresponding economy for the §207 repeated-factor formula, but the same observation applies there.
- **The "complementary fraction is free" remark of §210 is structural.** In the iterative procedure, the polynomial *being* divided at the last step is already the numerator of the leftover fraction. Modern implementations of partial-fraction decomposition exploit the same fact.

## Why this chapter matters

For *integration*, the goal is a sum of pieces each of which has a known antiderivative. Real linear pieces $A/(p - qz)$ integrate to logarithms; real quadratic pieces $(P + Qz)/(p^2 - 2pqz\cos\phi + q^2z^2)$ integrate to a logarithm plus an arctangent. By insisting on real denominators, Chapter 12 is the prerequisite for the [[partial-fraction-decomposition|partial-fractions integration technique]] developed in Euler's later *Institutiones calculi integralis* — and for everything in modern calculus textbooks under the same heading.

For *series expansion*, the [[recurrent-series|recurrent-series machinery]] of [[chapter-4-on-the-development-of-functions-in-infinite-series|Chapter 4]] reads coefficients off the denominator. A real partial-fraction decomposition lets the same machinery operate even when the denominator has complex roots — each real quadratic piece contributes a recurrent series with denominator $1 - 2(\cos\phi)Z + Z^2$, exactly the [[trigonometric-recurrent-progression|§129 trigonometric recurrent progression]].

## Related pages

- [[real-partial-fraction-decomposition]]
- [[partial-fraction-decomposition]]
- [[improper-rational-function]]
- [[trinomial-factor]]
- [[factoring-polynomials]]
- [[fundamental-theorem-of-algebra]]
- [[de-moivre-formula]]
- [[trigonometric-addition-formulas]]
- [[trigonometric-recurrent-progression]]
- [[chapter-2-on-the-transformation-of-functions]]
- [[chapter-9-on-trinomial-factors]]
