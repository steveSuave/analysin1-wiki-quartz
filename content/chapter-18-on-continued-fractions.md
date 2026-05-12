# Chapter 18 — On Continued Fractions

**Summary**: Euler's closing chapter of Book I introduces the third kind of infinite expression — the continued fraction. It develops the convergent three-term recurrence and the alternation property, the bidirectional dictionary between continued fractions and alternating series (yielding Brouncker's $4/\pi$, a continued fraction for $\log 2$, and the celebrated $(e-1)/2$ continued fraction whose partial quotients form an arithmetic progression), the use of periodic continued fractions to approximate quadratic irrationals, the Euclidean-algorithm interpretation of rational continued fractions, and the best-rational-approximation principle — applied to $\pi \approx 355/113$ and to the leap-year calculation behind the Gregorian calendar.

**Sources**: `raw/chapter18.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 18: "On Continued Fractions", §356–§382).

**Last updated**: 2026-05-11

---

## Context

Euler opens (§356) by announcing the topic as a "third kind of infinite expression," alongside the infinite series of chapters 4–17 and the infinite products of chapters 9–11. He predicts that continued fractions "will be much more widely used in the analysis of the infinite in the times to come," especially in arithmetic and algebra — a prediction borne out by Lagrange, Gauss, and the 19th-century number theorists.

A [[continued-fraction]] in Euler's notation takes one of two forms: with all numerators 1 (the *simple* form),

$$a + \cfrac{1}{b + \cfrac{1}{c + \cfrac{1}{d + \cdots}}}\,,$$

or with arbitrary numerators $\alpha, \beta, \gamma, \ldots$ (the *generalised* form),

$$a + \cfrac{\alpha}{b + \cfrac{\beta}{c + \cfrac{\gamma}{d + \cdots}}}\,.$$

## Movement 1 — Convergents (§358–§362)

Truncating the continued fraction after $n$ levels produces a sequence of [[convergents-of-a-continued-fraction|convergents]] whose numerators and denominators each obey the same three-term linear recurrence. Euler tabulates the law:

$$N_k = b_k\,N_{k-1} + \beta_k\,N_{k-2},\qquad D_k = b_k\,D_{k-1} + \beta_k\,D_{k-2},$$

with the cosmetic prefix $1/0$ before $a/1$ so that the recurrence applies from the start. In the simple form $\beta_k = 1$. The convergents alternate around the true value, each closer than its predecessor — so the truncations are simultaneously *good rational approximations*.

## Movement 2 — Continued fraction → alternating series (§363–§364)

Subtracting consecutive convergents gives the [[continued-fraction-series-equivalence|telescoping identity]]

$$z = a + \frac{\alpha}{P} - \frac{\alpha\beta}{PQ} + \frac{\alpha\beta\gamma}{QR} - \frac{\alpha\beta\gamma\delta}{RS} + \cdots$$

where $P, Q, R, S, \ldots$ are the successive denominators of the convergents. So every continued fraction is also an alternating series.

## Movement 3 — Alternating series → continued fraction (§365–§373)

Conversely, given $x = A - B + C - D + E - \cdots$, Euler matches term by term against the §363 expansion and shows that the partial numerators $\alpha, \beta, \gamma, \ldots$ are determined up to the free choice of partial denominators $b, c, d, \ldots$ (§366–§367). Choosing the partial denominators to clear fractions yields several elegant *templates* (§368–§373):

- $x = A - B + C - D + \cdots$ with $A, B, \ldots$ integers gives
  $\displaystyle x = \cfrac{A}{1 + \cfrac{B}{A - B + \cfrac{AC}{B - C + \cfrac{BD}{C - D + \cdots}}}}$
- $x = 1/A - 1/B + 1/C - \cdots$ gives
  $\displaystyle x = \cfrac{1}{A + \cfrac{A^2}{B - A + \cfrac{B^2}{C - B + \cdots}}}$
- $x = 1/A - 1/(AB) + 1/(ABC) - \cdots$ gives
  $\displaystyle x = \cfrac{1}{A + \cfrac{A}{B - 1 + \cfrac{B}{C - 1 + \cdots}}}$
- Power-series and product-power templates in §371–§373.

The named identities that drop out are:

- [[continued-fraction-for-log-2]] (§369 Example I): $\log 2 = 1/(1 + 1/(1 + 4/(1 + 9/(1 + 16/(1 + \cdots)))))$ — partial numerators are the squares.
- [[brouncker-formula]] (§369 Example II): $4/\pi = 1 + 1^2/(2 + 3^2/(2 + 5^2/(2 + 7^2/(2 + \cdots))))$ — partial numerators are the odd squares.
- §370 Example IV: continued fraction for $\pi\cos(m\pi/n)/(n\sin(m\pi/n))$ via the [[cotangent-partial-fraction|§178]] partial-fraction series.
- §373 Example I: continued fraction for $1/(e - 1)$ via the alternating $1/n!$ series.
- §373 Example II: continued fraction for $\cos 1$ via the alternating $1/(2!4!6!\cdots)$ series.

## Movement 4 — When the conversion fails (§374–§375)

Although series-to-continued-fraction always works in principle, the converse — given a continued fraction whose value we don't know, find the series and sum it — typically fails. Euler illustrates with $x = 1/(2 + 1/(2 + 1/(2 + \cdots)))$ which the series identity rewrites as

$$x = \tfrac{1}{2} - \tfrac{1}{2\cdot 5} + \tfrac{1}{5\cdot 12} - \tfrac{1}{12\cdot 29} + \cdots,$$

a strongly convergent series whose value is *not* obvious from the series itself, but which §376 immediately recovers from the continued fraction as $\sqrt 2 - 1$.

## Movement 5 — Periodic continued fractions (§376–§379)

If the partial denominators repeat with period $k$, the continued fraction satisfies a polynomial equation of degree at most $2$, so its value is a [[periodic-continued-fractions|quadratic irrational]]. Single-letter period (§377): $x = 1/(a + x)$ gives $x = (\sqrt{a^2 + 4} - a)/2$, so for $a = 1, 2, 3, 4, \ldots$ we obtain $\sqrt 5, \sqrt 2, \sqrt{13}, \sqrt 5, \sqrt{29}, \sqrt{10}, \sqrt{53}, \ldots$. Two-letter periods (§378) give the roots of $ax^2 + abx = b$, extending the catalog to all square roots. The §378 worked example computes $\sqrt 7$ with error $< 3/10^7$ from six convergents.

## Movement 6 — Quadratic equations (§380)

The same equation $x^2 = ax + b$ that produced the periodic continued fraction can be solved *by* a continued fraction: $x = a + b/x$ substituted into itself gives $x = a + b/(a + b/(a + b/(a + \cdots)))$ — but with numerators $b \neq 1$ this is "not too convenient" compared with the simple-form CF.

## Movement 7 — Rational continued fractions = Euclidean algorithm (§381)

Any rational $A/B$ with $A > B$ has a *finite* continued fraction whose partial quotients are exactly the [[euclidean-algorithm-continued-fraction|Euclidean-algorithm quotients]] of $A$ and $B$. The same procedure applied to a long decimal expansion of an irrational produces its (infinite) simple-CF expansion — Example II recovers $\sqrt 2 = [1; 2, 2, 2, \ldots]$ matching §376, and **Example III** computes $(e-1)/2 = [0; 1, 6, 10, 14, 18, 22, 26, 30, 34, \ldots]$ — partial quotients forming an arithmetic progression with common difference $4$. This is the [[continued-fraction-for-e|celebrated continued fraction for $e$]], confirmed (Euler notes) by "infinitesimal calculus."

## Movement 8 — Best rational approximations (§382)

The convergents are the [[best-rational-approximations|best rational approximations]] in the Wallis sense: no fraction with smaller denominator gives a closer approximation. **Example I** applies this to $\pi$: from the partial quotients $3, 7, 15, 1, 292, 1, 1, \ldots$ the convergents $3/1, 22/7, 333/106, \mathbf{355/113}, 103993/33102, \ldots$ give the *Archimedean* and *Metian* ratios — with $355/113$ accurate to better than $1/(113\cdot 33102)$. **Example II** does the same for the solar year $365 + 20935/86400$ days, whose convergents $1/4, 7/29, \mathbf{8/33}, \ldots, 181/747$ give the leap-day-frequency progression from the Julian calendar (1 in 4) up to the *Gregorian* compromise (97 in 400) — Euler's last calculation before "END OF THE FIRST BOOK."

## Related pages

- [[continued-fraction]]
- [[convergents-of-a-continued-fraction]]
- [[continued-fraction-series-equivalence]]
- [[brouncker-formula]]
- [[continued-fraction-for-log-2]]
- [[continued-fraction-for-e]]
- [[periodic-continued-fractions]]
- [[euclidean-algorithm-continued-fraction]]
- [[best-rational-approximations]]
- [[arctangent-series]] — the Leibniz $\pi/4$ series sieved in chapter 15 and converted to Brouncker here
- [[logarithmic-series]] — $\log 2$ series, converted in §369 Example I
- [[eulers-number]] — first appearance of $e$; the CF in §381 Example III
