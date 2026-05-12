# Infinite Products for Tangent, Cotangent, Secant, Cosecant

**Summary**: §186–§187: dividing the [[linear-factors-of-sine-cosine|§184 linear-factor products]] for $\sin(m\pi/2n)$ by the corresponding ones for $\cos(m\pi/2n)$ yields infinite product representations for $\tan(m\pi/2n)$, $\cot(m\pi/2n)$, $\sec(m\pi/2n)$, $\csc(m\pi/2n)$. Replacing $m$ with another integer $k$ in the §184 formulas gives products for ratios $\sin(m\pi/2n)/\sin(k\pi/2n)$ and similar — once one trig value is known, all the others at the same denominator $2n$ follow without further computation.

**Sources**: chapter11.pdf

**Last updated**: 2026-05-01

---

## Tangent and cotangent

Dividing the *first* sine expression by the *first* cosine expression in [[linear-factors-of-sine-cosine|§184]]:

$$\tan\frac{m\pi}{2n} = \frac{m\pi/2n\cdot(2n - m)/2n\cdot(2n + m)/2n\cdots}{(n - m)/n\cdot(n + m)/n\cdot(3n - m)/3n\cdot(3n + m)/3n\cdots}$$

Pairing numerator and denominator factors of similar size and simplifying:

$$\boxed{\;\tan\frac{m\pi}{2n} = \frac{m}{n - m}\cdot\frac{2n - m}{n + m}\cdot\frac{2n + m}{3n - m}\cdot\frac{4n - m}{3n + m}\cdot\frac{4n + m}{5n - m}\cdots\;}$$

(source: chapter11.pdf, §186). The cotangent is the reciprocal:

$$\cot\frac{m\pi}{2n} = \frac{n - m}{m}\cdot\frac{n + m}{2n - m}\cdot\frac{3n - m}{2n + m}\cdot\frac{3n + m}{4n - m}\cdot\frac{5n - m}{4n + m}\cdots$$

## Secant and cosecant

The secant is $1/\cos$, but with the §184 cosine in the *denominator* form, the simplest expression is

$$\sec\frac{m\pi}{2n} = \frac{n}{n - m}\cdot\frac{n}{n + m}\cdot\frac{3n}{3n - m}\cdot\frac{3n}{3n + m}\cdot\frac{5n}{5n - m}\cdot\frac{5n}{5n + m}\cdots$$

Likewise, $\csc(m\pi/2n) = 1/\sin(m\pi/2n)$:

$$\csc\frac{m\pi}{2n} = \frac{n}{m}\cdot\frac{2n}{2n - m}\cdot\frac{2n}{2n + m}\cdot\frac{4n}{4n - m}\cdot\frac{4n}{4n + m}\cdots$$

(source: chapter11.pdf, §186). Each is a straightforward rearrangement of one of the four §184 products.

## Variants from the second pair

Using the *second* §184 expression (the one obtained via the co-function identity) in the quotient gives a different-looking formula for the same value. For tangent:

$$\tan\frac{m\pi}{2n} = \frac{\pi}{2}\cdot\frac{m}{n - m}\cdot\frac{1}{2}\cdot\frac{2n - m}{n + m}\cdot\frac{3}{2}\cdot\frac{2n + m}{3n - m}\cdot\frac{3}{4}\cdot\frac{4n - m}{3n + m}\cdots$$

(source: chapter11.pdf, §186). The redundancy mirrors the §185 [[wallis-product|Wallis]] phenomenon: two formulas for the same value differ by a Wallis-style factor that telescopes to $\pi/2$.

## Ratios — §187

Replace $m$ by another integer $k$ in the §184 sine formula: the ratio

$$\frac{\sin(m\pi/2n)}{\sin(k\pi/2n)}$$

is an infinite product whose factors come in pairs from the corresponding terms of the two products. For instance:

$$\frac{\sin(m\pi/2n)}{\sin(k\pi/2n)} = \frac{m}{k}\cdot\frac{2n - m}{2n - k}\cdot\frac{2n + m}{2n + k}\cdot\frac{4n - m}{4n - k}\cdot\frac{4n + m}{4n + k}\cdots$$

(source: chapter11.pdf, §187). Analogous formulas hold for $\sin/\cos$, $\cos/\cos$, etc. Euler's remark: "if we take $k\pi/2n$ as an angle whose sine and cosine are known, by means of the above formulas, we can find the sine and cosine of any other angle $m\pi/2n$" (source: chapter11.pdf, §187). One trig table entry generates all the others at the same denominator.

## Why two expressions per function?

Because the [[linear-factors-of-sine-cosine|§184 linear-factor split]] gives two product formulas for *each* of $\sin(m\pi/2n)$ and $\cos(m\pi/2n)$ — one direct, one via the co-function — the four functions $\tan, \cot, \sec, \csc$ all inherit two expressions each. Comparing the two routinely yields the [[wallis-product|Wallis-style identity]] $\pi/2 = (2/1)(2/3)(4/3)(4/5)\cdots$ as a "calibration constant" between them.

## Computational use

These products are *not* the practical route to numerical values of the trig functions: like Wallis, they converge geometrically in $1/k^2$ and need many factors per digit. Their value in chapter 11 is structural, not computational:

- The redundancy generates the [[wallis-product|Wallis product]] (§185).
- The ratio formulas (§187) reduce the *number* of independent table entries needed.
- The §188–§198 *log* trick — taking $\log$, expanding via the [[logarithmic-series|§118 series]], transposing the resulting double sum — converts even slowly-convergent products like these into fast-convergent series. See [[log-sine-via-products]].

For *direct* numerical computation of $\tan, \cot$, the better route is the [[cotangent-partial-fraction|§181 partial-fraction expansion]], which Euler picks up in §197–§198 of this same chapter.

## Related pages

- [[linear-factors-of-sine-cosine]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[wallis-product]]
- [[log-sine-via-products]]
- [[cotangent-partial-fraction]]
- [[trigonometric-addition-formulas]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
