# Continued Fraction ↔ Alternating Series

**Summary**: Every [[continued-fraction|continued fraction]] equals an alternating series whose terms are the differences of consecutive convergents, with denominators that are products of consecutive convergent denominators. Conversely, every alternating series can be written as a continued fraction — but only after a free choice of partial denominators, which Euler exploits with several elegant templates. The conversion specialises to Brouncker's $4/\pi$, the continued fraction for $\log 2$, the continued fractions for $1/(e-1)$ and $\cos 1$, and several parametric families.

**Sources**: `chapter18` (§363–§373).

**Last updated**: 2026-05-11

---

## Continued fraction → alternating series (§363–§366)

Let $P, Q, R, S, T, \ldots$ denote the successive *denominators* of the [[convergents-of-a-continued-fraction|convergents]] (after the trivial $1/0$ and $a/1$), so $P = b$, $Q = bc + \beta$, $R = bcd + \beta d + \gamma b$, $S = bcde + \beta de + \gamma be + \delta bc + \beta\delta$, etc. By the convergent recurrence these satisfy

$$Q = Pc + \beta,\qquad R = Qd + \gamma P,\qquad S = Re + \delta Q,\qquad T = Sf + \epsilon R, \ \ldots$$

Subtracting consecutive convergents (§363) gives a telescoping identity that Euler writes as

$$\boxed{\ z \;=\; a + \frac{\alpha}{P} - \frac{\alpha\beta}{PQ} + \frac{\alpha\beta\gamma}{QR} - \frac{\alpha\beta\gamma\delta}{RS} + \frac{\alpha\beta\gamma\delta\epsilon}{ST} - \cdots\ }$$

So the value of the continued fraction is an alternating series whose $k$-th term has numerator $\alpha\beta\gamma\cdots$ ($k$ factors of partial-numerator data) and denominator $\;P_{k-1}P_k$ (the product of two consecutive convergent denominators).

If the partial numerators are all $1$ and the partial denominators $a, b, c, \ldots$ are positive integers (the *simple* form), this series converges very rapidly — its terms decrease at least geometrically.

## Alternating series → continued fraction (§365–§368)

Given $x = A - B + C - D + E - \cdots$, Euler matches term by term against the §363 expansion:

$$\frac{\alpha}{P} = A,\quad \frac{\alpha\beta}{PQ} = B,\quad \frac{\alpha\beta\gamma}{QR} = C,\quad \frac{\alpha\beta\gamma\delta}{RS} = D,\quad \ldots$$

Solving sequentially:

$$\alpha = AP,\quad \beta = \frac{BQ}{A},\quad \gamma = \frac{CR}{BP},\quad \delta = \frac{DS}{CQ},\quad \epsilon = \frac{ET}{DR},\ldots$$

Since the convergent denominators $P, Q, R, S, \ldots$ depend on the partial denominators $b, c, d, e, \ldots$ which are *free*, this gives a one-parameter family per level. Euler exploits the freedom to clear fractions.

### Template I — $A, B, C, \ldots$ integers (§368)

Set $b = 1$, $c = A - B$, $d = B - C$, $e = C - D$, $f = D - E$, $\ldots$. Then

$$\alpha = A,\quad \beta = B,\quad \gamma = AC,\quad \delta = BD,\quad \epsilon = CE,\quad \ldots$$

and the continued fraction is

$$x = \cfrac{A}{1 + \cfrac{B}{A - B + \cfrac{AC}{B - C + \cfrac{BD}{C - D + \cfrac{CE}{D - E + \cdots}}}}}$$

### Template II — reciprocal terms (§369)

For $x = 1/A - 1/B + 1/C - 1/D + \cdots$, set $b = A$, $c = B - A$, $d = C - B$, $e = D - C$, $\ldots$. Then $\alpha = 1$, $\beta = A^2$, $\gamma = B^2$, $\delta = C^2$, $\ldots$ and

$$x = \cfrac{1}{A + \cfrac{A^2}{B - A + \cfrac{B^2}{C - B + \cfrac{C^2}{D - C + \cdots}}}}.$$

The two famous specialisations:

- $A = 1, B = 2, C = 3, \ldots$ gives the [[continued-fraction-for-log-2|continued fraction for $\log 2$]] (Example I).
- $A = 1, B = 3, C = 5, \ldots$ gives [[brouncker-formula|Brouncker's continued fraction for $4/\pi$]] (Example II).

A parametric example (III): $A = m, B = m + n, C = m + 2n, \ldots$ gives the continued fraction for $\sum (-1)^k/(m + kn)$. Example IV reuses [[cotangent-partial-fraction|§178]] to convert $\pi\cos(m\pi/n)/(n\sin(m\pi/n))$ into a continued fraction.

### Template III — products in denominators (§370)

For $x = 1/A - 1/(AB) + 1/(ABC) - 1/(ABCD) + \cdots$, set $b = A$, $c = B - 1$, $d = C - 1$, $e = D - 1$, $\ldots$. Then $\alpha = 1$, $\beta = A$, $\gamma = B$, $\delta = C$, $\ldots$ and

$$x = \cfrac{1}{A + \cfrac{A}{B - 1 + \cfrac{B}{C - 1 + \cfrac{C}{D - 1 + \cdots}}}}.$$

The two named specialisations (§370):

- $1/e = 1 - 1 + 1/2 - 1/6 + 1/24 - \cdots$ gives $\displaystyle \frac{1}{e - 1} = \cfrac{1}{1 + \cfrac{2}{2 + \cfrac{3}{3 + \cfrac{4}{4 + \cfrac{5}{5 + \cdots}}}}}\,.$
- $\cos 1 = 1 - 1/2 + 1/(2\cdot 12) - 1/(2\cdot 12\cdot 30) + \cdots$ gives $\displaystyle \cos 1 = \cfrac{1}{1 + \cfrac{1}{1 + \cfrac{2}{11 + \cfrac{12}{29 + \cfrac{30}{55 + \cdots}}}}}\,.$

### Templates IV–V — power-series and z-product variants (§371–§373)

For $x = A - Bz + Cz^2 - Dz^3 + \cdots$, set $b = 1$, $c = A - Bz$, $d = B - Cz$, $\ldots$, giving partial numerators $\alpha = A$, $\beta = Bz$, $\gamma = ACz$, $\delta = BDz$, $\ldots$ The more general template (§372) handles $x = A/L - By/(Mz) + Cy^2/(Nz^2) - \cdots$, and (§373) the product-form $x = A/L - ABy/(LMz) + ABCy^2/(LMNz^2) - \cdots$.

## The asymmetry of the conversion (§374–§375)

Series-to-continued-fraction always works; the converse is harder. Euler shows that the simple periodic CF $1/(2 + 1/(2 + \cdots))$ produces (via the §363 telescoping)

$$x = \tfrac{1}{2} - \tfrac{1}{2\cdot 5} + \tfrac{1}{5\cdot 12} - \tfrac{1}{12\cdot 29} + \cdots,$$

a strongly convergent series whose value is not visible from the series — but is immediately seen from the CF as $\sqrt 2 - 1$ by the §376 quadratic-equation trick. So continued fractions sometimes know more than their associated series do.

## Related pages

- [[chapter-18-on-continued-fractions]]
- [[continued-fraction]]
- [[convergents-of-a-continued-fraction]]
- [[brouncker-formula]] — Template II at $A, B, C, \ldots = 1, 3, 5, \ldots$
- [[continued-fraction-for-log-2]] — Template II at $A, B, C, \ldots = 1, 2, 3, \ldots$
- [[continued-fraction-for-e]] — Template III at $A, B, C, \ldots = 1, 2, 3, \ldots$ (after a one-term shift)
- [[logarithmic-series]] — source of the $\log 2$ alternating series
- [[arctangent-series]] — source of the $\pi/4$ alternating series
- [[cotangent-partial-fraction]] — source of the §370 Example IV trig series
