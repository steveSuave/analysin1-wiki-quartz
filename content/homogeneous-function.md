# Homogeneous Function

**Summary**: A function of $y, z$ is *homogeneous of degree $n$* if every term has the same total degree $n$. This extends cleanly to rational ($\deg P - \deg Q$), irrational ($P^{\mu/\nu}$ has degree $(\mu/\nu) n$), and implicit algebraic cases. Euler's central theorem (§88): under $y = uz$, any bivariate homogeneous function of degree $n$ becomes $z^n \cdot f(u)$; degree zero means $V$ is a function of $u = y/z$ alone. Every bivariate homogeneous polynomial factors into linear pieces $\alpha y + \beta z$, a property that fails in three or more variables.

**Sources**: chapter5

**Last updated**: 2026-04-23

---

## Degree

A variable has degree 1; a constant has degree 0; the degree of a product is the sum of degrees. So $\alpha y, \beta z$ are degree 1; $\alpha y^2, \beta y z, \gamma z^2$ are degree 2; and so on (source: chapter5, §83).

A *homogeneous* function is one in which every term has the same degree. A *heterogeneous* function is one with at least two different degrees among its terms — see [[heterogeneous-function]].

## Polynomial case (§84)

Homogeneous polynomials in $y, z$ of each degree have the obvious general form:

$$
\begin{aligned}
\text{degree } 1: & \quad \alpha y + \beta z \\
\text{degree } 2: & \quad \alpha y^2 + \beta yz + \gamma z^2 \\
\text{degree } 3: & \quad \alpha y^3 + \beta y^2 z + \gamma y z^2 + \delta z^3 \\
\text{degree } 4: & \quad \alpha y^4 + \beta y^3 z + \gamma y^2 z^2 + \delta y z^3 + \epsilon z^4
\end{aligned}
$$

Constant functions count as degree zero (source: chapter5, §84).

## Rational case (§85)

A rational function $P/Q$ is homogeneous iff both $P$ and $Q$ are homogeneous, and its degree is $\deg P - \deg Q$. Negative and zero degrees are admitted (source: chapter5, §85):

| function | degree |
| --- | --- |
| $(ay^2 + bz^2)/(\alpha y + \beta z)$ | 1 |
| $(y^5 + z^5)/(y^2 + z^2)$ | 3 |
| $(y^3 + z^3)/(y^2 z)$ | 0 |
| $y/z^2$ | $-1$ |
| $(y+z)/(y^4 + z^4)$ | $-3$ |
| $1/(y^5 + ayz^4)$ | $-5$ |

Sums of homogeneous pieces of matching degree are again homogeneous of that degree: $\alpha y + \beta z^2 / y + (\gamma y^4 - \delta z^4)/(y^2 z + y z^2)$ has degree 1 throughout.

## Irrational case (§86)

If $P$ is homogeneous of degree $n$, then $P^{\mu/\nu}$ is homogeneous of degree $(\mu/\nu) n$ (source: chapter5, §86). Examples:

- $\sqrt{y^2 + z^2}$ has degree 1.
- $(y^9 + z^9)^{1/3}$ has degree 3.
- $(yz + z^2)^{1/2}$ has degree 1.
- $\sqrt{y^2 + z^2}/\sqrt{y^4 + z^4}$ has degree 0.

Euler's sample worked expression

$$\frac{1}{y} + \frac{y \sqrt{y^2 + z^2}}{z^3} - \frac{y}{(y^6 - z^6)^{1/3}} + \frac{y \sqrt{z}}{z^2 \sqrt{y} + \sqrt{y^6 + z^6}}$$

is homogeneous of degree $-1$: each of the four summands evaluates to degree $-1$ under the rules.

## Implicit case (§87)

If $V$ satisfies the polynomial equation

$$V^k + P V^{k-1} + Q V^{k-2} + \cdots + R = 0$$

with $P, Q, \ldots, R$ polynomials in $y, z$, then $V$ is homogeneous of degree $n$ iff

$$\deg P = n, \quad \deg Q = 2n, \quad \ldots, \quad \deg R = kn$$

— i.e. each coefficient carries exactly the degree needed so every term of the equation is of total degree $kn$ (source: chapter5, §87). Example: $V^5 + (y^4 + z^4) V^3 + a y^8 V - z^{10} = 0$ has $V$ homogeneous of degree 2.

## §88 — Euler's reduction theorem

**Theorem.** If $V(y, z)$ is homogeneous of degree $n$, then under $y = uz$,

$$\boxed{\ V(y, z) = z^n \cdot f(u), \qquad u = y/z.\ }$$

*Argument.* Every term of $V$ has joint degree $n$ in $y, z$. Replacing $y$ by $uz$ converts joint degree into degree in $z$ alone, so each term acquires the factor $z^n$, leaving a function of $u$ (source: chapter5, §88).

Euler checks the three cases:

- **Polynomial.** $V = \alpha y^3 + \beta y^2 z + \gamma y z^2 + \delta z^3 \ \Rightarrow\ V = z^3(\alpha u^3 + \beta u^2 + \gamma u + \delta)$.
- **Rational.** $V = \dfrac{\alpha y + \beta z}{y^2 + z^2}$ (degree $-1$) $\ \Rightarrow\ V = z^{-1} \dfrac{\alpha u + \beta}{u^2 + 1}$.
- **Irrational.** $V = \dfrac{y + \sqrt{y^2 + z^2}}{z \sqrt{y^3 + z^3}}$ (degree $-3/2$) $\ \Rightarrow\ V = z^{-3/2} \dfrac{u + \sqrt{u^2 + 1}}{\sqrt{u^3 + 1}}$.

This theorem is the theoretical foundation for the parametrization trick Euler used empirically in Chapter 3 — see [[homogeneous-substitution]].

## §89 — Degree zero

If $n = 0$, the factor $z^n = 1$ vanishes from the expression, so

$$V \text{ homogeneous of degree } 0 \ \Longrightarrow\ V \text{ is a function of } u = y/z \text{ alone}$$

(source: chapter5, §89). Examples:

- $(y + z)/(y - z) = (u + 1)/(u - 1)$.
- $(y - \sqrt{y^2 - z^2})/z = u - \sqrt{u^2 - 1}$.

## §90–§91 — Linear factorization in two variables

**Theorem.** A homogeneous polynomial of degree $n$ in $y, z$ factors as a product of $n$ linear pieces $\alpha y + \beta z$ (with real or complex coefficients) (source: chapter5, §90–§91).

*Proof.* By §88, the polynomial becomes $z^n \cdot p(u)$ after $y = uz$. By the [[fundamental-theorem-of-algebra]], $p(u)$ factors into linear pieces $\alpha u + \beta$; multiplying each by $z$ recovers $\alpha y + \beta z$, giving $n$ factors in the original variables.

Corollaries:

- $ay^2 + byz + cz^2$ has two linear factors.
- $ay^3 + by^2 z + cy z^2 + dz^3$ has three.
- Every homogeneous bivariate polynomial is [[reducible-polynomial|reducible]].

**This fails in three or more variables.** The general degree-2 homogeneous form $ay^2 + byz + cz^2 + dyx + ezx + fx^2$ does not generally split as $(\alpha y + \beta z + \gamma x)(\delta y + \epsilon z + \zeta x)$, and the situation is worse for higher degree (source: chapter5, §91).

## Why this matters

The $y = uz$ reduction is Euler's first structure theorem for multivariate functions. It separates scale (the $z^n$ factor) from shape (the profile $f(u)$), and it reduces the study of homogeneous bivariate functions to single-variable analysis. Geometrically it corresponds to projecting the locus $V = 0$ from the origin — every line through the origin intersects the curve in a finite set, parametrized by the ratio $u = y/z$. This is the algebraic shadow of projective geometry, and it is the reason the substitution trick of Chapter 3 works for curves like the [[folium-of-descartes]].

In modern language, §88 says a homogeneous function on $\mathbb{R}^2 \setminus \{0\}$ of degree $n$ is determined by its restriction to the line $\{z = 1\}$ (i.e. by the profile $f(u) = V(u, 1)$) together with its degree. The degree-zero case §89 is the same as saying degree-zero functions descend to functions on the projective line $\mathbb{P}^1$.

## Related pages

- [[functions-of-several-variables]]
- [[heterogeneous-function]]
- [[homogeneous-substitution]]
- [[reducible-polynomial]]
- [[fundamental-theorem-of-algebra]]
- [[folium-of-descartes]]
- [[chapter-5-on-functions-of-two-or-more-variables]]
