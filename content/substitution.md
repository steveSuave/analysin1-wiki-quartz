# Substitution

**Summary**: Euler's second transformation technique: rather than rewrite $y = f(z)$ with the same variables, introduce a new variable $x$ such that both $y$ and $z$ become functions of $x$. Used to remove radicals and to make implicit relations explicit.

**Sources**: chapter3.pdf

**Last updated**: 2026-04-23

---

## The idea

Chapter 2 transforms a function by rewriting it with the same variable $z$. Chapter 3 transforms differently: *introduce a third variable* $x$ such that both the independent variable $z$ and the dependent variable $y$ are defined as functions of $x$ (source: chapter3.pdf, §46).

Setting any value of $x$ then simultaneously determines values of $z$ and $y$ that satisfy the original relation. The resulting pair $(z(x), y(x))$ is what we would today call a *parametrization*.

Euler's opening example: given $y = \dfrac{1 - z^2}{1 + z^2}$, let $z = \dfrac{1 - x}{1 + x}$. Substituting yields $y = \dfrac{2x}{1 + x^2}$. At $x = \tfrac{1}{2}$: $z = \tfrac{1}{3}$ and $y = \tfrac{4}{5}$, consistent with $y = (1 - z^2)/(1 + z^2)$ at $z = \tfrac{1}{3}$ (source: chapter3.pdf, §46).

## Why substitute

Euler gives two motivations (source: chapter3.pdf, §46):

1. **Remove radicals**. If $y$ as a function of $z$ contains a radical, a well-chosen substitution can express both $z$ and $y$ as rational functions of $x$. See [[rationalizing-substitutions]].
2. **Handle implicit relations**. If $y$ and $z$ are tied by an implicit equation of higher degree, so that neither can be solved for explicitly in terms of the other, a substitution may yield explicit formulas for both in terms of $x$. See [[homogeneous-substitution]].

Both motivations point to what modern language calls a *rational parametrization* of an algebraic curve.

## Position in the chapter

- §46 — motivation and the opening example.
- §47–§51 — removing radicals (see [[rationalizing-substitutions]]).
- §52–§58 — implicit relations, using $y = xz$ or $y = x^m z^n$ (see [[homogeneous-substitution]]).

## Related pages

- [[chapter-3-on-the-transformation-of-functions-by-substitution]]
- [[rationalizing-substitutions]]
- [[homogeneous-substitution]]
- [[rational-parametrization-of-the-circle]]
- [[folium-of-descartes]]
- [[chapter-2-on-the-transformation-of-functions]] — the first kind of transformation.
