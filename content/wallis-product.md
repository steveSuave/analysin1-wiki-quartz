# Wallis Product

**Summary**: §185: $\dfrac{\pi}{2} = \dfrac{2\cdot 2\cdot 4\cdot 4\cdot 6\cdot 6\cdot 8\cdot 8}{1\cdot 3\cdot 3\cdot 5\cdot 5\cdot 7\cdot 7\cdot 9}\cdots$. Euler derives Wallis's 1656 product as the quotient of two [[linear-factors-of-sine-cosine|§184 product expressions]] for $\cos(m\pi/2n)$, embedding it in a parametric family that includes analogous products for $\sqrt 2$ and other algebraic numbers.

**Sources**: chapter11.pdf

**Last updated**: 2026-05-11

---

## Statement

$$\boxed{\;\frac{\pi}{2} = \prod_{k=1}^{\infty}\frac{(2k)(2k)}{(2k-1)(2k+1)} = \frac{2\cdot 2}{1\cdot 3}\cdot\frac{4\cdot 4}{3\cdot 5}\cdot\frac{6\cdot 6}{5\cdot 7}\cdot\frac{8\cdot 8}{7\cdot 9}\cdots\;}$$

Equivalently, taking adjacent factors together:

$$\frac{\pi}{2} = \frac{2\cdot 2\cdot 4\cdot 4\cdot 6\cdot 6\cdot 8\cdot 8\cdot 10\cdot 10\cdot 12\cdot 12}{1\cdot 3\cdot 3\cdot 5\cdot 5\cdot 7\cdot 7\cdot 9\cdot 9\cdot 11\cdot 11\cdot 13}\cdots$$

(source: chapter11.pdf, §185). Euler attributes the formula directly: "this is the expression for $\pi$ which Wallis found in his *Arithmetic of the Infinite*" (Wallis, *Arithmetica Infinitorum*, 1656).

## Derivation as a quotient

The [[linear-factors-of-sine-cosine|§184 cosine identities]] give two product expressions for $\cos(m\pi/2n)$:

$$\cos\frac{m\pi}{2n} = \frac{n - m}{n}\cdot\frac{n + m}{n}\cdot\frac{3n - m}{3n}\cdot\frac{3n + m}{3n}\cdot\frac{5n - m}{5n}\cdot\frac{5n + m}{5n}\cdots$$

$$\cos\frac{m\pi}{2n} = \frac{(n - m)\pi}{2n}\cdot\frac{n + m}{2n}\cdot\frac{3n - m}{2n}\cdot\frac{3n + m}{4n}\cdot\frac{5n - m}{4n}\cdot\frac{5n + m}{6n}\cdots$$

Dividing the first by the second cancels every $(n - m), (n + m), (3n - m), \ldots$ numerator and produces

$$1 = \frac{\pi}{2}\cdot\frac{1}{2}\cdot\frac{3}{2}\cdot\frac{3}{4}\cdot\frac{5}{4}\cdot\frac{5}{6}\cdot\frac{7}{6}\cdot\frac{7}{8}\cdot\frac{9}{8}\cdots$$

(source: chapter11.pdf, §185), independent of $m$ and $n$. Solving for $\pi/2$ gives the Wallis product. The $m, n$ drop out: the identity is a structural fact about the §184 redundancy, not about any particular angle.

## Variants for other algebraic numbers

The general form (source: chapter11.pdf, §185) is

$$\frac{\pi}{2} = \frac{n}{m}\sin\frac{m\pi}{2n}\cdot\frac{2n}{2n - m}\cdot\frac{2n}{2n + m}\cdot\frac{4n}{4n - m}\cdot\frac{4n}{4n + m}\cdot\frac{6n}{6n - m}\cdots$$

Setting $m/n = 1$ recovers Wallis. Other rationals give:

**$m/n = 1/2$** ($\sin(\pi/4) = 1/\sqrt 2$):

$$\frac{\pi}{2} = \frac{\sqrt 2}{1}\cdot\frac{4}{3}\cdot\frac{4}{5}\cdot\frac{8}{7}\cdot\frac{8}{9}\cdot\frac{12}{11}\cdot\frac{12}{13}\cdot\frac{16}{15}\cdot\frac{16}{17}\cdots$$

**$m/n = 1/3$** ($\sin(\pi/6) = 1/2$):

$$\frac{\pi}{2} = \frac{3}{2}\cdot\frac{6}{5}\cdot\frac{6}{7}\cdot\frac{12}{11}\cdot\frac{12}{13}\cdot\frac{18}{17}\cdot\frac{18}{19}\cdot\frac{24}{23}\cdots$$

**Dividing the first by the second** (both equal $\pi/2$) eliminates $\pi$ entirely:

$$\sqrt 2 = \frac{2\cdot 6\cdot 6\cdot 10\cdot 10\cdot 14\cdot 14\cdot 18\cdot 18}{1\cdot 3\cdot 5\cdot 7\cdot 9\cdot 11\cdot 13\cdot 15\cdot 17\cdot 19}\cdots$$

(source: chapter11.pdf, §185). A "Wallis-style" product for $\sqrt 2$.

## Convergence is slow

The $k$-th Wallis factor is $1 + 1/(4k^2 - 1) = 1 + O(1/k^2)$, so the partial product converges to $\pi/2$ at rate $1/N$. Concretely:

| Factors | Approximation to $\pi/2$ |
| --- | --- |
| 10 | 1.55340 (3 correct digits) |
| 100 | 1.56688 (3 correct digits) |
| 1000 | 1.56999 (4 correct digits) |
| 10000 | 1.57072 (5 correct digits) |

Euler is explicit: "too many terms are required to obtain an accurate value of $\pi$ even to only ten decimal places" (source: chapter11.pdf, §188). The Wallis product is structurally important but computationally inferior to [[machin-like-formula|Machin's formula]] (chapter 8) or the [[arctangent-series|$\arctan$ series]].

## What it is good for

The Wallis product (and its variants) is the *form in which the §158 products land at rational angles*, and that form makes its logarithm tractable. Re-pairing factors gives

$$\frac{\pi}{2} = 2\prod_{k=1}^{\infty}\!\left(1 - \frac{1}{(2k+1)^2}\right) = 2\cdot\frac{8}{9}\cdot\frac{24}{25}\cdot\frac{48}{49}\cdot\frac{80}{81}\cdots$$

— each factor is $(1 - $ small$)$, so $\log\pi = \log 4 + \sum\log(1 - 1/(2k+1)^2)$ has every term tame. The double-sum transposition that follows (§188–§190) extracts $\log\pi$ to twenty digits. See [[log-pi-via-products]].

## Modern footnote

Wallis's original proof (1656) was a heroic interpolation of integrals of $(1-x^2)^n$ at half-integer $n$, giving him $\int_0^1 \sqrt{1 - x^2}\,dx = \pi/4$. Euler's derivation here — quotient of two ostensibly different products for the same trig value — is structurally cleaner and embeds Wallis in a parametric family. The full family is the start of the theory of *infinite products with positive factors* and is essentially a consequence of the $\Gamma$-function duplication formula, though Euler does not yet have $\Gamma$ in the *Introductio*.

## Related pages

- [[linear-factors-of-sine-cosine]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[log-pi-via-products]]
- [[trig-infinite-products]]
- [[pi]]
- [[machin-like-formula]]
- [[arctangent-series]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
- [[chapter-15-on-series-which-arise-from-products]]
- [[prime-sign-series-for-pi]]
- [[euler-product-formula]]
