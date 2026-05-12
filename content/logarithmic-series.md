# Logarithmic Series

**Summary**: §118–§121 of Chapter 7. Inverting the [[exponential-series|exponential series]] derivation, Euler obtains

$$\log(1+x) = \frac{1}{k}\left(\frac{x}{1} - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots\right),$$

valid for $|x| < 1$ (where $k = \log_e a$ is the base-dependent constant of [[exponential-series|§114–§116]]). The naive substitution $1 + x = a$ yields a *divergent* series for $k$ at $a = 10$; Euler resolves this with the fast-converging variant

$$\log\frac{1+x}{1-x} = \frac{2}{k}\left(\frac{x}{1} + \frac{x^3}{3} + \frac{x^5}{5} + \cdots\right),$$

obtained by subtracting the $\log(1-x)$ series from the $\log(1+x)$ series.

**Sources**: chapter7 (§118–§121)

**Last updated**: 2026-05-11

---

## Setup (§118)

From [[exponential-series|§114]], $a^\omega = 1 + k\omega$ for infinitely small $\omega$, and so $\omega = \log(1 + k\omega)$ in the system with base $a$. Raising to the $j$-th power:

$$j\omega = \log(1 + k\omega)^j.$$

Set $(1 + k\omega)^j = 1 + x$, where $x$ is a finite number. Then $j$ must be infinitely large for $j\omega$ — the logarithm of the finite number $1 + x$ — to be itself finite (source: chapter7, §118). The picture is the dual of the [[exponential-series]] setup: there $z = j\omega$ was the exponent; here $\log(1 + x) = j\omega$ is the logarithm.

## Derivation (§119)

From $(1 + k\omega)^j = 1 + x$, take $j$-th roots:

$$1 + k\omega = (1 + x)^{1/j}, \qquad k\omega = (1 + x)^{1/j} - 1, \qquad j\omega = \frac{j}{k}\bigl((1+x)^{1/j} - 1\bigr).$$

Since $j\omega = \log(1+x)$,

$$\log(1+x) = \frac{j}{k}(1+x)^{1/j} - \frac{j}{k}.$$

Expand $(1+x)^{1/j}$ by the binomial series ([[binomial-series]]):

$$(1+x)^{1/j} = 1 + \frac{1}{j} x - \frac{1(j-1)}{j \cdot 2j} x^2 + \frac{1(j-1)(2j-1)}{j \cdot 2j \cdot 3j} x^3 - \frac{1(j-1)(2j-1)(3j-1)}{j \cdot 2j \cdot 3j \cdot 4j} x^4 + \cdots$$

Multiply by $j/k$ and use the [[infinitesimal-and-infinite-numbers|$j$-collapse]] $(j-1)/(2j) = 1/2$, $(2j-1)/(3j) = 2/3$, $(3j-1)/(4j) = 3/4$, etc., for infinite $j$:

$$\frac{j}{k}(1+x)^{1/j} = \frac{j}{k} + \frac{1}{k}\left(\frac{x}{1} - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots\right).$$

The constant $j/k$ on each side cancels, leaving

$$\boxed{\;\log(1+x) = \frac{1}{k}\left(\frac{x}{1} - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots\right).\;}$$

(source: chapter7, §119). When the base is chosen so $k = 1$ (so $a = e$, see [[eulers-number]]), this becomes the canonical natural-log series

$$\log(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots$$

— the *Mercator series*, in modern naming.

## Computing $k$: the divergence paradox (§120)

Setting $1 + x = a$ in the boxed series gives, since $\log a = 1$,

$$1 = \frac{1}{k}\left(\frac{a-1}{1} - \frac{(a-1)^2}{2} + \frac{(a-1)^3}{3} - \cdots\right),$$

so

$$k = \frac{a-1}{1} - \frac{(a-1)^2}{2} + \frac{(a-1)^3}{3} - \frac{(a-1)^4}{4} + \cdots$$

For $a = 10$ this reads $2.30258 = 9 - 81/2 + 729/3 - 6561/4 + \cdots$ — the terms grow without bound. Euler flags it explicitly:

> 2.30258 = $\frac{9}{1} - \frac{9^2}{2} + \frac{9^3}{3} - \cdots$, but it is difficult to see how this can be since the terms of this series continually grow larger and the sum of several terms does not seem to approach any limit. We will soon have an answer to this paradox.

(source: chapter7, §120). The boxed series converges only for $|x| < 1$, and at $a = 10$ we have $x = 9$. The "answer" is to substitute differently.

## The fast-converging variant (§121)

Substitute $-x$ for $x$ in the boxed series. The signs of odd-power terms flip:

$$\log(1-x) = -\frac{1}{k}\left(\frac{x}{1} + \frac{x^2}{2} + \frac{x^3}{3} + \frac{x^4}{4} + \cdots\right).$$

Subtract from the original. Even-power terms cancel; odd-power terms double:

$$\log(1+x) - \log(1-x) = \log\frac{1+x}{1-x} = \frac{2}{k}\left(\frac{x}{1} + \frac{x^3}{3} + \frac{x^5}{5} + \frac{x^7}{7} + \cdots\right).$$

Now solve $(1+x)/(1-x) = a$ for $x$:

$$x = \frac{a - 1}{a + 1}.$$

For any $a > 0$ this gives $|x| < 1$ — the series always converges, geometrically. So

$$k = 2\left(\frac{a-1}{a+1} + \frac{(a-1)^3}{3(a+1)^3} + \frac{(a-1)^5}{5(a+1)^5} + \cdots\right).$$

For $a = 10$: $x = 9/11$ and

$$k = 2\left(\frac{9}{11} + \frac{9^3}{3 \cdot 11^3} + \frac{9^5}{5 \cdot 11^5} + \frac{9^7}{7 \cdot 11^7} + \cdots\right),$$

whose terms shrink by a factor of about $(9/11)^2 = 0.67$ each pair of steps — fast enough that "soon a satisfactory approximation for $k$ can be obtained" (source: chapter7, §121). The paradox of §120 is resolved: Euler swaps to a different algebraic representation of $\log a$ that converges where the first series fails.

## Key applications

When $k = 1$ (base $e$), the variant series becomes

$$\log\frac{1+x}{1-x} = 2\left(\frac{x}{1} + \frac{x^3}{3} + \frac{x^5}{5} + \frac{x^7}{7} + \cdots\right).$$

Sample values used by Euler in [[natural-logarithm|§123]] to build a table of $\log 1, \ldots, \log 10$:

| $x$ | $(1+x)/(1-x)$ | Computes |
|:--|:--|:--|
| $1/5$ | $3/2$ | $\log(3/2)$ |
| $1/7$ | $4/3$ | $\log(4/3)$ |
| $1/9$ | $5/4$ | $\log(5/4)$ |
| $1/99$ | $50/49$ | $\log(50/49)$, used to extract $\log 7$ |

Combined with the algebraic identities $\log(3/2) + \log(4/3) = \log 2$, $\log(3/2) + \log 2 = \log 3$, etc. (Chapter 6, [[logarithm|§104]]), these series produce all the integer logs to twenty decimal places.

## Two paradoxes worth noting

1. **The §120 series is correct as a formal manipulation but fails as a numerical computation when $|a - 1| \ge 1$.** Euler does not say "the series diverges"; he says "the sum of several terms does not seem to approach any limit", and offers a workaround. This is one of the clearest *Introductio* moments where formal series and numerical convergence part company.
2. **The variant series for $\log\frac{1+x}{1-x}$ has the same domain $|x| < 1$ but parameterizes positive arguments very differently.** Setting $(1+x)/(1-x) = y$ sweeps $y$ across $(0, \infty)$ as $x$ moves in $(-1, 1)$ — every positive number is reachable. So the $\log\frac{1+x}{1-x}$ series alone is enough to compute *every* logarithm.

## Related pages

- [[exponential-series]]
- [[exponential-function]]
- [[logarithm]]
- [[eulers-number]]
- [[natural-logarithm]]
- [[infinitesimal-and-infinite-numbers]]
- [[binomial-series]]
- [[log-pi-via-products]]
- [[log-sine-via-products]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
- [[geometric-mean-method-for-logarithms]]
- [[chapter-15-on-series-which-arise-from-products]]
- [[divergence-of-prime-reciprocals]]
- [[continued-fraction-for-log-2]] — chapter 18 converts the alternating-harmonic series at $x = 1$ into a continued fraction with square partial numerators
- [[chapter-18-on-continued-fractions]]
