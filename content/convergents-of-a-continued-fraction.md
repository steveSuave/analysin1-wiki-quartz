# Convergents of a Continued Fraction

**Summary**: Truncating a [[continued-fraction|continued fraction]] after $k$ levels gives a rational number called the $k$-th convergent. Numerators and denominators each obey the same three-term linear recurrence — multiply the previous fraction by the next partial denominator and add the partial numerator times the second-previous fraction. The convergents alternate around the true value, each closer than its predecessor, so the truncations provide fast and tight rational approximations.

**Sources**: `raw/chapter18.pdf` (§358–§362).

**Last updated**: 2026-05-11

---

## The truncation table (§358)

Breaking the simple continued fraction into successive levels:

$$\begin{aligned}
a &= a \\
a + \tfrac{1}{b} &= \tfrac{ab + 1}{b} \\
a + \tfrac{1}{b + \tfrac{1}{c}} &= \tfrac{abc + a + c}{bc + 1} \\
a + \tfrac{1}{b + \tfrac{1}{c + \tfrac{1}{d}}} &= \tfrac{abcd + ab + ad + cd + 1}{bcd + b + d} \\
&\;\;\vdots
\end{aligned}$$

Numerators and denominators look complicated, but Euler (§359) extracts a clean recurrence: each numerator is the previous numerator multiplied by the *new letter* introduced at that level, plus the second-previous numerator. Identical rule for denominators. To make the rule apply from the very first step Euler prefixes the trivial fraction $1/0$ (the "value" of the empty continued fraction):

$$\overset{a}{\frac{1}{0}}\quad \frac{a}{1}\quad \overset{b}{\frac{ab+1}{b}}\quad \overset{c}{\frac{abc + a + c}{bc + 1}}\quad \overset{d}{\frac{abcd + ab + ad + cd + 1}{bcd + b + d}}\quad \cdots$$

where the superscript above each fraction is the letter $a, b, c, d, \ldots$ used in forming it.

## The three-term recurrence (§361)

For the general form with both partial denominators $a, b, c, \ldots$ (superscripts) *and* partial numerators $\alpha, \beta, \gamma, \ldots$ (subscripts), Euler's table is

$$\overset{a}{\underset{\phantom\alpha}{\tfrac{1}{0}}}\quad \overset{b}{\underset{\alpha}{\tfrac{a}{1}}}\quad \overset{c}{\underset{\beta}{\tfrac{ab + \alpha}{b}}}\quad \overset{d}{\underset{\gamma}{\tfrac{abc + \beta a + \alpha c}{bc + \beta}}}\quad \overset{e}{\underset{\delta}{\tfrac{abcd + \beta ab + \alpha cd + \gamma ab + \alpha\gamma}{bcd + \beta d + \gamma b}}}\quad \cdots$$

and the law of formation is

$$N_k = b_k\,N_{k-1} + \beta_k\,N_{k-2},\qquad D_k = b_k\,D_{k-1} + \beta_k\,D_{k-2}$$

where $b_k$ is the *superscript* (next partial denominator) and $\beta_k$ is the *subscript* (next partial numerator) of fraction $k$. The convergent $N_k/D_k$ is the value of the continued fraction up to and including the partial denominator that is the superscript of fraction $k$.

In the simple form $\beta_k \equiv 1$ and the recurrence reduces to

$$N_k = b_k\,N_{k-1} + N_{k-2},\qquad D_k = b_k\,D_{k-1} + D_{k-2}.$$

This is the recurrence that drives every Euclidean-algorithm computation, every Pell-equation solution, and every best-rational-approximation theorem in 18th- and 19th-century number theory.

## Alternation around the true value (§362)

Let $z$ denote the value of the (possibly infinite) continued fraction. Then the convergents satisfy

$$\frac{1}{0} > z,\quad \frac{a}{1} < z,\quad \frac{ab + 1}{b} > z,\quad \frac{abc + a + c}{bc + 1} < z,\quad \ldots$$

— alternately greater than and less than $z$. Moreover, each convergent is closer to $z$ than any of its predecessors. So the truncations *bracket* the true value with shrinking error.

Euler notes that the approximation is especially good when the partial numerators $\alpha, \beta, \gamma, \ldots$ "do not become too large." For the simple form this restriction is automatic, and the convergence is then extremely fast — this is what makes [[best-rational-approximations|best-rational-approximation theory]] possible and what gives [[continued-fraction-for-e|Euler's continued fraction for $e$]] its accuracy on so few terms.

## The differences identity (§363)

The convergents not only alternate; their *differences* are explicit:

$$\frac{N_2}{D_2} - \frac{N_1}{D_1} = \frac{\alpha}{b},\qquad \frac{N_3}{D_3} - \frac{N_2}{D_2} = -\frac{\alpha\beta}{b(bc + \beta)},\qquad \frac{N_4}{D_4} - \frac{N_3}{D_3} = \frac{\alpha\beta\gamma}{(bc + \beta)(bcd + \beta d + \gamma b)},\quad \ldots$$

Summing this telescoping sequence is exactly the [[continued-fraction-series-equivalence|series representation]] of the continued fraction in §363.

## Related pages

- [[continued-fraction]]
- [[chapter-18-on-continued-fractions]]
- [[continued-fraction-series-equivalence]] — the telescoping sum of these differences
- [[best-rational-approximations]] — why the truncations are *optimal* among rationals with bounded denominator
- [[recurrent-series]] — the convergent numerators and denominators are recurrent series in the parameter $k$ with two-term scale $(b_k, \beta_k)$, though with non-constant scale unless the CF is periodic
