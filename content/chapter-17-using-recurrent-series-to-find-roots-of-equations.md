# Chapter 17 — Using Recurrent Series to Find Roots of Equations

**Summary**: §332–§355. Euler inverts the direction of [[chapter-13-on-recurrent-series|Chapter 13]]: there, the *roots* of the denominator were known and the closed-form general term was extracted; here, only the *coefficients* of an equation $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$ are given, and the recurrent series is run *in order to discover the roots*. Following Daniel Bernoulli (Volume III of the *Commentaries of the St. Petersburg Academy*), the quotient of consecutive coefficients $Q/P$ of the recurrent series with scale $\alpha, \beta, \gamma, \ldots$ approaches the **largest root in absolute value** — the [[bernoullis-method-for-roots|Bernoulli method]]. The chapter then catalogues the failure modes (roots close in size, $\pm p$ pairs, repeated roots, dominant complex pairs) and the remedies (the substitution $x = y + k$, alternate-ratio reading, numerator $=1$ as a safety, and the §348–§352 [[trinomial-factor-from-recurrent-series|trinomial-factor extraction]] that recovers both modulus *and* argument of a dominant complex conjugate pair).

**Sources**: chapter17.pdf

**Last updated**: 2026-05-11

---

## Movement 1 — The basic correspondence (§332–§338)

A rational function with constant term $1$ in the denominator,

$$\frac{a + bz + cz^2 + dz^3 + \cdots}{1 - \alpha z - \beta z^2 - \gamma z^3 - \cdots},$$

expands as a [[recurrent-series|recurrent series]] $A + Bz + Cz^2 + \cdots$ whose [[scale-of-the-relation|scale]] is $\alpha, \beta, \gamma, \ldots$ (the §63 setup). If the denominator factors into distinct real linear factors $(1 - pz)(1 - qz)(1 - rz)\cdots$, the [[general-term-of-recurrent-series|general term]] is

$$Pz^n = z^n(Up^n + Vq^n + Wr^n + \cdots),$$

with $p$ the largest of $|p|, |q|, |r|, \ldots$ Then $Up^n$ dominates for large $n$, so

$$\frac{Q}{P} \;=\; \frac{Up^{n+1} + Vq^{n+1} + \cdots}{Up^n + Vq^n + \cdots} \;\longrightarrow\; p.$$

Numerator coefficients $a, b, c, \ldots$ only affect $U, V, W, \ldots$ — they do not change the limit $p$ (§336). The equation $1 - \alpha z - \beta z^2 - \cdots = 0$ has roots $z = 1/p, 1/q, \ldots$; equivalently $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$ (substitute $z = 1/x$) has roots $p, q, r, \ldots$. So **the largest root of the original equation equals the limiting ratio $Q/P$ of the recurrent series whose scale is read off the equation's coefficients**.

Worked **Example I (§338)**: $x^2 - 3x - 1 = 0$. Form $\frac{1 + 2z}{1 - 3z - z^2}$ (numerator $1 + 2z$ is arbitrary; this happens to give Lucas-like terms). The recurrent series $1, 2, 7, 23, 76, 251, 829, 2738, \ldots$ gives $2738/829 = 3.3027744$, agreeing with the true $(3 + \sqrt{13})/2 = 3.3027756$ to six digits.

**Example II (§338)**: $3x - 4x^3 = 1/2$ has three roots $\sin 10°, \sin 50°, \sin 70°$ (since $\sin 3\theta = 1/2$ at $\theta = 10°, 50°, 70°$). Substituting $1 - 6x + 8x^3 = 0$, the smallest root comes from the recurrent series $0, 0, 1, 6, 36, 208, 1200, 6912, 39808, 229248$ with ratio $39808/229248 = 0.1736515$, vs. true $\sin 10° = 0.1736482$.

See [[bernoullis-method-for-roots]].

## Movement 2 — Failure modes (§339–§342)

### Roots of similar magnitude

**Example III (§338)** seeks the *largest* root of $1 - 6x + 8x^3 = 0$. After $x = y/2$ the equation becomes $y^3 - 3y + 1 = 0$ with roots $2\sin 10°, 2\sin 50°, -2\sin 70°$. The series $1, 1, 1, 2, 2, 5, 4, 13, 7, 35, 8, 98, -11, \ldots$ does not converge cleanly: the two largest roots in absolute value, $-2\sin 70°$ and $2\sin 50°$, are too close in size, and the powers of the second do not vanish quickly compared to the first (§339).

### Remedy: substitution shift (§340–§341)

Substitute $x = y - 1$ in $1 - 6x + 8x^3 = 0$ to obtain $8y^3 - 24y^2 + 18y - 1 = 0$ with roots $1 - \sin 70°, 1 + \sin 50°, 1 + \sin 10°$. Now the *smallest* of these new roots ($\approx 0.06$) is much smaller than the others, so it is reliably extracted by the recurrent series.

**Example IV (§340)** continues with $z = y/2$, giving $z^3 - 6z^2 + 9z - 1 = 0$, recurrent series $1, 1, 4, 31, 256, 2122, 17593, 145861$. Ratio $17593/145861 = 0.12061483$, hence $y = 0.06030741$ and $\sin 70° = 1 - y = 0.93969258$, matching the true value to all printed digits.

The general principle (§341): if $k$ is approximately known to be near some root, then $x = y + k$ makes the corresponding $y$ root much smaller than the others, and the smallest-root version of Bernoulli's method finds it cleanly. This **bootstrap to any root** is what makes the method universal.

### Roots of equal magnitude, opposite sign (§342)

If both $p$ and $-p$ are roots, then $U p^n + V(-p)^n$ oscillates: $Q/P$ never converges. But *alternate* ratios $R/P, S/Q, T/R, \ldots$ converge to $p^2$. Example: $x^3 - x^2 - 5x + 5 = 0$ has roots $\sqrt 5, -\sqrt 5, 1$. The series $1, 2, 3, 8, 13, 38, 63, 188, 313, 938, 1563$ has $1563/313 \approx 938/188 \approx 313/63 \approx 5 = (\sqrt 5)^2$.

## Movement 3 — Numerator choice (§343–§345)

The coefficient $U$ in $P = Up^n + \cdots$ depends only on the *numerator* of the rational function. By choosing the numerator equal to the product of all denominator factors *except* $(1 - pz)$, one cancels that factor entirely and the series becomes geometric in some *other* root. So a careless choice of numerator can secretly elide the largest root.

§345 fixes this: use **numerator $= 1$**. Then the recurrent series is determined by the scale alone, with no risk of accidental cancellation. The (signed) Example shows $y^3 - 3y + 1 = 0$ recovered correctly with numerator $1$ and scale $0, 3, -1$.

## Movement 4 — Repeated real factors (§346–§347)

If the denominator has $(1 - pz)^2$ with $p$ largest, the general term becomes $z^n((n+1)A p^n + B q^n + \cdots)$. The ratio $Q/P = (n+2)/(n+1)\cdot p \cdot \frac{(n+1)A + B q^n/p^n/(n+1)}{(n+1)A + \cdots}$ still tends to $p$, but slowly and always from above.

**Example I (§347)**: $x^3 - 3x^2 + 4 = 0$ has $x = 2$ as a double root. The series $1, 3, 9, 23, 57, 135, 313, 711, 1593$ has ratios always greater than $2$ — converging slowly because $(n+2)/(n+1)\to 1$ only as $1/n$.

For triple roots $(1-pz)^3$ the leading coefficient becomes $\binom{n+2}{2}A p^n$, with the same slow $1 + O(1/n)$ excess. The lesson: equations with repeated roots are intrinsically harder for Bernoulli's method than those with all distinct roots. See [[bernoullis-method-for-roots]] for full details.

## Movement 5 — Dominant complex factor (§348–§352)

When the denominator has a [[trinomial-factor|trinomial factor]] $1 - 2pz\cos\phi + p^2 z^2$ with $p$ greater than every other denominator pole, the general term (from [[general-term-of-recurrent-series|Chapter 13]]) is

$$P = \frac{A\sin(n+1)\phi + B\sin n\phi}{\sin\phi}\,p^n.$$

$Q/P$ involves $\sin(n+2)\phi/\sin(n+1)\phi$, which oscillates and never converges. Yet two consecutive recurrent-series relations $Pp^2 + R = 2Qp\cos\phi$ and $Qp^2 + S = 2Rp\cos\phi$ eliminate the unknown amplitudes $A, B$ and the index $n$ entirely, yielding the closed-form pair

$$p = \sqrt{\frac{R^2 - QS}{Q^2 - PR}},\qquad \cos\phi = \frac{QR - PS}{2\sqrt{(Q^2 - PR)(R^2 - QS)}}.$$

This recovers both *modulus* $p$ and *argument* $\phi$ of the dominant complex conjugate pair from four consecutive terms $P, Q, R, S$ of the recurrent series. See [[trinomial-factor-from-recurrent-series]].

§349 warns of the threshold: the procedure works only when the product of the complex conjugate pair (which equals $p^2$ in the trinomial) is *less* than the square of the largest real root. Equal magnitudes produce a periodic series; complex roots dominating give nothing at all from a $Q/P$ analysis without the §351–§352 trick.

**Example I (§349)**: $x^3 - 2x - 4 = 0$ factors as $(x - 2)(x^2 + 2x + 2)$. The complex-pair product is $2 < 2^2 = 4$, so the real root dominates. Series $1, 0, 2, 4, 4, 16, 24, 48, 112, 192, 416, 832 \to$ ratio $2$. **Example II**: $x^3 - 4x^2 + 8x - 8 = 0$ has real root $2$ and complex pair with product $4 = 2^2$ (equal magnitude); the series $1, 2, 2, 1, 0, 0, 1, 2, 2, 1, 0, 0, \ldots$ is *periodic* and no root is read off. **Example III**: $x^3 - 3x^2 + 4x - 2 = 0$ has real root $1$ and complex pair with product $2 > 1$; the series $1, 3, 5, 5, 1, -7, -15, -15, 1, 33, 65, 65, 1, \ldots$ shows the real root $1$ recurring as a coincidence — it is *not* the dominant root and the method cannot recover it directly.

## Movement 6 — Multiple equal trinomial factors and substitution rescue (§353)

When several equal trinomial factors stack, the analysis is impractical. If a real root is already known approximately, the §341 substitution $x = k + y$ converts to an equation in $y$ whose smallest root is the offset; the smallest-root version of Bernoulli's method handles it.

**Example (§353)**: $x^3 - 3x^2 + 5x - 4 = 0$ has a root near $1$. Substituting $x = 1 + y$ gives $1 - 2y - y^3 = 0$. With scale $2, 0, 1$ the recurrent series is $1, 2, 4, 9, 20, 44, 97, 214, 472, 1041, 2296, \ldots$, ratio $1041/2296 = 0.453397$, so $x = 1.453397$.

## Movement 7 — Geometric progression as a root detector (§354)

If the recurrent series eventually settles into a geometric progression $P, Q, R, S, T, \ldots$ with common ratio $x = Q/P$, then because the scale of the relation $\alpha, \beta, \gamma, \delta$ governs $T = \alpha S + \beta R + \gamma Q + \delta P$, substituting $R/P = x^2$, $S/P = x^3$, $T/P = x^4$ produces

$$x^4 = \alpha x^3 + \beta x^2 + \gamma x + \delta,$$

i.e. $x$ is a root of the characteristic equation $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$. This is the *theoretical* reason Bernoulli's method works: the tail of the recurrent series, dominated by the largest root, becomes geometric with ratio $p$, and that ratio satisfies the equation.

## Movement 8 — Application to transcendental equations (§355)

The method generalizes formally to *infinite* equations. Euler's example: from the [[sine-and-cosine-series|sine series]],

$$\frac{1}{2} = z - \frac{z^3}{6} + \frac{z^5}{120} - \frac{z^7}{5040} + \cdots\quad\text{has smallest root } z = \pi/6.$$

Rewriting $0 = 1 - 2z + z^3/3 - z^5/60 + z^7/2520 - \cdots$, the scale is $2, 0, -1/3, 0, 1/60, 0, -1/2520, 0, \ldots$. Taking the first few terms of the recurrent series gives $1, 2, 4, 23/3, 44/3, 1681/60, 2408/45$, with ratio $\frac{1681\cdot 45}{2408\cdot 60} = \frac{5043}{9632} = 0.52356$, agreeing with $\pi/6 = 0.523598$ to four digits — error $3/100000$. The method works because *all* roots of $\sin z = 1/2$ are real and the smallest (in absolute value) is well-separated from the next. For most transcendental equations this is not the case, so the method is rarely useful in the transcendental setting.

## Significance

Chapter 17 turns the recurrent-series machinery into a **general-purpose root-finder**:

- Numerically, **every** root of every polynomial equation is reachable by combining Bernoulli's method with the substitution shift $x = y + k$. Convergence is governed by the *ratio* of consecutive root magnitudes — fast when one root dominates, slow when several are close.
- Algorithmically, the method is what we now recognize as the **power method** for the largest eigenvalue of the [[scale-of-the-relation|companion matrix]]: iterating $v \mapsto Mv$, the dominant eigenvector emerges and the dominant eigenvalue is the Rayleigh quotient $\langle Mv, v\rangle/\langle v, v\rangle$ — precisely the $Q/P$ ratio when $v$ is encoded as consecutive terms of the recurrent series.
- The §351–§352 closed form $p = \sqrt{(R^2 - QS)/(Q^2 - PR)}$, $\cos\phi = (QR - PS)/(2\sqrt{(Q^2 - PR)(R^2 - QS)})$ is a 1748 ancestor of techniques for finding **complex** dominant eigenvalues from real iterations (Wilkinson shifts, Bairstow's method).

Chapter 17 is the computational counterpart of [[chapter-13-on-recurrent-series|Chapter 13]] — the inverse direction of the same correspondence between the [[scale-of-the-relation|scale of the relation]] of a recurrent series and the roots of its generating polynomial.

## Related pages

- [[bernoullis-method-for-roots]]
- [[trinomial-factor-from-recurrent-series]]
- [[recurrent-series]]
- [[scale-of-the-relation]]
- [[general-term-of-recurrent-series]]
- [[closed-form-two-term-recurrence]]
- [[trinomial-factor]]
- [[real-partial-fraction-decomposition]]
- [[sine-and-cosine-series]]
- [[chapter-13-on-recurrent-series]]
- [[chapter-9-on-trinomial-factors]]
