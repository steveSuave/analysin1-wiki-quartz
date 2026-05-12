# Euclidean Algorithm = Continued Fraction Expansion

**Summary**: For any rational $A/B$ with $A > B$, the Euclidean algorithm's successive quotients are exactly the partial denominators of $A/B$'s simple continued fraction expansion. The same algorithm applied to a long decimal expansion of an irrational produces (a truncation of) its infinite simple continued fraction — Euler uses this to verify $\sqrt 2 = [1; 2, 2, 2, \ldots]$, to discover the arithmetic-progression continued fraction for $(e-1)/2$, and (in §382) to find the convergents of $\pi$.

**Sources**: `chapter18` (§381).

**Last updated**: 2026-05-11

---

## The algorithm

Apply the Euclidean algorithm to $A$ and $B$ ($A > B$):

$$\begin{aligned}
A &= aB + C,\qquad &\text{so}\qquad \tfrac{A}{B} &= a + \tfrac{C}{B}, \\
B &= bC + D,\qquad &\text{so}\qquad \tfrac{B}{C} &= b + \tfrac{D}{C}, \\
C &= cD + E,\qquad &\text{so}\qquad \tfrac{C}{D} &= c + \tfrac{E}{D}, \\
D &= dE + F,\qquad &\text{so}\qquad \tfrac{D}{E} &= d + \tfrac{F}{E},
\end{aligned}$$

and so on. Substituting each line into the previous gives

$$\frac{A}{B} = a + \cfrac{1}{b + \cfrac{1}{c + \cfrac{1}{d + \cfrac{1}{e + \cdots}}}}.$$

The partial denominators of the simple continued fraction are exactly the *quotients* in the Euclidean algorithm; the algorithm terminates iff the input is rational, in which case the CF terminates with the same number of steps.

## Example I — $1461/59$ (§381)

$$\begin{aligned}
1461/59 &= 24 + 45/59,\\
59/45 &= 1 + 14/45,\\
45/14 &= 3 + 3/14,\\
14/3 &= 4 + 2/3,\\
3/2 &= 1 + 1/2,\\
2/1 &= 2 + 0.
\end{aligned}$$

So $\;1461/59 = [24; 1, 3, 4, 1, 2]$.

## Example II — verifying $\sqrt 2 = [1; 2, 2, 2, \ldots]$ (§381)

Take $\sqrt 2 \approx 1.41421356 = 141421356/10^8$ and run the algorithm:

$$\begin{aligned}
141421356/10^8 &= 1 + 41421356/10^8,\\
10^8/41421356 &= 2 + 17157288/41421356,\\
41421356/17157288 &= 2 + 7106780/17157288,\\
\vdots&
\end{aligned}$$

The quotients come out $1, 2, 2, 2, 2, \ldots$, matching the [[periodic-continued-fractions|§376 periodic continued fraction]] $1 + 1/(2 + 1/(2 + \cdots))$ for $\sqrt 2$.

## Example III — the continued fraction for $e$ (§381)

Running the algorithm on $(e - 1)/2 = 0.8591409142295\ldots$ produces the quotients $1, 6, 10, 14, 18, 22, \ldots$ — an arithmetic progression with common difference $4$. This is the [[continued-fraction-for-e|celebrated continued fraction for $e$]], discovered empirically by Euler running this decimal algorithm and asserted (he says) to be provable by "infinitesimal calculus."

## Why the algorithm yields best approximations

The convergents produced by the Euclidean-algorithm CF are exactly the [[best-rational-approximations|best rational approximations]] in the Wallis sense: any fraction with denominator at most $D_k$ that is closer to the target than $N_k/D_k$ does not exist. This is why §382 immediately applies the algorithm to $\pi = 3.14159265\ldots$ to obtain the famous convergents $3/1, 22/7, 333/106, 355/113, \ldots$ and to the solar-year fraction to derive the Gregorian leap-day rule.

## Related pages

- [[continued-fraction]]
- [[convergents-of-a-continued-fraction]]
- [[periodic-continued-fractions]] — Example II recovers the $\sqrt 2$ pattern
- [[continued-fraction-for-e]] — Example III discovers the AP pattern for $e$
- [[best-rational-approximations]] — §382 applies the algorithm to $\pi$ and the solar year
- [[chapter-18-on-continued-fractions]]
