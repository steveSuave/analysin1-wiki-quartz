# Scale of the Relation

**Summary**: De Moivre's name (preserved by Euler in §224) for the list of multipliers $\alpha, \beta, \gamma, \ldots$ that appear in the linear recurrence governing a [[recurrent-series|recurrent series]]. The scale of the relation is the same data as the (sign-flipped) coefficients of the denominator of the generating rational function. [[chapter-16-on-the-partition-of-numbers|Chapter 16]] supplies the most famous *infinite-but-sparse* example: the partition function's scale, supported on the pentagonal-number lattice (see [[eulers-pentagonal-number-theorem]]). [[chapter-17-using-recurrent-series-to-find-roots-of-equations|Chapter 17]] reads the scale directly off the coefficients of any algebraic equation $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$ and uses [[bernoullis-method-for-roots|Bernoulli's method]] on a recurrent series with that scale to find the equation's largest root.

**Sources**: chapter13, chapter16, chapter17

**Last updated**: 2026-05-11

---

## Definition (§224)

For a [[recurrent-series|recurrent series]] $A + Bz + Cz^2 + Dz^3 + \cdots$ in which each term beyond the first $k$ is determined by its $k$ predecessors via

$$D = \alpha C + \beta B + \gamma A,\qquad E = \alpha D + \beta C + \gamma B,\qquad F = \alpha E + \beta D + \gamma C,\qquad \ldots$$

(more generally, $X_{n+k} = \alpha X_{n+k-1} + \beta X_{n+k-2} + \cdots$), the list of multipliers $\alpha, \beta, \gamma, \ldots$ is the *scale of the relation* (source: chapter13, §224). De Moivre named it; Euler adopts the term verbatim.

## Equivalence with the denominator

The recurrence $X_n = \alpha X_{n-1} + \beta X_{n-2} + \gamma X_{n-3} + \cdots$ is precisely the condition that

$$1 - \alpha z - \beta z^2 - \gamma z^3 - \cdots$$

annihilates the generating function $A + Bz + Cz^2 + \cdots$ up to a polynomial of degree less than the scale length. Equivalently: the series arises from a rational function with denominator $1 - \alpha z - \beta z^2 - \gamma z^3 - \cdots$. The scale and the denominator carry exactly the same information (source: chapter13, §224 — "the law of progression is contained in the scale of the relation, and the scale of the relation immediately gives us the denominator of the rational function from which the series arose").

This is the principle that makes the theory of [[recurrent-series|recurrent series]] reversible: from the *series* one reads off the scale; from the scale one reads off the *denominator*; from the denominator (via [[real-partial-fraction-decomposition|real partial fractions]]) one obtains the [[general-term-of-recurrent-series|closed-form general term]] and the [[sum-of-recurrent-series|sum]].

## How to recover the rational function (§225)

Given a recurrent series with scale of length $k$:

1. Form the denominator $1 - \alpha z - \beta z^2 - \cdots - \kappa z^k$ from the scale.
2. Factor it (real linear and quadratic factors).
3. The general term has the *form* dictated by the factorization:
   - distinct real roots $p, q, r$: general term is $(Ap^n + Bq^n + Cr^n)z^n$;
   - repeated root $q = p$: $((An + B)p^n + Cr^n)z^n$;
   - triple root $r = q = p$: $(An^2 + Bn + C)p^n z^n$;
   - quadratic factor $1 - 2pz\cos\phi + p^2 z^2$ (no further factor): general term is $\left(Ap^n + \dfrac{B\sin(n+1)\phi + C\sin n\phi}{\sin\phi}q^n\right) z^n$ (source: chapter13, §225).
4. Determine the unknowns $A, B, C, \ldots$ by setting $n = 0, 1, 2, \ldots$ and matching the first few series coefficients.

This is the *constructive* form of De Moivre's correspondence: the scale tells you the *shape* of the closed-form general term up to constants; the first few terms of the series fix the constants.

## Examples

### Lucas-like sequence (Example III of §216)

The series $1, 3, 4, 7, 11, 18, 29, 47, \ldots$ has scale of the relation $\alpha = 1, \beta = 1$ (each term is the sum of the two preceding). Hence the denominator is $1 - z - z^2$, and the rational function is $(1 + 2z)/(1 - z - z^2)$ once the numerator is matched to $A = 1, B = 3$.

### General two-member scale

Scale $\alpha, \beta$ with first two terms $A, B$: rational function $\dfrac{A + (B - \alpha A)z}{1 - \alpha z - \beta z^2}$, closed-form general term $(Up^n + Vq^n)z^n$ where $p, q$ are the roots of $1 - \alpha z - \beta z^2$. See [[closed-form-two-term-recurrence]].

### General three-member scale (§230)

Scale $\alpha, -\beta, \gamma$, denominator $1 - \alpha z + \beta z^2 - \gamma z^3 = (1-pz)(1-qz)(1-rz)$. Term is $Up^n + Vq^n + Wr^n$. From $p+q+r = \alpha$, $pq+pr+qr = \beta$, $pqr = \gamma$, the relation between three consecutive terms $P, Q, R$ becomes a *cubic* in $R$ given $P, Q$ — Euler writes the cubic explicitly in §230.

### Pentagonal-number scale ([[chapter-16-on-the-partition-of-numbers|Chapter 16]] §324)

The partition function $p(n)$ has generating series $1/\prod_{k\geq 1}(1-x^k)$. By [[eulers-pentagonal-number-theorem|Euler's pentagonal number theorem]] the denominator expands as

$$\prod_{k\geq 1}(1-x^k) = 1 - x - x^2 + x^5 + x^7 - x^{12} - x^{15} + x^{22} + x^{26} - \cdots,$$

so the scale of the relation is

$$(+1, +1, 0, 0, -1, 0, -1, 0, 0, 0, 0, +1, 0, 0, +1, 0, 0, 0, 0, 0, 0, -1, 0, 0, 0, -1, 0, \ldots),$$

with non-zero entries only at positions $(3k^2 \pm k)/2$ and signs $(-1)^{k+1}$. Although the scale is infinite, only $O(\sqrt n)$ of its entries are non-zero in any prefix of length $n$, so the recurrence

$$p(n) = p(n-1) + p(n-2) - p(n-5) - p(n-7) + p(n-12) + p(n-15) - \cdots$$

computes $p(n)$ in $O(\sqrt n)$ operations — the first classical example of a sparse-support scale of the relation.

## Notable points

- **The scale is sign-flipped from the denominator.** Euler's convention puts the denominator as $1 - \alpha z - \beta z^2 - \cdots$ so the scale entries $\alpha, \beta, \ldots$ are *positive when the recurrence has positive coefficients* (source: chapter13, §63 and §224). This is purely a sign-of-convention choice.
- **Same data, three views.** The scale (a list), the denominator (a polynomial in $z$), and the characteristic equation $x^k - \alpha x^{k-1} - \beta x^{k-2} - \cdots = 0$ (whose roots are the *reciprocals* of the roots of the denominator $1 - \alpha z - \cdots$) are equivalent. Modern textbooks usually state the recurrence via the characteristic equation; Euler uses the denominator directly. The characteristic-equation view is precisely the one [[chapter-17-using-recurrent-series-to-find-roots-of-equations|Chapter 17]] exploits: given an equation, read off the scale, run the recurrent series, and the ratio $Q/P$ of consecutive coefficients tends to the equation's largest root — [[bernoullis-method-for-roots|Daniel Bernoulli's method]].
- **Why "scale".** A *scale* in 18th-century usage means a graduated rule or sequence of marks. The list $\alpha, \beta, \gamma, \ldots$ is precisely such a graduated set of multipliers, applied at increasing offsets in the recurrence.

## Related pages

- [[recurrent-series]]
- [[general-term-of-recurrent-series]]
- [[closed-form-two-term-recurrence]]
- [[sum-of-recurrent-series]]
- [[partial-fraction-decomposition]]
- [[real-partial-fraction-decomposition]]
- [[chapter-13-on-recurrent-series]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
- [[eulers-pentagonal-number-theorem]]
- [[partition-of-numbers]]
- [[chapter-16-on-the-partition-of-numbers]]
- [[bernoullis-method-for-roots]]
- [[trinomial-factor-from-recurrent-series]]
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]]
