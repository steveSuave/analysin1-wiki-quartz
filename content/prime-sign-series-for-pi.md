# Prime-Sign Series for π

**Summary**: §285–§296. Applying the [[euler-product-formula|sieve-based Euler product derivation]] to the [[arctangent-series|Leibniz series]] $\pi/4 = 1 - 1/3 + 1/5 - \cdots$ and its higher analogues from [[circular-arc-series|Chapter 10]] produces a vast catalogue of identities in which $\pi$ (or $\pi/\sqrt 3$, $\pi/\sqrt 2$, $\pi^3$, etc.) is expressed as a sum or product over primes, with **signs determined by the residue class of each prime mod 4, mod 6, or mod 8**. These are the simplest non-trivial **Dirichlet $L$-series in their Euler-product form** — although Euler computes them a century before Dirichlet names them.

**Sources**: chapter15.pdf

**Last updated**: 2026-05-11

---

## The mechanism

The starting point is the §284 generalisation of the [[euler-product-formula|§283 sieve]] applied to a series with a sign pattern $\chi$ on the natural numbers, where $\chi$ is **completely multiplicative**:

$$A = \sum_{k=1}^{\infty}\frac{\chi(k)}{k^n}\qquad\Longrightarrow\qquad A = \prod_{p\text{ prime}}\frac{1}{1 - \chi(p)/p^n}.$$

When $\chi(p) = +1$ the factor is $1/(1-1/p^n)$; when $\chi(p) = -1$ the factor is $1/(1+1/p^n)$; when $\chi(p) = 0$ the prime is **excluded** entirely from the product. Euler does not articulate this general framework, but he applies it to four different character-like patterns from Chapters 8 and 10.

## At $n = 1$ — primes mod 4 (§285–§289)

From [[arctangent-series|Leibniz]]: $\pi/4 = 1 - 1/3 + 1/5 - 1/7 + \cdots$ uses the sign pattern $\chi_4$:

$$\chi_4(k) = \begin{cases} +1 & k \equiv 1\bmod 4 \\ -1 & k \equiv 3\bmod 4 \\ 0 & k\text{ even}\end{cases}$$

(extended multiplicatively to composites). The sieve gives (§285):

$$\frac{\pi}{4} = \prod_p \frac{p}{p \mp 1}\quad\text{where }\mp\text{ means } \begin{cases} -1 & p \equiv 1\bmod 4 \\ +1 & p \equiv 3\bmod 4\end{cases}$$

i.e. $\pi/4 = (3/4)(5/4)(7/8)(11/12)(13/12)(17/16)(19/20)(23/24)\cdots$ Numerator is the odd prime, denominator is whichever of $p\pm 1$ is divisible by 4.

Combined with the [[basel-problem|Basel-problem]] product expression for $\pi^2/6$, §285 derives:

$$\frac{\pi}{2} = \frac{3}{2}\cdot\frac{5}{6}\cdot\frac{7}{6}\cdot\frac{11}{10}\cdot\frac{13}{14}\cdot\frac{17}{18}\cdot\frac{19}{18}\cdot\frac{23}{22}\cdots$$

where the **denominators are the oddly-even neighbours** ($p\pm 1$ chosen so as to be $\equiv 2\bmod 4$).

§286 compares these to [[wallis-product|Wallis]]:

$$\frac{\pi^2}{8} = \frac{3\cdot 3}{2\cdot 4}\cdot\frac{5\cdot 5}{4\cdot 6}\cdot\frac{7\cdot 7}{6\cdot 8}\cdots,\quad \frac{32}{\pi^3} = \frac{9\cdot 9}{8\cdot 10}\cdot\frac{15\cdot 15}{14\cdot 16}\cdot\frac{21\cdot 21}{20\cdot 22}\cdots$$

(the latter has only **non-prime odd** numbers in the numerators — a curious complement to the prime-only versions).

Multiplying the §285 product by factors $\frac{1\pm 1/p}{1\mp 1/p}$ for selected primes converts an odd-prime-only product into one over **all** primes, with composite signs given multiplicatively (§288–§289). The resulting series:

$$\frac{\pi}{6} = 1 - \frac{1}{2} - \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6} - \frac{1}{7} - \frac{1}{8} + \frac{1}{9} - \cdots,$$

$$\frac{\pi}{2} = 1 + \frac{1}{3} - \frac{1}{5} + \frac{1}{7} + \frac{1}{9} - \frac{1}{11} - \frac{1}{13} + \cdots,$$

$$\pi = 1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} - \frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8} + \frac{1}{9} - \frac{1}{10} - \cdots,$$

with the sign of each composite determined by the product of the signs of its prime factors.

§290–§291 push this further: by including or excluding finitely many primes from the "negative" pile one can make the series sum to $0$, $3\pi/2$, $\infty$, or any number from a related family. Euler observes (source: chapter15.pdf, §291):

> "If all but a finite collection of primes have positive signs, then the sum of the series will be infinitely large. ... [If] all prime numbers, except for a finite collection, have negative signs, then the sum of the series will be equal to zero."

## At $n = 3$ — primes mod 4 again (§287)

The same machinery applied to the [[circular-arc-series|§174 series]] $\pi^3/32 = 1 - 1/3^3 + 1/5^3 - 1/7^3 + \cdots$ gives

$$\frac{\pi^3}{32} = \prod_p \frac{p^3}{p^3 \mp 1},\quad\text{sign by }p\bmod 4.$$

Numerically (§287): $\pi^3/32 = (27/28)(125/124)(343/344)(1331/1332)\cdots$, and the comparison with $\pi^5/945 = \zeta(6)\cdot\text{const}$ produces the analogous **cubic** Wallis-style identities.

## At $n = 1$ — primes mod 6 (§292–§294)

From [[circular-arc-series|§176]]: $\frac{\pi}{3\sqrt 3} = 1 - 1/5 + 1/7 - 1/11 + 1/13 - \cdots$ (an alternating sum over numbers coprime to 6, signed by $\equiv 1$ vs $\equiv -1\bmod 6$). The sieve gives

$$\frac{\pi}{3\sqrt 3} = \prod_{p\neq 2,3} \frac{p}{p \mp 1}\quad\text{with sign by }p\bmod 6,$$

i.e. $\pi/(3\sqrt 3) = (5/6)(7/6)(11/12)(13/12)(17/18)(19/18)\cdots$ — denominators divisible by 6.

§293 combines this with the $\pi^2/6$ product (with the $1/2, 1/3$ factors stripped out) to get analogues of the §285 ratios with **denominators not divisible by 6**:

$$\frac{\pi\sqrt 3}{2} = \frac{9}{4}\cdot\frac{5}{4}\cdot\frac{7}{8}\cdot\frac{11}{10}\cdot\frac{13}{14}\cdots$$

Multiplying by individual factors gives (§293, §294) full-prime series for $\sqrt 3/2$, $2/\sqrt 3$, etc.:

$$\frac{\sqrt 3}{2} = \frac{2}{3}\cdot\frac{4}{3}\cdot\frac{8}{9}\cdot\frac{10}{9}\cdot\frac{14}{15}\cdots\quad(\text{primes }\equiv \pm 1\bmod 12)$$

## At $n = 1$ — primes mod 8 (§295)

From [[circular-arc-series|§179]]: $\frac{\pi}{2\sqrt 2} = 1 + 1/3 - 1/5 - 1/7 + 1/9 + 1/11 - 1/13 - 1/15 + \cdots$, with sign $+1$ on $k \equiv 1, 3\bmod 8$ and $-1$ on $k \equiv 5, 7\bmod 8$. Sieving yields

$$\frac{\pi}{2\sqrt 2} = \prod_{p\text{ odd}} \frac{p}{p\mp 1}\quad\text{with sign by }p\bmod 8,$$

so $\pi/(2\sqrt 2) = (3/2)(5/6)(7/8)(11/12)(13/12)(17/16)(19/18)(23/24)\cdots$

The numerator/denominator of each fraction differs from the odd prime $p$ by 1; whether the smaller (matching $p-1$) or larger (matching $p+1$) is in the denominator depends on $p \bmod 8$.

## Closing remark (§296)

Euler signals (source: chapter15.pdf, §296):

> "In a like manner the other series, which express circular arcs, found in sections 179 and following, could be expressed as products dependent on the prime numbers. In this way we could develop important properties of both infinite series and infinite products, but since we have discussed the principal results, we will not delay any longer to develop more."

He leaves the analogues for higher moduli, mod 12, mod 16, etc. — which would come to be classified by Dirichlet (1837) as the characters mod $m$, with each non-trivial $\chi$ giving an $L$-function $L(s, \chi) = \prod_p (1 - \chi(p)/p^s)^{-1}$.

## Modern dictionary

| Euler's series | Modern $L$-function | Value at $s=1$ |
|---|---|---|
| §284, $n=1$: $1 - 1/3 + 1/5 - \cdots$ | $L(s, \chi_{-4})$ | $\pi/4$ |
| §287, $n=3$: $1 - 1/27 + 1/125 - \cdots$ | $L(3, \chi_{-4})$ | $\pi^3/32$ |
| §292, mod 6: $1 - 1/5 + 1/7 - \cdots$ | $L(s, \chi_{-3})$ | $\pi/(3\sqrt 3)$ |
| §295, mod 8: $1 + 1/3 - 1/5 - 1/7 + \cdots$ | $L(s, \chi_{8})$ | $\pi/(2\sqrt 2)$ |

Each is the Dirichlet $L$-function of a (real, primitive) character of small conductor; each is associated to an imaginary or real quadratic field via the Dirichlet class number formula. Euler had every example one would meet in an introductory analytic number theory course — without the unifying vocabulary.

## Worked example: §285 derivation in detail

Start with $A = \pi/4 = 1 - 1/3 + 1/5 - 1/7 + \cdots$. To sieve out primes:

- Add $A/3 = 1/3 - 1/9 + 1/15 - \cdots$ to remove the $1/3$ term and (with sign-tracking) all multiples of 3:

$$B = (1 + 1/3)A = 1 + 1/5 - 1/7 - 1/11 + 1/13 + 1/17 - \cdots\quad(\text{indices not divisible by 3}).$$

- Subtract $B/5 = 1/5 + 1/25 - 1/35 - \cdots$ to remove multiples of 5:

$$C = (1 - 1/5)B = 1 - 1/7 - 1/11 + 1/13 + 1/17 + \cdots$$

- Add $C/7$ to remove multiples of 7:

$$D = (1 + 1/7)C = 1 - 1/11 + 1/13 + 1/17 - 1/19 - 1/23 + \cdots$$

Continue: at each prime, **add** $C/p^n$ if $p \equiv 3\bmod 4$ and **subtract** $C/p^n$ if $p \equiv 1\bmod 4$. At the end only 1 remains, giving

$$1 = A\cdot\prod_{p \equiv 3\bmod 4}\Bigl(1 + \tfrac{1}{p^n}\Bigr)\prod_{p \equiv 1\bmod 4}\Bigl(1 - \tfrac{1}{p^n}\Bigr).$$

At $n = 1$ this is the §285 identity for $\pi/4$.

## Related pages

- [[chapter-15-on-series-which-arise-from-products]]
- [[euler-product-formula]]
- [[squarefree-and-mobius-series]]
- [[arctangent-series]]
- [[circular-arc-series]]
- [[wallis-product]]
- [[basel-problem]]
- [[divergence-of-prime-reciprocals]]
- [[zeta-at-even-integers]]
