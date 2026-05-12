# Chapter 8: On Transcendental Quantities Which Arise from the Circle

**Summary**: Euler turns from $a^z$ and $\log y$ to the second great class of transcendentals — circular arcs, sines, and cosines on the unit circle. After fixing notation (radius $= 1$, [[pi|$\pi$]] = half the circumference, $\sin z$ and $\cos z$ as functions of arc length), he derives the algebraic apparatus of trigonometry: addition formulas, product-to-sum, half-angle, and a [[trigonometric-recurrent-progression|recurrent-series]] structure for arcs in arithmetic progression. The complex factorization $(\cos z + i\sin z)(\cos z - i\sin z) = 1$ leads to [[de-moivre-formula|De Moivre's formula]]. Reapplying the [[infinitesimal-and-infinite-numbers|$\omega$/$j$ device]] of Chapter 7 produces the [[sine-and-cosine-series|power series]] for $\sin v$ and $\cos v$, and combining it with $(1 + z/j)^j = e^z$ yields the most famous identity in mathematics, [[eulers-formula|$e^{iv} = \cos v + i\sin v$]]. Inverting, the arc-from-tangent series gives [[arctangent-series|$\arctan t = t - t^3/3 + t^5/5 - \cdots$]], and a small change of variable gives [[machin-like-formula|Machin-style]] fast series for $\pi$.

**Sources**: chapter8

**Last updated**: 2026-04-27

---

## Overview

Chapters 6 and 7 built the first transcendental class — exponentials and logarithms — analytically. Chapter 8 builds the second: the *circular* transcendentals. Euler's stated motivation (§126) is twofold: these are an independent genus of transcendental quantity, *and* they will turn out to coincide with logarithms and exponentials of complex arguments. Both promises are kept by §138.

The chapter has four movements:

1. **§126–§131 — synthetic trigonometry on the unit circle.** Euler fixes the modern conventions (radius 1, arc as the independent variable, $\sin$ and $\cos$ as named functions) and then catalogs the algebraic identities every reader of the *Introductio* will need: Pythagorean identity, sum/difference, periodicity, product-to-sum, sum-to-product, half-angle. The arithmetic-progression remark of §129 — sines/cosines of $z, y+z, 2y+z, \ldots$ form a [[recurrent-series|recurrent progression]] with denominator $1 - 2nz + (m^2+n^2)z^2$ — links this material back to Chapter 4.
2. **§132–§134 — complex factorization and the trig power series.** Recognizing $(\cos z)^2 + (\sin z)^2 = 1$ as $(\cos z + i\sin z)(\cos z - i\sin z) = 1$ unlocks [[de-moivre-formula|De Moivre's formula]] $(\cos z \pm i\sin z)^n = \cos nz \pm i\sin nz$, and binomial expansion gives finite-$n$ identities for $\cos nz$ and $\sin nz$ in powers of $\sin z$ and $\cos z$. Then comes the master move: let $z$ be infinitely small (so $\sin z = z$, $\cos z = 1$) and $n$ infinitely large with $nz = v$ finite. The same coefficient-collapse $(j-m)/(nj) = 1/n$ used in Chapter 7 produces the [[sine-and-cosine-series|canonical series]] $\cos v = 1 - v^2/2! + v^4/4! - \cdots$ and $\sin v = v - v^3/3! + v^5/5! - \cdots$.
3. **§135–§137 — practical computation.** Tangent and cotangent series by division. Construction of trigonometric tables: it suffices to know $\sin$ and $\cos$ for arcs up to 30°; everything else follows by addition. Half-arc and double-arc formulas extend the range. Euler's table-builder pragmatism is on full display — the §134 series for $\sin(m\pi/(2n))$ already runs to 28-digit accuracy.
4. **§138–§142 — the bridge to logarithms and applications to $\pi$.** §138 returns to De Moivre with $\cos z = 1$, $\sin z = z$ infinitesimal, and recognizes $(1 \pm iv/j)^j = e^{\pm iv}$ from Chapter 7. The result is [[eulers-formula|$e^{iv} = \cos v + i\sin v$]], $\cos v = (e^{iv} + e^{-iv})/2$, $\sin v = (e^{iv} - e^{-iv})/(2i)$ — sines and cosines as complex exponentials. §139 inverts: $z = \frac{1}{2i}\log\bigl((\cos z + i\sin z)/(\cos z - i\sin z)\bigr)$. §140 substitutes $\tan z$ to get the [[arctangent-series|arctangent series]] $\arctan t = t - t^3/3 + t^5/5 - \cdots$, and at $t = 1$ recovers Leibniz's $\pi/4 = 1 - 1/3 + 1/5 - \cdots$. §141 uses $t = 1/\sqrt 3$ for a faster series, and §142 the [[machin-like-formula|Machin decomposition]] $\pi/4 = \arctan(1/2) + \arctan(1/3)$ for fastest convergence.

See also: [[pi]], [[sine-and-cosine]], [[trigonometric-addition-formulas]], [[trigonometric-recurrent-progression]], [[de-moivre-formula]], [[sine-and-cosine-series]], [[eulers-formula]], [[arctangent-series]], [[machin-like-formula]].

## Structure of the chapter

### §126 — Setup: the unit circle and the symbol $\pi$

Radius (= "total sine") is 1. Half the circumference is irrational; Euler reports the value to 113 digits beginning $3.14159\,26535\,89793\,23846\ldots$ "For the sake of brevity we will use the symbol $\pi$ for this number" (source: chapter8, §126). This sentence is the moment $\pi$ enters mainstream notation. See [[pi]].

### §127 — Notation: $\sin z$, $\cos z$, $\tan z$, $\cot z$

The arc $z$ is the independent variable. $\sin z$ and $\cos z$ are functions of arc length, not angle measure (though the two coincide for radius 1 in radians). Special values $\sin 0 = 0$, $\cos 0 = 1$, $\sin(\pi/2) = 1$, $\cos(\pi/2) = 0$, $\sin\pi = 0$, $\cos\pi = -1$, etc. The Pythagorean identity $(\sin z)^2 + (\cos z)^2 = 1$. Co-function relations $\cos z = \sin(\pi/2 - z)$. Tangent and cotangent as ratios. See [[sine-and-cosine]].

### §128 — Sum/difference formulas and periodicity

The four addition identities

$$\sin(y \pm z) = \sin y\cos z \pm \cos y\sin z,\qquad \cos(y \pm z) = \cos y\cos z \mp \sin y\sin z$$

are taken as known. Substituting $y = \pi/2, \pi, 3\pi/2, 2\pi$ produces a 16-row table reducing $\sin\bigl((4n+k)\pi/2 \pm z\bigr)$ and $\cos$ of the same to $\pm \sin z$ or $\pm \cos z$ for $k = 1,2,3,4$ and any integer $n$ (positive or negative). This is the periodicity catalog. See [[trigonometric-addition-formulas]].

### §129 — Arcs in arithmetic progression are a recurrent series

Let $\sin z = p$, $\cos z = q$, $\sin y = m$, $\cos y = n$. Then

$$\sin(y+z) = mq + np,\qquad \cos(y+z) = nq - mp,$$

$$\sin(2y+z) = 2mnq + (n^2-m^2)p,\qquad \cos(2y+z) = (n^2-m^2)q - 2mnp,$$

and so on. The arcs $z, y+z, 2y+z, 3y+z, \ldots$ form an arithmetic progression, and the sines (and cosines) form a [[recurrent-series|recurrent progression]] with denominator $1 - 2nz + (m^2+n^2)z^2$. Read off the recurrence:

$$\sin((k+1)y + z) = 2\cos y\cdot\sin(ky + z) - \sin((k-1)y + z),$$

with the same identity for cosine. See [[trigonometric-recurrent-progression]].

### §130–§131 — Product-to-sum, sum-to-product, half-angle

Adding and subtracting the §128 sum/difference formulas:

$$\sin y\cos z = \tfrac12\bigl(\sin(y+z) + \sin(y-z)\bigr),\qquad \cos y\cos z = \tfrac12\bigl(\cos(y-z) + \cos(y+z)\bigr),$$

$$\sin y\sin z = \tfrac12\bigl(\cos(y-z) - \cos(y+z)\bigr).$$

Setting $y = z = v/2$ gives the half-angle formulas $\cos(v/2) = \sqrt{(1 + \cos v)/2}$, $\sin(v/2) = \sqrt{(1 - \cos v)/2}$.

§131 changes variables: let $a = y + z$, $b = y - z$, so $y = (a+b)/2$, $z = (a-b)/2$. The identities above become the four sum-to-product theorems

$$\sin a + \sin b = 2\sin\tfrac{a+b}{2}\cos\tfrac{a-b}{2},$$

$$\sin a - \sin b = 2\cos\tfrac{a+b}{2}\sin\tfrac{a-b}{2},$$

$$\cos a + \cos b = 2\cos\tfrac{a+b}{2}\cos\tfrac{a-b}{2},$$

$$\cos a - \cos b = -2\sin\tfrac{a+b}{2}\sin\tfrac{a-b}{2},$$

from which Euler reads off six ratio identities (e.g. $\frac{\sin a + \sin b}{\sin a - \sin b} = \frac{\tan((a+b)/2)}{\tan((a-b)/2)}$). See [[trigonometric-addition-formulas]].

### §132 — Complex factorization

The Pythagorean identity factors:

$$(\cos z + i\sin z)(\cos z - i\sin z) = (\cos z)^2 + (\sin z)^2 = 1.$$

Multiplying two such factors:

$$(\cos y + i\sin y)(\cos z + i\sin z) = \cos y\cos z - \sin y\sin z + i(\sin y\cos z + \cos y\sin z) = \cos(y+z) + i\sin(y+z).$$

The conjugate factor multiplies to $\cos(y+z) - i\sin(y+z)$, and the three-factor case to $\cos(x+y+z) \pm i\sin(x+y+z)$ (source: chapter8, §132). Even though the factors are complex, "they are quite useful in combining and multiplying arcs." See [[de-moivre-formula]].

### §133 — De Moivre's formula and the binomial expansions

Iterating §132 yields

$$(\cos z \pm i\sin z)^n = \cos nz \pm i\sin nz$$

for any integer $n$. Solving for the real and imaginary parts:

$$\cos nz = \frac{(\cos z + i\sin z)^n + (\cos z - i\sin z)^n}{2},\qquad \sin nz = \frac{(\cos z + i\sin z)^n - (\cos z - i\sin z)^n}{2i}.$$

Expanding both sides by Newton's binomial gives the finite-$n$ identities

$$\cos nz = (\cos z)^n - \tfrac{n(n-1)}{2!}(\cos z)^{n-2}(\sin z)^2 + \tfrac{n(n-1)(n-2)(n-3)}{4!}(\cos z)^{n-4}(\sin z)^4 - \cdots,$$

$$\sin nz = n(\cos z)^{n-1}\sin z - \tfrac{n(n-1)(n-2)}{3!}(\cos z)^{n-3}(\sin z)^3 + \cdots.$$

(source: chapter8, §133). See [[de-moivre-formula]].

### §134 — The power series for $\sin v$ and $\cos v$

The infinitesimal/infinite move: let $z$ be infinitely small, so $\sin z = z$ and $\cos z = 1$; let $n$ be infinitely large, so that $nz = v$ is finite. Substituting into §133 — and using the Chapter 7 collapse $n(n-1)\cdots(n-k+1) = n^k$ for $n$ infinite, hence each $\binom{n}{k}(\cos z)^{n-k}(\sin z)^k = (nz)^k/k! = v^k/k!$ — yields

$$\cos v = 1 - \frac{v^2}{2!} + \frac{v^4}{4!} - \frac{v^6}{6!} + \cdots,$$

$$\sin v = v - \frac{v^3}{3!} + \frac{v^5}{5!} - \frac{v^7}{7!} + \cdots.$$

Euler immediately tabulates $\sin(m\pi/(2n))$ and $\cos(m\pi/(2n))$ as power series in $m/n$, with leading coefficients $\pi/2 = 1.5707963267948966\ldots$ and $\pi^3/3!\cdot 2^3$ (correctly $0.6459640975\ldots$) (source: chapter8, §134). The coefficients shrink fast enough that 28-digit accuracy is reached in a handful of terms when $m/n < 1/2$. See [[sine-and-cosine-series]].

### §135 — Tangent and cotangent series

By long division $\tan v = \sin v/\cos v$ and $\cot v = \cos v/\sin v$. Euler writes out 25-digit numerical series in $m/n$ for $\tan(m\pi/(2n))$ and $\cot(m\pi/(2n))$. The closed-form expansions $\tan v = v + v^3/3 + 2v^5/15 + \cdots$ and $\cot v = 1/v - v/3 - v^3/45 - \cdots$ are *not* derived here — Euler defers their justification to §197.

### §136–§137 — Building the table

Once $\sin$ and $\cos$ are known up to 30°, all other values follow by addition. Setting $y = \pi/6$ in the §130 sum-to-product identity, and using $\sin(\pi/6) = 1/2$:

$$\cos z = \sin(\pi/6 + z) + \sin(\pi/6 - z),\qquad \sin z = \cos(\pi/6 - z) - \cos(\pi/6 + z).$$

So sines/cosines from 30° to 60° follow from those of $z$ and $\pi/6 - z$, both below 30°. §137 does the same for tangent (using $\tan 2a = 2\tan a/(1 - \tan^2 a)$) and notes the secant/cosecant formulas $\csc z = \cot(z/2) - \cot z$, $\sec z = \cot(\pi/4 - z/2) - \tan z$.

### §138 — Euler's formula

Apply §133 with the §134 substitutions $z = v/j$ (infinitesimal) and $n = j$ (infinite):

$$\cos v = \frac{(1 + iv/j)^j + (1 - iv/j)^j}{2},\qquad \sin v = \frac{(1 + iv/j)^j - (1 - iv/j)^j}{2i}.$$

But $(1 + z/j)^j = e^z$ from Chapter 7. Setting $z = iv$ in one factor and $z = -iv$ in the other:

$$\cos v = \frac{e^{iv} + e^{-iv}}{2},\qquad \sin v = \frac{e^{iv} - e^{-iv}}{2i}.$$

Adding $i\sin v$ to $\cos v$ gives the most famous identity in analysis:

$$e^{iv} = \cos v + i\sin v,\qquad e^{-iv} = \cos v - i\sin v.$$

(source: chapter8, §138). "From these equations we understand how complex exponentials can be expressed by real sines and cosines." See [[eulers-formula]].

### §139 — Logarithms of complex numbers and the arc

Let $n$ be infinitely small, $n = 1/j$ with $j$ infinitely large. Then $\cos(z/j) = 1$ and $\sin(z/j) = z/j$. From the §125 inverse-binomial identity $\log(1+x) = j((1+x)^{1/j} - 1)$, substitute $1 + x = \cos z + i\sin z$ and $\cos z - i\sin z$; the cosine equation gives a tautology, but the sine equation gives

$$\frac{z}{j} = \frac{\frac{1}{j}\log(\cos z + i\sin z) - \frac{1}{j}\log(\cos z - i\sin z)}{2i},$$

hence

$$z = \frac{1}{2i}\log\frac{\cos z + i\sin z}{\cos z - i\sin z}.$$

The arc itself is the imaginary part of a complex logarithm. See [[arctangent-series]].

### §140 — The arctangent series

Divide numerator and denominator inside the log by $\cos z$:

$$z = \frac{1}{2i}\log\frac{1 + i\tan z}{1 - i\tan z}.$$

But [[logarithmic-series|§123]] already gave $\log\frac{1+x}{1-x} = 2(x + x^3/3 + x^5/5 + \cdots)$. Substituting $x = i\tan z$ — and noting $i^2 = -1$ kills the even powers in the right way — yields

$$z = \tan z - \frac{(\tan z)^3}{3} + \frac{(\tan z)^5}{5} - \frac{(\tan z)^7}{7} + \cdots.$$

Calling the arc whose tangent is $t$ by $\arctan t$:

$$\arctan t = t - \frac{t^3}{3} + \frac{t^5}{5} - \frac{t^7}{7} + \cdots.$$

At $t = 1$: $z = \pi/4$ and Leibniz's formula

$$\frac{\pi}{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots.$$

(source: chapter8, §140). See [[arctangent-series]].

### §141 — Faster convergence via $\arctan(1/\sqrt 3)$

Leibniz's series converges too slowly for practical $\pi$ computation. Try instead $t = 1/\sqrt 3$, so $z = \pi/6$:

$$\frac{\pi}{6} = \frac{1}{\sqrt 3} - \frac{1}{3\cdot 3\sqrt 3} + \frac{1}{5\cdot 3^2\sqrt 3} - \cdots,$$

$$\pi = \frac{2\sqrt 3}{1} - \frac{2\sqrt 3}{3\cdot 3} + \frac{2\sqrt 3}{5\cdot 3^2} - \cdots.$$

Each term is about a third the previous, but every term is irrational. Euler's verdict: "By means of this series the value of $\pi$ itself, which was previously exhibited, was determined with incredible labor."

### §142 — Machin's decomposition

If $a + b = \pi/4$, then $\tan a\tan b = (1 - \tan a)/(1 + \tan a)$ via $\tan(a+b) = 1$. Choose $\tan a = 1/2$; then $\tan b = (1 - 1/2)/(1 + 1/2) = 1/3$, so

$$\frac{\pi}{4} = \arctan\frac{1}{2} + \arctan\frac{1}{3},$$

$$\pi = 4\left(\frac{1}{1\cdot 2} - \frac{1}{3\cdot 2^3} + \frac{1}{5\cdot 2^5} - \cdots\right) + 4\left(\frac{1}{1\cdot 3} - \frac{1}{3\cdot 3^3} + \frac{1}{5\cdot 3^5} - \cdots\right).$$

Both series are rational and converge geometrically — "with much more ease than with the series mentioned before." (source: chapter8, §142). See [[machin-like-formula]].

## Notable points

- **The chapter is a mirror of Chapter 7, with a quarter-turn in the complex plane.** Chapter 7 took $a^\omega = 1 + k\omega$ for an infinitesimal real $\omega$ and produced $e^z$ and $\log y$. Chapter 8 takes $\sin z = z$, $\cos z = 1$ for an infinitesimal real $z$ and produces the trig series; the identical machinery — collapse $(j-m)/(nj) = 1/n$, raise to the $j$-th power — works identically. The bridge §138 simply observes that the real and imaginary copies of the same machinery agree once $i$ is allowed.
- **Euler's formula is *forced* by the Chapter 7 machinery.** $e^{iv} = \cos v + i\sin v$ is not posited — it is the *only* way the §134 trig series and the §122 exponential series can coexist with De Moivre's formula. Euler does not present the identity as a deep insight but as an unavoidable computation.
- **Every value of every trig function is now computable.** The §134 series, refined by the §136–§137 reduction-to-30° tricks, gives any $\sin$, $\cos$, $\tan$, $\cot$, $\sec$, $\csc$ to arbitrary precision. The need for laborious geometric constructions in old trig tables disappears, just as the §123 logarithmic series replaced Briggs's geometric-mean computation.
- **$\pi$ enters the canon here, computed by a fast series.** Pre-Newtonian computations of $\pi$ relied on Archimedes-style polygon perimeters (slow, error-prone). Leibniz's $1 - 1/3 + 1/5 - \cdots$ is conceptually beautiful but practically useless. The Euler version (§141 with $t = 1/\sqrt 3$, §142 Machin-style) makes $\pi$ a routine table-lookup quantity. By this chapter's end, both $e$ and $\pi$ have been pinned down by rapidly convergent rational series.
- **"Logarithms of complex numbers" appears casually.** §139 writes $\log(\cos z + i\sin z)$ without flinching. It is well-defined (= $iz$) up to $2\pi i k$ — a multivaluedness Euler will treat properly only later. Here the focus is on extracting *real* arcs from the formula, and the multivaluedness is invisible.

## Why this chapter matters

Chapters 6, 7, 8 form a unit. After Chapter 6 introduces $a^z$ and $\log y$, Chapter 7 makes them analytic, and Chapter 8 does the same for $\sin$, $\cos$, $\tan$. The unifying observation — every "transcendental" Euler considers is the limit of a binomial expansion controlled by the same $(j-m)/j = 1$ identity — reduces the entire elementary transcendental world to a single technique.

The byproducts are immense: Euler's formula $e^{iv} = \cos v + i\sin v$ becomes the reusable instrument of the rest of the *Introductio*; the arctangent series is the main rapid-computation tool for $\pi$ from this point until the early 20th century; the Machin-style decomposition will be re-applied (with smaller fractions) to push $\pi$'s digit count into the hundreds within a few decades of the *Introductio*'s publication.

## Related pages

- [[pi]]
- [[sine-and-cosine]]
- [[trigonometric-addition-formulas]]
- [[trigonometric-recurrent-progression]]
- [[de-moivre-formula]]
- [[sine-and-cosine-series]]
- [[eulers-formula]]
- [[arctangent-series]]
- [[machin-like-formula]]
- [[infinitesimal-and-infinite-numbers]]
- [[exponential-series]]
- [[logarithmic-series]]
- [[eulers-number]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
