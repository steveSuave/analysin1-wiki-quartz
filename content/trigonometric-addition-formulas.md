# Trigonometric Addition Formulas

**Summary**: §128, §130, §131 of Chapter 8. Starting from the four sum/difference identities $\sin(y \pm z) = \sin y\cos z \pm \cos y\sin z$ and $\cos(y \pm z) = \cos y\cos z \mp \sin y\sin z$ — taken as known — Euler generates the entire algebraic apparatus of trigonometry: the periodicity catalog for $\sin$ and $\cos$ of $(4n+k)\pi/2 \pm z$, the product-to-sum and sum-to-product theorems, the half-angle formulas, and a family of derived ratios.

**Sources**: chapter8.pdf (§128, §130, §131)

**Last updated**: 2026-04-27

---

## §128 — The four base identities

Euler takes the four sum/difference formulas as part of "what is known from trigonometry":

$$\sin(y + z) = \sin y\cos z + \cos y\sin z,\qquad \sin(y - z) = \sin y\cos z - \cos y\sin z,$$

$$\cos(y + z) = \cos y\cos z - \sin y\sin z,\qquad \cos(y - z) = \cos y\cos z + \sin y\sin z.$$

These are not derived in the *Introductio*; their geometric proof is left to standard trigonometry. Every later identity in the chapter is a consequence of these four together with the [[sine-and-cosine|Pythagorean identity]] $(\sin z)^2 + (\cos z)^2 = 1$.

## §128 — The periodicity catalog

Substituting $y = \pi/2, \pi, 3\pi/2, 2\pi$ produces the full quadrant-shift table:

$$\sin(\pi/2 + z) = +\cos z,\qquad \sin(\pi/2 - z) = +\cos z,$$

$$\cos(\pi/2 + z) = -\sin z,\qquad \cos(\pi/2 - z) = +\sin z,$$

$$\sin(\pi + z) = -\sin z,\qquad \sin(\pi - z) = +\sin z,$$

$$\cos(\pi + z) = -\cos z,\qquad \cos(\pi - z) = -\cos z,$$

$$\sin(3\pi/2 + z) = -\cos z,\qquad \sin(3\pi/2 - z) = -\cos z,$$

$$\cos(3\pi/2 + z) = +\sin z,\qquad \cos(3\pi/2 - z) = -\sin z,$$

$$\sin(2\pi + z) = +\sin z,\qquad \sin(2\pi - z) = -\sin z,$$

$$\cos(2\pi + z) = +\cos z,\qquad \cos(2\pi - z) = +\cos z.$$

Euler then states the general law: for any integer $n$ (positive or negative), the eight cases

$$\sin\bigl(\tfrac{4n+k}{2}\pi \pm z\bigr),\qquad \cos\bigl(\tfrac{4n+k}{2}\pi \pm z\bigr),\qquad k = 1, 2, 3, 4$$

reduce to $\pm \sin z$ or $\pm \cos z$ according to a $k$-mod-4 cycle (source: chapter8.pdf, §128). This is the periodicity-with-period-$2\pi$ statement, plus the half-period symmetries.

## §130 — Product-to-sum

Adding and subtracting the §128 sum/difference formulas:

$$\sin y\cos z = \tfrac12\bigl(\sin(y+z) + \sin(y-z)\bigr),$$

$$\cos y\sin z = \tfrac12\bigl(\sin(y+z) - \sin(y-z)\bigr),$$

$$\cos y\cos z = \tfrac12\bigl(\cos(y-z) + \cos(y+z)\bigr),$$

$$\sin y\sin z = \tfrac12\bigl(\cos(y-z) - \cos(y+z)\bigr).$$

These convert products of trig values into sums — useful when integrating, multiplying tabulated entries, or analyzing recurrences (cf. [[trigonometric-recurrent-progression]]).

## §130 — Half-angle

Setting $y = z = v/2$ in the cosine product-to-sum formulas:

$$\bigl(\cos(v/2)\bigr)^2 = \frac{1 + \cos v}{2},\qquad \bigl(\sin(v/2)\bigr)^2 = \frac{1 - \cos v}{2},$$

hence

$$\cos\frac{v}{2} = \sqrt{\frac{1 + \cos v}{2}},\qquad \sin\frac{v}{2} = \sqrt{\frac{1 - \cos v}{2}}.$$

(source: chapter8.pdf, §130). Reading the formula in reverse: knowing $\cos v$ determines $\sin(v/2)$ and $\cos(v/2)$. Iteration of this halving is the core of the §136 table-construction strategy and is the trigonometric analogue of the [[geometric-mean-method-for-logarithms|geometric-mean method]] for logarithms.

## §131 — Sum-to-product

Change variables: let $a = y + z$, $b = y - z$, so $y = (a+b)/2$, $z = (a-b)/2$. Substituting in §130's product-to-sum identities and rearranging gives the four sum-to-product theorems:

$$\sin a + \sin b = 2\sin\tfrac{a+b}{2}\cos\tfrac{a-b}{2},$$

$$\sin a - \sin b = 2\cos\tfrac{a+b}{2}\sin\tfrac{a-b}{2},$$

$$\cos a + \cos b = 2\cos\tfrac{a+b}{2}\cos\tfrac{a-b}{2},$$

$$\cos a - \cos b = -2\sin\tfrac{a+b}{2}\sin\tfrac{a-b}{2}.$$

(source: chapter8.pdf, §131). These convert sums of sines/cosines into products — useful when factoring trigonometric polynomials and when reading off ratios.

## §131 — Derived ratios

Dividing the §131 identities pairwise produces a family of ratio-and-product identities:

$$\frac{\sin a + \sin b}{\sin a - \sin b} = \frac{\tan\tfrac{a+b}{2}}{\tan\tfrac{a-b}{2}},$$

$$\frac{\sin a + \sin b}{\cos a + \cos b} = \tan\tfrac{a+b}{2},\qquad \frac{\sin a + \sin b}{\cos b - \cos a} = \cot\tfrac{a-b}{2},$$

$$\frac{\sin a - \sin b}{\cos a + \cos b} = \tan\tfrac{a-b}{2},\qquad \frac{\sin a - \sin b}{\cos b - \cos a} = \cot\tfrac{a+b}{2},$$

$$\frac{\cos a + \cos b}{\cos b - \cos a} = \cot\tfrac{a+b}{2}\cot\tfrac{a-b}{2},$$

$$\frac{\sin a + \sin b}{\cos a + \cos b} = \frac{\cos b - \cos a}{\sin a - \sin b},$$

$$\frac{\sin a + \sin b}{\sin a - \sin b}\cdot\frac{\cos a + \cos b}{\cos b - \cos a} = \cot^2\tfrac{a-b}{2},$$

$$\frac{\sin a + \sin b}{\sin a - \sin b}\cdot\frac{\cos b - \cos a}{\cos a + \cos b} = \tan^2\tfrac{a+b}{2}.$$

Each is a one-line consequence of §131. Euler's purpose in writing them all out is mostly catalogue: every standard identity of high-school trigonometry is on the table for use in later chapters.

## How these formulas are used in Chapter 8

- [[trigonometric-recurrent-progression|§129]] uses the §128 sum/difference formulas to derive the recurrent-progression structure of $\sin(ky + z)$ and $\cos(ky + z)$.
- §136 uses the §131 sum-to-product formulas (with $y = \pi/6$) to extend a table of sines and cosines from arcs $\le 30°$ to arcs in $[30°, 60°]$, and hence to all arcs by periodicity.
- §137 uses $\tan(2a) = 2\tan a/(1 - \tan^2 a)$ (a one-line consequence of §128 applied to $\tan = \sin/\cos$) for the same extension on tangents and cotangents.

## Related pages

- [[sine-and-cosine]]
- [[pi]]
- [[trigonometric-recurrent-progression]]
- [[de-moivre-formula]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
