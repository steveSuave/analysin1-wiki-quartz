# Homogeneous Substitution

**Summary**: When $y$ and $z$ are tied by an implicit polynomial equation in which all terms have restricted combinations of total degrees, the substitution $y = xz$ (or the more general $y = x^m z^n$) collapses the equation so that $z$ can be solved for in terms of the new variable $x$. This is Euler's §52–§58 technique.

**Sources**: chapter3.pdf

**Last updated**: 2026-04-23

---

## The trick

Given an implicit relation $F(y, z) = 0$ that cannot be solved explicitly for $y$ or $z$, introduce $x$ by

$$y = x z \qquad \text{(or more generally}\quad y = x^m z^n\text{).}$$

Substituting into $F$ often produces an equation whose powers of $z$ can be factored out, leaving a single power of $z$ equal to a rational function of $x$. That in turn gives $z$ as a root of a rational expression in $x$, and then $y = xz$ follows.

The technique presupposes that the implicit relation has enough "homogeneity" — either literal (all terms of the same total degree in $y, z$) or arithmetic structure across the set of monomials that appear.

## §52 — Three-term equation with one mixed monomial

For equations of the form

$$a y^\alpha + b z^\beta + c y^\gamma z^\delta = 0,$$

Euler substitutes $y = x^m z^n$ to get

$$a x^{\alpha m} z^{\alpha n} + b z^\beta + c x^{\gamma m} z^{\gamma n + \delta} = 0.$$

He then chooses $n$ to make two of the three exponents of $z$ equal, so they can be collected and the common power of $z$ factored out. Three choices of $n$ are available (source: chapter3.pdf, §52):

- **I.** $\alpha n = \beta$, giving $n = \beta/\alpha$.
- **II.** $\beta = \gamma n + \delta$, giving $n = (\beta - \delta)/\gamma$.
- **III.** $\alpha n = \gamma n + \delta$, giving $n = \delta/(\alpha - \gamma)$.

Each choice expresses $z$ and $y$ as rational powers of rational functions of $x$. Any integer choice of $m$ gives the most convenient form of the formula. The classic example is the [[folium-of-descartes]].

## §53 — A posteriori construction

Given a rational parametrization $z = \left(\frac{ax^\alpha + bx^\beta + \cdots}{A + Bx^\mu + \cdots}\right)^{p/r}$ and $y = x z^{q/p}$, one can reverse-engineer the implicit relation $F(y, z) = 0$ it parametrizes. Euler uses $y^p = x^p z^q$, so $x = y z^{-q/p}$, and substitutes back (source: chapter3.pdf, §53). The construction is the inverse of §52.

## §54–§57 — Exactly two total degrees

If the monomials of $F(y, z)$ come in exactly two total degrees $m$ and $n$ (with $m > n$), let $y = xz$. The equation becomes

$$(\text{polynomial in } x) \cdot z^m + (\text{polynomial in } x) \cdot z^n = 0,$$

or, after dividing by $z^n$,

$$z^{m - n} = \frac{\text{polynomial in } x}{\text{polynomial in } x}.$$

So $z$ is an $(m-n)$-th root of a rational function of $x$.

Explicit cases Euler works out:

- **§54.** $a y^2 + b y z + c z^2 + d y + e z = 0$. Degrees $2$ and $1$. Gives $z = -\frac{dx + e}{ax^2 + bx + c}$ and $y = -\frac{(dx + e) x}{ax^2 + bx + c}$ — both rational in $x$ (source: chapter3.pdf, §54).
- **§55.** $ay^3 + by^2 z + cyz^2 + dz^3 + ey^2 + fyz + gz^2 = 0$. Degrees $3$ and $2$. Gives $z = -\frac{ex^2 + fx + g}{ax^3 + bx^2 + cx + d}$, and $y = xz$ (source: chapter3.pdf, §55).
- **§56.** $ay^2 + byz + cz^2 = d$. Degrees $2$ and $0$. Gives $z = \sqrt{d / (a x^2 + bx + c)}$, $y = x \sqrt{d / (ax^2 + bx + c)}$ (source: chapter3.pdf, §56).
- **§57.** General case, degrees $m$ and $n$: $z = \left(\dfrac{\alpha x^n + \beta x^{n-1} + \cdots}{a x^m + b x^{m-1} + \cdots}\right)^{1/(m - n)}$ (source: chapter3.pdf, §57).

## §58 — Three total degrees in arithmetic progression

If the monomials of $F$ have exactly three total degrees $m_1 < m_2 < m_3$ with $m_3 - m_2 = m_2 - m_1$, let $y = xz$ and divide by $z^{m_1}$. The equation becomes a *quadratic* in $z^{m_2 - m_1}$, solvable by the quadratic formula (source: chapter3.pdf, §58).

Example: $a y^3 + b y^2 z + c y z^2 + d z^3 = 2 e y^2 + 2 f y z + 2 g z^2 + h y + j z$ has total degrees $3, 2, 1$. After $y = xz$ and dividing by $z$,

$$(a x^3 + b x^2 + c x + d)\, z^2 = 2(e x^2 + f x + g)\, z + (h x + j),$$

and the quadratic formula gives $z$.

## Why this matters

These are the first systematic algebraic parametrizations in Euler's treatise. They anticipate the modern observation that a plane algebraic curve of genus zero admits a rational parametrization, and that a genus-zero curve with two "singular" behaviours at infinity (e.g. a nodal cubic like the [[folium-of-descartes]]) can be parametrized by projecting from the singular point — which is exactly what $y = xz$ does when the equation is homogeneous enough.

## Theoretical justification (Chapter 5, §88)

In Chapter 3 Euler uses $y = xz$ as a procedure that "happens to work" when the equation is homogeneous enough. The theorem that justifies it appears only in Chapter 5, §88 (see [[homogeneous-function]]):

> *If $V(y, z)$ is homogeneous of degree $n$, then under $y = uz$ we have $V = z^n \cdot f(u)$, where $u = y/z$.*

This is why the §54–§57 cases all reduce cleanly to "$z^{m-n} = $ rational function of $x$": the left-hand side of $F(y, z) = 0$ splits into homogeneous pieces of degrees $m$ and $n$, each piece becomes $z^{\deg} \cdot (\text{poly in } x)$ under $y = xz$, and equating gives an equation in $z$ whose powers are $m$ and $n$ alone — so $z^{m-n}$ is determined by a rational function of $x$.

The degree-zero case §89 (where $V$ becomes a function of $u$ alone, with the $z$-factor disappearing) corresponds to §56's totally homogeneous equation $ay^2 + byz + cz^2 = d$, where the ratio $y/z$ is not enough to pin down $z$ and an extra radical survives.

## Related pages

- [[substitution]]
- [[chapter-3-on-the-transformation-of-functions-by-substitution]]
- [[folium-of-descartes]]
- [[rationalizing-substitutions]]
- [[rational-parametrization-of-the-circle]]
- [[homogeneous-function]]
- [[chapter-5-on-functions-of-two-or-more-variables]]
