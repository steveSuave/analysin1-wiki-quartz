# General Term of a Recurrent Series

**Summary**: Closed-form expression for the coefficient of $z^n$ in any [[recurrent-series|recurrent series]], obtained by decomposing the generating rational function into [[real-partial-fraction-decomposition|real partial fractions]] and summing the general term of each. Two engines: the linear-factor brick $A/(1-pz)^k$ gives a polynomial-in-$n$ times $p^n$, and the quadratic-factor brick $(A+Bpz)/(1-2pz\cos\phi+p^2 z^2)^k$ gives a trigonometric form involving $\sin n\phi$, $\cos n\phi$. [[chapter-17-using-recurrent-series-to-find-roots-of-equations|Chapter 17]] inverts the perspective: when only the *coefficients* of an equation are known, the dominant term in the general term still controls the ratio $Q/P$, which converges to the largest root — see [[bernoullis-method-for-roots]].

**Sources**: chapter13, chapter17

**Last updated**: 2026-05-11

---

## The strategy (§211–§214)

Let

$$\frac{a + bz + cz^2 + \cdots}{1 - \alpha z - \beta z^2 - \gamma z^3 - \cdots} \;=\; A + Bz + Cz^2 + Dz^3 + \cdots$$

be a proper rational function expanded as a [[recurrent-series|recurrent series]]. Decompose the left side by [[partial-fraction-decomposition|partial fractions]] (real, using [[real-partial-fraction-decomposition|Chapter 12]] when the denominator has complex roots), so each piece is one of two types:

- $\dfrac{A}{(1 - pz)^k}$ — from a real linear factor $(1-pz)^k$ of the denominator,
- $\dfrac{A + Bpz}{(1 - 2pz\cos\phi + p^2 z^2)^k}$ — from a real quadratic ([[trinomial-factor|trinomial]]) factor.

Each piece expands into its own recurrent series, with a known general term. The general term of the original series is the *sum* of the general terms of the partial-fraction series (source: chapter13, §213).

Equality of two power series in $z$ is justified by setting $z = 0$ (giving $A = a + a' + a'' + \cdots$), subtracting, dividing by $z$, and repeating: the coefficient of every power matches (source: chapter13, §214).

## Linear-factor brick (§215–§216)

The basic series is

$$\frac{A}{1 - pz} \;=\; A + Apz + Ap^2 z^2 + Ap^3 z^3 + \cdots,\qquad \text{general term } A p^n z^n.$$

Differentiating ($k$ times) — or equivalently expanding by [[binomial-series|Newton's binomial theorem]] with negative integer exponent — gives

$$\frac{A}{(1 - pz)^k} \;=\; A + kAp z + \frac{k(k+1)}{2!}A p^2 z^2 + \frac{k(k+1)(k+2)}{3!}A p^3 z^3 + \cdots,$$

with general term

$$\frac{(n+1)(n+2)\cdots(n+k-1)}{(k-1)!}\,A p^n z^n \;=\; \binom{n + k - 1}{k - 1}\, A p^n z^n.$$

Euler verifies the equivalence of the two factorial expressions $\dfrac{(n+1)\cdots(n+k-1)}{1\cdot 2\cdots(k-1)}$ and $\dfrac{k(k+1)\cdots(k+n-1)}{1\cdot 2\cdots n}$ by cross-multiplication: both equal $\dfrac{(n+k-1)!}{n!\,(k-1)!}$ (source: chapter13, §215).

## Examples I–V (§216, p. 183–186)

### Example I — distinct real factors

$$\frac{1 - z}{1 - z - 2z^2} \;=\; \frac{2/3}{1 + z} + \frac{1/3}{1 - 2z}.$$

General term: $\left(\tfrac{2}{3}(-1)^n + \tfrac{1}{3}\,2^n\right) z^n = \dfrac{2^n \pm 2}{3}\,z^n$ (positive sign for even $n$). The series begins $1 + 0z + 2z^2 + 2z^3 + 6z^4 + 10z^5 + 22z^6 + \cdots$.

### Example II — distinct real factors

$$\frac{1 - z}{1 - 5z + 6z^2} \;=\; \frac{-1}{1 - 2z} + \frac{2}{1 - 3z}.$$

General term: $(2\cdot 3^n - 2^n)z^n$.

### Example III — Lucas numbers (Binet form)

$$\frac{1 + 2z}{1 - z - z^2}$$

has roots $(1 \pm \sqrt 5)/2$ and partial fractions $\dfrac{(\sqrt 5 + 1)/2}{1 - \tfrac{1+\sqrt 5}{2}z} + \dfrac{(1 - \sqrt 5)/2}{1 - \tfrac{1-\sqrt 5}{2}z}$. General term:

$$\left(\tfrac{1+\sqrt 5}{2}\right)^{n+1} z^n + \left(\tfrac{1-\sqrt 5}{2}\right)^{n+1} z^n.$$

This is the [[closed-form-two-term-recurrence|Binet-type formula]] for the Lucas-like sequence $1, 3, 4, 7, 11, 18, 29, 47, \ldots$.

### Example IV — symbolic two-term recurrence

For the general $\dfrac{a + bz}{1 - \alpha z - \beta z^2}$, partial fractions over the roots $(\alpha \pm \sqrt{\alpha^2 + 4\beta})/2$ give general term

$$\frac{a(\sqrt{\alpha^2+4\beta} + \alpha) + 2b}{2\sqrt{\alpha^2+4\beta}}\!\left(\!\frac{\alpha + \sqrt{\alpha^2+4\beta}}{2}\!\right)^{\!n}\!z^n + \frac{a(\sqrt{\alpha^2+4\beta} - \alpha) - 2b}{2\sqrt{\alpha^2+4\beta}}\!\left(\!\frac{\alpha - \sqrt{\alpha^2+4\beta}}{2}\!\right)^{\!n}\!z^n.$$

Euler comments: "from this result it becomes reasonably easy to express the general term of any recurrent series in which each term is determined by the two preceding terms" (source: chapter13, §216 Example IV). See [[closed-form-two-term-recurrence]].

### Example V — repeated linear factor

$$\frac{1}{1 - z - z^2 + z^3} \;=\; \frac{1}{(1 - z)^2(1 + z)} \;=\; \frac{1/2}{(1 - z)^2} + \frac{1/4}{1 - z} + \frac{1/4}{1 + z}.$$

General term: $\tfrac{1}{2}(n+1)z^n + \tfrac{1}{4}z^n + \tfrac{1}{4}(-1)^n z^n = \dfrac{2n + 3 \pm 1}{4}z^n$ (positive sign for even $n$).

## Quadratic-factor brick (§217–§222)

For complex roots, [[real-partial-fraction-decomposition|Chapter 12]] gives a real partial fraction with [[trinomial-factor|trinomial]] denominator. Euler now needs the general term of

$$\frac{A + Bpz}{(1 - 2pz\cos\phi + p^2 z^2)^k}.$$

### Base case $k = 1$ (§217–§218)

The series for $\dfrac{A}{1 - 2pz\cos\phi + p^2 z^2}$ is the [[trigonometric-recurrent-progression|§129 sin/cos progression]]:

$$A + 2Apz\cos\phi + Ap^2 z^2\bigl(2(2\cos^2\phi) - 1\bigr) + \cdots,$$

whose coefficients satisfy $\cos n\phi = 2\cos\phi\cos(n-1)\phi - \cos(n-2)\phi$ (source: chapter13, §217). The general term of the series is

$$\frac{\sin(n+1)\phi}{\sin\phi}\,A p^n z^n.$$

For the more general numerator $A + Bpz$, decompose

$$\frac{A + Bpz}{1 - 2pz\cos\phi + p^2 z^2} \;=\; \frac{P pz\sin\phi}{1 - 2pz\cos\phi + p^2 z^2} + \frac{Q - Qpz\cos\phi}{1 - 2pz\cos\phi + p^2 z^2},$$

with $Q = A$ and $P = A\cot\phi + B\csc\phi$ (source: chapter13, §218). The first piece has general term $P\sin(n\phi)\,p^n z^n$; the second has $Q\cos(n\phi)\,p^n z^n$. Sum and simplify:

$$\boxed{\frac{A\sin(n+1)\phi + B\sin n\phi}{\sin\phi}\,p^n z^n.}$$

### Higher $k$ (§219–§222)

For $k \ge 2$, Euler decomposes into a complex pair

$$\frac{A + Bpz}{(1 - 2pz\cos\phi + p^2 z^2)^k} \;=\; \frac{\tilde a}{(1 - (\cos\phi+i\sin\phi)pz)^k} + \frac{\tilde b}{(1 - (\cos\phi-i\sin\phi)pz)^k},$$

applies the §215 linear-factor brick to each piece (giving binomial coefficients), and converts back to real form via $f = \tilde a + \tilde b$, $g = (\tilde a - \tilde b)/i$. The result for $k = 2$ (§220) is

$$\frac{(n+3)\sin(n+1)\phi - (n+1)\sin(n+3)\phi}{4\sin^3\phi}\,A p^n z^n + \frac{(n+2)\sin n\phi - n\sin(n+2)\phi}{4\sin^3\phi}\,B p^n z^n.$$

For $k = 3$ (§221) the formula expands with denominator $16\sin^5\phi$ and three sine multiples in the numerator, using the identity $16\sin^5\phi = 10\sin\phi - 5\sin 3\phi + \sin 5\phi$. For $k = 4$ (§222), denominator $64\sin^7\phi$ and four sine multiples, via $64\sin^7\phi = 35\sin\phi - 21\sin 3\phi + 7\sin 5\phi - \sin 7\phi$. The pattern continues with higher Chebyshev-like identities

$$256\sin^9\phi = 126\sin\phi - 84\sin 3\phi + 36\sin 5\phi - 9\sin 7\phi + \sin 9\phi,\;\ldots$$

(source: chapter13, §222). The same odd-power table is derived systematically — alongside the even-power $\cos kz$ companion — in Chapter 14 §262; see [[powers-of-sine-and-cosine]].

## Combining the bricks: §223 examples

### Example I — mixed factors with mod-6 cases

$$\frac{1}{(1-z)(1-z^2)(1-z^3)} \;=\; \frac{1}{(1-z)^3(1+z)(1+z+z^2)}$$

decomposes as

$$\frac{1/6}{(1-z)^3} + \frac{1/4}{(1-z)^2} + \frac{17/72}{1-z} + \frac{1/8}{1+z} + \frac{(2+z)/9}{1+z+z^2}.$$

Each piece has a general term; the last (with $\phi = \pi/3$) gives $\dfrac{4\sin\tfrac{(n+1)\pi}{3} - 2\sin\tfrac{n\pi}{3}}{9\sqrt 3}(-1)^n z^n$. Summing all five gives a single formula

$$\left(\frac{n^2}{12} + \frac{n}{2} + \frac{47}{72}\right) z^n \pm \frac{1}{8}z^n \pm \frac{4\sin\tfrac{(n+1)\pi}{3} - 2\sin\tfrac{n\pi}{3}}{9\sqrt 3}\,z^n,$$

which simplifies into *six* cases by residue $n \bmod 6$ — for example, $n = 6m$ gives $\left(\tfrac{n^2}{12} + \tfrac{n}{2} + 1\right)z^n$, $n = 6m+1$ gives $\left(\tfrac{n^2}{12} + \tfrac{n}{2} + \tfrac{5}{12}\right)z^n$, and so on (source: chapter13, §223 Example I). At $n = 50$: $n = 6\cdot 8 + 2$, so the coefficient is $\tfrac{2500}{12} + 25 + \tfrac{2}{3} = 234$, i.e. $234 z^{50}$. (This series is the partition-counting generating function $\prod (1-z^k)^{-1}$ truncated at $k = 3$ — the number of partitions of $n$ into parts $\le 3$.)

### Example II — four cases mod 4

$$\frac{1+z+z^2}{1 - z - z^4 + z^5} \;=\; \frac{1+z+z^2}{(1-z)^2(1+z)(1+z^2)}$$

decomposes as

$$\frac{3/4}{(1-z)^2} + \frac{3/8}{1-z} + \frac{1/8}{1+z} - \frac{(1+z)/4}{1+z^2}.$$

The last piece has $\cos\phi = 0$, $\phi = \pi/2$, giving general term $\bigl(-\tfrac{1}{4}\sin\tfrac{(n+1)\pi}{2} + \tfrac{1}{4}\sin\tfrac{n\pi}{2}\bigr) z^n$. The full general term is $\left(\tfrac{3n}{4} + \tfrac{9}{8}\right)z^n \pm \tfrac{1}{8}z^n - \tfrac{1}{4}\bigl(\sin\tfrac{(n+1)\pi}{2} - \sin\tfrac{n\pi}{2}\bigr)z^n$, splitting into four mod-4 cases. At $n = 50$: $n = 4\cdot 12 + 2$, coefficient $\tfrac{3\cdot 50}{4} + \tfrac{3}{2} = 39$, i.e. $39 z^{50}$.

## Dominant term and Bernoulli's method (Chapter 17)

Reading the linear-factor brick $(**)$ component by component, $P_n = U p^n + V q^n + \cdots$ with $|p| > |q| > \cdots$, the *largest-magnitude* term $U p^n$ swamps the rest as $n \to \infty$. Hence the **ratio of consecutive terms** converges:

$$\frac{P_{n+1}}{P_n} \;=\; \frac{U p^{n+1} + V q^{n+1} + \cdots}{U p^n + V q^n + \cdots} \;\longrightarrow\; p.$$

This is the algebraic content of [[bernoullis-method-for-roots|Daniel Bernoulli's method]] for finding the largest root of an algebraic equation: from the equation's coefficients, read the [[scale-of-the-relation|scale]], run the recurrent series, and the quotient $Q/P$ approximates the largest root in absolute value. The quadratic-factor brick complicates this: if a [[trinomial-factor|trinomial factor]] dominates, $P_n$ is sinusoidal in $n$ and $Q/P$ oscillates — [[trinomial-factor-from-recurrent-series|§348–§352]] then extracts both modulus and argument of the dominant complex conjugate pair from four consecutive coefficients in closed form.

## Why this matters

The general-term machinery makes the recurrent series a genuine *closed-form* object: the $n$-th coefficient is computable directly from $n$, without iterating the recurrence. The trigonometric form for quadratic factors anticipates the modern theory of constant-coefficient linear recurrences with complex roots (oscillatory solutions $r^n\cos n\phi$, $r^n\sin n\phi$), and the casework on residues mod the period $k$ is the discrete analogue of the splitting of solutions by characteristic root.

For combinatorial generating functions this technique gives explicit asymptotic and even *exact* formulas — Euler's §223 Example I is essentially the formula for the number of partitions of $n$ into parts of size $\le 3$, with the answer split by residue class.

## Related pages

- [[recurrent-series]]
- [[scale-of-the-relation]]
- [[closed-form-two-term-recurrence]]
- [[sum-of-recurrent-series]]
- [[partial-fraction-decomposition]]
- [[real-partial-fraction-decomposition]]
- [[trinomial-factor]]
- [[trigonometric-recurrent-progression]]
- [[binomial-series]]
- [[de-moivre-formula]]
- [[powers-of-sine-and-cosine]]
- [[chapter-13-on-recurrent-series]]
- [[bernoullis-method-for-roots]]
- [[trinomial-factor-from-recurrent-series]]
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]]
