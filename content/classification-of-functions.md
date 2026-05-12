# Classification of Functions

**Summary**: Euler organizes functions by which operations are used to build them and how those operations involve the variable. The result is a tree: algebraic vs. transcendental, then non-irrational vs. irrational, then polynomial vs. rational.

**Sources**: chapter1

**Last updated**: 2026-04-23

---

## The tree

```
function
|-- algebraic           (only algebraic operations on the variable)
|   |-- non-irrational  (no radicals involving the variable)
|   |   |-- polynomial  (non-negative integer exponents of $z$ only)
|   |   `-- rational    ($z$ appears in denominators or with negative exponents)
|   `-- irrational      (variable affected by radical signs)
|       |-- explicit    (radicals written out)
|       `-- implicit    (defined by an unsolved polynomial equation)
`-- transcendental      (transcendental operation actually affects the variable)
```

The splits are defined by:

- **Algebraic vs. transcendental** (§7): a function is algebraic if it uses only the algebraic operations listed in [[function]] — addition, subtraction, multiplication, division, integer powers, roots, solving polynomial equations. It is transcendental if a transcendental operation (exponential, logarithm, etc.) actually affects the variable. An expression with a transcendental *constant* but no transcendental operation on the variable is still algebraic; Euler's examples are $c + z$, $cz^2$, $4z^c$ with $c$ the circumference of a unit-radius circle (source: chapter1, §7).
- **Non-irrational vs. irrational** (§8): non-irrational uses only addition, subtraction, multiplication, division, and integer-exponent powers of $z$; irrational has the variable inside a radical.
- **Polynomial vs. rational** (§9): polynomial has no negative exponents and no $z$ in denominators; rational allows either.

## General forms

**Polynomial**:

$$
a + b z + c z^2 + d z^3 + e z^4 + f z^5 + \dots
$$

Every polynomial function fits this template (source: chapter1, §9).

**Rational** (numerator and denominator are polynomials):

$$
\frac{a + b z + c z^2 + d z^3 + \dots}{\alpha + \beta z + \gamma z^2 + \delta z^3 + \dots}
$$

Every rational function reduces to this form by combining fractions over a common denominator. The coefficients $a, b, c, \dots$ and $\alpha, \beta, \gamma, \dots$ may be "positive or negative, integers or fractions, rational or irrational, or even transcendental" without changing the classification (source: chapter1, §9).

## Irrational functions

Irrational functions are split into:

- **Explicit**: written with radical signs, e.g. $\sqrt{z}$, $a + \sqrt{a^2 - z^2}$, $(a - 2z + z^2)^{1/3}$, $\frac{a^2 - z \sqrt{a^2 + z^2}}{a + z}$ (source: chapter1, §8). These arise from the **extraction of roots** operation.
- **Implicit**: defined by an equation that cannot be solved explicitly by radicals, e.g. $Z$ defined by $Z^7 = az$ or by the irreducible equation $Z^6 = az^2 Z^3 - bz^4 Z^2 + cz^3 Z - 1$ (source: chapter1, §7, §8). These arise from the **solution of equations** operation.

Euler is careful to distinguish solvability in principle from solvability in current practice: "common algebra has not yet developed to such a degree of perfection" (source: chapter1, §8).
 This is an 18th-century remark, written before Ruffini (1799) and Abel (1824) proved the impossibility of solving the general quintic by radicals.

## Edge case: exponents

An expression like $z^c$, where $c$ is the transcendental constant $\pi$ (unit-circle circumference = $2\pi$, but Euler here uses $c$ for the circumference itself), is strictly algebraic under Euler's rule because the transcendental enters only as a constant. Some authors prefer to call such expressions "intercendental" rather than algebraic; Euler himself notes the dispute but treats it as unimportant (source: chapter1, §7).

## Extension to several variables (Chapter 5, §79–§80)

The same tree is used verbatim for multivariate functions. A function of $y, z, \ldots$ is transcendental if a transcendental operation affects some variable; a "mixed" case is allowed where the transcendental involves only some variables — e.g. $z^2 + y \log z$ is transcendental in $y, z$ jointly but becomes algebraic in $y$ when $z$ is fixed (source: chapter5, §79). Algebraic multivariate functions split the same way: irrational (explicit or implicit) vs. non-irrational, and non-irrational into polynomial and rational. The general polynomial in $y, z$ is

$$\alpha + \beta y + \gamma z + \delta y^2 + \epsilon yz + \zeta z^2 + \eta y^3 + \theta y^2 z + \iota y z^2 + \kappa z^3 + \cdots$$

and the general rational function is $P/Q$ for polynomials $P, Q$ (source: chapter5, §80). Multivariate polynomials and rational functions admit the additional classifications of *homogeneity*, *order*, and *reducibility* developed in [[chapter-5-on-functions-of-two-or-more-variables]] — see [[homogeneous-function]] and [[reducible-polynomial]].

## Related pages

- [[function]]
- [[variable-and-constant]]
- [[single-valued-and-multi-valued-functions]]
- [[chapter-1-on-functions-in-general]]
- [[functions-of-several-variables]]
- [[homogeneous-function]]
- [[reducible-polynomial]]
