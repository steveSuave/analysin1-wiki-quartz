# Intermediate Value Property

**Summary**: Euler's §33 statement that a (single-valued) polynomial function takes every intermediate value between any two of its values — a precursor to the intermediate value theorem.

**Sources**: chapter2

**Last updated**: 2026-04-23

---

## Statement

> If the polynomial function $Z$ takes the value $A$ when $z = a$ and takes the value $B$ when $z = b$, then there is a value of $z$ between $a$ and $b$ for which the function $Z$ takes any value between $A$ and $B$. (source: chapter2, §33)

## Euler's justification

Euler's argument is informal and rests on single-valuedness plus an implicit continuity intuition:

> Since $Z$ is a single valued function of $z$, for whatever real value is assigned to $z$, there is a real value for the function $Z$. ... the function cannot pass from $A$ to $B$ without taking on all of the intermediate values. (source: chapter2, §33)

He reformulates the claim in terms of linear factors: if $Z - A = 0$ and $Z - B = 0$ each have a real root, then $Z - C = 0$ has a real root whenever $C$ lies between $A$ and $B$ (source: chapter2, §33). That is the version actually used in §34–§37.

## How the property is used

The intermediate value property is the engine behind Euler's argument that every odd-degree polynomial has a real root: at $z = +\infty$ the polynomial is $+\infty$ and at $z = -\infty$ it is $-\infty$, so by the intermediate value property it takes every intermediate value, including $0$ (source: chapter2, §34). See [[real-roots-by-degree-parity]].

## Modern remarks

The modern intermediate value theorem requires continuity, proved rigorously only in the 19th century (Bolzano, Cauchy). For polynomials the result is in fact true and Euler's usage is sound, even if his justification is informal. See also [[single-valued-and-multi-valued-functions]] for Euler's notion of single-valued function.

## Related pages

- [[real-roots-by-degree-parity]]
- [[factoring-polynomials]]
- [[single-valued-and-multi-valued-functions]]
- [[chapter-2-on-the-transformation-of-functions]]
