# Newton's Identities

**Summary**: §165–§166: the recurrence that converts the elementary symmetric coefficients of a polynomial (or a "polynomial of infinite degree", i.e. a power series) into the power sums of its reciprocal roots. The pivotal computational engine of [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series|Chapter 10]].

**Sources**: chapter10

**Last updated**: 2026-04-30

---

## Setup

Suppose

$$1 + Az + Bz^2 + Cz^3 + Dz^4 + \cdots = (1 + \alpha z)(1 + \beta z)(1 + \gamma z)(1 + \delta z)\cdots$$

— with finitely or infinitely many factors. Multiplying out and matching powers of $z$ identifies $A, B, C, \ldots$ as the **elementary symmetric polynomials** in $\alpha, \beta, \gamma, \ldots$:

$$A = \alpha + \beta + \gamma + \delta + \cdots,$$

$$B = \alpha\beta + \alpha\gamma + \alpha\delta + \beta\gamma + \beta\delta + \gamma\delta + \cdots,$$

$$C = \alpha\beta\gamma + \alpha\beta\delta + \alpha\gamma\delta + \beta\gamma\delta + \cdots,$$

$$D = \alpha\beta\gamma\delta + \cdots,\quad \text{etc.}$$

(source: chapter10, §165). Euler describes these as "products taken one at a time, two at a time, three at a time, ..."

## Power sums

Define

$$P = \alpha + \beta + \gamma + \delta + \cdots,\quad Q = \alpha^2 + \beta^2 + \gamma^2 + \delta^2 + \cdots,$$

$$R = \alpha^3 + \beta^3 + \gamma^3 + \delta^3 + \cdots,\quad S = \alpha^4 + \cdots,\quad T = \alpha^5 + \cdots,\quad V = \alpha^6 + \cdots.$$

These are the **power sums** of the roots $\alpha, \beta, \gamma, \ldots$ (which, in the parametrization above, are minus the reciprocals of the roots of the polynomial $1 + Az + Bz^2 + \cdots$).

## The recurrence

$$\boxed{\;\begin{aligned} P &= A,\\ Q &= AP - 2B,\\ R &= AQ - BP + 3C,\\ S &= AR - BQ + CP - 4D,\\ T &= AS - BR + CQ - DP + 5E,\\ V &= AT - BS + CR - DQ + EP - 6F,\\ &\vdots\end{aligned}\;}$$

(source: chapter10, §166). Each line uses all previously-known $A, B, C, \ldots$ and $P, Q, R, \ldots$, so the sequence $P, Q, R, S, \ldots$ can be computed mechanically once the elementary symmetrics $A, B, C, \ldots$ are known.

The general pattern: the $n$-th line is

$$P_n = AP_{n-1} - BP_{n-2} + CP_{n-3} - DP_{n-4} + \cdots + (-1)^{n+1}\,n\,(\text{coefficient of }z^n).$$

Euler comments: "The truth of these formulas is intuitively clear, but a rigorous proof will be given in the differential calculus" (source: chapter10, §166).

## Why it works

The squared sum identity $(\alpha + \beta + \gamma + \cdots)^2 = \alpha^2 + \beta^2 + \cdots + 2(\alpha\beta + \alpha\gamma + \cdots)$ is the simplest case: $P^2 = Q + 2B$, hence $Q = P^2 - 2B = AP - 2B$.

The general case follows from the same accounting: when one expands $P\cdot P_{n-1}$, one obtains the genuine $n$-th power sum $P_n$ together with all the "off-diagonal" products, which are exactly $B P_{n-2}$, $C P_{n-3}$, etc., with alternating signs from the elementary symmetric structure. A modern proof uses logarithmic differentiation: take $\log$ of the product side, differentiate, and read off the coefficient identity.

## Use in Chapter 10

Euler's strategy: take a transcendental function whose [[exponential-infinite-product|infinite product]] expansion is known (so the elementary symmetrics $A, B, C, \ldots$ of its zeros are read off the power-series coefficients) and apply the recurrence to obtain the power sums of the *reciprocals of the zeros*.

The first application: let

$$\frac{e^x - e^{-x}}{2x} = 1 + \frac{x^2}{1\cdot 2\cdot 3} + \frac{x^4}{1\cdot 2\cdot 3\cdot 4\cdot 5} + \cdots = \prod_{k=1}^{\infty}\left(1 + \frac{x^2}{k^2\pi^2}\right).$$

Substitute $x^2 = \pi^2 z$. The roots in the new variable are $z = -1, -1/4, -1/9, \ldots$, so the parametrization $1 + Az + Bz^2 + \cdots = \prod(1 + \alpha_k z)$ holds with $\alpha_k = 1/k^2$. Hence:

- $A = \pi^2/6$, $B = \pi^4/120$, $C = \pi^6/5040$, $D = \pi^8/362880$, $\ldots$ (read off from the power series).
- $P = \sum 1/k^2 = A = \pi^2/6$. → [[basel-problem|the Basel sum]].
- $Q = \sum 1/k^4 = AP - 2B = \pi^4/90$.
- $R = \sum 1/k^6 = \pi^6/945$.
- $S = \sum 1/k^8 = \pi^8/9450$, etc.

See [[zeta-at-even-integers]] for the table extended through $\zeta(26)$.

The same recurrence drives every subsequent computation in the chapter — from $\sum 1/(2k+1)^{2n}$ via the [[cosine-infinite-product]] (§169) to the [[circular-arc-series|character sums of §171–§180]] and the [[cotangent-partial-fraction|cot/csc partial fractions]] of §181–§183.

## Modern footnote

These are the **Newton–Girard formulas**, also called **Newton's identities**: a basic tool in the theory of symmetric functions and the bridge between elementary symmetric polynomials $e_n$ and power sum polynomials $p_n$. The variant Euler uses, with signs alternating because the parametrization is $\prod(1 + \alpha z)$ rather than $\prod(z - \alpha)$, is one of two standard forms.

In modern notation, with $E(z) = \prod(1 + \alpha_k z)$ and $\log E(z) = \sum_{k}\log(1 + \alpha_k z) = \sum_{k}\sum_{n\ge 1}(-1)^{n+1}\alpha_k^n z^n/n$:

$$\frac{E'(z)}{E(z)} = \sum_{n\ge 1}(-1)^{n+1}P_n z^{n-1}.$$

Multiplying out $E'(z) = E(z)\cdot E'(z)/E(z)$ gives the Newton recurrence directly. Euler's identity-by-identity verification and the modern logarithmic-derivative proof are the same calculation, just written differently.

## Related pages

- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[odd-and-alternating-zeta-decomposition]]
- [[circular-arc-series]]
- [[cotangent-partial-fraction]]
- [[exponential-infinite-product]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
