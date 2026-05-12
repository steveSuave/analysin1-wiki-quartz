# Folium of Descartes

**Summary**: The cubic curve $y^3 + z^3 - c y z = 0$ admits the rational parametrization $z = \dfrac{cx}{1 + x^3}$, $y = \dfrac{c x^2}{1 + x^3}$, derived by Euler in §52 as an application of the $y = x^m z^n$ substitution.

**Sources**: chapter3.pdf

**Last updated**: 2026-04-23

---

## Setup

Euler writes the curve as

$$y^3 + z^3 - c y z = 0$$

and identifies it with his general §52 template $a y^\alpha + b z^\beta + c y^\gamma z^\delta = 0$ by setting

$$a = -1,\quad b = -1,\quad \alpha = 3,\quad \beta = 3,\quad \gamma = 1,\quad \delta = 1$$

(source: chapter3.pdf, §52 example).

## Parametrization by Method I

Method I of §52 chooses $n = \beta/\alpha = 1$, so $y = x^m z$. Taking $m = 1$:

$$y = x z.$$

Substituting into $y^3 + z^3 - cyz = 0$:

$$x^3 z^3 + z^3 - c x z^2 = 0 \iff z^2 (z (x^3 + 1) - cx) = 0,$$

giving $z = \dfrac{c x}{1 + x^3}$ and hence

$$\boxed{\; z = \frac{c x}{1 + x^3}, \qquad y = \frac{c x^2}{1 + x^3}. \;}$$

Both are rational functions of $x$ (source: chapter3.pdf, §52 example).

## The other two methods

Euler also records the two alternative choices of $n$ from §52:

- **Method II** ($n = (\beta - \delta)/\gamma = 2$) gives $z = \dfrac{1}{x}(cx - 1)^{1/3}$ and $y = \dfrac{1}{x}(cx - 1)^{2/3}$.
- **Method III** ($n = \delta/(\alpha - \gamma) = 1/2$, with $m = 1$ in the formula as shown) gives $z = (cx - x^3)^{2/3}$ and $y = x (cx - x^3)^{1/3}$.

Only Method I produces a rational parametrization; the others are "radical but single-valued in $x$" forms (source: chapter3.pdf, §52 example).

## Geometric interpretation

The folium of Descartes has a node at the origin. The substitution $y = xz$ is geometrically *projection from the node*: $x = y/z$ is the slope of the line through the origin, and each non-origin point of the curve lies on a unique such line. This is the same projection-from-a-special-point trick that produces the rational parametrization of the circle from the point $(-a, 0)$, but applied to a singular point rather than an ordinary one.

In modern language, the folium is a rational (genus-zero) cubic, and §52 Method I is explicitly its rational parametrization.

## Related pages

- [[homogeneous-substitution]]
- [[substitution]]
- [[chapter-3-on-the-transformation-of-functions-by-substitution]]
- [[rational-parametrization-of-the-circle]]
