# Common Logarithm

**Summary**: The base-10 [[logarithm]], distinguished by §112 because our arithmetic is decimal. Each common log splits into an integer *characteristic* (which encodes how many digits the number has) and a decimal *mantissa* (which encodes the digit pattern, independent of decimal placement) — see [[characteristic-and-mantissa]].

**Sources**: chapter6.pdf (§112)

**Last updated**: 2026-04-26

---

## Why base 10 is special

Logarithms in any base are equivalent up to a multiplicative constant (see [[change-of-base]]), but base 10 has a structural advantage tied to our decimal numeral system. Powers of 10 are *exactly* the place-value boundaries:

$$\log 1 = 0, \quad \log 10 = 1, \quad \log 100 = 2, \quad \log 1000 = 3, \ldots$$

So logarithms of numbers between 1 and 10 lie in $[0, 1)$; between 10 and 100 in $[1, 2)$; and so forth (source: chapter6.pdf, §112). Every common logarithm splits cleanly into an integer part and a fractional part — a feature unique (in clean form) to base 10.

## Structure: characteristic + mantissa

A common logarithm is written as

$$\log_{10} N = c + m, \qquad c \in \mathbb{Z}, \quad m \in [0, 1),$$

where $c$ is the *characteristic* and $m$ is the *mantissa*. See [[characteristic-and-mantissa]] for the detailed reading.

In one sentence:

- The **characteristic** $c$ depends only on the *order of magnitude* of $N$: $c = (\text{digit count of integer part of } N) - 1$ (for $N \ge 1$); $c$ is negative for $N < 1$.
- The **mantissa** $m$ depends only on the *digit pattern* of $N$, independent of where the decimal point sits.

## Briggs and Vlacq

The original tables of common logarithms were computed by Henry Briggs (1561–1630) and Adriaan Vlacq (1600–1667), using the [[geometric-mean-method-for-logarithms|geometric-mean method]] of §106 — extracting square roots until the geometric mean stabilized at the desired number. By Euler's time these tables, supplemented by §109's "logs of primes only" reduction, were the universal tool of practical computation.

## What you read off a common log

Given a tabulated value such as $\log_{10} 78509 = 4.8949437$, the table provides directly:

- **Digit count.** The characteristic $4$ says: $78509$ has $4 + 1 = 5$ digits.
- **The number from the log.** Conversely, the mantissa $0.8949437$ corresponds (in the table) to the digit string $78509$; the characteristic determines decimal placement.

## Why Euler emphasizes this

Common logarithms are not theoretically more fundamental than any other base — but they are practically optimal:

1. They convert multiplications, divisions, powers, and roots into additions, subtractions, and rational multiples (the algebra of §104).
2. The integer/fractional split makes table use almost mechanical: one looks up the mantissa for a digit string, then reads off the characteristic for the order of magnitude.
3. A single table covers all of $(0, \infty)$ at uniform precision — *because* same-mantissa logs differ only by a power of 10.

For Chapter 6's §110–§111 worked examples — population growth, compound debt, time to a tenfold population — the entire arithmetic is performed in common logs.

## Related pages

- [[logarithm]]
- [[characteristic-and-mantissa]]
- [[change-of-base]]
- [[geometric-mean-method-for-logarithms]]
- [[chapter-6-on-exponentials-and-logarithms]]
