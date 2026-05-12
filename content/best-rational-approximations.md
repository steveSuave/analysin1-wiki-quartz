# Best Rational Approximations

**Summary**: Euler's closing principle of the *Introductio* (§382, attributed to Wallis): the convergents of a continued fraction are the *best* rational approximations to its value — no fraction with smaller denominator gives a closer approximation. He applies this to two famous problems: the rational approximation of $\pi$ (giving the Archimedean $22/7$, the Metian $355/113$, and the cosmically accurate $103993/33102$), and the leap-year calculation for the solar year (giving $1/4$ as the Julian rule and $97/400$ as the Gregorian compromise).

**Sources**: `chapter18` (§382).

**Last updated**: 2026-05-11

---

## The principle

Euler (§382, attributing the formulation to Wallis): "Our fractions, obtained by this method, have a value so close to the continued fraction from which they come, that there are no other numbers, unless they be larger, which give a closer approximation."

Modern statement: if $N_k/D_k$ is the $k$-th convergent of the simple continued fraction expansion of $x$, then for every rational $p/q$ with $0 < q < D_{k+1}$ that is not itself a convergent of $x$, we have $|x - N_k/D_k| < |x - p/q|$.

The proof uses the [[convergents-of-a-continued-fraction|three-term recurrence]] and the [[continued-fraction-series-equivalence|telescoping-difference identity]]: the error of the $k$-th convergent is bounded by $1/(D_k D_{k+1})$, while any non-convergent rational with comparable denominator does worse by an amount controllable from the same recurrence.

## Example I — Rational approximations of $\pi$ (§382)

Apply the [[euclidean-algorithm-continued-fraction|Euclidean algorithm]] to $\pi = 3.14159265\ldots$. The successive quotients are

$$3, 7, 15, 1, 292, 1, 1, \ldots$$

and the resulting convergents are

$$\frac{3}{1},\quad \frac{22}{7},\quad \frac{333}{106},\quad \frac{355}{113},\quad \frac{103993}{33102},\quad \ldots$$

Euler comments on each:

- $\mathbf{3/1}$: "the ratio of the diameter to circumference to be $1:3$ … the most accurate approximation unless larger numbers are used."
- $\mathbf{22/7}$: the *Archimedean* ratio (Archimedes' bound $223/71 < \pi < 22/7$).
- $\mathbf{355/113}$: the *Metian* ratio (after the Dutch engineer Adriaan Metius, 1571–1635). Euler notes the error is less than $1/(113\cdot 33102)$ — i.e., better than $1/3{,}700{,}000$, accurate to about 7 decimal places. The unusually large next quotient ($292$) is *why* $355/113$ is so good: the next convergent denominator $33102$ is enormous compared to $113$, so the error at $113$ is suppressed by a factor of about $292$.

Convergents alternate above and below $\pi$, as is true for every continued fraction.

## Example II — The solar year and the Gregorian calendar (§382)

The solar year is $365$ days, $5$ hours, $48$ minutes, $55$ seconds. Convert the excess over $365$ days to a fraction of a day:

$$\frac{5\cdot 3600 + 48\cdot 60 + 55}{86400} = \frac{20935}{86400}\ \text{days}.$$

Apply the [[euclidean-algorithm-continued-fraction|Euclidean algorithm]]: quotients are

$$4, 71, 1, 6, 1, 2, 2, 4$$

(a *finite* CF because $20935/86400$ is rational). The convergents are

$$\frac{0}{1},\quad \frac{1}{4},\quad \frac{7}{29},\quad \frac{8}{33},\quad \frac{55}{227},\quad \frac{63}{260},\quad \frac{181}{747}.$$

Euler reads off each:

- $\mathbf{1/4}$: "about one day in four years" — the **Julian** rule, instituted by Julius Caesar in 45 BCE. One extra day every $4$ years.
- $\mathbf{8/33}$: "more exact, however, is the eight days in 33 years, or 181 days in 747 years." This is the so-called *Persian calendar* rule (used in the Jalali calendar).
- $\mathbf{97/400}$: in $400$ years the Julian calendar inserts $100$ extra days, but the true year requires only $\approx 97.0125$. The **Gregorian** reform of 1582 fixed this by removing three leap days every $400$ years (the years divisible by $100$ but not $400$). Euler notes: "in 400 years there are 97 extra days, while the Julian calendar gives 100 extra days. This is the reason that the Gregorian calendar in 400 years converts three years, which would be leap years, into ordinary years."

Note that $97/400$ is not literally a convergent — but it is a close convergent-like compromise; the actual convergent path through $\ldots, 55/227, 63/260, 181/747$ approaches the true ratio $20935/86400 = 0.24230\ldots$ while $97/400 = 0.2425$ matches to four decimals and uses an arithmetically convenient century-aligned denominator.

## Closing line

Euler's calculation of $97/400$ as the rational approximation behind the Gregorian leap-year rule is the *last computation* in Book I of the *Introductio*. The chapter — and the book — ends with:

> **END OF THE FIRST BOOK.**

## Related pages

- [[continued-fraction]]
- [[convergents-of-a-continued-fraction]]
- [[euclidean-algorithm-continued-fraction]] — the procedure used to obtain the partial quotients
- [[periodic-continued-fractions]] — gives best approximations to quadratic irrationals
- [[pi]] — the constant being approximated in Example I
- [[brouncker-formula]] — a different (much worse-converging) continued fraction for $\pi$
- [[chapter-18-on-continued-fractions]]
