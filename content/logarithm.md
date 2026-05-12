# Logarithm

**Summary**: For base $a > 1$, the *logarithm* of $y > 0$ is the unique real $z$ such that $a^z = y$, written $z = \log y$ (§102). Logarithms convert multiplication into addition (§104) and turn the algebra of [[exponential-function|exponentials]] inside out. They are real-valued only for positive arguments; for "generic" arguments they are transcendental — see [[transcendence-of-logarithms]].

**Sources**: chapter6.pdf (§102–§104)

**Last updated**: 2026-04-26

---

## Definition

Fix a *base* $a > 1$. For each $y > 0$, the [[exponential-function]] $a^z$ takes the value $y$ exactly once, so the equation $a^z = y$ has a unique real solution $z$. This $z$ is called the **logarithm of $y$** to the base $a$, and is denoted

$$z = \log y \quad \text{when} \quad a^z = y$$

(source: chapter6.pdf, §102). The base must be specified for the symbol $\log$ to be unambiguous; "infinitely many systems of logarithms" exist, one for each base (see [[change-of-base]]).

Euler restricts to bases $a > 1$ throughout the chapter — the only setting in which $\log$ is real-valued on $(0, \infty)$ and increasing.

## When the logarithm is real

- $y > 0$: $\log y$ is a real number.
- $y = 0$: no real $z$ satisfies $a^z = 0$ (the equation has $z = -\infty$ as a limit, not a value).
- $y < 0$: no real $z$ satisfies $a^z = y$ when $a > 1$; "the logarithm is complex" (source: chapter6.pdf, §103).

## First values (§103)

$$\log 1 = 0, \qquad \log a = 1, \qquad \log a^2 = 2, \qquad \log a^n = n,$$

and

$$\log\frac{1}{a} = -1, \qquad \log\frac{1}{a^2} = -2, \qquad \log\frac{1}{a^n} = -n.$$

So $\log y > 0$ for $y > 1$ and $\log y < 0$ for $0 < y < 1$, in any system. The base $a$ itself is identified after the fact as *the unique number whose logarithm is 1*.

## Algebraic rules (§104)

The properties of the [[exponential-function]] translate into four rules:

| Exponential identity | Logarithmic identity |
|:--|:--|
| $y^n = a^{nz}$ | $\log y^n = n \log y$ |
| $\sqrt[n]{y} = a^{z/n}$ | $\log \sqrt[n]{y} = \tfrac{1}{n} \log y$ |
| $vy = a^{x+z}$ | $\log(vy) = \log v + \log y$ |
| $v/y = a^{x-z}$ | $\log(v/y) = \log v - \log y$ |

These four are the entire algebra of logarithms (source: chapter6.pdf, §104). Their power: a complicated arithmetic expression in $v, y, n, \ldots$ becomes a *linear combination* of the logarithms $\log v, \log y, \ldots$ — the trick that makes logarithm tables a universal calculation tool (cf. §110).

## Consequences

- Logarithms of *powers* and *roots* of a known number $y$ follow from $\log y$ alone.
- Logarithms of *products* and *quotients* of known numbers reduce to sums and differences.
- A table of $\log p$ for each prime $p$ therefore generates the logarithm of every positive rational by additions, subtractions, and rational multiples (see [[change-of-base]] and §109).

## Why "transcendental" (§105)

Most logarithms are not rational, not even algebraic — see [[transcendence-of-logarithms]]. This forces them to be computed approximately, and motivates the [[geometric-mean-method-for-logarithms|geometric-mean algorithm]] of §106 and the table-driven calculations of §110–§111.

## Related pages

- [[exponential-function]]
- [[transcendence-of-logarithms]]
- [[geometric-mean-method-for-logarithms]]
- [[change-of-base]]
- [[common-logarithm]]
- [[characteristic-and-mantissa]]
- [[chapter-6-on-exponentials-and-logarithms]]
