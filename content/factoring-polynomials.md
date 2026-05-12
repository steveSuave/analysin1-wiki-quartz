# Factoring Polynomials

**Summary**: Euler's account of resolving a polynomial function into linear and (real) quadratic factors, via its roots.

**Sources**: chapter2.pdf

**Last updated**: 2026-04-23

---

## Why factor?

"When a polynomial function is factored in this way, its nature is more easily seen; it is immediately clear for what values of $z$ the function is equal to zero" (source: chapter2.pdf, §28). For example, $6 - 7z + z^3 = (1 - z)(2 - z)(3 + z)$ lays bare that the function vanishes exactly at $z = 1, 2, -3$.

## Linear, quadratic, cubic factors

A polynomial has three basic kinds of factors (source: chapter2.pdf, §28):

- *Linear factor*: $f + g z$.
- *Quadratic factor*: $f + g z + h z^2$.
- *Cubic factor*: $f + g z + h z^2 + j z^3$.

A quadratic factor is a product of two linear factors, a cubic of three, and so on. A polynomial of degree $n$ contains exactly $n$ linear factors in total (possibly complex).

## Roots and linear factors (§29)

The linear factors of $Z$ are obtained from the roots of the equation $Z = 0$. If $z = f$ is a root, then $z - f$ divides $Z$. So if $Z = A z^n + B z^{n-1} + \cdots$ has roots $f, g, h, \ldots$,

$$ Z = A (z - f)(z - g)(z - h) \cdots $$

Equivalently, starting from $Z = A + B z + C z^2 + \cdots$,

$$ Z = A \left(1 - \frac{z}{f}\right) \left(1 - \frac{z}{g}\right) \left(1 - \frac{z}{h}\right) \cdots $$

The leading-coefficient factor $A$ must not be dropped.

## Real vs. complex factors (§30)

Linear factors are either real or complex, and **the number of complex linear factors is always even** (source: chapter2.pdf, §30). If $P$ is the product of the real factors of $Z$, then $Z/P$ must be real, which forces the complex factors to multiply in pairs to give real quadratic factors.

See [[complex-conjugate-factors]] for Euler's explicit pairing argument.

## Factorization into real linear and quadratic factors (§32)

Euler's main claim:

> Every polynomial function of $z$ can be expressed as the product of real factors, either linear or quadratic.

He admits the claim "has not been proved with complete rigor" and points forward to later chapters for corroboration (source: chapter2.pdf, §32). This is essentially the [[fundamental-theorem-of-algebra]] stated over $\mathbb{R}$.

## Related pages

- [[complex-conjugate-factors]]
- [[fundamental-theorem-of-algebra]]
- [[real-roots-by-degree-parity]]
- [[intermediate-value-property]]
- [[partial-fraction-decomposition]]
- [[chapter-2-on-the-transformation-of-functions]]
