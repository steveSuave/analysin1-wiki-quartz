# Recurrent Series

**Summary**: A series $A + Bz + Cz^2 + Dz^3 + \cdots$ whose coefficients satisfy a fixed linear recurrence. Euler (§62) credits the name to De Moivre — one must "run back" to previous terms to compute a new one. Every rational function with non-vanishing constant in its denominator expands into a recurrent series, and the recurrence is read directly off the denominator. The closed-form general term, the inverse problem, and the sum are developed in [[chapter-13-on-recurrent-series|Chapter 13]]. [[chapter-16-on-the-partition-of-numbers|Chapter 16]] applies the theory to **partition generating functions** $1/\prod_{k=1}^m(1-x^k)$. [[chapter-17-using-recurrent-series-to-find-roots-of-equations|Chapter 17]] inverts the construction to turn recurrent series into a **root-finder** for algebraic equations.

**Sources**: chapter4.pdf, chapter13.pdf, chapter16.pdf, chapter17.pdf

**Last updated**: 2026-05-11

---

## Definition (§62)

A series $A + Bz + Cz^2 + \cdots$ is *recurrent* if there is a fixed law — independent of the position — by which each coefficient is determined from a fixed number of its predecessors. The order of the recurrence equals the degree of the denominator of the rational function that produced the series (source: chapter4.pdf, §62).

Euler attributes the name to Abraham de Moivre, "who has examined their nature very carefully": the name comes from the need to *run back* to preceding terms in order to compute subsequent ones.

## Canonical form (§63)

Any rational function whose denominator has a nonzero constant term can be written, after normalizing the constant to $1$ and putting the remaining terms with negative signs, as

$$ \frac{a + b z + c z^2 + d z^3 + \cdots}{1 - \alpha z - \beta z^2 - \gamma z^3 - \delta z^4 - \cdots}. $$

Setting this equal to $A + B z + C z^2 + \cdots$ and multiplying out gives

$$ A = a, \quad B = \alpha A + b, \quad C = \alpha B + \beta A + c, \quad D = \alpha C + \beta B + \gamma A + d, \quad \ldots $$

Each coefficient is a weighted sum of preceding coefficients (with weights $\alpha, \beta, \gamma, \ldots$) plus the corresponding numerator entry (source: chapter4.pdf, §63). Once the numerator runs out, the recurrence becomes homogeneous:

$$ N = \alpha M + \beta L + \gamma K + \cdots $$

where $N, M, L, K, \ldots$ are consecutive coefficients. The negative signs in the denominator are Euler's convention so that the recurrence comes out with all positive coefficients (source: chapter4.pdf, §63).

## Properness requirement (§63)

The law of the recurrence holds for all coefficients *only if the rational function is proper* — numerator degree strictly less than denominator degree. If the function is improper, the polynomial part disturbs early terms and the fixed law fails there.

Euler's illustrating example: $\dfrac{1 + 2z - z^3}{1 - z - z^2}$ gives the series

$$ 1 + 3z + 4z^2 + 6z^3 + 10z^4 + 16z^5 + 26z^6 + 42z^7 + \cdots $$

The Fibonacci-like law "each coefficient is the sum of the two before" works everywhere *except* at the $6z^3$ term, where the $-z^3$ in the numerator intervenes (source: chapter4.pdf, §63). The remedy is to first split off the polynomial part using an [[improper-rational-function]] decomposition.

## Examples

### Fibonacci-like (§61)

$\dfrac{1 + 2z}{1 - z - z^2} = 1 + 3z + 4z^2 + 7z^3 + 11z^4 + 18z^5 + \cdots$ — each coefficient is the sum of the two preceding ones (Lucas numbers).

### Arithmetic progression (§64)

$\dfrac{1}{(1 - z)^2} = 1 + 2z + 3z^2 + 4z^3 + 5z^4 + \cdots$ — arithmetic progression $1, 2, 3, \ldots$ as a recurrent series with denominator $1 - 2z + z^2$, recurrence $C = 2B - A$. See [[higher-order-arithmetic-progressions]].

### Higher-order progression (§65–§66)

Denominators $(1-z)^3, (1-z)^4, \ldots$ produce progressions of second, third, … order — those with constant higher differences.

## Non-constant laws (§68)

If the denominator is the *power* of a multinomial — $(1 - \alpha z - \beta z^2 - \gamma z^3 - \cdots)^{m+1}$ — the coefficient law still involves a fixed number of predecessors, but the coefficients in the recurrence depend on the index $n$:

$$ N \;=\; \frac{m + n}{n} \alpha M + \frac{2m + n}{n} \beta L + \frac{3m + n}{n} \gamma K + \cdots $$

where $N$ is the coefficient of $z^n$ (source: chapter4.pdf, §68). Euler notes this non-constant law applies only when the numerator is $1$ (or a constant); a general numerator makes the recurrence more complicated, a problem he defers to differential calculus.

The same non-constant law arises in §76 for the binomial expansion $(1 + \alpha z + \beta z^2 + \cdots)^{m-1}$ — see [[binomial-series]].

## Zero constant term (§69)

When the denominator factors as $z^m \cdot (1 - \alpha z - \beta z^2 - \cdots)$, i.e. its constant term vanishes, the series acquires negative powers of $z$:

$$ \frac{a + b z + \cdots}{z^m (1 - \alpha z - \beta z^2 - \cdots)} \;=\; \frac{A}{z^m} + \frac{B}{z^{m-1}} + \frac{C}{z^{m-2}} + \cdots $$

The coefficients $A, B, C, \ldots$ are those of the corresponding recurrent series for the rational function without the factor $z^m$ (source: chapter4.pdf, §69). In modern language this is a Laurent expansion at the origin.

## Non-uniqueness (§70)

A single rational function admits *infinitely many* distinct recurrent-series representations, because one can always reparametrize by substitution (see [[chapter-3-on-the-transformation-of-functions-by-substitution]]). Euler illustrates with $y = (1 + z)/(1 - z - z^2)$: under $z = 1/x$ and $z = (1-x)/(1+x)$ one obtains entirely different recurrent series for the same $y$ (source: chapter4.pdf, §70).

## Closed-form theory ([[chapter-13-on-recurrent-series|Chapter 13]])

Chapter 4 gave the *recurrence*; [[chapter-13-on-recurrent-series|Chapter 13]] gives the *closed-form general term and sum* by combining [[real-partial-fraction-decomposition|real partial fractions]] with explicit per-fraction expansions:

- The [[general-term-of-recurrent-series|general term]] is obtained by partial-fractioning the rational function and summing per-piece closed forms — a polynomial-times-$p^n$ for each linear factor and a $\sin(n+1)\phi/\sin\phi$ form for each [[trinomial-factor|quadratic factor]].
- The recurrence multipliers $\alpha, \beta, \gamma, \ldots$ are De Moivre's [[scale-of-the-relation|*scale of the relation*]] (§224), equivalent data to the denominator of the generating rational function.
- For two-member scales, the [[closed-form-two-term-recurrence|Binet-type closed form]] $X_n = Up^n + Vq^n$ has invariant $UV = (B^2 - \alpha AB + \beta A^2)/(4\beta - \alpha^2)$.
- The [[sum-of-recurrent-series|sum]] of the infinite series equals the rational function; the partial sum has its own clean closed form.

## Applications in Chapter 16 — partition generating functions

[[chapter-16-on-the-partition-of-numbers|Chapter 16]] uses recurrent series to enumerate integer partitions. For each $m$ the rational function

$$\frac{x^{m(m+1)/2}}{(1-x)(1-x^2)\cdots(1-x^m)}\qquad\text{or}\qquad\frac{x^m}{(1-x)(1-x^2)\cdots(1-x^m)}$$

is the [[partition-generating-functions|generating function]] for partitions of $n$ into $m$ distinct or unrestricted parts respectively (§307, §313). The scale of the relation is the signed expansion of $\prod_{k=1}^m(1-x^k)$.

For the full partition function $p(n)$, generated by $1/\prod_{k\geq 1}(1-x^k)$, the [[eulers-pentagonal-number-theorem|pentagonal number theorem]] gives an **infinite but sparse** [[scale-of-the-relation|scale of the relation]] supported on the pentagonal-number lattice $\{(3k^2\pm k)/2\}$, the first known recurrent series whose effective recurrence uses only $O(\sqrt n)$ predecessors.

## Inverse use in Chapter 17 — roots from the scale

[[chapter-17-using-recurrent-series-to-find-roots-of-equations|Chapter 17]] runs the chapter-13 correspondence backwards. Given an algebraic equation $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$, the [[scale-of-the-relation|scale]] $\alpha, \beta, \gamma, \ldots$ is read off the coefficients; any recurrent series with that scale (the cleanest choice is the one arising from numerator $= 1$) has consecutive-term ratio $Q/P$ converging to the **largest root in absolute value** — see [[bernoullis-method-for-roots|Daniel Bernoulli's method]]. The complex-pair analogue ([[trinomial-factor-from-recurrent-series]]) extracts both modulus and argument of a dominant conjugate pair from four consecutive terms. Combined with the substitution $x = y + k$, the method finds *every* root of any algebraic equation.

## Why recurrent series matter

- They are the bridge between rational generating functions and linear recurrences — a modern viewpoint first systematized here.
- They reduce the computation of every coefficient to a small fixed arithmetic rule, making it practical to generate as many terms as desired.
- They make explicit the correspondence between the denominator of a rational function and the characteristic polynomial of the recurrence, foreshadowing the later theory of linear difference equations.

## Related pages

- [[geometric-series]]
- [[method-of-undetermined-coefficients]]
- [[higher-order-arithmetic-progressions]]
- [[binomial-series]]
- [[improper-rational-function]]
- [[general-term-of-recurrent-series]]
- [[scale-of-the-relation]]
- [[closed-form-two-term-recurrence]]
- [[sum-of-recurrent-series]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
- [[chapter-13-on-recurrent-series]]
- [[partition-generating-functions]]
- [[eulers-pentagonal-number-theorem]]
- [[chapter-16-on-the-partition-of-numbers]]
- [[bernoullis-method-for-roots]]
- [[trinomial-factor-from-recurrent-series]]
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]]
