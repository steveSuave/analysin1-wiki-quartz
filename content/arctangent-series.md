# The Arctangent Series

**Summary**: §139–§141 of Chapter 8. Inverting [[eulers-formula|Euler's formula]] gives $z = \frac{1}{2i}\log\frac{\cos z + i\sin z}{\cos z - i\sin z}$, which simplifies via $\tan z = \sin z/\cos z$ to $z = \frac{1}{2i}\log\frac{1 + i\tan z}{1 - i\tan z}$. Substituting $x = i\tan z$ in the [[logarithmic-series|fast-converging logarithmic series]] of Chapter 7 yields

$$\arctan t = \frac{t}{1} - \frac{t^3}{3} + \frac{t^5}{5} - \frac{t^7}{7} + \cdots.$$

At $t = 1$ this is Leibniz's $\pi/4 = 1 - 1/3 + 1/5 - \cdots$. At $t = 1/\sqrt 3$ it becomes $\pi/6 = (1/\sqrt 3)(1 - 1/(3\cdot 3) + 1/(5\cdot 9) - \cdots)$, converging at geometric rate.

**Sources**: chapter8 (§139, §140, §141)

**Last updated**: 2026-05-11

---

## §139 — The arc as a complex logarithm

Take [[eulers-formula|§138]]: $\cos z + i\sin z = e^{iz}$ and $\cos z - i\sin z = e^{-iz}$. Their ratio is $e^{2iz}$, so

$$\log\frac{\cos z + i\sin z}{\cos z - i\sin z} = 2iz,\qquad z = \frac{1}{2i}\log\frac{\cos z + i\sin z}{\cos z - i\sin z}.$$

Euler arrives at this formula not via §138 (which he derives independently a few sections earlier) but via a parallel infinitesimal/infinite calculation: with $n = 1/j$ infinitely small, $\cos(z/j) = 1$ and $\sin(z/j) = z/j$, then using $\log(1+x) = j((1+x)^{1/j} - 1)$ from [[logarithmic-series|§125]] with $1 + x = \cos z + i\sin z$ and $\cos z - i\sin z$ in turn (source: chapter8, §139). The cosine equation collapses to a tautology; the sine equation yields the boxed formula above.

The interpretation: every arc $z$ is the imaginary part (up to the $1/2i$ prefactor) of a complex logarithm. This anticipates the full theory of complex logarithms — the multivaluedness, the branch cuts — but Euler stays within a real-valued reading here.

## §140 — Substituting tangent

Divide numerator and denominator inside the logarithm by $\cos z$:

$$\frac{\cos z + i\sin z}{\cos z - i\sin z} = \frac{1 + i\tan z}{1 - i\tan z},$$

so

$$z = \frac{1}{2i}\log\frac{1 + i\tan z}{1 - i\tan z}.$$

But the §123 series gives

$$\log\frac{1 + x}{1 - x} = \frac{2x}{1} + \frac{2x^3}{3} + \frac{2x^5}{5} + \frac{2x^7}{7} + \cdots,$$

so substituting $x = i\tan z$:

$$\log\frac{1 + i\tan z}{1 - i\tan z} = 2i\tan z + \frac{2i^3(\tan z)^3}{3} + \frac{2i^5(\tan z)^5}{5} + \cdots.$$

Using $i^3 = -i$, $i^5 = i$, $i^7 = -i$, $\ldots$:

$$\log\frac{1 + i\tan z}{1 - i\tan z} = 2i\left(\tan z - \frac{(\tan z)^3}{3} + \frac{(\tan z)^5}{5} - \cdots\right).$$

Dividing by $2i$:

$$z = \tan z - \frac{(\tan z)^3}{3} + \frac{(\tan z)^5}{5} - \frac{(\tan z)^7}{7} + \cdots.$$

(source: chapter8, §140). Setting $t = \tan z$, so $z = \arctan t$:

$$\boxed{\;\arctan t = \frac{t}{1} - \frac{t^3}{3} + \frac{t^5}{5} - \frac{t^7}{7} + \frac{t^9}{9} - \cdots\;}$$

The series converges for $|t| \le 1$ (an observation Euler does not formalize but uses).

## §140 — Leibniz's $\pi/4$

At $t = 1$, the arc whose tangent is 1 is $\pi/4$, so

$$\frac{\pi}{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \frac{1}{9} - \cdots.$$

(source: chapter8, §140). Euler attributes this discovery to Leibniz. This series gives $\pi$ in closed form as an alternating sum of reciprocal odd integers — beautiful, but practically useless for computation: each correct decimal digit costs about ten new terms.

[[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series|Chapter 10]] re-derives Leibniz's formula as a special case of a vast family of [[circular-arc-series|character-style series]] obtained by applying [[newtons-identities|Newton's identities]] to the [[chapter-9-on-trinomial-factors|§164 arc-form products]]. [[chapter-15-on-series-which-arise-from-products|Chapter 15]] then sieves Leibniz's series by primes to obtain the [[euler-product-formula|Euler-product form]] $\pi/4 = \prod_p p/(p\mp 1)$ — a Dirichlet $L$-function in disguise (see [[prime-sign-series-for-pi]]). [[chapter-18-on-continued-fractions|Chapter 18]] converts Leibniz's series to [[brouncker-formula|Brouncker's continued fraction]] $4/\pi = 1 + 1^2/(2 + 3^2/(2 + 5^2/(2 + \cdots)))$ via the §369 reciprocal-series template.

## §141 — A faster series via $\arctan(1/\sqrt 3)$

For practical $\pi$ computation, choose $t < 1$ to get geometric-rate convergence. Try $t = 1/\sqrt 3$, the tangent of $\pi/6$:

$$\frac{\pi}{6} = \frac{1}{\sqrt 3} - \frac{1}{3\cdot 3\sqrt 3} + \frac{1}{5\cdot 3^2\sqrt 3} - \frac{1}{7\cdot 3^3\sqrt 3} + \cdots,$$

i.e.

$$\pi = \frac{2\sqrt 3}{1} - \frac{2\sqrt 3}{3\cdot 3} + \frac{2\sqrt 3}{5\cdot 3^2} - \frac{2\sqrt 3}{7\cdot 3^3} + \cdots.$$

(source: chapter8, §141). Each term is about a third of the previous, so a dozen terms give roughly six correct digits. Euler comments: "By means of this series the value of $\pi$ itself, which was previously exhibited, was determined with incredible labor" — the prior 113-digit decimal of [[pi|§126]] was computed exactly this way.

§141 first considers $t = 1/10$, which converges spectacularly fast but does not correspond to any "nice" fraction of the circumference, so $\pi$ cannot be extracted from $\arctan(1/10)$ alone. The §141 lesson: for a useful arctangent identity, $t$ must be both small (for convergence) and a *known* fraction of $\pi$.

The remaining inconvenience of the §141 series is that every term is irrational ($\sqrt 3$ in the denominator). [[machin-like-formula|§142]] resolves this by splitting $\pi/4$ as a sum of arctangents of rational numbers.

## Why the series exists at all

The arctangent series is *not* derivable by elementary trigonometry. It requires the bridge between trig and exponentials (Euler's formula, §138) plus the logarithmic series of Chapter 7. Without that bridge, the function $\arctan$ is defined only implicitly, and there is no algebraic technique in pre-Eulerian mathematics for expanding it as a power series.

After Euler, the series is in some sense *trivial*: it is just $\log\frac{1 + i\tan z}{1 - i\tan z}$ divided by $2i$, expanded by the standard logarithm series, with $i\tan z$ in place of $x$. The whole derivation is two lines once §138–§140 are accepted.

## Convergence rate at a glance

| $t$ | Arc | Series | Terms for 6 digits |
|:--|:--|:--|:--|
| $1$ | $\pi/4$ | $1 - 1/3 + 1/5 - \cdots$ | ~$10^6$ |
| $1/\sqrt 3$ | $\pi/6$ | $(1/\sqrt 3)(1 - 1/9 + 1/(5\cdot 9) - \cdots)$ | ~13 |
| $1/2$ | $\arctan(1/2) \approx 26.57°$ | $1/2 - 1/(3\cdot 8) + 1/(5\cdot 32) - \cdots$ | ~10 |
| $1/3$ | $\arctan(1/3) \approx 18.43°$ | $1/3 - 1/81 + 1/(5\cdot 243) - \cdots$ | ~6 |

The §142 [[machin-like-formula|Machin decomposition]] uses the last two rows.

## Related pages

- [[eulers-formula]]
- [[logarithmic-series]]
- [[de-moivre-formula]]
- [[sine-and-cosine-series]]
- [[machin-like-formula]]
- [[pi]]
- [[circular-arc-series]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[chapter-15-on-series-which-arise-from-products]]
- [[euler-product-formula]]
- [[prime-sign-series-for-pi]]
- [[brouncker-formula]] — Leibniz's $\pi/4$ converted to a continued fraction in chapter 18
- [[chapter-18-on-continued-fractions]]
