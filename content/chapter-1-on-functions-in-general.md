# Chapter 1: On Functions in General

**Summary**: Euler's opening chapter of the *Introductio* lays the foundation for the entire work by defining constants, variables, and functions, and classifying functions by their method of construction.

**Sources**: chapter1

**Last updated**: 2026-04-23

---

## Overview

This chapter defines the basic vocabulary of analysis as Euler conceives it. He begins from the distinction between [[variable-and-constant]] quantities, gives his famous definition of a [[function]] as an "analytic expression," and then builds a taxonomy that organizes functions by the operations used to construct them. He ends with three structural topics: [[single-valued-and-multi-valued-functions]], [[even-and-odd-functions]], and [[similar-functions]].

## Structure of the chapter

Paragraphs 1-3 establish notation and the concept of a variable quantity, which "encompasses within itself absolutely all numbers, both positive and negative, integers and rationals, irrationals and transcendentals" — and even zero and complex numbers (source: chapter1, §3).

Paragraph 4 gives the pivotal definition: a function of a variable is an analytic expression composed from the variable, numbers, and constants. See [[function]].

Paragraphs 6-9 develop the [[classification-of-functions]]:

- algebraic vs. transcendental (§7),
- algebraic split into non-irrational vs. irrational, with irrational further split into explicit and implicit (§8),
- non-irrational split into polynomial and rational (§9).

Paragraphs 10-15 treat [[single-valued-and-multi-valued-functions]], introducing $n$-valued functions defined by degree-$n$ polynomial equations with single-valued coefficients, together with the Vieta-style relations between the values and the coefficients.

Paragraphs 16-17 note the reciprocity of functional relations: if $y$ is a function of $z$, then $z$ is a function of $y$; and if $y$ and $x$ are both functions of $z$, each is a function of the other.

Paragraphs 18-25 develop [[even-and-odd-functions]], including the multiplicative rules (even $\times$ odd = odd, odd $\times$ odd = even, etc.).

Paragraph 26 closes with [[similar-functions]]: $Y$ and $Z$ are similar functions of $y$ and $z$ when each is built from its variable by the same formal expression.

## Notable points

- Euler admits complex values into the domain of a variable. The square root $\sqrt{9 - z^2}$, though bounded by 3 on the reals, takes every value when $z$ is allowed to be complex, e.g. $z = 5i$ (source: chapter1, §5).
- "Apparent functions" like $z^0$, $1^z$, and $\frac{a^2 - az}{a - z}$ look like functions of $z$ but are actually constants (source: chapter1, §5).
- An expression with a transcendental constant but no transcendental operation on the variable is still algebraic: $c + z$, $cz^2$, and $4z^c$ (with $c$ the circumference of a unit-radius circle) count as algebraic functions of $z$ (source: chapter1, §7).
- A definition by an unsolvable polynomial equation, such as $Z^6 = az^2 Z^3 - bz^4 Z^2 + cz^3 Z - 1$, still counts as defining $Z$ as an (implicit) algebraic function of $z$ (source: chapter1, §7).
- If $n$ is odd, $P^{m/n}$ has a single real value and may be treated as single-valued; if $n$ is even and $m/n$ is in lowest terms, $P^{m/n}$ is two-valued (source: chapter1, §15).

## Why this chapter matters

This is the chapter where the modern idea of "function" takes a recognizable shape. Euler's definition as an analytic expression dominated 18th-century analysis and was only later displaced by the set-theoretic notion of a rule or mapping. The parity and multi-valuedness notions introduced here return throughout the *Introductio*.

## Related pages

- [[function]]
- [[variable-and-constant]]
- [[classification-of-functions]]
- [[single-valued-and-multi-valued-functions]]
- [[even-and-odd-functions]]
- [[similar-functions]]
