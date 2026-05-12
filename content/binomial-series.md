# Binomial Series

**Summary**: Newton's "universal theorem" for $(P + Q)^{m/n}$ as an infinite series in powers of $Q$ — Euler's §71 principal tool for expanding irrational functions. When $P = 1$ and $Q$ is a polynomial in $z$, the expansion is a recurrent series with a non-constant law (§73–§76).

**Sources**: chapter4.pdf

**Last updated**: 2026-04-23

---

## The universal theorem (§71)

Euler states Newton's binomial theorem for arbitrary rational exponent $m/n$:

$$ (P + Q)^{m/n} \;=\; P^{m/n} + \frac{m}{n} P^{(m-n)/n} Q + \frac{m(m-n)}{n \cdot 2n} P^{(m-2n)/n} Q^2 + \frac{m(m-n)(m-2n)}{n \cdot 2n \cdot 3n} P^{(m-3n)/n} Q^3 + \cdots $$

The series terminates iff $m/n$ is a positive integer; otherwise it has infinitely many terms (source: chapter4.pdf, §71).

### Sample cases (§71)

Explicit expansions tabulated by Euler:

- $(P + Q)^{1/2} = P^{1/2} + \tfrac{1}{2} P^{-1/2} Q - \tfrac{1 \cdot 1}{2 \cdot 4} P^{-3/2} Q^2 + \tfrac{1 \cdot 1 \cdot 3}{2 \cdot 4 \cdot 6} P^{-5/2} Q^3 - \cdots$
- $(P + Q)^{-1/2} = P^{-1/2} - \tfrac{1}{2} P^{-3/2} Q + \tfrac{1 \cdot 3}{2 \cdot 4} P^{-5/2} Q^2 - \tfrac{1 \cdot 3 \cdot 5}{2 \cdot 4 \cdot 6} P^{-7/2} Q^3 + \cdots$
- $(P + Q)^{1/3} = P^{1/3} + \tfrac{1}{3} P^{-2/3} Q - \tfrac{1 \cdot 2}{3 \cdot 6} P^{-5/3} Q^2 + \tfrac{1 \cdot 2 \cdot 5}{3 \cdot 6 \cdot 9} P^{-8/3} Q^3 - \cdots$
- $(P + Q)^{-1/3} = P^{-1/3} - \tfrac{1}{3} P^{-4/3} Q + \tfrac{1 \cdot 4}{3 \cdot 6} P^{-7/3} Q^2 - \tfrac{1 \cdot 4 \cdot 7}{3 \cdot 6 \cdot 9} P^{-10/3} Q^3 + \cdots$
- $(P + Q)^{2/3} = P^{2/3} + \tfrac{2}{3} P^{-1/3} Q - \tfrac{2 \cdot 1}{3 \cdot 6} P^{-4/3} Q^2 + \tfrac{2 \cdot 1 \cdot 4}{3 \cdot 6 \cdot 9} P^{-7/3} Q^3 - \cdots$

## Term-to-term recurrence (§72)

From one term to the next: if a term has the form $M P^{(m - kn)/n} Q^k$, the next term is

$$ \frac{m - kn}{(k+1) n} \, M \, P^{(m - (k+1) n)/n} Q^{k+1}. $$

The exponent of $P$ decreases by $1$ each step; the exponent of $Q$ increases by $1$. Equivalently, extracting $P^{m/n}$ as an overall factor gives $(P + Q)^{m/n} = P^{m/n} (1 + Q/P)^{m/n}$, and setting $Z = Q/P$,

$$ (1 + Z)^m \;=\; 1 + \frac{m}{1} Z + \frac{m(m-1)}{1 \cdot 2} Z^2 + \frac{m(m-1)(m-2)}{1 \cdot 2 \cdot 3} Z^3 + \cdots $$

which Euler remarks is the form he will usually use (source: chapter4.pdf, §72). Here $m$ may be any real number — fractional or integer.

## Polynomial $Z$: recurrent laws (§73–§76)

When $Z$ is a polynomial in $z$, the expansion of $(1 + Z)^{m-1}$ is itself a series in $z$, and its coefficients satisfy a recurrence whose order equals the number of nonzero coefficients in $Z$.

### $Z = \alpha z$ (§73)

$$ (1 + \alpha z)^{m - 1} = 1 + \frac{m - 1}{1} \alpha z + \frac{(m-1)(m-2)}{1 \cdot 2} \alpha^2 z^2 + \frac{(m-1)(m-2)(m-3)}{1 \cdot 2 \cdot 3} \alpha^3 z^3 + \cdots $$

Writing the series as $1 + A z + B z^2 + C z^3 + \cdots + M z^{n-1} + N z^n + \cdots$, the recurrence is

$$ N = \frac{m - n}{n} \alpha M. $$

So each coefficient is determined by the one before (source: chapter4.pdf, §73).

### $Z = \alpha z + \beta z^2$ (§74)

$(1 + \alpha z + \beta z^2)^{m-1}$ has coefficients determined from the *two* preceding ones:

$$ N = \frac{m - n}{n} \alpha M + \frac{2m - n}{n} \beta L. $$

Starting values: $A = \tfrac{m-1}{1}\alpha$, $B = \tfrac{m-2}{2}\alpha A + \tfrac{2m-2}{2}\beta$, etc. (source: chapter4.pdf, §74).

### $Z = \alpha z + \beta z^2 + \gamma z^3$ (§75)

Three-term recurrence:

$$ N = \frac{m - n}{n} \alpha M + \frac{2m - n}{n} \beta L + \frac{3m - n}{n} \gamma K. $$

### General $Z = \alpha z + \beta z^2 + \gamma z^3 + \delta z^4 + \cdots$ (§76)

$(1 + \alpha z + \beta z^2 + \gamma z^3 + \cdots)^{m-1}$ has each coefficient determined by as many predecessors as $Z$ has nonzero terms, with coefficients depending on the index $n$ — a *non-constant* law (source: chapter4.pdf, §76).

## Connection to §68

The recurrent law of §76 matches the §68 law for $(1 - \alpha z - \beta z^2 - \cdots)^{-(m+1)}$ — the two statements are related by $m \mapsto -m$ together with the sign flip on $\alpha, \beta, \gamma, \ldots$ (source: chapter4.pdf, §76). This is the shadow of a single underlying theorem. Euler does not prove the general law here but says it "can be done so much more easily with the aid of some principles of differential calculus" and, for the moment, treats the agreement with §68 and the many worked examples as evidence enough. See [[recurrent-series]] §68.

## Identities used later

Euler singles out two forms of the expansion for later use (source: chapter4.pdf, §72):

$$ (1 + Z)^m \;=\; 1 + \tfrac{m}{1} Z + \tfrac{m(m-1)}{1 \cdot 2} Z^2 + \tfrac{m(m-1)(m-2)}{1 \cdot 2 \cdot 3} Z^3 + \cdots $$

$$ (1 + Z)^{m-1} \;=\; 1 + \tfrac{m-1}{1} Z + \tfrac{(m-1)(m-2)}{1 \cdot 2} Z^2 + \tfrac{(m-1)(m-2)(m-3)}{1 \cdot 2 \cdot 3} Z^3 + \cdots $$

## Notable points

- No convergence discussion: Euler works formally, content with the term-to-term consistency.
- The deferral of a rigorous proof to differential calculus (§76) is historically significant — a rigorous binomial theorem for arbitrary exponents was one of the motivating problems for 18th-century analysis.
- The series for $(1 + Z)^{-1}$ specializes to the [[geometric-series]] $1 - Z + Z^2 - Z^3 + \cdots$, which is where Euler's story began.

## Related pages

- [[recurrent-series]]
- [[geometric-series]]
- [[method-of-undetermined-coefficients]]
- [[higher-order-arithmetic-progressions]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
