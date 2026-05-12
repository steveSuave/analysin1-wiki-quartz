# Chapter 11: On Other Infinite Expressions for Arcs and Sines

**Summary**: Euler reworks the [[sine-infinite-product|§158]] sine and cosine products at rational angles $z = m\pi/(2n)$, splitting each quadratic factor into two linear factors. The §158 quadratic-factor products thus become four linear-factor products — two each for sine and cosine. Comparing them yields the [[wallis-product|Wallis product]] for $\pi/2$ (§185); their quotients give [[trig-infinite-products|infinite products for tan, cot, sec, csc]] (§186). Taking logarithms and applying the [[logarithmic-series|§118 series]] $\log(1 - x) = -x - x^2/2 - \cdots$ converts these products into double sums whose columns are the already-known [[zeta-at-even-integers|even-zeta values]]. The result is rapidly convergent series for [[log-pi-via-products|$\log\pi$]] (§188–§190) and for [[log-sine-via-products|$\log\sin$, $\log\cos$, $\log\tan$, $\log\cot$]] (§191–§198) — the practical engine that made Euler's logarithm tables for trigonometric functions feasible.

**Sources**: chapter11.pdf

**Last updated**: 2026-05-01

---

## Overview

Chapter 9 produced infinite products for $\sin z$ and $\cos z$ as quadratic factors $(1 - z^2/k^2\pi^2)$. Chapter 10 expanded those products and matched coefficients to compute zeta values. Chapter 11 takes a different turn: it specializes the products to rational arguments $z = m\pi/(2n)$, where each quadratic factor $1 - m^2/(kn)^2$ splits as $((kn-m)/kn)\cdot((kn+m)/kn)$ over the rationals. The two factors per quadratic, paired with the co-function identity $\sin((n-m)\pi/2n) = \cos(m\pi/2n)$, give *two* infinite product representations for each of $\sin(m\pi/2n)$ and $\cos(m\pi/2n)$.

Two product expressions for the same value give a third by quotient. Three things follow:

1. **[[wallis-product|The Wallis product]]** — dividing the two expressions for $\cos(m\pi/2n)$ (or for $\sin(m\pi/2n)$) gives $1 = (\pi/2)\cdot(1/2)\cdot(3/2)\cdot(3/4)\cdot(5/4)\cdots$, hence $\pi/2 = (2\cdot 2\cdot 4\cdot 4\cdot 6\cdot 6\cdots)/(1\cdot 3\cdot 3\cdot 5\cdot 5\cdot 7\cdots)$ (§185). Special choices of $m/n$ give analogous products for $\sqrt 2$ etc.

2. **[[trig-infinite-products|Products for the other trig functions]]** — quotients of the §184 products yield infinite linear-factor representations for $\tan$, $\cot$, $\sec$, $\csc$ (§186); replacing $m$ with another integer $k$ in the formulas gives products for the *ratios* $\sin(m\pi/2n)/\sin(k\pi/2n)$, etc. (§187).

3. **Logarithms of $\pi$ and of the trig functions** — the products are bad for computing $\pi$ directly (convergence is geometric in $1/k^2$, so each correct decimal digit costs many factors), but they are excellent for computing the *logarithm* of $\pi$ or of $\sin(m\pi/2n)$ etc. The trick: take the log, expand each $\log(1 - 1/(2k+1)^2)$ or $\log(1 - m^2/k^2 n^2)$ as a power series via [[logarithmic-series|§118]], and transpose the double sum. The columns of the transposed sum are the already-tabulated [[zeta-at-even-integers|odd-square sums $A = \pi^2/8$, $B = \pi^4/96$, …]] and even-integer-reciprocal sums $\alpha = \pi^2/24$, $\beta = \pi^4/1440$, …. Each column converges absurdly fast, giving 15+ digit precision in a handful of terms (§188–§196).

The chapter closes (§197–§198) with a *faster* route to $\tan$ and $\cot$ via the [[cotangent-partial-fraction|§181 partial fractions]] $\sum 1/(k^2 - m^2/n^2)$, which avoids the long division of two sine/cosine series and is the method Euler actually used to prepare trig log tables.

## Structure of the chapter

### §184 — Linear factors

The §158 products

$$\sin z = z\prod_{k=1}^{\infty}\left(1 - \frac{z^2}{k^2\pi^2}\right),\qquad \cos z = \prod_{k=0}^{\infty}\left(1 - \frac{4z^2}{(2k+1)^2\pi^2}\right),$$

evaluated at $z = m\pi/(2n)$, become products with rational entries $1 - m^2/(2kn)^2$ and $1 - m^2/((2k+1)n)^2$. Factoring each $1 - r^2 = (1-r)(1+r)$:

$$\sin\frac{m\pi}{2n} = \frac{m\pi}{2n}\cdot\frac{2n - m}{2n}\cdot\frac{2n + m}{2n}\cdot\frac{4n - m}{4n}\cdot\frac{4n + m}{4n}\cdot\frac{6n - m}{6n}\cdot\frac{6n + m}{6n}\cdots$$

$$\cos\frac{m\pi}{2n} = \frac{n - m}{n}\cdot\frac{n + m}{n}\cdot\frac{3n - m}{3n}\cdot\frac{3n + m}{3n}\cdot\frac{5n - m}{5n}\cdot\frac{5n + m}{5n}\cdots$$

The co-function identity $\sin((n - m)\pi/2n) = \cos(m\pi/2n)$ — substituting $n - m$ for $m$ in the sine product — gives a second expression for each:

$$\cos\frac{m\pi}{2n} = \frac{(n - m)\pi}{2n}\cdot\frac{n + m}{2n}\cdot\frac{3n - m}{2n}\cdot\frac{3n + m}{4n}\cdot\frac{5n - m}{4n}\cdot\frac{5n + m}{6n}\cdots$$

$$\sin\frac{m\pi}{2n} = \frac{m}{n}\cdot\frac{2n - m}{3n}\cdot\frac{2n + m}{3n}\cdot\frac{4n - m}{5n}\cdot\frac{4n + m}{5n}\cdot\frac{6n - m}{7n}\cdots$$

Two products per function. See [[linear-factors-of-sine-cosine]].

### §185 — Wallis product

Dividing the two cosine expressions (or the two sine expressions) for the same $m\pi/2n$ yields

$$1 = \frac{\pi}{2}\cdot\frac{1}{2}\cdot\frac{3}{2}\cdot\frac{3}{4}\cdot\frac{5}{4}\cdot\frac{5}{6}\cdot\frac{7}{6}\cdot\frac{7}{8}\cdots,$$

hence

$$\frac{\pi}{2} = \frac{2\cdot 2\cdot 4\cdot 4\cdot 6\cdot 6\cdot 8\cdot 8\cdot 10\cdot 10\cdot 12\cdot 12}{1\cdot 3\cdot 3\cdot 5\cdot 5\cdot 7\cdot 7\cdot 9\cdot 9\cdot 11\cdot 11\cdot 13}\cdots,$$

"the expression for $\pi$ which Wallis found in his *Arithmetic of the Infinite*" (source: chapter11.pdf, §185). Other choices of $m/n$ produce variants:

- $m/n = 1/2$, $\sin(\pi/4) = 1/\sqrt 2$: $\pi/2 = (\sqrt 2/1)\cdot(4/3)\cdot(4/5)\cdot(8/7)\cdot(8/9)\cdot(12/11)\cdot(12/13)\cdots$
- $m/n = 1/3$, $\sin(\pi/6) = 1/2$: $\pi/2 = (3/2)\cdot(6/5)\cdot(6/7)\cdot(12/11)\cdot(12/13)\cdot(18/17)\cdot(18/19)\cdots$
- Dividing the first by the second gives a product for $\sqrt 2$:

$$\sqrt 2 = \frac{2\cdot 6\cdot 6\cdot 10\cdot 10\cdot 14\cdot 14\cdot 18\cdot 18}{1\cdot 3\cdot 5\cdot 7\cdot 9\cdot 11\cdot 13\cdot 15\cdot 17\cdot 19}\cdots$$

See [[wallis-product]].

### §186–§187 — Products for the other trig functions and ratios

Quotients of the §184 products give

$$\tan\frac{m\pi}{2n} = \frac{m}{n - m}\cdot\frac{2n - m}{n + m}\cdot\frac{2n + m}{3n - m}\cdot\frac{4n - m}{3n + m}\cdot\frac{4n + m}{5n - m}\cdots$$

$$\cot\frac{m\pi}{2n} = \frac{n - m}{m}\cdot\frac{n + m}{2n - m}\cdot\frac{3n - m}{2n + m}\cdot\frac{3n + m}{4n - m}\cdots$$

with similar formulas for $\sec$ and $\csc$ (source: chapter11.pdf, §186). Replacing $m$ with a different integer $k$ and dividing yields products for the ratios $\sin(m\pi/2n)/\sin(k\pi/2n)$ etc. (§187), so once one trig value is known the others follow without further transcendental computation. See [[trig-infinite-products]].

### §188–§190 — $\log\pi$ from products

Re-pair the Wallis product to read $\pi/2 = 2(1 - 1/9)(1 - 1/25)(1 - 1/49)\cdots$ — equivalently $\pi = 4\prod_{k\ge 1}(1 - 1/(2k+1)^2)$. Take logs:

$$\log\pi = \log 4 + \sum_{k\ge 1}\log\!\left(1 - \frac{1}{(2k+1)^2}\right).$$

Expand each log by [[logarithmic-series|§118]]:

$$\log\!\left(1 - \frac{1}{(2k+1)^2}\right) = -\frac{1}{(2k+1)^2} - \frac{1}{2(2k+1)^4} - \frac{1}{3(2k+1)^6} - \cdots$$

The double sum, read column by column, becomes

$$\log\pi = \log 4 - (A - 1) - \tfrac{1}{2}(B - 1) - \tfrac{1}{3}(C - 1) - \tfrac{1}{4}(D - 1) - \cdots,$$

where $A = \sum_{k\ge 0} 1/(2k+1)^2 = \pi^2/8$, $B = \sum 1/(2k+1)^4 = \pi^4/96$, $C = \sum 1/(2k+1)^6 = \pi^6/960$, $\ldots$ are the [[zeta-at-even-integers|§169 odd-square sums]]. Tabulating $A, B, \ldots, X$ to 18+ digits gives

$$\log_e \pi = 1.144729885849400174\ldots,\qquad \log_{10}\pi = 0.497149872694133854\ldots$$

(source: chapter11.pdf, §190). See [[log-pi-via-products]].

### §191–§196 — $\log\sin$ and $\log\cos$

The same trick on the §184 sine and cosine products gives

$$\log\sin\frac{m\pi}{2n} = \log m + \log(2n - m) + \log(2n + m) - 3\log n + \log\pi - \log 8 - \frac{m^2}{n^2}\!\!\left(\alpha - \tfrac{1}{2^2}\right) - \frac{m^4}{2n^4}\!\!\left(\beta - \tfrac{1}{2^4}\right) - \cdots$$

$$\log\cos\frac{m\pi}{2n} = \log(n - m) + \log(n + m) - 2\log n - \frac{m^2}{n^2}(A - 1) - \frac{m^4}{2n^4}(B - 1) - \cdots$$

where $\alpha = \sum_{k\ge 1} 1/(2k)^2 = \pi^2/24$, $\beta = \sum 1/(2k)^4 = \pi^4/1440$, $\ldots$ are reciprocal-power sums over *even* integers. Both series converge geometrically in $(m/n)^2$; for $m/n \le 1/2$ (which co-function reduction always achieves) ten terms give about thirty correct digits. Euler tabulates the coefficients so that any sine or cosine logarithm can be computed by addition (source: chapter11.pdf, §194–§195). See [[log-sine-via-products]].

### §197–§198 — A faster route for tan and cot

For the *tangent* and *cotangent*, taking $\log\sin - \log\cos$ doubles the work. A better starting point is the [[cotangent-partial-fraction|§181 partial fraction]]

$$\tan\frac{m\pi}{2n} = \frac{4mn}{\pi}\!\left(\frac{1}{n^2 - m^2} + \frac{1}{9n^2 - m^2} + \frac{1}{25n^2 - m^2} + \cdots\right).$$

Each fraction expands as a geometric series in $m^2/(kn)^2$, the double sum transposes, and the column sums are again the $A, B, C, \ldots$ table. Euler obtains

$$\tan\frac{m\pi}{2n} = \frac{4mn}{\pi(n^2 - m^2)} + \frac{4m}{\pi n}\!\left[(A - 1) + \frac{m^2}{n^2}(B - 1) + \frac{m^4}{n^4}(C - 1) + \cdots\right]$$

(reorganized; source: chapter11.pdf, §198) with $1/\pi = 0.318309886183790671\ldots$, "for which we have already found the value." The cotangent has an analogous formula. See [[log-sine-via-products]].

## Notable points

- **The sine and cosine products are reused four times.** §158 gives them; §184 splits them into linear factors; §185 turns the redundancy into the Wallis product; §188 takes logs to compute $\log\pi$; §191 generalizes the same log trick to $\log\sin$ and $\log\cos$. Each step uses only the previous one. Chapter 11 is a sustained exercise in extracting computational value from a single object.
- **Convergence depends on the operation.** The infinite products themselves converge geometrically in $1/k^2$ — too slowly to be practical for $\pi$ (Euler is explicit: "too many terms are required to obtain an accurate value of $\pi$ even to only ten decimal places", §188). But after transposition, the columns are dominated by $1/2^{2k}$, so a handful of column terms suffice. **The transposition is what makes the products useful.**
- **The Wallis product was already known.** Wallis published it in 1656 in *Arithmetica Infinitorum*, almost a century before Euler. What is new here is the embedding into a parametric family of products at all rational angles $m\pi/(2n)$, and the realization that the whole family is *one* identity — the §158 products in disguise.
- **The chapter sets up the trig log tables.** A *Tabula Sinuum, Tangentium et Secantium* in 1748 had thirty-digit common logarithms of every trigonometric function. Chapter 11 is the *recipe* for those tables. Without it the entries would have to be computed by long division of 28-digit power series, which is what Euler means by "even now we have no better methods" (§188).
- **The all-purpose table of constants is small.** The same values $A, B, C, \ldots$ ($\pi^{2k}/(\text{rational})$, sums over odd squares) and $\alpha, \beta, \gamma, \ldots$ (sums over even squares) appear in *every* formula of §190–§198. Euler tabulates them once and re-uses them throughout. The §168 table of $\zeta(2k)$ values is essentially a third copy of the same numbers.

## Why this chapter matters

Where Chapter 10 used the §158 products for *theoretical* harvest (exact values of $\zeta(2k)$, partial fractions of $\cot$ and $\csc$), Chapter 11 uses them for *computational* harvest. The same technique that closed the Basel problem — equating an infinite product to a power series — turns out to be the most efficient way to generate logarithm tables for the trigonometric functions.

Two themes carry forward:

- **Series acceleration by transposition.** A slowly-converging single sum becomes a doubly-convergent double sum after taking logs and expanding; transposing reveals that one direction converges fast. This is the same trick Euler uses for [[zeta-at-even-integers|the higher zeta values]] and prefigures the **Euler–Maclaurin formula** (Chapter 13) and modern series-acceleration methods.
- **Logarithms as the universal computational currency.** Euler routinely converts a problem about products into a problem about sums by taking logs, then converts back at the end. The decimal-fraction infrastructure of [[characteristic-and-mantissa|the §112 logarithm tables]] makes this the cheapest available reduction.

After Chapter 11 the *Introductio*'s analytic-function project is essentially complete: the elementary transcendentals $e^z, \log z, \sin z, \cos z$ have been defined, expanded as series, factored as products, summed over their zeros, and tabulated. Chapters 12–18 turn to other topics (continued fractions, partition identities, prime products) that share methods but not a unified theme.

## Related pages

- [[linear-factors-of-sine-cosine]]
- [[wallis-product]]
- [[trig-infinite-products]]
- [[log-pi-via-products]]
- [[log-sine-via-products]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[cotangent-partial-fraction]]
- [[zeta-at-even-integers]]
- [[logarithmic-series]]
- [[pi]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
