# Cotangent Partial Fraction

**Summary**: §181–§183: combining the [[circular-arc-series|§172/§174 series]] in pairs and substituting $a = m^2/n^2$ yields the partial-fraction expansions $\sum 1/(k^2 - a)$ and $\sum (-1)^{k+1}/(k^2 - a)$ in closed form via $\pi\cot(\pi\sqrt a)$ and $\pi/\sin(\pi\sqrt a)$. The hyperbolic version (§183) treats negative $a$ via $a = -b$ with [[eulers-formula|$e^{\pm\pi\sqrt b}$]].

**Sources**: chapter10

**Last updated**: 2026-04-30

---

## The combination in §181

From [[circular-arc-series|§172]] (alternating, in $m, n$) and [[circular-arc-series|§174]] (alternating, in $m, n$, cot variant), Euler's $P$-formulas give

$$\frac{k\pi}{2n} + \frac{\pi}{2nk} = \frac{(k^2 + 1)\pi}{2nk}\quad\text{with}\quad k = \tan\frac{m\pi}{2n},$$

and using $\sin(m\pi/n) = 2\sin(m\pi/2n)\cos(m\pi/2n)$, $1 + k^2 = 1/\cos^2(m\pi/2n)$:

$$\frac{2k}{1 + k^2} = \sin\frac{m\pi}{n}\quad\Longrightarrow\quad \frac{(k^2 + 1)\pi}{2nk} = \frac{\pi}{n\sin(m\pi/n)}.$$

The two series sums combine to

$$\frac{\pi}{n\sin(m\pi/n)} = \frac{1}{m} + \frac{1}{n - m} - \frac{1}{n + m} - \frac{1}{2n - m} + \frac{1}{2n + m} + \frac{1}{3n - m} - \cdots$$

(source: chapter10, §178). Difference gives

$$\frac{\pi\cos(m\pi/n)}{n\sin(m\pi/n)} = \frac{1}{m} - \frac{1}{n-m} + \frac{1}{n+m} - \frac{1}{2n-m} + \frac{1}{2n+m} - \cdots$$

which Euler describes as "more easily derived through differentiation, which we will do later" (source: chapter10, §178).

## Combining "two by two" — §181

Pairing adjacent terms in the §178 series:

$$\frac{\pi}{n\sin(m\pi/n)} = \frac{1}{m} + \frac{2m}{n^2 - m^2} - \frac{2m}{4n^2 - m^2} + \frac{2m}{9n^2 - m^2} - \frac{2m}{16n^2 - m^2} + \cdots,$$

so

$$\frac{1}{n^2 - m^2} - \frac{1}{4n^2 - m^2} + \frac{1}{9n^2 - m^2} - \cdots = \frac{\pi}{2mn\sin(m\pi/n)} - \frac{1}{2m^2}$$

(source: chapter10, §181). The companion series (cot variant):

$$\frac{1}{n^2 - m^2} + \frac{1}{4n^2 - m^2} + \frac{1}{9n^2 - m^2} + \cdots = \frac{1}{2m^2} - \frac{\pi}{2mn\tan(m\pi/n)}.$$

## §182: the closed form

Substitute $m/n = p$, then $p^2 = a$, multiplying by $n^2$:

$$\boxed{\;\sum_{k=1}^{\infty}\frac{1}{k^2 - a} = \frac{1}{2a} - \frac{\pi}{2\sqrt a\,\tan(\pi\sqrt a)}\;}$$

$$\boxed{\;\sum_{k=1}^{\infty}\frac{(-1)^{k+1}}{k^2 - a} = \frac{\pi}{2\sqrt a\,\sin(\pi\sqrt a)} - \frac{1}{2a}\;}$$

(source: chapter10, §182). "Provided $a$ is not negative nor the square of an integer, then the sum of these series can be represented in terms of the circle" — the reservation being that integer-square values of $a$ create a singularity (the term $1/(k^2 - a)$ with $k = \sqrt a$ blows up).

## Recovery of cot and csc

Rearrange the first formula:

$$\frac{\pi}{\tan(\pi\sqrt a)} = \frac{\sqrt a}{a} - 2\sqrt a\sum_{k=1}^{\infty}\frac{1}{k^2 - a} = \frac{1}{\sqrt a} + 2\sqrt a\sum_{k=1}^{\infty}\frac{1}{a - k^2}.$$

Setting $z = \pi\sqrt a$, so $a = z^2/\pi^2$:

$$\pi\cot z = \frac{1}{z}\cdot\pi^2/\pi^2 \cdot \pi/\sqrt a \cdot \ldots$$

After cleaning up,

$$\pi\cot(\pi z) = \frac{1}{z} + \sum_{k=1}^{\infty}\frac{2z}{z^2 - k^2}.$$

This is the **Mittag-Leffler partial-fraction expansion of cotangent**. Euler is computing it from the right — he uses the [[circular-arc-series|product expansion]] of $\sin$ to evaluate the series, where the modern derivation goes the other way (a cotangent identity → series). Both routes yield the same identity.

Similarly, the csc expansion:

$$\frac{\pi}{\sin(\pi z)} = \frac{1}{z} + \sum_{k=1}^{\infty}\frac{(-1)^k\,2z}{z^2 - k^2}.$$

## §183: hyperbolic version

For negative argument $a = -b$ with $b > 0$, Euler uses [[eulers-formula]]: $\cos(yi) = (e^{-y} + e^y)/2$, $\sin(yi) = (e^{-y} - e^y)/(2i)$. Setting $y = \pi\sqrt b$, so $\sqrt a = i\sqrt b$:

$$\sin(\pi\sqrt{-b}) = \sin(i\pi\sqrt b) = \frac{e^{-\pi\sqrt b} - e^{\pi\sqrt b}}{2i},\qquad \cos(\pi\sqrt{-b}) = \frac{e^{-\pi\sqrt b} + e^{\pi\sqrt b}}{2},$$

hence

$$\tan(\pi\sqrt{-b}) = \frac{e^{-\pi\sqrt b} - e^{\pi\sqrt b}}{(e^{-\pi\sqrt b} + e^{\pi\sqrt b})\,i}.$$

Substituting into the §182 formulas with $a = -b$:

$$\sum_{k=1}^{\infty}\frac{1}{k^2 + b} = \frac{(e^{\pi\sqrt b} + e^{-\pi\sqrt b})\,\pi\sqrt b}{2b\,(e^{\pi\sqrt b} - e^{-\pi\sqrt b})} - \frac{1}{2b},$$

$$\sum_{k=1}^{\infty}\frac{(-1)^{k+1}}{k^2 + b} = \frac{1}{2b} - \frac{\pi\sqrt b}{(e^{\pi\sqrt b} - e^{-\pi\sqrt b})\,b}$$

(source: chapter10, §183). In modern hyperbolic notation:

$$\boxed{\;\sum_{k=1}^{\infty}\frac{1}{k^2 + b} = \frac{\pi\sqrt b\,\coth(\pi\sqrt b)}{2b} - \frac{1}{2b}\;}$$

$$\boxed{\;\sum_{k=1}^{\infty}\frac{(-1)^{k+1}}{k^2 + b} = \frac{1}{2b} - \frac{\pi\sqrt b}{2b\,\sinh(\pi\sqrt b)}\;}$$

This is the partial-fraction expansion of $\coth$ and $\text{csch}$, dual to the trigonometric versions above.

Euler comments: "These same series can be derived from section 162, using the same method which was used in this chapter. However, I have preferred to treat it in this way, since it is a nice illustration of the reduction of sines and cosines of complex arcs to real exponentials" (source: chapter10, §183) — i.e. he is showcasing the unifying power of [[eulers-formula]].

## A worked example

For $b = 1$:

$$\sum_{k=1}^{\infty}\frac{1}{k^2 + 1} = \frac{\pi\,\coth\pi}{2} - \frac{1}{2} \approx 1.0767195\ldots$$

For $a = 1/4$ (i.e. $\sqrt a = 1/2$):

$$\sum_{k=1}^{\infty}\frac{1}{k^2 - 1/4} = 2 - \frac{\pi}{\tan(\pi/2)} = 2 - 0 = 2,$$

which can be checked directly from $\sum 1/(k - 1/2)(k + 1/2) = \sum [1/(k - 1/2) - 1/(k + 1/2)] = 2/1 = 2$ (telescoping after extracting the leading term).

## Why this matters

The §181–§183 results are the first explicit **partial-fraction expansions of meromorphic functions** in mathematics. Each formula expresses a transcendental function as a sum over its poles, with the residue at each pole given by the coefficient of the corresponding $1/(z - z_k)$ term. The general principle — every meromorphic function decomposes as the sum of its principal parts plus a holomorphic remainder — became Mittag-Leffler's theorem more than a century later (1884).

Euler's specific formulas

$$\pi\cot(\pi z) = \frac{1}{z} + 2z\sum_{k=1}^{\infty}\frac{1}{z^2 - k^2},\qquad \frac{\pi}{\sin(\pi z)} = \frac{1}{z} + 2z\sum_{k=1}^{\infty}\frac{(-1)^k}{z^2 - k^2}$$

are still the canonical examples taught in every complex analysis course, and they remain the principal route by which Bernoulli numbers, the Riemann zeta function at even integers, and the functional equation $\zeta(s) = \zeta(1-s)\cdot(\text{factor})$ are linked.

## Finite analogue in Chapter 14

Chapter 14 (§237, §246–§256) derives the *finite*-$n$ counterparts of these formulas. For example, $n\cot nz = \cot z + \cot(\pi/n + z) + \cot(2\pi/n + z) + \cdots$ (sum of $n$ cotangents), and $n/\sin nz$ as a sum of $n$ cosecants. As $n \to \infty$ with $nz$ fixed these finite sums limit to the §181–§183 infinite partial-fraction expansions. See [[trig-multiple-angle-partial-fractions]].

## Related pages

- [[circular-arc-series]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[newtons-identities]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[exponential-infinite-product]]
- [[eulers-formula]]
- [[log-sine-via-products]]
- [[trig-infinite-products]]
- [[trig-multiple-angle-partial-fractions]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
