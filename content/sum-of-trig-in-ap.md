# Sum of Trig Functions in Arithmetic Progression

**Summary**: §258–§260. Sines and cosines of angles in arithmetic progression form a [[recurrent-series|recurrent series]] with scale of relation $2\cos b, -1$. Euler sums the infinite series $\sin a + \sin(a+b) + \sin(a+2b) + \cdots$ in closed form by evaluating the generating rational function at $z = 1$, obtaining $(\sin a - \sin(a-b)) / (2 - 2\cos b)$. He then derives the finite sum through $\sin(a+nb)$ by subtracting the tail of the infinite series from the head.

**Sources**: chapter14 (§258–§260)

**Last updated**: 2026-05-11

---

## Setup (§258)

Let the angles $a, a+b, a+2b, a+3b, \ldots$ be an arithmetic progression with common difference $b$. Define

$$s = \sin a + \sin(a+b) + \sin(a+2b) + \sin(a+3b) + \cdots$$

From [[trigonometric-recurrent-progression|§129]], the sequence of sines is recurrent with scale of relation $2\cos b, -1$, generating rational function denominator $1 - 2\cos b\cdot Z + Z^2$ (source: chapter14, §258).

## The rational generating function

The general theory of [[recurrent-series|recurrent series]] (Chapter 4 / Chapter 13) says that the generating function of the series $\{a_k\}$ is a rational function $A(z)/B(z)$ where $B(z)$ is read from the scale of relation. Here $B(z) = 1 - 2\cos b\cdot z + z^2$.

For the numerator, Euler uses the §129 initial-value construction. The rational function for $\sum_{k=0}^{\infty}\sin(a+kb)z^k$ is:

$$F(z) = \frac{\sin a + z(\sin(a+b) - 2\cos b\cdot\sin a)}{1 - 2\cos b\cdot z + z^2} = \frac{\sin a + z(\sin(a+b) - 2\sin a\cos b)}{1 - 2\cos b\cdot z + z^2}$$

Using the addition formula $\sin(a+b) - 2\sin a\cos b = \sin a\cos b + \cos a\sin b - 2\sin a\cos b = -\sin(a-b) + \sin a - \sin a = -\sin(a-b)$... more directly, Euler writes (source: chapter14, §258):

$$F(z) = \frac{\sin a + z(\sin(a+b) - 2\cos b\cdot\sin a)}{1 - 2z\cos b + z^2}$$

## Closed-form sum at $z = 1$ (§258)

Setting $z = 1$:

$$s = F(1) = \frac{\sin a + \sin(a+b) - 2\cos b\cdot\sin a}{2 - 2\cos b}$$

Now $\sin(a+b) - 2\cos b\cdot\sin a = \sin a\cos b + \cos a\sin b - 2\sin a\cos b = -\sin a\cos b + \cos a\sin b = -\sin(a-b)$. Thus:

$$\boxed{s = \frac{\sin a - \sin(a-b)}{2(1 - \cos b)}}$$

(source: chapter14, §258). The denominator $2(1-\cos b) = 4\sin^2(b/2)$ by the half-angle formula, so equivalently

$$s = \frac{\sin a - \sin(a-b)}{4\sin^2(b/2)} = \frac{2\cos(a - b/2)\sin(b/2)}{4\sin^2(b/2)} = \frac{\cos(a - b/2)}{2\sin(b/2)}$$

This is the standard closed form: the infinite sum of sines in arithmetic progression is $\frac{1}{2}\csc(b/2)\cos(a - b/2)$, provided $|z| < 1$ (i.e., convergence requires the generating series to converge, which for $z = 1$ requires the series to sum in the sense of the rational function's analytic continuation).

## Convergence note

Euler does not address convergence explicitly here. The formula $z = 1$ is on the boundary of convergence of the generating function (since the denominator $1 - 2z\cos b + z^2$ has roots $z = e^{\pm ib}$ on the unit circle). The sum is valid in the sense of the Cesàro or Abel sum; a modern reader would recognize this as the real-part version of the geometric series $\sum e^{i(a+kb)} = e^{ia}/(1-e^{ib})$.

## Cosine series

By an identical argument (replacing $\sin$ by $\cos$ throughout):

$$\cos a + \cos(a+b) + \cos(a+2b) + \cdots = \frac{\cos a - \cos(a-b)}{2(1-\cos b)} = \frac{\cos(a-b/2)}{2\sin(b/2)}\cdot\frac{\cos(b/2)}{\cos(b/2)}$$

More precisely:

$$\frac{\cos a - \cos(a-b)}{2(1-\cos b)} = \frac{2\sin(a-b/2)\sin(b/2)}{4\sin^2(b/2)} = \frac{\sin(a-b/2)}{2\sin(b/2)}$$

## Finite sum (§259–§260)

For the sum through $n+1$ terms,

$$s = \sin a + \sin(a+b) + \sin(a+2b) + \cdots + \sin(a+nb),$$

Euler subtracts the tail of the infinite series from the head (source: chapter14, §259). The infinite head sums to $\cos(a - b/2)/(2\sin(b/2))$ and the tail starting at $\sin(a + (n+1)b)$ sums to $\cos(a + (n + 1/2)b)/(2\sin(b/2))$. Their difference is

$$s = \frac{\cos(a - \tfrac{1}{2}b) - \cos(a + (n + \tfrac{1}{2})b)}{2\sin(\tfrac{1}{2}b)} = \frac{\sin(a + \tfrac{1}{2}nb)\sin(\tfrac{1}{2}(n+1)b)}{\sin(\tfrac{1}{2}b)}$$

after applying the sum-to-product identity. The cosine version (§260) is the same calculation with $\cos$ replacing $\sin$ in the head and a sign flip from $\cos f - \cos g = -2\sin\!\bigl(\tfrac{f+g}{2}\bigr)\sin\!\bigl(\tfrac{f-g}{2}\bigr)$, giving

$$\cos a + \cos(a+b) + \cdots + \cos(a+nb) = \frac{\cos(a + \tfrac{1}{2}nb)\sin(\tfrac{1}{2}(n+1)b)}{\sin(\tfrac{1}{2}b)}.$$

Both finite formulas are convergent in the ordinary sense for any real $b$ with $\sin(b/2)\ne 0$ — the infinite-sum step is just a bookkeeping device.

## Connection to Chapter 13 and Chapter 9

This §258 application is the same recurrent-series machinery from [[sum-of-recurrent-series|§231–§233]] applied to a trigonometric sequence. Euler is closing a circle: sines and cosines were first shown to be recurrent in [[trigonometric-recurrent-progression|§129]], the recurrent-series sum formula was established in [[sum-of-recurrent-series|§231]], and now in §258 the two threads meet to give trig sums in closed form. The same formula also relates to [[circular-arc-series|§171–§172]], where Newton's identities were applied to products of shifted sines — the §258 result is the additive rather than multiplicative side of the same structure.

## Related pages

- [[recurrent-series]]
- [[trigonometric-recurrent-progression]]
- [[sum-of-recurrent-series]]
- [[circular-arc-series]]
- [[sine-and-cosine]]
- [[trigonometric-addition-formulas]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
- [[chapter-13-on-recurrent-series]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
