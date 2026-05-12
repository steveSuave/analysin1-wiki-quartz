# Chapter 2: On the Transformation of Functions

**Summary**: Euler explains what it means to transform a function without changing its value, then develops two central techniques: factoring polynomials into real linear and quadratic factors, and decomposing rational functions into partial fractions.

**Sources**: chapter2

**Last updated**: 2026-04-23

---

## Overview

A function is *transformed* either by changing its form while keeping the same variable, or by introducing a new variable through a substitution. This chapter is about the first kind; the second kind is deferred to Chapter 3 (source: chapter2, §27).

The two large topics are:

1. **Factoring polynomial functions** into linear and quadratic factors (§28–§37). See [[factoring-polynomials]], [[complex-conjugate-factors]], [[fundamental-theorem-of-algebra]], [[intermediate-value-property]], and [[real-roots-by-degree-parity]].
2. **Decomposing rational functions** into partial fractions (§38–§46). See [[improper-rational-function]] and [[partial-fraction-decomposition]].

## Structure of the chapter

### §27 — What "transformation" means

A function's form can change in two ways: by rewriting with the same variable (e.g. $2 - 3z + z^2 = (1 - z)(2 - z)$, or $\sqrt{1 + z^2} + z = \tfrac{1}{\sqrt{1 + z^2} - z}$), or by substitution (e.g. letting $y = a - z$ turns $a^4 - 4a^3 z + 6a^2 z^2 - 4a z^3 + z^4$ into $y^4$). Substitution is postponed to Chapter 3 (source: chapter2, §27).

### §28–§32 — Factoring polynomials

Euler develops the theory of factoring a polynomial $Z$ into linear factors coming from its roots:

- A polynomial of degree $n$ has $n$ linear factors, and if the roots are $f, g, h, \ldots$ with leading coefficient $A$, then $Z = A(z - f)(z - g)(z - h) \cdots$ or equivalently $Z = A(1 - z/f)(1 - z/g)\cdots$ (source: chapter2, §28–§29).
- Complex linear factors come in pairs; their product is real (§30).
- Any real product of four complex linear factors splits into two real quadratic factors (§31). See [[complex-conjugate-factors]].
- Every polynomial of $z$ can be expressed as a product of real linear and real quadratic factors. Euler concedes the claim "has not been proved with complete rigor" but announces it will be corroborated later (§32). This is essentially the [[fundamental-theorem-of-algebra]] stated over $\mathbb{R}$.

### §33 — Intermediate value property

If $Z$ takes the value $A$ at $z = a$ and $B$ at $z = b$, then for any $C$ between $A$ and $B$ there is a $z$ between $a$ and $b$ with $Z = C$. Euler justifies this by saying a (single-valued) function "cannot pass from $A$ to $B$ without taking on all of the intermediate values" (source: chapter2, §33). See [[intermediate-value-property]].

### §34–§37 — Real roots from degree parity and sign

A series of corollaries of the intermediate value property:

- An odd-degree polynomial has at least one real linear factor, and in fact an odd number of them (§34–§35).
- An even-degree polynomial has an even number of real linear factors (§36).
- An even-degree polynomial whose constant term is negative has at least two real roots, one positive and one negative (§37).

See [[real-roots-by-degree-parity]].

### §38 — Improper rational functions

If the numerator's degree is greater than or equal to the denominator's, polynomial division splits the function into a polynomial part plus a *proper* rational remainder. Example: $\tfrac{1 + z^4}{1 + z^2} = z^2 - 1 + \tfrac{2}{1 + z^2}$ (source: chapter2, §38). See [[improper-rational-function]].

### §39–§46 — Partial fractions

The computational heart of the chapter. A proper rational function $M/N$ whose denominator has distinct linear factors $p - qz$ decomposes as a sum of simple fractions $A/(p - qz)$, one per factor. Euler gives the shortcut $A = M/S$ evaluated at $z = p/q$, where $N = (p - qz) S$ (§41). Repeated linear factors $(p - qz)^n$ generate a tower of partial fractions $A/(p-qz)^n + B/(p-qz)^{n-1} + \cdots + K/(p-qz)$, computed by an iterative algorithm (§42–§45). Section §46 assembles everything into a general procedure and a full worked example. See [[partial-fraction-decomposition]].

## Notable points

- Euler explicitly allows an equation like $Z = z^{2n+1} + \cdots$ to have "$z = \infty$" as a root of $Z - \infty = 0$, and uses this as the limiting input to the intermediate value property to argue that odd-degree polynomials have real roots (source: chapter2, §34). The reasoning is informal by modern standards but prefigures the modern argument.
- The §32 factorization theorem is stated without a rigorous proof. Euler justifies believing it by pointing ahead to later chapters where polynomials of the forms $a + b z^n$, $a + b z^n + c z^{2n}$, etc. will be explicitly resolved into real quadratic factors (source: chapter2, §32).
- The partial-fractions algorithm is stated in a form that computes each numerator by substituting the root of the corresponding factor into a ratio of the remaining pieces — essentially the modern "cover-up method" and its generalization for repeated roots.

## Why this chapter matters

This chapter is Euler's toolkit for turning a polynomial or rational function into a sum of maximally simple pieces — linear and quadratic factors, or simple partial fractions. These decompositions are what make the later *Introductio* chapters on series, logarithms, and trigonometric functions work: integrating or summing a complicated rational function is reduced, via partial fractions, to integrating or summing a few simple fragments.

It is also where Euler first states, even if without rigor, that every real polynomial factors over the reals into linear and quadratic pieces — a cornerstone of 18th-century analysis.

## Related pages

- [[factoring-polynomials]]
- [[fundamental-theorem-of-algebra]]
- [[complex-conjugate-factors]]
- [[intermediate-value-property]]
- [[real-roots-by-degree-parity]]
- [[improper-rational-function]]
- [[partial-fraction-decomposition]]
- [[chapter-1-on-functions-in-general]]
