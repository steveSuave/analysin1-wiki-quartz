# Trinomial Factor from a Recurrent Series

**Summary**: §348–§353. The complex-roots counterpart to [[bernoullis-method-for-roots|Bernoulli's method]]. When the dominant pole of the generating rational function is a complex conjugate pair — equivalently, a real quadratic [[trinomial-factor|trinomial factor]] $1 - 2pz\cos\phi + p^2 z^2$ in the denominator — the ratio $Q/P$ of consecutive recurrent-series coefficients oscillates and does not converge. Yet four consecutive coefficients $P, Q, R, S$ suffice to determine *both* the modulus $p$ and the argument $\phi$ in closed form: $p = \sqrt{(R^2 - QS)/(Q^2 - PR)}$, $\cos\phi = (QR - PS)/(2\sqrt{(Q^2-PR)(R^2-QS)})$ — Euler's beautiful §351–§352 elimination.

**Sources**: chapter17

**Last updated**: 2026-05-11

---

## Setup: complex factor in the denominator (§348)

For a rational function

$$\frac{a + bz + cz^2 + \cdots}{1 - \alpha z - \beta z^2 - \cdots}$$

whose denominator has real linear factors $1 - qz, 1 - rz, \ldots$ together with an irreducible [[trinomial-factor|trinomial factor]] $1 - 2pz\cos\phi + p^2 z^2$, the [[general-term-of-recurrent-series|closed-form general term]] from [[chapter-13-on-recurrent-series|Chapter 13]] is

$$P_n z^n \;=\; \left(\frac{A\sin(n+1)\phi + B\sin n\phi}{\sin\phi}\,p^n + Cq^n + Dr^n + \cdots\right) z^n.$$

The trinomial factor contributes a *sinusoidal-amplitude-times-$p^n$* term; the real linear factors contribute geometric terms.

## Case 1: complex pair dominated by a real root (§348)

If some real root $q$ satisfies $|q| > p$, then $Cq^n$ dominates absolutely for large $n$ and $Q/P \to q$ — i.e. the [[bernoullis-method-for-roots|standard Bernoulli ratio]] still works and the largest *real* root is found, *exactly as if the complex roots were absent*. Euler emphasizes: "the method of finding the largest real root is not disturbed by the presence of complex roots, as long as the product of the two conjugate complex roots is smaller than the square of the largest real root" (source: chapter17, §348–§349).

The threshold for this case is $p^2 < q^2$, equivalently, **the product of the complex conjugate pair is less than the square of the largest real root**.

**Example I (§349)**: $x^3 - 2x - 4 = 0$ factors as $(x - 2)(x^2 + 2x + 2)$. The complex pair has product $2$, less than $2^2 = 4$. With scale $0, 2, 4$, numerator $1$:

$$1,\ 0,\ 2,\ 4,\ 4,\ 16,\ 24,\ 48,\ 112,\ 192,\ 416,\ 832,\ \ldots$$

Ratios approach $2$ — the real root is recovered, unaffected by the complex pair.

## Case 2: complex pair of magnitude equal to a real root (§349)

If $p^2 = q^2$ (equal magnitudes), the contributions of the complex pair and the real root persist at the same rate and produce a *periodic* or near-periodic pattern.

**Example II (§349)**: $x^3 - 4x^2 + 8x - 8 = 0$ has real root $2$ and complex pair with product $4 = 2^2$. With $x = 2y$ to simplify: $y^3 - 2y^2 + 2y - 1 = 0$. Initial terms $1, 2, 2$:

$$1,\ 2,\ 2,\ 1,\ 0,\ 0,\ 1,\ 2,\ 2,\ 1,\ 0,\ 0,\ 1,\ 2,\ 2,\ 1,\ \ldots$$

A six-periodic sequence. No root is read off from the ratio, but the *period* (here $6$) is itself informative: it encodes $\phi = \pi/3$ in the complex pair.

## Case 3: complex pair dominates (§349–§352)

If $p^2 > $ the square of every real root, the trinomial-factor contribution dominates everything else. In this regime $P_n \approx \frac{A\sin(n+1)\phi + B\sin n\phi}{\sin\phi}\,p^n$, and the ratio

$$\frac{Q}{P} = \frac{A\sin(n+2)\phi + B\sin(n+1)\phi}{A\sin(n+1)\phi + B\sin n\phi}\cdot p$$

is a quotient of two sines and *never settles down* — the sines oscillate and the ratio with them.

**Example III (§349)**: $x^3 - 3x^2 + 4x - 2 = 0$ factors as $(x - 1)(x^2 - 2x + 2)$. Real root $1$, complex pair with product $2 > 1$. Scale $3, -4, 2$, numerator $1$:

$$1,\ 3,\ 5,\ 5,\ 1,\ -7,\ -15,\ -15,\ 1,\ 33,\ 65,\ 65,\ 1,\ \ldots$$

The real root $1$ recurs as a *coincidence* (every fourth term), but the standard $Q/P$ analysis cannot extract anything from this oscillation.

## Eliminating $A$, $B$, and $n$ (§350–§352)

The trinomial-factor recurrent series satisfies a §63-style three-term relation involving only the **scale** of the trinomial. Specifically, the partial-fraction component $\frac{A + Bpz}{1 - 2pz\cos\phi + p^2 z^2}$ has recurrence $X_{n+2} = 2p\cos\phi\,X_{n+1} - p^2 X_n$, equivalently

$$P p^2 + R = 2Q p\cos\phi \qquad\text{and}\qquad Q p^2 + S = 2R p\cos\phi.$$

Two equations in two unknowns $p, \cos\phi$ — provided $P, Q, R, S$ are far enough out in the series that the complex pair dominates absolutely and contamination from the smaller terms is negligible.

Solving: from the first equation $\cos\phi = (Pp^2 + R)/(2Qp)$, and from the second $\cos\phi = (Qp^2 + S)/(2Rp)$. Equating and clearing denominators,

$$R(Pp^2 + R) = Q(Qp^2 + S) \quad\Longleftrightarrow\quad p^2(PR - Q^2) = QS - R^2,$$

so

$$\boxed{\;p = \sqrt{\frac{R^2 - QS}{Q^2 - PR}}.\;}$$

Once $p$ is known, $\cos\phi$ follows from either equation. Euler simplifies further using $\sin a\sin b = \tfrac{1}{2}(\cos(a-b) - \cos(a+b))$ to give a symmetric expression in all four coefficients (source: chapter17, §352):

$$\boxed{\;\cos\phi = \frac{QR - PS}{2\sqrt{(Q^2 - PR)(R^2 - QS)}}.\;}$$

Once $p$ and $\cos\phi$ are in hand, the trinomial factor $1 - 2pz\cos\phi + p^2 z^2$ is fully determined; its two complex linear factors give the dominant complex conjugate pair of roots of the original equation:

$$z = \frac{1}{p}(\cos\phi \pm i\sin\phi),\quad\text{i.e. the equation's roots are}\quad p(\cos\phi \pm i\sin\phi).$$

## The derivation in detail (§352)

From $Q/P$ and $R/Q$ in $\frac{A\sin(n+1)\phi + B\sin n\phi}{\sin\phi}p^n$ form, write

$$\frac{A}{B} = \frac{Q\sin n\phi - Pp\sin(n+1)\phi}{Pp\sin(n+2)\phi - Q\sin(n+1)\phi} = \frac{R\sin(n+1)\phi - Qp\sin(n+2)\phi}{Qp\sin(n+3)\phi - R\sin(n+2)\phi}.$$

Cross-multiplying gives a determinantal identity, and applying

$$\sin a\sin b = \tfrac{1}{2}\cos(a - b) - \tfrac{1}{2}\cos(a + b)$$

collapses index-$n$ dependence. The result is

$$(Pp^2 + R)(1 - \cos 2\phi) = Qp(\cos\phi - \cos 3\phi).$$

Using $\cos\phi - \cos 3\phi = 2\sin 2\phi\sin\phi = 4\sin^2\phi\cos\phi$ and $1 - \cos 2\phi = 2\sin^2\phi$:

$$Pp^2 + R = 2Qp\cos\phi,$$

the §350 relation. The companion $Qp^2 + S = 2Rp\cos\phi$ comes from shifting the index by $1$. Eliminating $\cos\phi$ as above yields the boxed formulas.

## Repeated trinomial factor (§353)

If the denominator has $(1 - 2pz\cos\phi + p^2 z^2)^k$ with $k \ge 2$, the general term acquires polynomial-in-$n$ factors (see [[general-term-of-recurrent-series|§220–§222]]), and the analysis becomes prohibitively complicated. Euler does not give a closed form for this case. The practical workaround: if some *real* root is already approximately known, use the [[bernoullis-method-for-roots|substitution shift $x = k + y$]] to convert the equation into one where the smallest root is small, and run smallest-root Bernoulli on the new equation.

**Example (§353)**: $x^3 - 3x^2 + 5x - 4 = 0$. Inspection (substitute $x = 1$: $-1 < 0$; substitute $x = 2$: $2 > 0$) shows a root between $1$ and $2$, near $1$. Substitute $x = 1 + y$:

$$1 - 2y - y^3 = 0,$$

with scale $2, 0, 1$, smallest root $y$ near $0.45$. Initial $1, 2, 4$:

$$1,\ 2,\ 4,\ 9,\ 20,\ 44,\ 97,\ 214,\ 472,\ 1041,\ 2296,\ \ldots$$

Smallest-root ratio (i.e. the *reciprocal* obtained from $1/y = $ largest root of scale-flipped equation): $1041/2296 = 0.453397$. Hence $x = 1.453397$, accurate to all visible digits.

## Why this is beautiful

The §348–§352 result is one of the *Introductio*'s most polished computational discoveries. It says:

> Four consecutive coefficients of a recurrent series determine, in closed form, the **modulus and argument** of the dominant complex conjugate pair of its generating rational function.

In modern eigenvalue language, this is the power method augmented to find a dominant *complex* eigenvalue from real iterations — the prototype for techniques like the Wilkinson shift and Bairstow's method (the latter explicitly extracts a quadratic factor from a polynomial by an iterative procedure built on exactly this kind of relation).

Euler does not pursue the §348–§352 result further — having stated it, he immediately points out the limitations (repeated trinomial factors, equal-magnitude cases) and the substitution rescue. But the formula is general: given any equation, run the recurrent series with [[scale-of-the-relation|scale]] read from coefficients, watch whether $Q/P$ converges (real-dominant case, [[bernoullis-method-for-roots|standard Bernoulli]]) or oscillates (complex-dominant case, §348–§352 extraction); from a long-enough tail one always extracts the dominant factor of the denominator.

## Related pages

- [[bernoullis-method-for-roots]]
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]]
- [[trinomial-factor]]
- [[general-term-of-recurrent-series]]
- [[real-partial-fraction-decomposition]]
- [[recurrent-series]]
- [[scale-of-the-relation]]
- [[de-moivre-formula]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-13-on-recurrent-series]]
