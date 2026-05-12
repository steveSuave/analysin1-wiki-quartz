# Factorization of $a^n \pm z^n$

**Summary**: §150–§153: closed-form decomposition of $a^n + z^n$, $a^n - z^n$, and $a^{2n} - 2a^n z^n\cos g + z^{2n}$ into real linear and [[trinomial-factor|trinomial]] factors, with the cosines indexed by equally spaced arcs.

**Sources**: chapter9.pdf

**Last updated**: 2026-04-29

---

## $a^n + z^n$ (§150)

Apply the §148 method (see [[trinomial-factor]]) with $\alpha = a^n$, only $\zeta z^n$ nonzero (coefficient $1$). Setting $r = p/q$, the two real equations become

$$0 = a^n + r^n\cos n\phi,\qquad 0 = r^n\sin n\phi.$$

The second forces $n\phi = k\pi$. Among integer $k$, the value of $\cos n\phi$ is either $+1$ (if $k$ is even, $n\phi = 2k\pi$) or $-1$ (if $k$ is odd, $n\phi = (2k+1)\pi$). The first equation $a^n + r^n\cos n\phi = 0$ requires $\cos n\phi = -1$, hence

$$n\phi = (2k+1)\pi,\qquad \phi = \frac{(2k+1)\pi}{n},\qquad r = a.$$

So $p = a$, $q = 1$, and the trinomial factor of $a^n + z^n$ is

$$\boxed{\;a^2 - 2az\cos\frac{(2k+1)\pi}{n} + z^2\;}$$

Substituting $2k+1 = 1, 3, 5, \ldots$ produces every factor; values past $n$ repeat because $\cos(2\pi \pm \phi) = \cos\phi$ (source: chapter9.pdf, §150).

If $n$ is odd, choosing $2k + 1 = n$ gives $\phi = \pi$ and the factor $a^2 + 2az + z^2 = (a+z)^2$. Take only the square root: $a + z$ is the real linear factor. So

| $n$ | $a^n + z^n$ factors |
|---|---|
| $1$ | $a + z$ |
| $2$ | $a^2 + z^2$ |
| $3$ | $(a + z)(a^2 - 2az\cos(\pi/3) + z^2)$ |
| $4$ | $(a^2 - 2az\cos(\pi/4) + z^2)(a^2 - 2az\cos(3\pi/4) + z^2)$ |
| $5$ | $(a + z)(a^2 - 2az\cos(\pi/5) + z^2)(a^2 - 2az\cos(3\pi/5) + z^2)$ |
| $6$ | $(a^2 - 2az\cos(\pi/6) + z^2)(a^2 - 2az\cos(3\pi/6) + z^2)(a^2 - 2az\cos(5\pi/6) + z^2)$ |

(source: chapter9.pdf, §150 examples).

## $a^n - z^n$ (§151)

The same calculation, but now the first equation $a^n - r^n\cos n\phi = 0$ requires $\cos n\phi = +1$, hence $n\phi = 2k\pi$, $\phi = 2k\pi/n$, $r = a$. The trinomial factor is

$$\boxed{\;a^2 - 2az\cos\frac{2k\pi}{n} + z^2\;}$$

with $2k = 0, 2, 4, \ldots$ up to $n$. At $2k = 0$ the factor degenerates to $a^2 - 2az + z^2 = (a-z)^2$, so $a - z$ is a real linear factor. If $n$ is even, $2k = n$ gives $a^2 + 2az + z^2 = (a+z)^2$, so $a + z$ is also a real linear factor (source: chapter9.pdf, §151).

| $n$ | $a^n - z^n$ factors |
|---|---|
| $1$ | $a - z$ |
| $2$ | $(a - z)(a + z)$ |
| $3$ | $(a - z)(a^2 - 2az\cos(2\pi/3) + z^2)$ |
| $4$ | $(a - z)(a + z)(a^2 - 2az\cos(2\pi/4) + z^2)$ |
| $5$ | $(a - z)(a^2 - 2az\cos(2\pi/5) + z^2)(a^2 - 2az\cos(4\pi/5) + z^2)$ |
| $6$ | $(a - z)(a + z)(a^2 - 2az\cos(2\pi/6) + z^2)(a^2 - 2az\cos(4\pi/6) + z^2)$ |

These tables are the *cyclotomic* factorization, written in terms of cosines rather than primitive roots of unity. Modern notation: the roots of $z^n - a^n = 0$ are $z = a\zeta^k$ with $\zeta = e^{2\pi i/n}$, and $z = a\cos(2k\pi/n) + ia\sin(2k\pi/n)$.

## $a^{2n} - 2a^n z^n\cos g + z^{2n}$ (§152–§153)

This expression — the product of two complex factors $a^n - z^n e^{ig}$ and $a^n - z^n e^{-ig}$ — has no factor of the simple form $\eta + \theta z^n$. Apply §149 with $m = 2n$ to obtain $r = a$ and $\sin 2n\phi = 2\cos g\sin n\phi$, hence $\cos n\phi = \cos g$ and $n\phi = 2k\pi \pm g$. The general trinomial factor is

$$\boxed{\;a^2 - 2az\cos\frac{2k\pi \pm g}{n} + z^2\;}$$

over $2k = 0, 2, 4, \ldots \le n$ (source: chapter9.pdf, §153).

Examples:

- $n = 1$: $a^2 - 2az\cos g + z^2$ has the single factor $a^2 - 2az\cos g + z^2$.
- $n = 2$: $a^4 - 2a^2 z^2\cos g + z^4 = (a^2 - 2az\cos(g/2) + z^2)(a^2 + 2az\cos(g/2) + z^2)$.
- $n = 3$: $a^6 - 2a^3 z^3\cos g + z^6$ splits into three trinomials with arcs $g/3$, $(2\pi - g)/3$, $(2\pi + g)/3$.

The case $g = 0$ recovers $(a^n - z^n)^2$ — square root gives $a^n - z^n$ — and the case $g = \pi$ recovers $(a^n + z^n)^2$ giving $a^n + z^n$. Setting $g = 2\pi k/n$ recovers the §150–§151 results, so this is the master formula.

## Why these matter for what follows

§154 observes that any polynomial in $z^n$ — for instance $\alpha + \beta z^n + \gamma z^{2n}$ — first factors over $\mathbb{R}$ into pieces of the forms just handled, and each piece then splits into trinomials by the formulas above. So **every polynomial admits a constructive factorization into real linear and trinomial factors**, fulfilling the §32 promise (see [[fundamental-theorem-of-algebra]]).

§155 onwards extends the same trick to *infinite series*. Treating $e^x$, $\sin x$, $\cos x$ as polynomials of "infinite degree", Euler applies the §150–§153 formulas with $n$ infinite to obtain the infinite-product expansions of [[sine-infinite-product]], [[cosine-infinite-product]], and [[exponential-infinite-product|the exponential family]].

## Related pages

- [[trinomial-factor]]
- [[factoring-polynomials]]
- [[fundamental-theorem-of-algebra]]
- [[de-moivre-formula]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[exponential-infinite-product]]
- [[chapter-9-on-trinomial-factors]]
