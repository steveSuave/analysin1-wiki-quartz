# Chapter 9: On Trinomial Factors

**Summary**: Euler develops a constructive method for finding the real quadratic ([[trinomial-factor|"trinomial"]]) factors of any polynomial, then extends the method from polynomials to power series. Applied to $e^z$, $\sin z$, $\cos z$, the technique yields the first infinite-product representations of analytic functions: the [[sine-infinite-product|sine product]], the [[cosine-infinite-product|cosine product]], and the [[exponential-infinite-product|exponential family]]. These products drive [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series|Chapter 10's]] [[basel-problem|Basel solution]] and the [[zeta-at-even-integers|family of even-zeta values]].

**Sources**: chapter9.pdf

**Last updated**: 2026-04-29

---

## Overview

Chapter 2 promised that every real polynomial decomposes into real linear and real quadratic factors (the [[fundamental-theorem-of-algebra]]) but gave no algorithm. Chapter 9 supplies one — and then notices that the algorithm survives a passage to "polynomials of infinite degree", producing a new representation theory for transcendental functions.

The chapter has three movements:

1. **§143–§154 — the trinomial factorization theorem.** Find the *real quadratic* factors of a polynomial directly, in the canonical form $p^2 - 2pqz\cos\phi + q^2z^2$ (a [[trinomial-factor|trinomial factor]]). Using [[de-moivre-formula|De Moivre]], the factor condition splits into two real equations in the unknowns $r = p/q$ and $\phi$. Applied to $a^n + z^n$ and $a^n - z^n$, the method produces the closed-form cyclotomic factorization indexed by equally spaced cosines (see [[factorization-of-an-plus-minus-zn]]).
2. **§155–§158 — infinite products for the elementary transcendentals.** Treat $e^z = (1 + z/j)^j$ as a degree-$j$ polynomial with $j$ infinite, apply the Step-1 formulas, and pass to the limit. The result: infinite-product expansions for $e^x - 1$, $(e^x - e^{-x})/2$, $(e^x + e^{-x})/2$ (see [[exponential-infinite-product]]). Substituting $x = iz$ via [[eulers-formula]] gives the [[sine-infinite-product|sine]] and [[cosine-infinite-product|cosine]] infinite products.
3. **§159–§164 — generalization to $e^z - 2\cos g + e^{-z}$ and circular reformulations.** The same recipe applied to a parametrized "binomial-of-binomials" produces a family of infinite products for $(\cos v + \cos g)/(1 + \cos g)$, $(\cos v - \cos g)/(1 - \cos g)$, $(\sin g + \sin v)/\sin g$, and a fourth variant — collectively the four formulas of §163, plus their circular-arc reformulations in §164.

See also: [[trinomial-factor]], [[factorization-of-an-plus-minus-zn]], [[exponential-infinite-product]], [[sine-infinite-product]], [[cosine-infinite-product]].

## Structure of the chapter

### §143–§144 — Why trinomial factors

A linear factor $p - qz$ of a polynomial $\alpha + \beta z + \gamma z^2 + \cdots$ corresponds to a root $z = p/q$. Real linear factors are easy in principle (solve the equation); the difficulty is the *complex* roots. Since complex roots come in conjugate pairs (see [[complex-conjugate-factors]]), their product is a real quadratic. Euler's strategy: search for the real quadratic factor directly, in a parametrization that exposes the discriminant condition.

### §145 — The canonical form

A real quadratic $p - qz + rz^2$ has complex linear factors when $4pr > q^2$, i.e. $q/(2\sqrt{pr}) < 1$. Set $q/(2\sqrt{pr}) = \cos\phi$ for some real arc $\phi$, absorb $\sqrt{pr}$ into the names $p, q$, and the factor takes the canonical form

$$p^2 - 2pqz\cos\phi + q^2z^2,$$

with complex linear factors $qz - p(\cos\phi \pm i\sin\phi)$. When $\cos\phi = \pm 1$ the two linear factors coincide and are real. See [[trinomial-factor]].

### §146–§149 — Two real equations for $r$ and $\phi$

If the canonical trinomial divides a polynomial $\alpha + \beta z + \gamma z^2 + \cdots$, then the polynomial vanishes at $z = (p/q)(\cos\phi \pm i\sin\phi)$. Substitute, use [[de-moivre-formula]] $z^n = r^n(\cos n\phi \pm i\sin n\phi)$ where $r = p/q$, separate real and imaginary parts, and obtain

$$0 = \alpha + \beta r\cos\phi + \gamma r^2\cos 2\phi + \delta r^3\cos 3\phi + \cdots,$$

$$0 = \beta r\sin\phi + \gamma r^2\sin 2\phi + \delta r^3\sin 3\phi + \cdots.$$

(source: chapter9.pdf, §148). Two real equations, two unknowns. §149 gives a slick generalization: multiplying by $\cos m\phi$ and $\sin m\phi$ before adding produces the family

$$0 = \alpha\cos m\phi + \beta r\cos(m \mp 1)\phi + \gamma r^2\cos(m \mp 2)\phi + \cdots,$$

any pair of which determines $r$ and $\phi$. Multiple solutions yield multiple trinomial factors, and (Euler claims) all of them.

### §150 — Factoring $a^n + z^n$

Apply the §148 method with $\alpha = a^n$ and only $\zeta z^n$ nonzero. The second equation $r^n\sin n\phi = 0$ gives $n\phi = k\pi$, the first then forces $\cos n\phi = -1$, so $n\phi = (2k+1)\pi$ and $r = a$. Trinomial factor:

$$a^2 - 2az\cos\frac{(2k+1)\pi}{n} + z^2.$$

Run $2k + 1$ over odd integers $\le n$. If $n$ is odd, $2k + 1 = n$ produces the perfect square $(a + z)^2$, giving the lone real linear factor $a + z$. See [[factorization-of-an-plus-minus-zn]].

### §151 — Factoring $a^n - z^n$

The same setup, but the first equation now requires $\cos n\phi = +1$, hence $n\phi = 2k\pi$. Trinomial factor:

$$a^2 - 2az\cos\frac{2k\pi}{n} + z^2.$$

$2k = 0$ gives $(a - z)^2$ → real linear factor $a - z$; if $n$ is even, $2k = n$ gives $(a + z)^2$ → real linear factor $a + z$. See [[factorization-of-an-plus-minus-zn]].

### §152–§153 — The master formula

The expression $a^{2n} - 2a^n z^n\cos g + z^{2n}$ has no factor of the form $\eta + \theta z^n$ but is the product of two complex factors $a^n - z^n e^{\pm ig}$. Apply §149 with $m = 2n$ to get $r = a$, $\cos n\phi = \cos g$, hence $n\phi = 2k\pi \pm g$. Trinomial factor:

$$a^2 - 2az\cos\frac{2k\pi \pm g}{n} + z^2.$$

This subsumes §150 ($g = \pi$, after factoring out a square root) and §151 ($g = 0$). See [[factorization-of-an-plus-minus-zn]].

### §154 — Every polynomial admits real factorization

§154 stitches the pieces together. A polynomial $\alpha + \beta z^n + \gamma z^{2n}$ either has two real factors of the form $\eta + \theta z^n$ (each handled by §150–§151) or has none, in which case it is exactly an instance of §153. Polynomials of higher degree in $z^n$ reduce in the same way. Conclusion: "every polynomial can be expressed as a product of real linear and real quadratic factors" — the existence claim of [[fundamental-theorem-of-algebra|§32]] is now constructive, *modulo* finding the cosine arcs.

### §155 — Infinite product for $e^z - 1$

From [[exponential-series|Chapter 7]], $e^z - 1 = (1 + z/j)^j - 1$ for $j$ infinite. Compare with §151 ($a^n - z^n$ at $a = 1 + z/j$, $z = 1$, $n = j$). Each factor $a^2 - 2az\cos(2k\pi/j) + z^2$ becomes, after using $\cos(2k\pi/j) = 1 - 2k^2\pi^2/j^2$ from [[sine-and-cosine-series|§134]] and dropping high-order $j$ terms,

$$\propto 1 + \frac{z}{j} + \frac{z^2}{4k^2\pi^2}.$$

The $k = 0$ factor degenerates to $z^2/j^2$; take the square root $z/j \propto z$. Hence $e^z - 1 = z\prod_{k=1}^\infty(1 + z/j + z^2/(4k^2\pi^2))$ — but the $z/j$ terms are infinitesimal yet collectively non-negligible (there are $\tfrac12 j$ of them, contributing $z/2$). Euler resolves this in §156.

### §156 — Infinite product for $(e^x - e^{-x})/2$

Now compare $(1 + x/j)^j - (1 - x/j)^j$ (which by binomial is $2(x + x^3/3! + x^5/5! + \cdots) = e^x - e^{-x}$) with §151 at $a = 1 + x/j$, $z = 1 - x/j$, $n = j$. Each factor cleans up to $1 + x^2/(k^2\pi^2)$ (no troublesome $x/j$ remainder), and the $k = 0$ factor square-roots to $x$:

$$\frac{e^x - e^{-x}}{2} = x\prod_{k=1}^{\infty}\left(1 + \frac{x^2}{k^2\pi^2}\right).$$

See [[exponential-infinite-product]].

### §157 — Infinite product for $(e^x + e^{-x})/2$

Same setup with §150 ($a^n + z^n$): each factor has arc $(2k+1)\pi/j$, and after simplification,

$$\frac{e^x + e^{-x}}{2} = \prod_{k=0}^{\infty}\left(1 + \frac{4x^2}{(2k+1)^2\pi^2}\right).$$

See [[exponential-infinite-product]].

### §158 — Sine and cosine infinite products

Substitute $x = iz$ into §156 and §157, using [[eulers-formula]] $(e^{iz} - e^{-iz})/(2i) = \sin z$ and $(e^{iz} + e^{-iz})/2 = \cos z$:

$$\sin z = z\prod_{k=1}^{\infty}\left(1 - \frac{z^2}{k^2\pi^2}\right),$$

$$\cos z = \prod_{k=0}^{\infty}\left(1 - \frac{4z^2}{(2k+1)^2\pi^2}\right).$$

The zeros of $\sin z$ ($z = k\pi$) and $\cos z$ ($z = (2k+1)\pi/2$) appear directly as the roots of the respective factors. See [[sine-infinite-product]] and [[cosine-infinite-product]].

### §159–§163 — The $e^z - 2\cos g + e^{-z}$ family

Apply §152 to $(1 + x/j)^j - 2\cos g + (1 - x/j)^j$ with $2n = j$, after which the factor takes the form $(2k\pi \pm g)$ in the cosine. Cleaning up:

$$\frac{e^x - 2\cos g + e^{-x}}{2(1 - \cos g)} = \prod_{k=1}^{\infty}\left(1 + \frac{x^2}{(2k\pi - g)^2}\right)\left(1 + \frac{x^2}{(2k\pi + g)^2}\right)\cdot\left(1 + \frac{x^2}{g^2}\right).$$

(source: chapter9.pdf, §159, with the convention that $k$ runs from $0$ for the trailing factor). Substituting $zi$ for $x$ converts this into

$$\frac{\cos z - \cos g}{1 - \cos g} = \left(1 - \frac{z}{g}\right)\left(1 + \frac{z}{g}\right)\left(1 - \frac{z}{2\pi - g}\right)\left(1 + \frac{z}{2\pi - g}\right)\cdots,$$

which, in the limit $g \to 0$, recovers the [[cosine-infinite-product]] (after some bookkeeping). §160–§162 specialize the parameters; §163 collects four formulas:

$$\frac{\cos v + \cos g}{1 + \cos g},\quad \frac{\cos v - \cos g}{1 - \cos g},\quad \frac{\sin g + \sin v}{\sin g},\quad \frac{\sin g - \sin v}{\sin g}$$

each as an explicit infinite product in $v$ (with $g$ a parameter). The systematic catalog establishes that the trinomial-factor technique is general — every elementary trig combination has an infinite product expansion.

### §164 — Reformulation using arcs

The same expressions written in terms of $\cos z + \tan(g/2)\sin z$, $\cos(z) - \cot(g/2)\sin z$, etc. The point is that if $b$ and $c$ in the §161 formulas are interpreted as $b = 0$, $c = ig$, then $e^c \pm e^{-c} = 2\cos g$, $\pm 2i\sin g$ — and the abstract identities of §161 become circular-trigonometric statements (source: chapter9.pdf, §164). Euler closes: "The law of formation for these factors is sufficiently simple and uniform."

## Notable points

- **The trinomial form encodes polar coordinates.** $p^2 - 2pqz\cos\phi + q^2z^2$ is exactly $(qz - p e^{i\phi})(qz - p e^{-i\phi})$, with $p/q$ playing the role of the modulus and $\phi$ the argument of the complex root. Euler does not invoke $e^{i\phi}$ here, but the polar form is implicit.
- **The §148 system is De Moivre in disguise.** The two real equations are the real and imaginary parts of a single complex equation $\sum c_n r^n e^{in\phi} = 0$. Euler is doing complex analysis without writing complex exponentials, decades before the conceptual machinery existed.
- **The cyclotomic factorization predates the term.** §150–§151 are the modern factorizations of $z^n - a^n$ over $\mathbb{R}$, indexed by primitive roots of unity. Gauss's *Disquisitiones* (1801), where the term *cyclotomic* arises, is half a century later.
- **Infinite products are the dual representation to power series.** A power series captures local behavior at $0$; an infinite product captures global zero structure. Euler is the first to systematically exploit both.
- **The sine product is the precursor of Weierstrass factorization.** Modern complex analysis recovers Euler's formula as the canonical product representation of an entire function of order 1, with explicit elementary factors and a genus-1 exponential. Euler's manipulation, free of any convergence theory, hits the right answer because $\sin z/z$ has order exactly $1$ and no genus-1 correction is needed.
- **The Basel problem is one comparison away.** Equating $z^3$ coefficients in $\sin z = z - z^3/6 + \cdots$ and $\sin z = z\prod(1 - z^2/k^2\pi^2)$ gives $\sum 1/k^2 = \pi^2/6$. Euler does the comparison in [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series|Chapter 10]] (see [[basel-problem]]).

## Why this chapter matters

Chapter 9 is where Euler turns *factorization* — a tool for polynomials — into a representation theory for transcendentals. The constructive solution of [[fundamental-theorem-of-algebra|the §32 problem]] is satisfying on its own, but the real prize is the second movement: $\sin z$, $\cos z$, $e^x \pm e^{-x}$ all become products. Each product is a list of zeros; each zero is a piece of geometric or algebraic data. Comparing product expansions to power-series expansions (Chapter 10) instantly evaluates infinite sums that resisted Bernoulli, Leibniz, and the entire mathematical world for a generation.

The technique extends much further than Chapter 9 demonstrates. Euler will use the same products to construct the partial-fraction expansions of $\cot z$, $\tan z$, $\csc z$, and to derive the entire family of even-zeta values $\zeta(2), \zeta(4), \zeta(6), \ldots$. The shape of nineteenth-century complex analysis — Mittag-Leffler, Hadamard, Weierstrass — is laid out here in embryo.

## Related pages

- [[trinomial-factor]]
- [[factorization-of-an-plus-minus-zn]]
- [[exponential-infinite-product]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[de-moivre-formula]]
- [[eulers-formula]]
- [[sine-and-cosine-series]]
- [[exponential-series]]
- [[factoring-polynomials]]
- [[complex-conjugate-factors]]
- [[fundamental-theorem-of-algebra]]
- [[chapter-2-on-the-transformation-of-functions]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[newtons-identities]]
- [[circular-arc-series]]
- [[cotangent-partial-fraction]]
