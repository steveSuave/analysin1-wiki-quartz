# De Moivre's Formula

**Summary**: §132–§133 of Chapter 8. The Pythagorean identity factors as $(\cos z + i\sin z)(\cos z - i\sin z) = 1$, and Euler observes that "although these factors are complex, still they are quite useful in combining and multiplying arcs." Multiplying two such factors gives $(\cos y + i\sin y)(\cos z + i\sin z) = \cos(y+z) + i\sin(y+z)$. Iteration yields De Moivre's formula

$$(\cos z \pm i\sin z)^n = \cos nz \pm i\sin nz$$

for any integer $n$. Solving for the real and imaginary parts and expanding by the binomial theorem produces finite-$n$ identities for $\cos nz$ and $\sin nz$ as polynomials in $\sin z$ and $\cos z$.

**Sources**: chapter8 (§132–§133)

**Last updated**: 2026-04-27

---

## §132 — Complex factorization of unity

The [[sine-and-cosine|Pythagorean identity]] $(\sin z)^2 + (\cos z)^2 = 1$ rewrites as a difference of squares:

$$1 = (\cos z)^2 - (i\sin z)^2 = (\cos z + i\sin z)(\cos z - i\sin z).$$

The factors $\cos z + i\sin z$ and $\cos z - i\sin z$ are complex conjugates with product $1$, so each is the multiplicative inverse of the other. Euler writes (source: chapter8, §132): "Although these factors are complex, still they are quite useful in combining and multiplying arcs."

## §132 — Multiplicativity of arcs

Computing the product of two such factors with different arcs:

$$(\cos y + i\sin y)(\cos z + i\sin z) = \cos y\cos z - \sin y\sin z + i(\sin y\cos z + \cos y\sin z).$$

The real part equals $\cos(y + z)$ and the imaginary part equals $\sin(y + z)$, by the [[trigonometric-addition-formulas|sum formulas]]. Hence

$$(\cos y + i\sin y)(\cos z + i\sin z) = \cos(y + z) + i\sin(y + z),$$

with the conjugate identity

$$(\cos y - i\sin y)(\cos z - i\sin z) = \cos(y + z) - i\sin(y + z).$$

The map $z \mapsto \cos z + i\sin z$ is a *homomorphism* from arc-addition to complex multiplication. Three factors compose the same way: $(\cos x \pm i\sin x)(\cos y \pm i\sin y)(\cos z \pm i\sin z) = \cos(x + y + z) \pm i\sin(x + y + z)$.

## §133 — The formula

Iterating the §132 multiplication with $n$ copies of the same factor yields, for any positive integer $n$,

$$(\cos z + i\sin z)^n = \cos nz + i\sin nz,\qquad (\cos z - i\sin z)^n = \cos nz - i\sin nz.$$

(source: chapter8, §133). The same identity holds for negative integers via the inverse $(\cos z + i\sin z)^{-1} = \cos z - i\sin z = \cos(-z) + i\sin(-z)$.

This is De Moivre's formula. Euler does not credit De Moivre by name in §133, but the substance of the identity had been published by Abraham de Moivre in 1722 and was familiar to Euler's audience.

## §133 — Solving for $\cos nz$ and $\sin nz$

Adding and subtracting the two De Moivre identities:

$$\cos nz = \frac{(\cos z + i\sin z)^n + (\cos z - i\sin z)^n}{2},$$

$$\sin nz = \frac{(\cos z + i\sin z)^n - (\cos z - i\sin z)^n}{2i}.$$

Expanding both $(\cos z \pm i\sin z)^n$ by Newton's binomial theorem and pairing terms (the even-power terms in $i\sin z$ cancel in the difference, the odd-power terms in $i\sin z$ cancel in the sum):

$$\cos nz = (\cos z)^n - \binom{n}{2}(\cos z)^{n-2}(\sin z)^2 + \binom{n}{4}(\cos z)^{n-4}(\sin z)^4 - \binom{n}{6}(\cos z)^{n-6}(\sin z)^6 + \cdots,$$

$$\sin nz = \binom{n}{1}(\cos z)^{n-1}\sin z - \binom{n}{3}(\cos z)^{n-3}(\sin z)^3 + \binom{n}{5}(\cos z)^{n-5}(\sin z)^5 - \cdots.$$

(source: chapter8, §133). For positive integer $n$ both series terminate; they are the *Chebyshev polynomials of the first and second kind*, in disguise. Euler does not name them; he uses these expansions purely as algebraic identities.

Sample low-$n$ cases:

- $n = 2$: $\cos 2z = (\cos z)^2 - (\sin z)^2$ and $\sin 2z = 2\sin z\cos z$ (the standard double-angle formulas).
- $n = 3$: $\cos 3z = (\cos z)^3 - 3\cos z(\sin z)^2$ and $\sin 3z = 3(\cos z)^2\sin z - (\sin z)^3$.

## The bridge to the trig power series

Up to here every formula is finite and algebraic — no series. The key §134 move is to allow $n$ to be infinitely large while $z$ is infinitely small, with $nz = v$ a finite arc. Under that limit each $\binom{n}{k}(\cos z)^{n-k}(\sin z)^k$ collapses (by the same $(j-m)/(nj) = 1/n$ identity used in [[exponential-series|Chapter 7]]) to $v^k/k!$, and the De Moivre expansions become the canonical [[sine-and-cosine-series|power series]] for $\cos v$ and $\sin v$.

## The bridge to Euler's formula

Combining the §133 expressions with the Chapter 7 identity $(1 + z/j)^j = e^z$:

$$(\cos z + i\sin z)^j\bigm|_{z\,\text{infinitesimal},\,jz = v} = (1 + iv/j)^j = e^{iv}.$$

Reading this off both sides yields [[eulers-formula|$e^{iv} = \cos v + i\sin v$]] (§138). De Moivre's formula is therefore the algebraic skeleton on which Euler's formula is built.

## Extension in Chapter 14

Chapter 14 (§249) uses De Moivre directly to derive $\tan nz$ as a rational function of $t = \tan z$:

$$\tan nz = \frac{(1+ti)^n - (1-ti)^n}{[(1+ti)^n + (1-ti)^n]\,i}$$

from which the $n$ roots $\tan z, \tan(\pi/n + z), \tan(2\pi/n + z), \ldots$ are identified and their [[vietas-formulas|Vieta sum/product relations]] read off. See [[trig-multiple-angle-partial-fractions]] and [[trig-values-as-roots]].

## Related pages

- [[sine-and-cosine]]
- [[trigonometric-addition-formulas]]
- [[binomial-series]]
- [[sine-and-cosine-series]]
- [[eulers-formula]]
- [[infinitesimal-and-infinite-numbers]]
- [[multiple-angle-polynomials]]
- [[trig-multiple-angle-partial-fractions]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
