# Functions of Several Variables

**Summary**: Starting in §77, Euler introduces several *independent* variables and defines a function of them as any expression built from them. The algebraic/transcendental and single/multi-valued classifications from Chapter 1 carry over verbatim, and §82 gives his first statement of the equation-counting rule behind implicit functions.

**Sources**: chapter5

**Last updated**: 2026-04-23

---

## Independent variables

Through Chapter 4 every "variable" had been a function of one independent $z$. In §77 Euler changes the setting: quantities $x, y, z, \ldots$ vary independently. Fixing a value of one leaves the others "completely unrestricted" (source: chapter5, §77). A function of several variables is any expression composed from them — e.g. $x^3 + xyz + az^3$ is a function of $x, y, z$; it becomes a function of $x, y$ when $z$ is fixed, and a function of $x$ alone when $y$ and $z$ are both fixed (source: chapter5, §78).

The admissible values form what Euler calls an "infinity of infinite determinations" — a two-variable function admits infinitely many choices for each variable, so "infinitely many" per value of the other. A three-variable function has one more level of infinity, and so on.

## Classification carries over

- *Algebraic vs. transcendental* (§79): same split as in [[classification-of-functions]]. A transcendental operation in a multivariate function may involve all, some, or only one of the variables — e.g. $z^2 + y \log z$ is transcendental in $y, z$ jointly, but algebraic in $y$ once $z$ is fixed (source: chapter5, §79).
- *Irrational vs. non-irrational; polynomial vs. rational* (§80): a non-irrational function is free of radicals; if no variable appears in a denominator it is a polynomial, otherwise a rational function $P/Q$. The general polynomial in $y, z$ is $\alpha + \beta y + \gamma z + \delta y^2 + \epsilon y z + \zeta z^2 + \cdots$ (source: chapter5, §80).
- *Explicit vs. implicit irrational* (§80): an implicit irrational function is given by an unsolvable polynomial equation, e.g. $V^5 = (ayz + z^3) V^2 + (y^4 + z^4) V + y^5 + 2ayz^3 + z^5$.
- *Single- vs. multi-valued* (§81): as in [[single-valued-and-multi-valued-functions]], $V$ is $k$-valued if $V^k - PV^{k-1} + QV^{k-2} - \cdots = 0$ for single-valued $P, Q, \ldots$ Non-irrational functions are automatically single-valued (source: chapter5, §81).

## §82 — Implicit definition by equations

Setting a multivariate function equal to zero (or to a constant, or to another function) ties its variables together: each becomes a function of the rest. The general rule Euler states (source: chapter5, §82):

> *The number of equations determines the number of functions defined.*

Concretely:

- One equation in two variables $y, z$ makes $y$ a function of $z$ (and vice versa).
- One equation in three variables $x, y, z$ makes any one of them a function of the other two.
- Two equations in three variables make a *pair* of them functions of the third.
- In general, $k$ equations in $n$ variables leave $n - k$ degrees of freedom.

This is a very early — and still informal — statement of the [[implicit-function-and-equation-counting]] idea. Euler does not ask when the resulting function is single-valued, or when the implicit relation is solvable at all.

## Related pages

- [[classification-of-functions]]
- [[single-valued-and-multi-valued-functions]]
- [[implicit-function-and-equation-counting]]
- [[homogeneous-function]]
- [[chapter-5-on-functions-of-two-or-more-variables]]
