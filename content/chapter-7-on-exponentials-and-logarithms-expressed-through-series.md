# Chapter 7: Exponentials and Logarithms Expressed through Series

**Summary**: Euler returns to $a^z$ and $\log y$ from Chapter 6 and now develops them analytically. Using a single heuristic — let $\omega$ be infinitely small and $j = z/\omega$ infinitely large, so $a^z = (1 + k\omega)^j = (1 + kz/j)^j$ — he produces the [[exponential-series]] $a^z = \sum (kz)^n/n!$ and the [[logarithmic-series]] $\log(1+x) = (1/k)(x - x^2/2 + \cdots)$. Choosing the base so that $k = 1$ defines [[eulers-number|$e$]]; the resulting [[natural-logarithm]] system is the simplest, and $k = \log_e a$ is the modern conversion factor of [[change-of-base]].

**Sources**: chapter7

**Last updated**: 2026-04-26

---

## Overview

Chapter 6 set the stage: $a^z$ exists, its inverse $\log y$ exists, and most of their values are transcendental. The two computational tools available there were ad hoc — iterated geometric means (§106) for individual logarithms and table lookup (§109–§111) for everything else. Chapter 7 replaces those with *infinite series* that compute exponentials and logarithms to any precision.

The chapter has three movements:

1. **§114–§117 — the exponential series.** Set $a^\omega = 1 + k\omega$ with $\omega$ infinitely small; the proportionality constant $k$ depends on the base. Raise to the $j$-th power, let $j = z/\omega$ be infinitely large, and the binomial expansion of $(1 + kz/j)^j$ collapses (since $(j-m)/j = 1$ for finite $m$) into $a^z = \sum (kz)^n/n!$. The general $b^z$ follows from $b = a^{\log b}$.
2. **§118–§121 — the logarithmic series.** Run the same machinery in reverse. From $a^\omega = 1 + k\omega$ get $\omega = \log(1+k\omega)$; setting $(1 + k\omega)^j = 1 + x$ and expanding $(1+x)^{1/j}$ binomially yields $\log(1+x) = (1/k)(x - x^2/2 + x^3/3 - \cdots)$. The natural derivative — set $1+x = a$ to extract $k$ — *diverges* for $a = 10$, but the trick of subtracting $\log(1-x)$ from $\log(1+x)$ gives the rapidly convergent $\log\frac{1+x}{1-x} = (2/k)(x + x^3/3 + x^5/5 + \cdots)$, from which $k$ can be computed for any base.
3. **§122–§125 — the natural logarithm and $e$.** Choose the base so $k = 1$. Then $a = 1 + 1/1! + 1/2! + 1/3! + \cdots$, which Euler computes as $2.71828182845904523536028\ldots$, denotes $e$, and calls "the base of natural or hyperbolic logarithms" (§122). The series collapse to the canonical $e^z = \sum z^n/n!$, $\log(1+x) = x - x^2/2 + x^3/3 - \cdots$. Euler tabulates $\log 1, \ldots, \log 10$ to twenty digits and shows that for any other base $a$, $k = \log_e a$ is the conversion factor.

See also: [[infinitesimal-and-infinite-numbers]], [[exponential-series]], [[logarithmic-series]], [[eulers-number]], [[natural-logarithm]], [[change-of-base]].

## Structure of the chapter

### §114 — Setup: $a^\omega = 1 + k\omega$ and the constant $k$

For $a > 1$ and any infinitely small positive $\omega$, $a^\omega$ exceeds 1 by an infinitely small amount: $a^\omega = 1 + \psi$. Since $\omega$ being infinitely small forces $\psi$ to be infinitely small (and vice versa), they are commensurable and Euler writes $\psi = k\omega$, so

$$a^\omega = 1 + k\omega, \qquad \omega = \log(1 + k\omega).$$

The constant $k$ is finite and *depends on $a$*. Worked example: with $a = 10$ and $1 + k\omega = 1 + 1/1{,}000{,}000$, the common log table gives $\omega = \log(1 + 10^{-6}) = 0.00000043429$, so $1/k = 0.43429$ and $k \approx 2.30258$ (source: chapter7, §114). This is the same $k$ that turns out to equal $\log_e 10$ — but at this stage Euler only knows it as a base-dependent finite quantity.

### §115 — Binomial expansion of $a^{j\omega}$

Raising $a^\omega = 1 + k\omega$ to the $j$-th power gives $a^{j\omega} = (1 + k\omega)^j$. Expanding the right side by Newton's binomial (Chapter 4, [[binomial-series]]):

$$a^{j\omega} = 1 + \frac{j}{1} k\omega + \frac{j(j-1)}{1\cdot 2} k^2\omega^2 + \frac{j(j-1)(j-2)}{1\cdot 2\cdot 3} k^3\omega^3 + \cdots$$

Now substitute $j = z/\omega$, so $j$ is *infinitely large* and $\omega = z/j$ is *infinitely small*:

$$a^z = \left(1 + \frac{kz}{j}\right)^j = 1 + \frac{1}{1}kz + \frac{1(j-1)}{1\cdot 2 j}k^2 z^2 + \frac{1(j-1)(j-2)}{1\cdot 2 j \cdot 3 j}k^3 z^3 + \cdots$$

(source: chapter7, §115). This is true *because* $j$ is infinitely large.

### §116 — Collapsing the coefficients

Since $j$ is infinitely large, $(j - m)/j = 1$ and $(j - m)/(nj) = 1/n$ for every finite $m, n$ (source: chapter7, §116). Each binomial coefficient of $(1 + kz/j)^j$ collapses to a reciprocal factorial:

$$a^z = 1 + \frac{kz}{1} + \frac{k^2 z^2}{1\cdot 2} + \frac{k^3 z^3}{1\cdot 2\cdot 3} + \frac{k^4 z^4}{1\cdot 2\cdot 3\cdot 4} + \cdots$$

Setting $z = 1$ gives the *defining relation* between $a$ and $k$:

$$a = 1 + \frac{k}{1} + \frac{k^2}{1\cdot 2} + \frac{k^3}{1\cdot 2\cdot 3} + \frac{k^4}{1\cdot 2\cdot 3\cdot 4} + \cdots$$

For $a = 10$, this series in $k$ must equal 10, recovering $k \approx 2.30258$. See [[exponential-series]].

### §117 — The general exponential $b^z$

If $b = a^n$ then $\log_a b = n$, and $b^z = a^{nz}$. Substituting $nz$ for $z$ in §116 and then writing $n = \log b$:

$$b^z = 1 + \frac{kz \log b}{1} + \frac{k^2 z^2 (\log b)^2}{1\cdot 2} + \frac{k^3 z^3 (\log b)^3}{1\cdot 2\cdot 3} + \cdots$$

So once $k$ is known for a chosen base $a$, every other exponential $b^z$ has a power series in $z$ whose coefficients are powers of $\log b$ (source: chapter7, §117).

### §118–§119 — Inverting: the logarithmic series

§118 starts the inversion. From $a^\omega = 1 + k\omega$, $\omega = \log(1 + k\omega)$ and $j\omega = \log(1 + k\omega)^j$. Setting

$$(1 + k\omega)^j = 1 + x \quad\Longrightarrow\quad \log(1 + x) = j\omega.$$

For $j\omega$ to remain a *finite* number (the logarithm), $j$ must be infinitely large (and so $\omega$ infinitely small).

§119 inverts the relation: $1 + k\omega = (1 + x)^{1/j}$, so $k\omega = (1+x)^{1/j} - 1$ and $j\omega = (j/k)\bigl((1+x)^{1/j} - 1\bigr)$. Hence

$$\log(1 + x) = \frac{j}{k}(1+x)^{1/j} - \frac{j}{k}.$$

Expand $(1+x)^{1/j}$ by the binomial series:

$$(1+x)^{1/j} = 1 + \frac{1}{j}x - \frac{1(j-1)}{j\cdot 2j}x^2 + \frac{1(j-1)(2j-1)}{j\cdot 2j\cdot 3j}x^3 - \cdots$$

For $j$ infinite, $(j-1)/(2j) = 1/2$, $(2j-1)/(3j) = 2/3$, etc. — the same collapse as §116 — and the leading $j/k$ cancels the constant term, leaving

$$\log(1 + x) = \frac{1}{k}\left(\frac{x}{1} - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots\right).$$

See [[logarithmic-series]].

### §120 — The divergence paradox

Set $1 + x = a$ in the §119 series. Since $\log a = 1$,

$$k = \frac{a-1}{1} - \frac{(a-1)^2}{2} + \frac{(a-1)^3}{3} - \frac{(a-1)^4}{4} + \cdots$$

For $a = 10$ this reads $2.30258 = 9/1 - 81/2 + 729/3 - 6561/4 + \cdots$ — manifestly divergent in any pre-modern reading (source: chapter7, §120). Euler flags this as a paradox to be resolved in §121.

### §121 — The fast-convergent $\log\frac{1+x}{1-x}$

Substituting $-x$ for $x$ in the §119 series:

$$\log(1-x) = -\frac{1}{k}\left(\frac{x}{1} + \frac{x^2}{2} + \frac{x^3}{3} + \frac{x^4}{4} + \cdots\right).$$

Subtract from $\log(1+x)$: even-power terms cancel, odd-power terms double:

$$\log\frac{1+x}{1-x} = \frac{2}{k}\left(\frac{x}{1} + \frac{x^3}{3} + \frac{x^5}{5} + \frac{x^7}{7} + \cdots\right).$$

Now solve $(1+x)/(1-x) = a$ for $x$: $x = (a-1)/(a+1)$. For $a = 10$, $x = 9/11 < 1$, so

$$k = 2\left(\frac{9}{11} + \frac{9^3}{3 \cdot 11^3} + \frac{9^5}{5 \cdot 11^5} + \cdots\right)$$

— a series whose terms decrease *geometrically*, giving fast convergence to $k \approx 2.30258$ (source: chapter7, §121). The paradox of §120 is resolved: the divergent series of §120 is the wrong tool for $a > 2$; the §121 series is the right one.

### §122 — Defining $e$ as the base where $k = 1$

The base $a$ is at the analyst's disposal — choose it so $k = 1$. Then the §116 defining series collapses to

$$a = 1 + \frac{1}{1} + \frac{1}{1\cdot 2} + \frac{1}{1\cdot 2\cdot 3} + \frac{1}{1\cdot 2\cdot 3\cdot 4} + \cdots = 2.71828182845904523536028\ldots$$

(source: chapter7, §122). Euler denotes this number $e$ — the first appearance of the symbol — and calls the resulting logarithms *natural* or *hyperbolic* (the latter "since the quadrature of a hyperbola can be expressed through these logarithms"). See [[eulers-number]].

### §123 — The canonical natural-log series and a logarithm table

With $k = 1$ the three master identities take their cleanest form (source: chapter7, §123):

$$e^z = 1 + z + \frac{z^2}{2!} + \frac{z^3}{3!} + \cdots,$$

$$\log(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \frac{x^5}{5} - \cdots,$$

$$\log\frac{1+x}{1-x} = \frac{2x}{1} + \frac{2x^3}{3} + \frac{2x^5}{5} + \frac{2x^7}{7} + \cdots.$$

Sample applications: $x = 1/5$ gives $\log(3/2) = 2/(1\cdot 5) + 2/(3 \cdot 5^3) + \cdots$; $x = 1/7$ gives $\log(4/3)$; $x = 1/9$ gives $\log(5/4)$. Combining these by the Chapter 6 algebraic rules ($\log(3/2) + \log(4/3) = \log 2$, etc.) yields all integer logs $\log 2, \ldots, \log 6, \log 8, \log 9, \log 10$. For $\log 7$, set $x = 1/99$ to get $\log(50/49) = \log 50 - 2\log 7$, then $\log 7 = (\log 50 - \log(50/49))/2$. Euler writes out the resulting table to twenty decimal places (e.g. $\log 2 = 0.69314\,71805\,59945\,30941\,72321$, $\log 10 = 2.30258\,50929\,94045\,68401\,79914$).

### §124 — $k$ is the natural log of $a$

For an arbitrary base $a$, let $y = \log_e(1+x)$ and $v = \log_a(1+x)$. The §119 series for $v$ differs from the §123 series for $y$ only by the factor $1/k$, so $v = y/k$ and

$$k = \frac{y}{v} = \frac{\log_e(1+x)}{\log_a(1+x)}.$$

Setting $1 + x = a$ gives $v = 1$ and $k = \log_e a$ (source: chapter7, §124). For $a = 10$: $k = \log_e 10 = 2.30258\,50929\,94045\,68401\,79914$, exactly the value computed in §114, §121, §123. Conversely, dividing every natural log by $k$ (or multiplying by $1/k = 0.43429\,44819\,03251\,82765\,11289$) gives common logs — recovering [[change-of-base]] from Chapter 6.

### §125 — Two more identities

From $e^z$ and $a^y = e^{y \log a}$ (with $\log = \log_e$, since $\log e = 1$):

$$a^y = 1 + \frac{y \log a}{1} + \frac{y^2 (\log a)^2}{1\cdot 2} + \frac{y^3 (\log a)^3}{1\cdot 2\cdot 3} + \cdots.$$

And from the underlying $j$-form:

$$e^z = \left(1 + \frac{z}{j}\right)^j, \qquad a^y = \left(1 + \frac{y \log a}{j}\right)^j, \qquad \log(1 + x) = j\bigl((1+x)^{1/j} - 1\bigr),$$

with $j$ infinitely large (source: chapter7, §125). Euler closes the chapter by noting that further uses of natural logs are deferred to integral calculus.

## Notable points

- **The chapter's logical machine is Euler's [[infinitesimal-and-infinite-numbers|infinitesimal–infinite identification]].** Every derivation rests on simultaneously using $\omega \to 0$ and $j = z/\omega \to \infty$, then setting $(j - m)/j = 1$ for finite $m$. This is not modern limit-taking; it is treated as a transparent algebraic identity. The whole power-series theory of $e^z$ and $\log$ falls out by one move.
- **$e$ is *defined* analytically, not geometrically.** Unlike $\pi$, which Euler will reach via the circle, $e$ enters as the unique base for which the multiplicative constant $k$ in $a^\omega = 1 + k\omega$ equals 1. The geometric ("hyperbolic") interpretation is mentioned only as etymology; the working definition is the series $\sum 1/n!$.
- **The §120 divergence is honest.** Euler does not hide that his most natural inversion of the exponential series fails for $a = 10$. He resolves it not by qualifying the original series but by deriving a *different* series (the $\log\frac{1+x}{1-x}$ one) whose convergence properties are favorable. The interplay of two series, one slow/divergent and one fast, computing the same quantity, will recur throughout the *Introductio*.
- **Every transcendental computation in Chapter 6 now has a series counterpart.** [[geometric-mean-method-for-logarithms|Geometric means]] still work but are no longer needed: §123 produces $\log 2, \log 3, \log 5, \log 7$ from $x = 1/5, 1/7, 1/9, 1/99$ in a few quickly-converging terms, and the rest follow by the algebraic rules of [[logarithm|§104]].
- **Chapter 7 is the analytic counterpart of Chapter 6 in the same sense Chapter 4 was for Chapters 2–3.** Where Chapter 4 expanded *algebraic* functions (rational, then irrational via Newton's binomial) in series, Chapter 7 expands the *transcendental* exponential and logarithm. The `(1 + z/j)^j` representation of $e^z$ is the bridge: a transcendental function exhibited as the limit of an algebraic family.

## Why this chapter matters

Chapters 6 and 7 together are the foundation of every later chapter that mentions $e$, $\log$, sines, cosines, or $\pi$. Chapter 6 secured existence; Chapter 7 secures *computation* — every value of $a^z$ and $\log y$ is now reachable by summing a power series. The exponential series $e^z = \sum z^n/n!$ in particular will be the input to Chapter 8's derivation of the trigonometric series and the Euler formula $e^{ix} = \cos x + i \sin x$.

The chapter also installs Euler's main analytic technique — the simultaneous use of an infinitely small $\omega$ and an infinitely large $j$ with $j\omega$ finite — as the standard tool of the *Introductio*. The next several chapters will reuse this device almost verbatim, with $z$ replaced by $iz$, by trigonometric arguments, and by other parameters.

## Related pages

- [[infinitesimal-and-infinite-numbers]]
- [[exponential-series]]
- [[logarithmic-series]]
- [[eulers-number]]
- [[natural-logarithm]]
- [[exponential-function]]
- [[logarithm]]
- [[change-of-base]]
- [[binomial-series]]
- [[geometric-mean-method-for-logarithms]]
- [[chapter-6-on-exponentials-and-logarithms]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
