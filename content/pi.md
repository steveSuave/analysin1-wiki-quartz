# $\pi$

**Summary**: §126 of Chapter 8. With the radius of the circle taken as 1, half the circumference is irrational. Euler reports its decimal expansion to about 113 digits and writes: "For the sake of brevity we will use the symbol $\pi$ for this number." This is the moment $\pi$ is established in mainstream mathematical notation.

**Sources**: chapter8.pdf (§126)

**Last updated**: 2026-04-27

---

## Setup

Euler fixes the convention that anchors all of trigonometry in the *Introductio*: the radius of the circle is 1. Under this convention the *arc length* and the *angle measure in radians* coincide, so the sine and cosine become functions of arc length rather than of an angular degree. The full circumference of the unit circle is then $2\pi$, the semicircle is $\pi$, and 90° corresponds to the arc $\pi/2$.

## The decimal expansion

Euler quotes the value of $\pi$ to about 113 digits (source: chapter8.pdf, §126):

$$\pi = 3.14159\,26535\,89793\,23846\,26433\,83279\,50288\,41971\,69399\,37510\,58209\,74944\,5923\ldots$$

(continuing to ~113 digits before he ends with "+", indicating the next digit). He notes that $\pi$ "cannot be expressed exactly as a rational number" — the irrationality is taken as known, not proved here. Lambert's proof of the irrationality of $\pi$ would not appear until 1761; Euler simply asserts the fact based on the failure of rational candidates.

The digits Euler reports here were computed before the *Introductio* by laborious classical methods — chiefly Archimedes-style polygon perimeters, refined by Ludolph van Ceulen (35 digits, c. 1610) and others. The chapter's later sections (§141–§142) replace those laborious methods with rapidly convergent [[arctangent-series|arctangent series]].

## The symbol $\pi$

Euler writes "we will use the symbol $\pi$ for this number." He is not the first to use the letter (William Jones, 1706, was earlier), but the *Introductio*'s circulation made the notation universal. From this section onward in the wiki — and from this section onward in mathematics — $\pi$ denotes the half-circumference of the unit circle.

The convention "$\pi$ is half the circumference, not the full one" is also Euler's choice. It survives because most circle and trig identities (e.g. $\sin\pi = 0$, $\cos\pi = -1$, $\sin(\pi/2) = 1$) read more naturally with this convention.

## Status of $\pi$ as a transcendental

By the time Chapter 8 begins, [[transcendence-of-logarithms|§105]] has already established the heuristic that "generic" outputs of transcendental functions are themselves transcendental, but Euler does not invoke that machinery for $\pi$ here. He simply notes the irrationality. The full transcendence of $\pi$ is Lindemann (1882), more than a century after Euler.

## How $\pi$ enters the rest of the chapter

- The arcs $\pi/2, \pi, 3\pi/2, 2\pi$ generate the periodicity catalog of [[trigonometric-addition-formulas|§128]].
- The half-arc $\pi/6$ is the pivot for the table-construction strategy of §136 — sines and cosines from 30° to 60° are derived from those of arcs below 30°.
- The series of [[sine-and-cosine-series|§134]] for $\sin(m\pi/(2n))$ and $\cos(m\pi/(2n))$ all carry $\pi/2$ as the leading coefficient, in the form $\pi/2 = 1.5707963267948966192313216916\ldots$ (a 28-digit value carved out of Euler's series).
- The [[arctangent-series|arctangent series]] of §140 lets $\pi$ itself be computed as $4\arctan 1$ (Leibniz), $6\arctan(1/\sqrt 3)$ (§141), or $4(\arctan(1/2) + \arctan(1/3))$ ([[machin-like-formula|§142]]).

## Later appearances in the *Introductio*

- [[basel-problem|§167]]: $\sum 1/k^2 = \pi^2/6$, and the [[zeta-at-even-integers|table of $\zeta(2k)$]] extending through $\zeta(26)$.
- [[wallis-product|§185]]: $\pi/2 = (2\cdot 2\cdot 4\cdot 4\cdot 6\cdot 6\cdots)/(1\cdot 3\cdot 3\cdot 5\cdot 5\cdot 7\cdots)$, the Wallis product, derived from the redundancy of two §184 product expressions for $\cos(m\pi/2n)$.
- [[log-pi-via-products|§188–§190]]: $\log_e\pi = 1.144729885849400174\ldots$ computed by transposing $\sum\log(1 - 1/(2k+1)^2)$ into a doubly-summed series whose columns are the [[zeta-at-even-integers|odd-square sums $A, B, C, \ldots$]].
- [[brouncker-formula|§369]]: $4/\pi = 1 + 1^2/(2 + 3^2/(2 + 5^2/(2 + \cdots)))$, the Brouncker continued fraction obtained by converting the Leibniz series.
- [[best-rational-approximations|§382]]: best rational approximations $22/7, 333/106, 355/113, 103993/33102$ from the Euclidean-algorithm continued-fraction expansion of $\pi$.

## Related pages

- [[sine-and-cosine]]
- [[trigonometric-addition-formulas]]
- [[sine-and-cosine-series]]
- [[arctangent-series]]
- [[machin-like-formula]]
- [[basel-problem]]
- [[wallis-product]]
- [[log-pi-via-products]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
- [[brouncker-formula]]
- [[best-rational-approximations]]
- [[chapter-18-on-continued-fractions]]
