# Bernoulli's Method for Roots

**Summary**: §332–§347, §354–§355. Daniel Bernoulli's procedure for finding the *largest root in absolute value* of an algebraic equation $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$: form the [[recurrent-series|recurrent series]] with [[scale-of-the-relation|scale]] $\alpha, \beta, \gamma, \ldots$ and read the limit of $Q/P$ (ratio of consecutive coefficients). Universality comes from the substitution shift $x = y + k$: once any root is approximately known, shift to make *that* root small and rerun the method on the new equation to extract it as the *smallest* root. The page covers the basic procedure, the failure modes (close roots, $\pm p$ pairs, repeated roots), the safety guarantee from numerator $= 1$, and the §354 theoretical justification via geometric progression of the tail.

**Sources**: chapter17.pdf

**Last updated**: 2026-05-11

---

## The principle (§332–§337)

Consider any equation

$$x^m - \alpha x^{m-1} - \beta x^{m-2} - \gamma x^{m-3} - \cdots = 0\qquad (*)$$

with $m$ roots $p, q, r, \ldots$ (real and distinct for the moment). Substituting $x = 1/z$ turns $(*)$ into

$$1 - \alpha z - \beta z^2 - \gamma z^3 - \cdots = 0,$$

whose roots are $1/p, 1/q, 1/r, \ldots$. Now expand any rational function with this denominator as a [[recurrent-series|recurrent series]] (§63):

$$\frac{a + bz + cz^2 + \cdots}{1 - \alpha z - \beta z^2 - \cdots} \;=\; A + Bz + Cz^2 + Dz^3 + \cdots$$

with coefficients satisfying $A = a$, $B = \alpha A + b$, $C = \alpha B + \beta A + c$, $\ldots$ — beyond the numerator's length, the recurrence is $X_{n+k} = \alpha X_{n+k-1} + \beta X_{n+k-2} + \cdots$ pure.

If the denominator factors as $(1 - pz)(1 - qz)\cdots$ into distinct real linear factors, then [[real-partial-fraction-decomposition|partial fractions]] give

$$\frac{a + bz + \cdots}{(1 - pz)(1 - qz)\cdots} \;=\; \frac{U}{1 - pz} + \frac{V}{1 - qz} + \cdots,$$

so by [[general-term-of-recurrent-series|§215]] the general term is

$$P_n z^n = z^n(U p^n + V q^n + W r^n + \cdots).\qquad(**)$$

Take $|p| > |q| > |r| > \cdots$. For large $n$ the $U p^n$ term dominates absolutely, so

$$\frac{P_{n+1}}{P_n} = \frac{Up^{n+1} + Vq^{n+1} + \cdots}{Up^n + Vq^n + \cdots} \xrightarrow{n\to\infty} p.\qquad(\heartsuit)$$

The numerator coefficients $a, b, c, \ldots$ only affect the *constants* $U, V, W, \ldots$ — they do not change the limit $(\heartsuit)$ (source: chapter17.pdf, §336). Hence:

**The largest root of $(*)$ — in absolute value — is the limit of the quotient of consecutive terms of any recurrent series whose scale of the relation is $\alpha, \beta, \gamma, \ldots$.**

This is Bernoulli's method.

## Setting up the computation (§338)

1. From the equation $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$, read off the [[scale-of-the-relation|scale]] $\alpha, \beta, \gamma, \ldots$.
2. Choose initial values $A, B, C, \ldots$ (the first $k$ terms; equivalently, choose the numerator of the rational function).
3. Generate as many terms as needed by the recurrence.
4. The ratio of the last two terms approximates the largest root in absolute value.

The more terms taken, the better the approximation; the speed of convergence depends on how dominant $p$ is over the next-largest $|q|$.

### Example I — quadratic (§338)

$x^2 - 3x - 1 = 0$. Scale: $\alpha = 3, \beta = 1$. Initial terms chosen as $A = 1, B = 2$. Recurrence $C = 3B + A$, $D = 3C + B$, $\ldots$:

$$1,\ 2,\ 7,\ 23,\ 76,\ 251,\ 829,\ 2738,\ \ldots$$

Quotient $2738/829 = 3.3027744\ldots$, vs. true value $(3 + \sqrt{13})/2 = 3.3027756\ldots$. Error one part per million. The successive quotients are *alternately greater than and less than* the true root.

### Example II — finding a small root via $z = 1/x$ (§338)

The equation $3x - 4x^3 = 1/2$ has three roots $\sin 10°, \sin 50°, \sin 70°$ (one-third the angle whose sine is $1/2$). Multiplying out: $1 - 6x + 8x^3 = 0$. The smallest root in absolute value is $\sin 10°$. To target it, work directly with $1 - 6x + 8x^3 = 0$ rather than substituting $z = 1/x$ — the *roots* of the equation $1 - 6x + 8x^3 = 0$ are $1/p, 1/q, 1/r$ where $p, q, r$ are sines, but read with $z$ as variable name. Choose numerator $a + bx + cx^2 = 0 + 0\cdot x + 1\cdot x^2$ for arithmetic convenience. Series:

$$0,\ 0,\ 1,\ 6,\ 36,\ 208,\ 1200,\ 6912,\ 39808,\ 229248,\ \ldots$$

Quotient $39808/229248 = 0.1736515$. True $\sin 10° = 0.1736482$.

## Failure modes

### Close roots (Example III, §338–§339)

Same equation $1 - 6x + 8x^3 = 0$, now seeking the *largest* root. With $x = y/2$ this becomes $y^3 - 3y + 1 = 0$, roots $2\sin 10°, 2\sin 50°, -2\sin 70°$. Scale $0, 3, -1$, initial $1, 1, 1$:

$$1,\ 1,\ 1,\ 2,\ 2,\ 5,\ 4,\ 13,\ 7,\ 35,\ 8,\ 98,\ -11,\ \ldots$$

Negative term reveals the largest root is negative ($x = -2\sin 70°$), but $-605/632 = -0.957$ is a poor approximation to $-2\sin 70° = -1.8794$. Why? The two largest roots in absolute value, $-2\sin 70°$ and $2\sin 50°$, are nearly equal in magnitude — their powers vanish at comparable rates, so the second-largest contribution decays slowly (§339). The approximations also alternate above and below the true value, because the powers of the second root alternate sign as $(2\sin 50°)^n$ stays positive while $(-2\sin 70°)^n$ flips.

### The remedy: substitution shift (§340–§341)

Substitute $x = y + k$ where $k$ is close to a target root. This shifts that root toward $y = 0$, making it the *smallest* in the new equation, and well-separated from the others (which are now near $\text{(other roots)} - k$). Then Bernoulli's method applied to the new equation extracts the small root cleanly.

Continuing the example: $1 - 6x + 8x^3 = 0$ with $x = y - 1$ becomes $8y^3 - 24y^2 + 18y - 1 = 0$, with roots $1 - \sin 70°, 1 + \sin 50°, 1 + \sin 10°$. The first is $\approx 0.06$, much smaller than the other two near $1.77, 1.17$.

**Example IV (§340)**: from this equation set $y = z/2$ to get $z^3 - 6z^2 + 9z - 1 = 0$, scale of relation $6, -9, 1$ (smallest root) or $9, -6, 1$ (largest, with $z = 1/y'$ tricks). With scale $9, -6, 1$ for the smallest root and numerator $1$:

$$1,\ 1,\ 4,\ 31,\ 256,\ 2122,\ 17593,\ 145861,\ \ldots$$

$17593/145861 = 0.12061483$, so $y = 0.06030741$, hence $\sin 70° = 1 - y = 0.93969258$, matching the true value in all digits shown.

**General principle (§341)**: if $k$ is approximately near some root, $x = y + k$ moves *that* root to a small $y$-value, which Bernoulli's method then resolves to high accuracy. This trick is what makes the method **universal** — any root can be located approximately by inspection of sign changes, refined to a few digits, then sharpened to many digits by the substitution-and-iterate cycle.

### Roots of equal magnitude, opposite sign (§342)

If $\pm p$ are both roots, $P_n = Up^n + V(-p)^n + \cdots$ does not have a single dominant term: the contributions $U + V(-1)^n$ oscillate. The ratio $Q/P$ never converges. **But** the alternate-term ratio

$$\frac{P_{n+2}}{P_n} = \frac{Up^{n+2} + V(-p)^{n+2} + \cdots}{Up^n + V(-p)^n + \cdots} = p^2\cdot\frac{U + V(-1)^n + \text{small}}{U + V(-1)^n + \text{small}}\to p^2$$

converges to **$p^2$** as long as the third-largest root has magnitude $< p$.

**Example (§342)**: $x^3 - x^2 - 5x + 5 = 0$ factors as $(x - 1)(x^2 - 5) = 0$, with roots $\sqrt 5, -\sqrt 5, 1$. Scale $1, 5, -5$, initial $1, 2, 3$:

$$1,\ 2,\ 3,\ 8,\ 13,\ 38,\ 63,\ 188,\ 313,\ 938,\ 1563,\ \ldots$$

Alternate ratios: $1563/313 \approx 4.994$, $938/188 \approx 4.99$, $313/63 \approx 4.97$ — all approximating $5 = (\sqrt 5)^2$. Once $p^2$ is known, $p = \sqrt 5$ is recovered (with sign determined by inspection).

Alternative: substitute $x = y + 2$ to get $1 - 3y - 5y^2 - y^3 = 0$ with smallest root $\sqrt 5 - 2$, scale $3, 5, 1$:

$$1,\ 1,\ 1,\ 9,\ 33,\ 145,\ 609,\ 2585,\ 10945,\ \ldots$$

$2585/10945 = 0.2361$, so $y = 0.2361$ and $x = 2.2361 = \sqrt 5$. The substitution rescue works as cleanly here as for close roots.

## Numerator choice (§343–§345)

The recurrent series depends on the numerator only through the constants $U, V, W, \ldots$ in $(**)$. Crucially, the numerator can be chosen so that $U = 0$ — in which case the largest root $p$ silently disappears from the series.

**Example (§343)**: $x^3 - 6x^2 + 10x - 3 = 0$ has largest root $3$. The rational function

$$\frac{1 - 3z}{1 - 6z + 10z^2 - 3z^3}$$

removes the factor $1 - 3z$ entirely (after cancellation it equals $\frac{1}{1 - 3z + z^2}$, whose largest root is the largest root of $z^2 - 3z + 1 = 0$, *not* $3$). The recurrent series $1, 3, 8, 21, 55, 144, 377, \ldots$ (Fibonacci-like) approaches $(3+\sqrt 5)/2$, *not* $3$.

§344 turns the bug into a feature: by choosing the numerator equal to the product of all denominator factors *except* the one corresponding to a desired root, the series becomes purely geometric in that root.

**Safe default (§345)**: take **numerator $= 1$**. Then the partial-fraction expansion has no zero coefficients (a $1/(1-pz)$ piece appears for every linear factor of the denominator), and the largest root is faithfully extracted. Confirming with $y^3 - 3y + 1 = 0$: scale $0, 3, -1$, numerator $1$, initial $1, 0, 3$:

$$1, 0, 3, -1, 9, -6, 28, -27, 90, -109, 297, -517, 1000, -1848, 3517, -6544, \ldots$$

Convergence to a constant ratio is clear, indicating a negative dominant root; $-6544/3517 = -1.860676$ vs. true $-1.8679385$. Slow because of the close-roots problem, but the method does *find* the right root rather than getting tricked.

## Repeated real roots (§346–§347)

If the denominator has $(1 - pz)^2$ with $p$ largest, the [[general-term-of-recurrent-series|general term]] becomes

$$P_n = ((n+1)A + B q^n/p^n + C r^n/p^n + \cdots) p^n.$$

So $Q/P = p\cdot\frac{(n+2)A + \text{decaying}}{(n+1)A + \text{decaying}} \to p$, but the ratio approaches $p$ slowly and always **from above** (since $(n+2)/(n+1) > 1$). For triple roots $(1 - pz)^3$ the leading coefficient is $\binom{n+2}{2}A p^n$, with quotient excess $p \cdot (1 + 2/(n+1)) > p$.

### Example I (§347, double root)

$x^3 - 3x^2 + 4 = 0$ has $2$ as a double root. Scale $3, 0, -4$, numerator $1$:

$$1,\ 3,\ 9,\ 23,\ 57,\ 135,\ 313,\ 711,\ 1593,\ \ldots$$

Ratios $1593/711 \approx 2.24$, always greater than $2$, converging slowly.

### Example II (§347, root much larger than the others)

$x^3 - x^2 - 5x - 3 = 0$ has largest root $3$, the others both $-1$ (a *non*-leading double root). Scale $1, 5, 3$:

$$1,\ 1,\ 6,\ 14,\ 47,\ 135,\ 412,\ 1228,\ \ldots$$

Ratios approach $3$ quickly because $|3|$ greatly exceeds $|-1|$, even though $-1$ is doubled: the doubling produces $(n+1)\cdot(-1)^n$ which still vanishes against $3^n$.

### Example III (§347, repeated root not dominant by much)

$x^3 + x^2 - 8x - 12 = 0$ has roots $3, -2, -2$. Scale $-1, 8, 12$:

$$1,\ -1,\ 9,\ -5,\ 65,\ 3,\ 457,\ 347,\ 3345,\ 4915,\ \ldots$$

Convergence to $3$ is sluggish: $|3|/|-2| = 1.5$ is small, *and* the $-2$ root is doubled with $(n+1)$ amplitude. Repeated near-dominant roots are the slow case of slow cases.

The general lesson: **equations with repeated roots are intrinsically harder for Bernoulli's method than those with all distinct roots.**

## Theoretical justification: geometric tail (§354)

Why does $(\heartsuit)$ hold? Take the tail of the recurrent series and suppose it is *exactly* a geometric progression with common ratio $x$. Write five consecutive terms $P, Q, R, S, T$ with $Q = xP$, $R = x^2P$, $S = x^3P$, $T = x^4P$. The recurrence $T = \alpha S + \beta R + \gamma Q + \delta P$ becomes, after dividing by $P$,

$$x^4 = \alpha x^3 + \beta x^2 + \gamma x + \delta,$$

i.e. $x$ is a root of the characteristic equation $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$. Conversely, if $x$ is *any* root, the pure geometric sequence $1, x, x^2, x^3, \ldots$ satisfies the recurrence. Bernoulli's method exploits the dominant root: for generic initial conditions, the recurrent-series tail is asymptotically geometric with common ratio $p$ (the dominant root), so $Q/P \to p$.

This identification is what lets the method work in reverse: **a recurrent series that *empirically* settles into a geometric progression reveals a root of the characteristic equation.**

## Application to transcendental equations (§355)

The procedure formally generalises to equations with infinitely many terms. The example: $\sin z = 1/2$ has smallest root $\pi/6$. From [[sine-and-cosine-series|the sine series]],

$$\frac{1}{2} = z - \frac{z^3}{6} + \frac{z^5}{120} - \frac{z^7}{5040} + \cdots,$$

or equivalently $0 = 1 - 2z + z^3/3 - z^5/60 + z^7/2520 - \cdots$. The "infinite scale" is $2, 0, -1/3, 0, 1/60, 0, -1/2520, 0, \ldots$. Initial terms chosen $1, 2$ and continuing by the recurrence:

$$1,\ 2,\ 4,\ 23/3,\ 44/3,\ 1681/60,\ 2408/45,\ \ldots$$

Ratio $\dfrac{1681/60}{2408/45} = \dfrac{1681\cdot 3}{2408\cdot 4} = \dfrac{5043}{9632} = 0.52356$, vs. true $\pi/6 = 0.523598$, error $3/100000$.

The method works for $\sin z = 1/2$ because *all* roots of this equation are real and the smallest in absolute value, $\pi/6$, is well-separated from the next-smallest. For most transcendental equations (oscillatory functions, infinitely many roots near zero, dominant complex pairs) this clean situation fails, so §355 closes with the caveat that the method is **seldom useful** for infinite equations.

## What about complex factors?

If the dominant pair of roots is complex conjugate (an irreducible [[trinomial-factor|trinomial factor]] $1 - 2pz\cos\phi + p^2 z^2$ in the denominator), the ratio $Q/P$ oscillates and Bernoulli's method as stated fails. Euler then derives a closed form for both modulus $p$ and argument $\phi$ from four consecutive terms — see [[trinomial-factor-from-recurrent-series]].

## Related pages

- [[trinomial-factor-from-recurrent-series]]
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]]
- [[recurrent-series]]
- [[scale-of-the-relation]]
- [[general-term-of-recurrent-series]]
- [[closed-form-two-term-recurrence]]
- [[real-partial-fraction-decomposition]]
- [[sine-and-cosine-series]]
- [[chapter-13-on-recurrent-series]]
