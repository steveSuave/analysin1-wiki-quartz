# Sine and Cosine

**Summary**: §127 of Chapter 8. With the unit-circle convention (radius $= 1$, [[pi|$\pi$]] = half the circumference), Euler names two functions of an arc $z$: $\sin z$ and $\cos z$. He fixes special values, the Pythagorean identity $(\sin z)^2 + (\cos z)^2 = 1$, the co-function relation $\cos z = \sin(\pi/2 - z)$, and the derived ratios $\tan z = \sin z/\cos z$ and $\cot z = \cos z/\sin z$. Sine and cosine are introduced as functions of arc length, not as ratios in a triangle.

**Sources**: chapter8.pdf (§127)

**Last updated**: 2026-04-27

---

## Definition by arc

The radius of the circle is 1; let $z$ be an arc of this circle. Euler writes $\sin z$ for *the sine of the arc $z$* and $\cos z$ for *the cosine of the arc $z$* (source: chapter8.pdf, §127). On the unit circle these are exactly the perpendicular and parallel components of the radius drawn to the endpoint of the arc — the same quantities classical geometry called the half-chord and the apothem-like projection — and they coincide with the angle measure in radians, since arc length = angle on the unit circle.

This is a notational shift relative to pre-Eulerian trigonometry. Pre-Euler tables tabulated *sin* and *cos* of an angle measured in degrees, on a circle of radius typically $10^7$ for precision. Euler measures the input as an *arc* and uses radius 1, so $\sin z$ and $\cos z$ are pure dimensionless real numbers in $[-1, 1]$ — exactly the modern conventions.

## Special values

Euler tabulates:

| arc $z$ | $\sin z$ | $\cos z$ |
|:--|:--|:--|
| $0$ | $0$ | $1$ |
| $\pi/2$ | $1$ | $0$ |
| $\pi$ | $0$ | $-1$ |
| $3\pi/2$ | $-1$ | $0$ |
| $2\pi$ | $0$ | $1$ |

All six values follow from the geometric interpretation on the unit circle. Periodicity with period $2\pi$ is implicit: every arc reduces modulo $2\pi$ to one in $[0, 2\pi)$, and the table extends to all reals.

## The Pythagorean identity

$$(\sin z)^2 + (\cos z)^2 = 1.$$

Euler states this as *the* fundamental algebraic relation between $\sin z$ and $\cos z$ (source: chapter8.pdf, §127). It encodes the geometry: $\sin z$ and $\cos z$ are the legs of a right triangle whose hypotenuse is the radius. In Chapter 8 the identity will be repeatedly factored as

$$1 = (\cos z + i\sin z)(\cos z - i\sin z),$$

and that complex factorization (§132) is the gateway to [[de-moivre-formula|De Moivre's formula]] and ultimately [[eulers-formula|Euler's formula]].

## Co-function relations

Every sine is a cosine of the complementary arc:

$$\cos z = \sin(\pi/2 - z),\qquad \sin z = \cos(\pi/2 - z).$$

Geometrically these are reflections of the unit circle across the line $y = x$. They generalize at §128 to the full periodicity table for $\sin\bigl((4n+k)\pi/2 \pm z\bigr)$.

## Sine is bounded between $-1$ and $+1$

Euler notes (§127) that "every sine and cosine lies between $+1$ and $-1$." This is built into the unit-circle definition: the projections of a point on the unit circle onto the two axes have absolute value at most 1.

## Tangent, cotangent, secant, cosecant

The four derived ratios:

$$\tan z = \frac{\sin z}{\cos z},\qquad \cot z = \frac{\cos z}{\sin z} = \frac{1}{\tan z}.$$

Secant and cosecant (introduced indirectly via §137) are $\sec z = 1/\cos z$, $\csc z = 1/\sin z$. Euler treats these as derived quantities; the primary objects are $\sin$ and $\cos$.

## Why functions of *arc* and not angle

Two reasons surface in subsequent sections:

1. The §134 series $\sin v = v - v^3/3! + v^5/5! - \cdots$ and $\cos v = 1 - v^2/2! + v^4/4! - \cdots$ are clean *only* when the input is an arc (i.e., radians). Inputs in degrees would carry irrational conversion factors $\pi/180$ in every term.
2. The bridge to logarithms and exponentials in §138 — $e^{iv} = \cos v + i\sin v$ — likewise requires the radian convention. Other choices muddy the analysis.

The decision to measure arcs rather than angles is therefore not cosmetic. It is the decision that makes [[sine-and-cosine-series|the trig series]] simple and [[eulers-formula|Euler's formula]] possible.

## Related pages

- [[pi]]
- [[trigonometric-addition-formulas]]
- [[sine-and-cosine-series]]
- [[de-moivre-formula]]
- [[eulers-formula]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
