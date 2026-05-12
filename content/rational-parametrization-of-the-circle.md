# Rational Parametrization of the Circle

**Summary**: The identity

$$z = \frac{a(1 - x^2)}{1 + x^2}, \qquad y = \frac{2ax}{1 + x^2}$$

parametrizes the circle $y^2 + z^2 = a^2$ by rational functions of $x$. Euler derives it in §46 (with $a = 1$) and again as a special case of the §50 substitution.

**Sources**: chapter3.pdf

**Last updated**: 2026-04-23

---

## Statement

For all real $x$,

$$\left(\frac{a(1 - x^2)}{1 + x^2}\right)^2 + \left(\frac{2ax}{1 + x^2}\right)^2 = a^2,$$

so the map $x \mapsto (z, y)$ traces points on the circle of radius $a$. Every point except $(-a, 0)$ is hit exactly once as $x$ ranges over $\mathbb{R}$.

## Derivation from §46

Euler opens Chapter 3 with the example $y = \frac{1 - z^2}{1 + z^2}$. Substituting $z = \frac{1 - x}{1 + x}$ gives $y = \frac{2x}{1 + x^2}$ (source: chapter3.pdf, §46). This is the parametrization with $a = 1$, in the "$z$-as-function-of-$x$" form.

## Derivation from §50

In §50 Euler handles $y = \sqrt{(a + bz)(c + dz)}$ by letting $\sqrt{(a+bz)(c+dz)} = (a + bz)x$. For $y = \sqrt{a^2 - z^2} = \sqrt{(a + z)(a - z)}$ — so $b = 1$, $c = a$, $d = -1$ — the general formula

$$z = \frac{c - a x^2}{b x^2 - d}, \qquad y = \frac{(bc - ad)x}{b x^2 - d}$$

specializes to

$$z = \frac{a - a x^2}{x^2 + 1} = \frac{a(1 - x^2)}{1 + x^2}, \qquad y = \frac{2ax}{1 + x^2}$$

(source: chapter3.pdf, §50). This is exactly the classical half-angle parametrization: with $x = \tan(\theta/2)$, one recovers $z = a\cos\theta$, $y = a\sin\theta$.

## Geometric meaning

The substitution $\sqrt{(a+z)(a-z)} = (a+z)x$ is the projection from the point $(-a, 0)$: it parametrizes the circle by the slope $x$ of the line through that point. The excluded value corresponds to the point at infinity in the direction of the line — equivalently, to $(-a, 0)$ itself.

## Significance

- First rational parametrization explicitly written down in the *Introductio* and used repeatedly in later chapters.
- A template for Euler's general strategy: remove a radical by exploiting one "obvious" point (or factor) and projecting from it.
- Modern reading: every smooth conic is rationally parametrizable because it has genus zero; the circle is the canonical example.

## Related pages

- [[substitution]]
- [[rationalizing-substitutions]]
- [[chapter-3-on-the-transformation-of-functions-by-substitution]]
- [[folium-of-descartes]] — another famous rational parametrization, from §52.
