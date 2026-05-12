# Exponential Infinite Products

**Summary**: §155–§157: applying the [[factorization-of-an-plus-minus-zn|§151 cyclotomic formula]] to $(1 + z/j)^j = e^z$ with $j$ infinite gives infinite-product expansions for $e^x - 1$, $(e^x - e^{-x})/2$, and $(e^x + e^{-x})/2$.

**Sources**: chapter9

**Last updated**: 2026-04-29

---

## $e^x - 1$ (§155–§156)

From [[exponential-series|Chapter 7]], $e^x = (1 + x/j)^j$ with $j$ infinitely large, so

$$e^x - 1 = (1 + x/j)^j - 1.$$

Compare with the §151 form for $a^n - z^n$ at $a = 1 + x/j$, $n = j$, $z = 1$. Each trinomial factor has the form

$$(1 + x/j)^2 - 2(1 + x/j)\cos\frac{2k\pi}{j} + 1.$$

For $k = 0$ this is the square $(x/j)^2$; take its square root, giving the linear factor $x/j$, i.e. simply $x$ once we pull out the constant.

For $k \ne 0$: since $j$ is infinite the arc $2k\pi/j$ is infinitesimal, so by [[sine-and-cosine-series|§134]] $\cos(2k\pi/j) = 1 - 2k^2\pi^2/j^2$. Substituting, expanding $(1 + x/j)^2$, and dropping terms with $j^3$ or higher in the denominator, each factor is

$$\frac{x^2}{j^2} + \frac{4k^2}{j^2}\pi^2 + \frac{4k^2}{j^3}\pi^2 x = \frac{4k^2\pi^2}{j^2}\left(1 + \frac{x}{j} + \frac{x^2}{4k^2\pi^2}\right).$$

Discarding the multiplicative constants (they get absorbed into the leading factor of $e^x - 1$, which is $x$), Euler obtains

$$e^x - 1 = x\left(1 + \frac{x}{1\cdot 2} + \frac{x^2}{1\cdot 2\cdot 3} + \cdots\right) = x\left(1 + \frac{x}{j} + \frac{x^2}{4\pi^2}\right)\left(1 + \frac{x}{j} + \frac{x^2}{16\pi^2}\right)\left(1 + \frac{x}{j} + \frac{x^2}{36\pi^2}\right)\cdots$$

(source: chapter9, §155). The infinitesimal $x/j$ in each factor is necessary: there are $\tfrac12 j$ factors and discarding it would lose a finite total $x/2$. Euler will eliminate this nuisance by combining $e^x - 1$ with $1 - e^{-x}$.

## $(e^x - e^{-x})/2$ — the sine–hyperbolic product (§156)

Compute $e^x - e^{-x} = (1 + x/j)^j - (1 - x/j)^j = 2(x + x^3/3! + x^5/5! + \cdots)$. Now compare with §151 for $a = 1 + x/j$, $z = 1 - x/j$, $n = j$. Each factor has the form

$$a^2 - 2az\cos\frac{2k\pi}{j} + z^2 = \frac{4x^2}{j^2} + \frac{4k^2\pi^2}{j^2} - \frac{4k^2\pi^2 x^2}{j^4}.$$

Drop the term with $j^4$ in the denominator; the resulting factor is proportional to $1 + x^2/(k^2\pi^2)$. The $k = 0$ factor, after square-rooting, contributes $x$ (not $2x$, because the square root of the *constant* leading term gets folded into the overall normalization). So

$$\boxed{\;\frac{e^x - e^{-x}}{2} = x\prod_{k=1}^{\infty}\left(1 + \frac{x^2}{k^2\pi^2}\right) = x\left(1 + \frac{x^2}{\pi^2}\right)\left(1 + \frac{x^2}{4\pi^2}\right)\left(1 + \frac{x^2}{9\pi^2}\right)\cdots\;}$$

(source: chapter9, §156). The series side is $x + x^3/3! + x^5/5! + \cdots$, that is $\sinh x$.

## $(e^x + e^{-x})/2$ — the cosine–hyperbolic product (§157)

$e^x + e^{-x} = (1 + x/j)^j + (1 - x/j)^j = 2(1 + x^2/2! + x^4/4! + \cdots)$. Use the §150 form for $a^n + z^n$ with the same $a, z$. Each factor has arc $(2k+1)\pi/n$:

$$a^2 - 2az\cos\frac{(2k+1)\pi}{j} + z^2 = \frac{4x^2}{j^2} + \frac{(2k+1)^2\pi^2}{j^2} - \cdots.$$

Cleaning up gives factor $1 + 4x^2/((2k+1)^2\pi^2)$. There is no exceptional $k = 0$ term to square-root; instead $2k + 1$ runs over all positive odd integers:

$$\boxed{\;\frac{e^x + e^{-x}}{2} = \prod_{k=0}^{\infty}\left(1 + \frac{4x^2}{(2k+1)^2\pi^2}\right) = \left(1 + \frac{4x^2}{\pi^2}\right)\left(1 + \frac{4x^2}{9\pi^2}\right)\left(1 + \frac{4x^2}{25\pi^2}\right)\cdots\;}$$

(source: chapter9, §157). The series side is $1 + x^2/2! + x^4/4! + \cdots = \cosh x$.

## What §158 does next

Substitute $x = iz$ into the boxed formulas: $(e^{iz} - e^{-iz})/(2i) = \sin z$ and $(e^{iz} + e^{-iz})/2 = \cos z$ from [[eulers-formula]]. The factor $1 + x^2/(k^2\pi^2)$ becomes $1 - z^2/(k^2\pi^2)$, and the products turn into the **infinite products for $\sin z$ and $\cos z$**. See [[sine-infinite-product]] and [[cosine-infinite-product]].

## Why this is striking

These formulas are the first appearance in mathematics of an *infinite product representation* of an analytic function. They are not power series — they encode the *zeros* of the function. $\sin z$ vanishes at $z = k\pi$, and the product makes this transparent: each factor $(1 - z^2/k^2\pi^2)$ vanishes at $z = \pm k\pi$. Likewise $\cosh x$ has no real zeros (every factor $1 + 4x^2/((2k+1)^2\pi^2)$ is positive), reflecting that $\cosh x \ge 1$ for real $x$.

Euler exploits these products in [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series|Chapter 10]] to evaluate $\sum 1/k^2 = \pi^2/6$ and the [[zeta-at-even-integers|Basel-family sums]]. The bridge is [[newtons-identities|Newton's identities]] applied to the "infinite polynomial" $\sin z/z = \prod(1 - z^2/k^2\pi^2)$.

## §159–§164 — generalizations

Sections 159–164 repeat the recipe with the more general $e^x - 2\cos g + e^{-x}$ in place of $e^x \pm e^{-x}$, producing infinite products for $(\cos v + \cos g)/(1 + \cos g)$, $(\cos v - \cos g)/(1 - \cos g)$, $(\sin g + \sin v)/\sin g$, and a fourth variant. They are mostly catalog material — the master technique is what matters.

## Related pages

- [[trinomial-factor]]
- [[factorization-of-an-plus-minus-zn]]
- [[exponential-series]]
- [[infinitesimal-and-infinite-numbers]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[eulers-formula]]
- [[newtons-identities]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
