# Chapter 5: On Functions of Two or More Variables

**Summary**: Euler generalizes the single-variable framework of Chapters 1–4 to functions of several *independent* variables, carries the algebraic/transcendental classification over verbatim, and introduces the central new concept — *homogeneous functions* — together with the substitution $y = uz$ that reduces every bivariate homogeneous function of degree $n$ to $z^n \cdot f(u)$.

**Sources**: chapter5.pdf

**Last updated**: 2026-04-23

---

## Overview

Through Chapter 4 every "variable" had implicitly been a function of a single independent $z$. Chapter 5 (§77) declares the opposite setting: several quantities $x, y, z$ may vary independently, and an expression built from them is a function of several variables (source: chapter5.pdf, §77–§78). A function of $k$ variables admits an "infinity of infinite determinations" — one chooses one variable and still has a full $(k-1)$-dimensional freedom (source: chapter5.pdf, §78). See [[functions-of-several-variables]].

The old classification — algebraic vs. transcendental, with algebraic split into polynomial, rational, and irrational — transfers without change (§79–§80). Multi-valuedness is still defined by single-valued coefficients in a polynomial equation $V^k - PV^{k-1} + QV^{k-2} - \cdots = 0$ (§81). Setting a multivariate function equal to zero (or a constant, or another function) implicitly defines each variable as a function of the rest — Euler's first statement of the [[implicit-function-and-equation-counting]] idea and the "count equations, count dependent variables" heuristic (§82).

The substantive new material is the theory of [[homogeneous-function]]s (§83–§91), together with its counterparts for [[heterogeneous-function]]s (§92–§93) and the classification of polynomials by [[order-of-a-polynomial|order]] and *reducibility* (§94–§95). The key theorem, §88, shows that every homogeneous function of degree $n$ in two variables is $z^n f(y/z)$ — the theoretical foundation for the [[homogeneous-substitution]] trick Euler used empirically in Chapter 3.

See also: [[functions-of-several-variables]], [[implicit-function-and-equation-counting]], [[homogeneous-function]], [[heterogeneous-function]], [[order-of-a-polynomial]], [[reducible-polynomial]].

## Structure of the chapter

### §77–§78 — Independent variables and functions of several variables

Up to now every "variable" was secretly a function of one $z$ (source: chapter5.pdf, §77). Now $x, y, z, \ldots$ may take values independently: fixing $z$ leaves the rest "completely unrestricted." A function of several variables is *any* expression composed from them — e.g. $x^3 + xyz + az^3$ is a function of $x, y, z$; fix $z$ and it becomes a function of $x, y$; fix $z$ and $y$ and it becomes a function of $x$ (source: chapter5.pdf, §78). The admissible values of an $n$-variable function form an "infinity of infinite determinations" of multiplicity $n$.

### §79–§80 — Classification carries over

The algebraic/transcendental split is the same as in Chapter 1 (see [[classification-of-functions]]). A transcendental operation in a multivariate function may involve all, some, or only one of the variables — e.g. $z^2 + y \log z$ is transcendental in $y, z$ jointly, but becomes algebraic in $y$ once $z$ is fixed (source: chapter5.pdf, §79). Algebraic functions split into irrational and non-irrational; the latter into polynomials (no variable in a denominator) and rationals $P/Q$ (ratio of polynomials) (source: chapter5.pdf, §80). Irrational functions may be *explicit* (a radical sign) or *implicit* (given by an unsolvable polynomial equation), e.g. $V^5 = (ayz + z^3) V^2 + (y^4 + z^4) V + y^5 + 2ayz^3 + z^5$.

### §81 — Multi-valued functions

Multi-valuedness is defined exactly as in Chapter 1 (see [[single-valued-and-multi-valued-functions]]): $V$ is $k$-valued if $V^k - PV^{k-1} + QV^{k-2} - \cdots = 0$ with single-valued $P, Q, \ldots$ (source: chapter5.pdf, §81). Non-irrational functions are automatically single-valued.

### §82 — Implicit definition from equations

Setting a function of $y$ and $z$ equal to zero makes each of $y, z$ a function of the other — previously independent, now tied. The same works if the function equals a constant, or equals another function. Extending: one equation in three variables makes any one of them a function of the remaining two; two equations define *a pair* of variables as functions of the rest; *in general the number of equations determines the number of functions defined* (source: chapter5.pdf, §82). This is Euler's first statement of the [[implicit-function-and-equation-counting]] principle.

### §83 — Homogeneous vs. heterogeneous

A function is *homogeneous* if every term has the same total degree, *heterogeneous* if different degrees appear. Each variable counts for one degree; constants count for zero; products of $k$ variables (repeats allowed) count for degree $k$. So $\alpha y, \beta z$ have degree 1; $\alpha y^2, \beta yz, \gamma z^2$ have degree 2; and so on (source: chapter5.pdf, §83). See [[homogeneous-function]].

### §84–§85 — Polynomial and rational cases

Homogeneous polynomials of given degree have the obvious form: $\alpha y + \beta z$ (degree 1); $\alpha y^2 + \beta yz + \gamma z^2$ (degree 2); etc. A constant function counts as degree zero (source: chapter5.pdf, §84).

A rational function $P/Q$ is homogeneous if both $P$ and $Q$ are, with degree $\deg P - \deg Q$. Negative and zero degrees are admitted: $y/z^2$ has degree $-1$, $(y+z)/(y^4 + z^4)$ has degree $-3$, $1/(y^5 + ayz^4)$ has degree $-5$, and $(y^3 + z^3)/(y^2 z)$ has degree 0 (source: chapter5.pdf, §85).

### §86 — Irrational case

The degree extends to irrational functions by the rule: if $P$ is homogeneous of degree $n$, then $P^{\mu/\nu}$ is homogeneous of degree $(\mu/\nu) n$ (source: chapter5.pdf, §86). So $\sqrt{y^2 + z^2}$ has degree 1; $(y^9 + z^9)^{1/3}$ has degree 3; $(yz + z^2)^{1/2}$ has degree 1; $\left( (y^2 + z^2)/(y^4 + z^4) \right)^{1/1}$ has degree $-2$; and so forth. Sums and ratios of homogeneous pieces of matching degree are again homogeneous of that degree.

### §87 — Implicit irrational case

If $V$ satisfies $V^k + P V^{k-1} + Q V^{k-2} + \cdots + R = 0$ with $P, Q, \ldots, R$ polynomials in $y, z$, then $V$ is homogeneous (of some degree $n$) iff $P$ has degree $n$, $Q$ has degree $2n$, $R$ has degree $kn$, etc. — each coefficient matches the degree required for the whole equation to be homogeneous (source: chapter5.pdf, §87). Example: $V^5 + (y^4 + z^4) V^3 + a y^8 V - z^{10} = 0$ has $V$ homogeneous of degree 2.

### §88 — Euler's reduction $y = uz$

**Theorem.** If $V$ is homogeneous of degree $n$ in $y, z$, then under $y = uz$ one has

$$V(y, z) = z^n \cdot f(u), \qquad u = y/z.$$

*Proof sketch.* Every term of $V$ has total degree $n$ in $y, z$; replacing $y$ by $uz$ converts joint degree into degree in $z$ alone, so each term carries a factor $z^n$ (source: chapter5.pdf, §88). Euler checks all three cases:

- Polynomial: $V = \alpha y^3 + \beta y^2 z + \gamma y z^2 + \delta z^3 \Rightarrow V = z^3(\alpha u^3 + \beta u^2 + \gamma u + \delta)$.
- Rational: $V = (\alpha y + \beta z)/(y^2 + z^2) \Rightarrow V = z^{-1} (\alpha u + \beta)/(u^2 + 1)$.
- Irrational: $V = (y + \sqrt{y^2 + z^2})/(z\sqrt{y^3 + z^3}) \Rightarrow V = z^{-3/2}(u + \sqrt{u^2 + 1})/\sqrt{u^3 + 1}$.

This theorem is the theoretical backbone of the [[homogeneous-substitution]] trick from Chapter 3, §52–§58.

### §89 — Degree zero: a function of one variable

When $n = 0$, the factor $z^0 = 1$ drops out: *a homogeneous function of degree zero in $y, z$ is a function of $u = y/z$ alone* (source: chapter5.pdf, §89). Example: $(y + z)/(y - z) = (u + 1)/(u - 1)$; $(y - \sqrt{y^2 - z^2})/z = u - \sqrt{u^2 - 1}$.

### §90–§91 — Homogeneous bivariate polynomials factor linearly

A homogeneous polynomial of degree $n$ in $y, z$ factors as the product of $n$ linear pieces $\alpha y + \beta z$ (real or complex) (source: chapter5.pdf, §90–§91). *Proof.* After $y = uz$, the polynomial becomes $z^n$ times a polynomial in $u$ alone, which factors into linear pieces $\alpha u + \beta$; multiplying each by $z$ gives $\alpha y + \beta z$.

Thus every homogeneous polynomial of degree $n$ in two variables is [[reducible-polynomial|reducible]], a product of the right number of linear factors.

*This property fails in three or more variables.* The general homogeneous degree-2 form in three variables, $ay^2 + byz + cz^2 + dyx + ezx + fx^2$, does *not* generally factor as $(\alpha y + \beta z + \gamma x)(\delta y + \epsilon z + \zeta x)$ (source: chapter5.pdf, §91).

### §92 — Heterogeneous functions; bifid, trifid, ...

Heterogeneous functions are classified by how many distinct degrees occur among their terms. A *bifid* function has two: e.g. $y^5 + 2y^3 z^2 + y^2 + z^2$ splits as (degree-5 part) + (degree-2 part). A *trifid* has three: e.g. $y^6 + y^2 z^2 + z^4 + y - z$ has parts of degrees 6, 4, 1. Some rational or irrational functions cannot be cleanly split this way at all — e.g. $(y^3 + ayz)/(by + z^2)$ (source: chapter5.pdf, §92).

### §93 — Reducing heterogeneous to homogeneous by substitution

Sometimes a substitution makes a heterogeneous function homogeneous. Examples (source: chapter5.pdf, §93):

- $y^5 + z^2 y + y^3 z + z^3/y$ under $z = x^2$ becomes $y^5 + x^4 y + y^3 x^2 + x^6/y$ — homogeneous of degree 5 in $x, y$.
- $y + y^2 x + y^3 x^2 + y^5 x^4 + a/x$ under $z = 1/x$ becomes $y + y^2/z + y^3/z^2 + y^5/z^4 + az$ — homogeneous of degree 1.

No general criterion is given; Euler is content with examples.

### §94 — Order of a polynomial

The [[order-of-a-polynomial|order]] of a polynomial is the greatest degree of any single term. So $z^2 + y^2 + z^2 + ay - a^2$ is of order 2 (even though the constant term has degree 0), and $y^4 + yz^3 - ay^2 x + abyz - a^2 y^2 + b^4$ is of order 4 (source: chapter5.pdf, §94). Order is the classification relevant to the study of algebraic curves.

### §95 — Reducible and irreducible polynomials

A polynomial is *reducible* if it is a product of two or more non-irrational factors, *irreducible* otherwise. Example: $y^4 - z^4 + 2az^3 - 2byz^2 - a^2 z^2 + 2abzy - b^2 y^2 = (y^2 + z^2 - az + by)(y^2 - z^2 + az - by)$. By §91, every homogeneous bivariate polynomial is reducible. In contrast, $y^2 + z^2 - a^2$ is irreducible. Reducibility is decided by examining divisors (source: chapter5.pdf, §95). See [[reducible-polynomial]].

## Notable points

- §77 marks a conceptual shift. The single-variable setting of Chapters 1–4 was implicitly a *curve*: one parameter, one-dimensional image. Several variables means several degrees of freedom — surfaces and higher — and the rest of Book I and Book II will develop both the algebraic theory (here and in later chapters) and the geometric applications to curves and surfaces.
- §82 is the first place in the *Introductio* where Euler states, in passing, the equation-counting rule: $k$ equations in $n$ variables leave $n - k$ free. The notion of "implicit function" is still informal — there is no discussion of when the resulting map is well defined or single-valued.
- §88 is the payoff. The reason the [[homogeneous-substitution]] $y = xz$ in §52–§58 *worked* is that it produced $z^{m-n} = $ rational$(x)$ — exactly what §88 guarantees. Euler now has the theorem under his belt: in Chapter 3 he used it as a procedure; here he names it.
- §91's observation that bivariate homogeneous polynomials factor completely into linear factors, but trivariate ones do not, is an early piece of geometric intuition: a homogeneous polynomial in two variables cuts out a finite set of lines through the origin, while a homogeneous polynomial in three variables cuts out a projective curve, which need not split.
- §92–§93 are comparatively unsystematic — Euler records the classes without developing them further. The distinction will return when he studies algebraic curves by their equations of given order.

## Why this chapter matters

Chapter 5 is short but structurally pivotal. It sets up the multivariate framework every later chapter on curves and surfaces will assume, and it supplies the missing theorem — the $y = uz$ reduction for homogeneous functions — that retroactively justifies the parametrization tricks of Chapter 3. The classifications introduced here (homogeneous/heterogeneous, order, reducibility) become the working vocabulary for the algebraic theory of curves that occupies much of the remainder of Book I.

## Related pages

- [[functions-of-several-variables]]
- [[implicit-function-and-equation-counting]]
- [[homogeneous-function]]
- [[heterogeneous-function]]
- [[order-of-a-polynomial]]
- [[reducible-polynomial]]
- [[homogeneous-substitution]]
- [[classification-of-functions]]
- [[single-valued-and-multi-valued-functions]]
- [[chapter-3-on-the-transformation-of-functions-by-substitution]]
