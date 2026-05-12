# Chapter 3: On the Transformation of Functions by Substitution

**Summary**: Euler introduces the second kind of transformation promised in Chapter 2: replacing the variable $z$ with a new variable $x$ in terms of which both $z$ and $y$ are defined. Two applications dominate the chapter — removing radicals, and making implicit algebraic relations explicit.

**Sources**: chapter3.pdf

**Last updated**: 2026-04-23

---

## Overview

Where Chapter 2 kept the same variable and rewrote the function, Chapter 3 introduces a fresh variable $x$ and simultaneously defines both $y$ and $z$ as functions of it (source: chapter3.pdf, §46). In modern terms, Euler is constructing rational — or at least radical-free — *parametrizations* of algebraic relations.

The chapter organizes around two large themes:

1. **Removing radicals** (§47–§51). See [[rationalizing-substitutions]].
2. **Parametrizing implicit polynomial relations** (§52–§58). See [[homogeneous-substitution]].

The generic tool used in (1) is a tailored substitution that exploits the form of the radical; in (2) it is the homogeneous ansatz $y = x z$ (or the more general $y = x^m z^n$).

## Structure of the chapter

### §46 — What substitution means

If $y$ is a function of $z$, we may introduce a new variable $x$ by specifying $z = g(x)$; both $y$ and $z$ then become functions of $x$. The method is justified either because it removes a radical from $y(z)$ or because it makes an implicit higher-degree relationship between $y$ and $z$ explicitly solvable (source: chapter3.pdf, §46). The opening example $y = (1 - z^2)/(1 + z^2)$ with $z = (1 - x)/(1 + x)$ is the [[rational-parametrization-of-the-circle]] (with $a = 1$).

See [[substitution]].

### §47–§51 — Removing radicals

A catalog of substitutions keyed to the form of the radical:

- §47: $y = \sqrt{a + bz}$ — set $y = bx$.
- §48: $y = (a + bz)^{m/n}$ — set $y = x^m$.
- §49: $y = \left(\frac{a + bz}{f + gz}\right)^{m/n}$ — set $y = x^m$.
- §50: $y = \sqrt{(a + bz)(c + dz)}$ — set the radical equal to $(a + bz) x$. Special case $y = \sqrt{a^2 - z^2}$ is the circle (source: chapter3.pdf, §47–§50).
- §51: $y = \sqrt{p + qz + r z^2}$ — cases I, II, III on the signs of $p$ and $r$; case III reduces to §50 when the quadratic has real factors, or is otherwise handled by a variant ansatz (source: chapter3.pdf, §51).

Euler acknowledges that other forms of radical relation exist and "cannot be reduced to a form without radicals by a substitution without radicals" (source: chapter3.pdf, §51). See [[rationalizing-substitutions]].

### §52 — Three-term relations

$$a y^\alpha + b z^\beta + c y^\gamma z^\delta = 0.$$

Substituting $y = x^m z^n$ gives three ways to choose $n$ so two exponents of $z$ match and the common factor of $z$ can be stripped. The worked example is $y^3 + z^3 - cyz = 0$, the [[folium-of-descartes]], whose Method-I form gives the classical rational parametrization $z = cx/(1+x^3)$, $y = cx^2/(1+x^3)$ (source: chapter3.pdf, §52).

### §53 — A posteriori construction

Given a rational parametrization $z(x), y(x)$ one can run §52 backwards and reconstruct an implicit polynomial relation $F(y, z) = 0$ (source: chapter3.pdf, §53).

### §54–§57 — Exactly two total degrees

When the monomials of the implicit relation involve exactly two total degrees $m > n$, $y = xz$ followed by division by $z^n$ leaves a single power $z^{m-n}$ equal to a rational function of $x$. Particular cases worked out:

- §54: $ay^2 + byz + cz^2 + dy + ez = 0$ (degrees 2 and 1).
- §55: degrees 3 and 2.
- §56: degrees 2 and 0 (i.e. $ay^2 + byz + cz^2 = d$).
- §57: general degrees $m, n$.

All reduce to $z = \left(\text{rational in } x\right)^{1/(m-n)}$, $y = xz$ (source: chapter3.pdf, §54–§57).

### §58 — Three total degrees in arithmetic progression

If the implicit relation involves exactly three total degrees forming an arithmetic progression, $y = xz$ produces an equation *quadratic* in a power of $z$, solvable via the quadratic formula. Euler gives three examples — a cubic-quadratic-linear relation, a sextic with degrees $5, 3, 1$, and a relation with degrees $10, 7, 4$ (source: chapter3.pdf, §58 examples I–III).

See [[homogeneous-substitution]].

## Notable points

- The chapter is remarkable for quietly discovering, case by case, that certain algebraic curves admit rational parametrizations. Modern language: these are precisely the genus-zero cases. Euler does not yet have the language, but the phenomenon is correctly identified.
- §46 and §50 together recover the classical half-angle parametrization of the circle.
- The §52 Method-I formula applied to $y^3 + z^3 = cyz$ gives the standard parametrization of the folium of Descartes.
- The §58 trick — reduce three AP-spaced degrees to a quadratic in $z^k$ — is an early instance of what would later be called "weighted homogeneity."
- At the end of §51 Euler explicitly admits the limits of algebraic substitution: "other cases, which are not discussed in this treatise, cannot be reduced to a form without radicals by a substitution without radicals" (source: chapter3.pdf, §51). This is a frank recognition that not every algebraic relation is rational.

## Why this chapter matters

Together with Chapter 2, this chapter completes Euler's algebraic toolkit for simplifying functions. Chapter 2 rewrote; Chapter 3 *reparametrizes*. Both are set-up: once an expression has been broken into simple pieces and/or written rationally in a convenient variable, later chapters can integrate, sum, and expand it as a series.

## Related pages

- [[substitution]]
- [[rationalizing-substitutions]]
- [[homogeneous-substitution]]
- [[rational-parametrization-of-the-circle]]
- [[folium-of-descartes]]
- [[chapter-2-on-the-transformation-of-functions]]
