# Exponential Function

**Summary**: Euler's exponential is the function $y = a^z$ with constant base $a$ and variable exponent $z$ (§96–§101). Defined first on integers, then on rationals by $a^{p/q} = \sqrt[q]{a^p}$ (taking the primary positive value), then extended by interpolation to irrational $z$. Restricting to $a > 1$ gives the canonical case: a single-valued, strictly increasing function from $\mathbb{R}$ onto $(0, \infty)$.

**Sources**: chapter6.pdf (§96–§101)

**Last updated**: 2026-04-26

---

## Why exponentials are not algebraic

A function built only from arithmetic operations and root extraction with *constant* exponents is algebraic (see [[classification-of-functions]]). The moment the exponent becomes a variable — as in $a^z$, $y^z$, $a^{a^z}$, $a^{y^z}$, $y^{x^z}$, $x^{y^z}$ — the function leaves the algebraic class (source: chapter6.pdf, §96). Euler treats $a^z$ as the canonical representative because the analysis of one variant settles the others.

## Definition by extension

Let $a > 0$. The exponential $a^z$ is defined in stages (source: chapter6.pdf, §97):

- **Positive integer $z$:** $a^z = a \cdot a \cdots a$ ($z$ factors).
- **$z = 0$:** $a^0 = 1$.
- **Negative integer $z = -n$:** $a^{-n} = 1/a^n$.
- **Rational $z = p/q$:** $a^{p/q} = \sqrt[q]{a^p}$. The $q$-th root is generally multi-valued, but Euler restricts to the *primary positive real value* so that $a^z$ is single-valued. So $a^{5/2}$ lies between $a^2$ and $a^3$, and equals $a^2 \sqrt{a}$ (not its negative).
- **Irrational $z$:** by interpolation. $a^{\sqrt 7}$ lies between $a^2$ and $a^3$ and is determined as the common value of all rational approximations from above and below. Euler does not prove this is well-defined; he treats it as evident from the monotonic interpolation.

Restriction to real exponents is explicit: complex $z$ is deferred to later chapters.

## Case analysis on the base

The qualitative behavior of $a^z$ depends on $a$ (source: chapter6.pdf, §98–§99):

| Range of $a$ | Behavior of $a^z$ |
|:--|:--|
| $a = 1$ | constant $1$ |
| $a > 1$ | strictly increasing; $a^z \to \infty$ as $z \to \infty$, $a^z \to 0$ as $z \to -\infty$ |
| $0 < a < 1$ | strictly decreasing; reduces to $a > 1$ via $1/a$, since $a^z = (1/a)^{-z}$ |
| $a = 0$ | $0^z = 0$ for $z > 0$; $0^0 = 1$; $0^{-n} = 1/0^n$ "is infinite" — discontinuous at $z = 0$ |
| $a < 0$ | integer $z$: alternating sign; rational $z$: real or pure-imaginary depending on parity ($(-2)^{1/2} = \sqrt{-2}$, $(-2)^{1/3} = -\sqrt[3]{2}$); irrational $z$: unpredictable |

§100 distills the conclusion: take $a > 1$ as the canonical case. The case $0 < a < 1$ then reduces via $1/a$, and $a \le 0$ is set aside as pathological.

## Properties (§101)

For $y = a^z$ and $v = a^x$:

$$y^n = a^{nz}, \qquad y^{1/n} = a^{z/n}, \qquad \frac{1}{y} = a^{-z},$$

$$vy = a^{x+z}, \qquad \frac{v}{y} = a^{x-z}.$$

These multiplicative-to-additive identities are what make logarithms (the inverse function — see [[logarithm]]) so useful.

For the example $a = 10$: $10^1 = 10$, $10^2 = 100$, $10^{-1} = 0.1$, $10^{1/2} = \sqrt{10} \approx 3.162277$, etc.

## Shape of the canonical case

When $a > 1$:

- Domain: all real $z$.
- Range: $(0, +\infty)$.
- Strictly increasing, continuous, single-valued.
- Crosses $1$ at $z = 0$.
- Asymptote $y = 0$ as $z \to -\infty$; unbounded as $z \to \infty$.

Every positive $y$ has a unique real $z$ with $a^z = y$ — this is what makes the inverse $\log y$ well-defined as a real-valued function on $(0, \infty)$.

## Related pages

- [[logarithm]]
- [[classification-of-functions]]
- [[function]]
- [[chapter-6-on-exponentials-and-logarithms]]
