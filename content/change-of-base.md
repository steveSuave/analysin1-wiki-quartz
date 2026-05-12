# Change of Base

**Summary**: §107–§108 of Chapter 6: any two systems of [[logarithm]]s differ only by a multiplicative constant, so a single table can be converted to any other base by one multiplication. Equivalently (§108), the *ratio* of the logarithms of two given numbers is base-independent — it records the algebraic relationship between the numbers, not the choice of base.

**Sources**: chapter6 (§107–§108)

**Last updated**: 2026-04-26

---

## The conversion rule (§107)

Let $n > 0$ and let $\log_a n = p$, $\log_b n = q$ be its logarithms in two different systems. By definition $a^p = n = b^q$, hence $a^p = b^q$, so $a = b^{q/p}$. The ratio $p/q$ is therefore the same constant for *every* $n$ — call it $\lambda = p/q = \log_b a$ (source: chapter6, §107).

Consequently: to convert a base-$a$ logarithm $p = \log_a n$ to base $b$, multiply by $1/\lambda$:

$$\log_b n = \frac{p}{\lambda} = \frac{\log_a n}{\log_a b}.$$

A single table of logarithms in any one system generates tables in every other system by one multiplication per entry.

## Worked example: base 10 → base 2

From the standard tables, $\log_{10} 2 = 0.3010300$ and $\log_2 2 = 1$. So $p/q = 0.3010300$, and the conversion factor is

$$\frac{1}{\log_{10} 2} = \frac{1}{0.3010300} = 3.3219277.$$

Multiplying every common (base-10) logarithm by $3.3219277$ produces the corresponding base-2 logarithm (source: chapter6, §107). The "golden rule for logarithms," in Euler's phrase.

## The base-free formulation (§108)

§108 reformulates the same fact without singling out a base. Take two numbers $M, N$. In base $a$, write $M = N^{m/n}$ (so $\log_a M / \log_a N = m/n$). In base $b$, write $M = N^{\mu/\nu}$ with the same $M, N$. Then

$$N^{m/n} = M = N^{\mu/\nu} \quad\Longrightarrow\quad \frac{m}{n} = \frac{\mu}{\nu},$$

so

$$\frac{\log M}{\log N} = \frac{m}{n}, \qquad \text{independent of base.}$$

In words: the *ratio of the logarithms of two numbers* is intrinsic — it is the rational (or transcendental) exponent expressing one number as a power of the other.

For powers of a common base, $y^m / y^n$ has $\log y^m / \log y^n = m/n$ — so log ratios of powers of a fixed number reduce to ratios of exponents.

## Consequences

- There is essentially *one* logarithm function, parameterized by base: every choice differs from every other by a multiplicative scalar.
- Equations of the form $a^x = b$ have the base-independent solution $x = \log b / \log a$ (source: chapter6, §111) — the ratio is the same in any system, so one can use the most convenient table.
- Computational interchange is trivial: a base-10 table built once (e.g. by [[geometric-mean-method-for-logarithms|the geometric-mean method]]) suffices for any other base via one multiplication.

## §109 — Tables built from primes

A direct corollary of the product rule and §107: only the logarithms of *primes* need be computed by the slow geometric-mean method. Logarithms of composites follow by addition (source: chapter6, §109):

$$\log 15 = \log 3 + \log 5, \qquad \log 45 = 2\log 3 + \log 5, \qquad \log 4 = 2 \log 2, \ldots$$

And $\log 2$ itself can be deduced from $\log 5$ by $\log 2 = \log 10 - \log 5 = 1 - 0.6989700 = 0.3010300$ (in base 10), so a single root extraction (for $\log 5$) supplies both prime logs needed to tabulate all numbers whose only prime factors are 2 and 5.

## Related pages

- [[logarithm]]
- [[geometric-mean-method-for-logarithms]]
- [[common-logarithm]]
- [[characteristic-and-mantissa]]
- [[chapter-6-on-exponentials-and-logarithms]]
