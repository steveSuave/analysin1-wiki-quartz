# Euler's Formula

**Summary**: §138 of Chapter 8. Combining [[de-moivre-formula|De Moivre's formula]] $(\cos z \pm i\sin z)^n = \cos nz \pm i\sin nz$ with the Chapter 7 limit $(1 + z/j)^j = e^z$, Euler arrives at

$$\cos v = \frac{e^{iv} + e^{-iv}}{2},\qquad \sin v = \frac{e^{iv} - e^{-iv}}{2i},\qquad e^{iv} = \cos v + i\sin v.$$

Sines and cosines are real linear combinations of complex exponentials, and the complex exponential is determined by its real and imaginary parts — sine and cosine. The promised connection of §126 between trigonometric and exponential transcendentals is realized.

**Sources**: chapter8 (§138)

**Last updated**: 2026-04-27

---

## The derivation

Take the §133 De Moivre representations

$$\cos nz = \frac{(\cos z + i\sin z)^n + (\cos z - i\sin z)^n}{2},\qquad \sin nz = \frac{(\cos z + i\sin z)^n - (\cos z - i\sin z)^n}{2i}.$$

Apply the §134 substitution: let $z$ be infinitely small, $n = j$ infinitely large, $jz = v$ finite. Then

$$\cos z = 1,\qquad \sin z = z = v/j,$$

so

$$\cos z \pm i\sin z = 1 \pm iv/j.$$

Substituting into the §133 expressions:

$$\cos v = \frac{(1 + iv/j)^j + (1 - iv/j)^j}{2},\qquad \sin v = \frac{(1 + iv/j)^j - (1 - iv/j)^j}{2i}.$$

Now invoke the [[exponential-series|Chapter 7]] identity $(1 + w/j)^j = e^w$ for $j$ infinite. Setting $w = iv$ in one factor and $w = -iv$ in the other:

$$(1 + iv/j)^j = e^{iv},\qquad (1 - iv/j)^j = e^{-iv}.$$

Therefore

$$\cos v = \frac{e^{iv} + e^{-iv}}{2},\qquad \sin v = \frac{e^{iv} - e^{-iv}}{2i}.$$

(source: chapter8, §138).

## Solving for the exponential

Compute $\cos v + i\sin v$:

$$\cos v + i\sin v = \frac{e^{iv} + e^{-iv}}{2} + i\cdot\frac{e^{iv} - e^{-iv}}{2i} = \frac{e^{iv} + e^{-iv}}{2} + \frac{e^{iv} - e^{-iv}}{2} = e^{iv}.$$

Likewise $\cos v - i\sin v = e^{-iv}$. So Euler's formula:

$$\boxed{\,e^{iv} = \cos v + i\sin v,\qquad e^{-iv} = \cos v - i\sin v.\,}$$

(source: chapter8, §138). Euler comments: "From these equations we understand how complex exponentials can be expressed by real sines and cosines."

## Why the formula is *forced*

The identity is not posited — it is the only way three earlier results can coexist:

1. The §133 De Moivre identity, which says $(\cos z + i\sin z)^n$ rotates by $nz$.
2. The §122 / §125 identity $(1 + w/j)^j = e^w$ for $j$ infinite.
3. The §134 infinitesimal substitution, which maps $(\cos z + i\sin z)^n$ to $(1 + iv/j)^j$ when $z = v/j$ is infinitesimal and $n = j$ infinite.

Stack these and there is exactly one possibility: the rotation $\cos v + i\sin v$ *equals* $e^{iv}$. Euler does not present the formula as a deep insight; he writes it down at the end of a five-line computation.

This is also consistent with the [[transcendence-of-logarithms|Chapter 7 §125]] hint: $\log(\cos z + i\sin z)$ should equal $iz$, since $e^{iz} = \cos z + i\sin z$.

## Equivalent forms

- $e^{iv} + e^{-iv} = 2\cos v$
- $e^{iv} - e^{-iv} = 2i\sin v$
- $\sin v = (e^{iv} - e^{-iv})/(2i)$
- $\cos v = (e^{iv} + e^{-iv})/2$
- $\tan v = -i(e^{iv} - e^{-iv})/(e^{iv} + e^{-iv})$
- $\cot v = i(e^{iv} + e^{-iv})/(e^{iv} - e^{-iv})$

These will be used freely throughout later chapters of the *Introductio*. In particular [[arctangent-series|§139]] inverts the formula to express the arc itself as a logarithm.

## What about $e^{i\pi} = -1$?

Setting $v = \pi$ in Euler's formula:

$$e^{i\pi} = \cos\pi + i\sin\pi = -1 + 0i = -1,$$

i.e., $e^{i\pi} + 1 = 0$. The "Euler identity" — celebrated as the most beautiful equation in mathematics — is an immediate corollary. Euler does not single it out in §138 — the formula is just one of many consequences he reads off — and the slogan "most beautiful equation" is a much later marketing flourish. But the substance is here.

## How the formula is used in the rest of Chapter 8

- [[arctangent-series|§139–§140]] inverts Euler's formula to express the arc as $z = (1/2i)\log\frac{\cos z + i\sin z}{\cos z - i\sin z}$.
- §139 shows that *every* logarithm of a complex number is a real number plus an arc, foreshadowing the full theory of complex logarithms in later sections.
- §142 uses the inverse to compute $\pi$ from rapidly convergent rational arctangent series.

In later chapters of the *Introductio*, Euler's formula recurs constantly — every factorization of a polynomial with complex roots, every Fourier-style decomposition, every bridge between exponential growth and oscillation passes through this identity.

## Related pages

- [[de-moivre-formula]]
- [[exponential-series]]
- [[sine-and-cosine-series]]
- [[infinitesimal-and-infinite-numbers]]
- [[eulers-number]]
- [[arctangent-series]]
- [[sine-and-cosine]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
