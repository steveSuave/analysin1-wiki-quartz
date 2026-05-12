# Powers of Sine and Cosine as Multiple-Angle Sums

**Summary**: §261–§263. Any integer power of $\sin z$ or $\cos z$ can be written as a finite linear combination of sines (or cosines) of multiple angles $kz$, with binomial-coefficient weights. This is the inverse of [[multiple-angle-polynomials|§234]]: instead of expanding $\sin nz$ in powers of $\sin z$, Euler expands $(\sin z)^n$ in $\sin kz$. The derivation uses only the four product-to-sum lemmas and induction.

**Sources**: chapter14 (§261–§263)

**Last updated**: 2026-05-11

---

## The lemma (§262)

The whole reduction rests on the four product-to-sum identities:

$$\begin{aligned}
2\sin a\sin z &= \cos(a-z) - \cos(a+z) \\
2\cos a\sin z &= \sin(a+z) - \sin(a-z) \\
2\sin a\cos z &= \sin(a+z) + \sin(a-z) \\
2\cos a\cos z &= \cos(a-z) + \cos(a+z)
\end{aligned}$$

(source: chapter14, §262). Each multiplication of an existing $\sin kz$ or $\cos kz$ by another $\sin z$ or $\cos z$ produces two terms whose arguments differ by $\pm z$. Iterating gives a sum supported on $\{0, \pm z, \pm 2z, \ldots, \pm nz\}$ collapsed by parity.

## Powers of sine (§262)

Multiplying the previous power's expansion by $\sin z$ via the lemma and collecting:

$$\begin{aligned}
\sin z &= \sin z \\
2(\sin z)^2 &= 1 - \cos 2z \\
4(\sin z)^3 &= 3\sin z - \sin 3z \\
8(\sin z)^4 &= 3 - 4\cos 2z + \cos 4z \\
16(\sin z)^5 &= 10\sin z - 5\sin 3z + \sin 5z \\
32(\sin z)^6 &= 10 - 15\cos 2z + 6\cos 4z - \cos 6z \\
64(\sin z)^7 &= 35\sin z - 21\sin 3z + 7\sin 5z - \sin 7z \\
128(\sin z)^8 &= 35 - 56\cos 2z + 28\cos 4z - 8\cos 6z + \cos 8z \\
256(\sin z)^9 &= 126\sin z - 84\sin 3z + 36\sin 5z - 9\sin 7z + \sin 9z
\end{aligned}$$

(source: chapter14, §262). The leading factor on the left is $2^{n-1}$. The non-constant coefficients are the **binomial coefficients $\binom{n}{k}$ from the row indexed by $n$**, signs alternating, and using $\sin$ for odd $n$ and $\cos$ for even $n$. The constant term in even $n$ is the central binomial coefficient $\binom{n}{n/2}$ of the previous (also even-indexed) row, equivalently the binomial coefficient at the centre of row $n$.

## Powers of cosine (§263)

The same procedure with $\cos z$ in place of $\sin z$ — but using $2\cos a\cos z = \cos(a-z) + \cos(a+z)$ instead of $2\sin a\sin z = \cos(a-z) - \cos(a+z)$ — yields:

$$\begin{aligned}
\cos z &= \cos z \\
2(\cos z)^2 &= 1 + \cos 2z \\
4(\cos z)^3 &= 3\cos z + \cos 3z \\
8(\cos z)^4 &= 3 + 4\cos 2z + \cos 4z \\
16(\cos z)^5 &= 10\cos z + 5\cos 3z + \cos 5z \\
32(\cos z)^6 &= 10 + 15\cos 2z + 6\cos 4z + \cos 6z \\
64(\cos z)^7 &= 35\cos z + 21\cos 3z + 7\cos 5z + \cos 7z
\end{aligned}$$

(source: chapter14, §263). All signs are positive; only $\cos kz$ appears (no sines), and the coefficients again follow the binomial law.

## Modern reading

These are the standard *power-reduction formulas*. The cleanest derivation uses [[eulers-formula|Euler's formula]] $\cos z = (e^{iz} + e^{-iz})/2$ and $\sin z = (e^{iz} - e^{-iz})/(2i)$ together with the binomial theorem:

$$(2\cos z)^n = (e^{iz} + e^{-iz})^n = \sum_{k=0}^{n}\binom{n}{k}e^{i(n - 2k)z},$$

which immediately produces Euler's tables on grouping conjugate pairs. Euler does not write the derivation this way in §261–§263 — he stays with the real product-to-sum lemma — but the result and its binomial-coefficient pattern are the same.

The pattern matters for integration: $\int(\cos z)^n\,dz$ becomes a sum of $\int\cos(kz)\,dz$, each of which is elementary. This is precisely how Euler and his successors evaluated such integrals before the substitution $u = \tan(z/2)$ became standard.

## Earlier use in Chapter 13 §222

The odd-power half of the §262 table appears earlier in the book, in [[chapter-13-on-recurrent-series|Chapter 13]] §222, where Euler invokes (without proof at that point)

$$4(\sin\phi)^3 = 3\sin\phi - \sin 3\phi,\qquad 16(\sin\phi)^5 = 10\sin\phi - 5\sin 3\phi + \sin 5\phi,\qquad 64(\sin\phi)^7 = \cdots$$

to convert the complex-derived [[general-term-of-recurrent-series|general term]] of $A/(1 - 2pz\cos\phi + p^2 z^2)^k$ back to real form for $k = 2, 3, 4$ (the denominators $(\sin\phi)^3, (\sin\phi)^5, (\sin\phi)^7$ that appear in those formulas are cleared using exactly these identities). The Chapter 14 derivation supplies the proof Euler postponed.

## Inverse relationship to Chapter 14's main thread

The chapter's main movement (§234–§256) expands $\sin nz$ as a polynomial in $\sin z$ — the [[multiple-angle-polynomials|Chebyshev]] direction. §261–§263 is the inverse: it expands $(\sin z)^n$ as a sum of $\sin kz$ (or $\cos kz$). Together the two directions form an invertible change of basis between $\{(\sin z)^k : k = 0, 1, \ldots, n\}$ and $\{1, \sin z, \cos z, \sin 2z, \cos 2z, \ldots\}$ on each finite-dimensional space of trig polynomials.

## Related pages

- [[multiple-angle-polynomials]]
- [[trigonometric-addition-formulas]]
- [[de-moivre-formula]]
- [[eulers-formula]]
- [[binomial-series]]
- [[sine-and-cosine]]
- [[general-term-of-recurrent-series]]
- [[chapter-13-on-recurrent-series]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
