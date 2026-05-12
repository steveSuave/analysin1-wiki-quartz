# Closed Form for a Two-Term Recurrence

**Summary**: Euler's Binet-type formula (§226–§229) for any [[recurrent-series|recurrent series]] whose [[scale-of-the-relation|scale of the relation]] has length two. From the recurrence $X_n = \alpha X_{n-1} + \beta X_{n-2}$ with first terms $A, B$, the general term is $X_n = U p^n + V q^n$ where $p, q$ are the roots of $1 - \alpha z - \beta z^2$. The pair $(U, V)$ satisfies the invariant $UV = (B^2 - \alpha AB + \beta A^2)/(4\beta - \alpha^2)$, which lets each term be obtained from a single predecessor by an apparent — but illusory — square root.

**Sources**: chapter13.pdf, chapter17.pdf

**Last updated**: 2026-05-11

---

## Setup (§226)

Let the [[scale-of-the-relation|scale]] have two members $\alpha, \beta$, so

$$C = \alpha B - \beta A,\qquad D = \alpha C - \beta B,\qquad E = \alpha D - \beta C,\qquad \ldots$$

(Euler now uses sign $-\beta$ rather than $+\beta$; both forms are equivalent up to the substitution $\beta \mapsto -\beta$.) The series arises from a rational function with denominator $1 - \alpha z + \beta z^2$, factored as $(1 - pz)(1 - qz)$ with $p + q = \alpha$ and $pq = \beta$.

By [[partial-fraction-decomposition|partial fractions]] the closed-form general term is

$$X_n \;=\; U p^n + V q^n.$$

## Determining $U$ and $V$ (§226)

Setting $n = 0$ and $n = 1$:

$$A = U + V,\qquad B = Up + Vq.$$

Solving,

$$U = \frac{Aq - B}{q - p},\qquad V = \frac{Ap - B}{p - q}.$$

Equivalently $V = (B - Ap)/(q - p)$ — the formula is symmetric in $(p, U) \leftrightarrow (q, V)$.

## The $UV$ invariant (§227)

From $U = (Aq - B)/(q - p)$ and $V = (Ap - B)/(p - q)$, multiply:

$$UV \;=\; -\frac{(Aq - B)(Ap - B)}{(q - p)^2} \;=\; -\frac{A^2 pq - AB(p+q) + B^2}{(p+q)^2 - 4pq}.$$

Substitute $p + q = \alpha$ and $pq = \beta$:

$$\boxed{\,UV \;=\; \frac{B^2 - \alpha AB + \beta A^2}{4\beta - \alpha^2}\,}$$

(source: chapter13.pdf, §227). This is the *principal property of the recurrent series*: it is a constant determined entirely by the scale $\alpha, \beta$ and the first two terms $A, B$, independent of which two consecutive terms one uses to compute it.

## Term from a single predecessor (§227)

If $P = X_n$ is known, then $Q = X_{n+1}$ satisfies $Q = Up^{n+1} + Vq^{n+1}$ and $P = Up^n + Vq^n$. Eliminating $V$ via the $UV$ identity and solving:

$$Q \;=\; \tfrac{1}{2}\alpha P + \sqrt{\bigl(\tfrac{1}{4}\alpha^2 - \beta\bigr)P^2 + (B^2 - \alpha AB + \beta A^2)\,\beta^n}.$$

Although this expression *appears* irrational, the right side is in fact always rational, since the series coefficients are themselves rational by construction (source: chapter13.pdf, §227). The square root must therefore evaluate to a rational every time. Euler does not prove this — he merely observes it.

## Remote terms from two consecutive (§228–§229)

Given two successive terms $P = X_n$ and $Q = X_{n+1}$, Euler derives a closed form for the *doubly indexed* term $X = X_{2n}$:

$$X \;=\; \frac{(2A\beta - \alpha B)P^2 + 2BPQ - AQ^2}{B^2 - \alpha AB + \beta A^2}$$

(source: chapter13.pdf, §228). Eliminating the $\beta^n$ term in favor of an expression purely in $P$ and $Q$:

$$X \;=\; \frac{(\beta A - \alpha B)P^2 + 2BPQ - AQ^2}{B^2 - \alpha AB + \beta A^2}.$$

For $Y = X_{2n+1}$:

$$Y \;=\; \frac{-\beta B P^2 + 2\beta APQ + (\alpha B - \alpha^2 A)Q^2}{B^2 - \alpha AB + \beta A^2}.$$

(Section §229 sketches the same kind of formula for $X_{4n}, X_{4n+1}, X_{8n}, X_{8n+1}, \ldots$, by iterating the doubling.)

## Worked Lucas example (§229 Example)

For the series $1, 3, 4, 7, 11, 18, 29, 47, \ldots$ — sum-of-two-previous, so scale $\alpha = 1$, $\beta = -1$ in the §226 sign convention — the first terms are $A = 1, B = 3$, giving

$$B^2 - \alpha AB + \beta A^2 \;=\; 9 - 3 - 1 \;=\; 5.$$

(Adjusting signs back to Euler's $4\beta - \alpha^2 = -5$ shows the $UV$ identity gives $UV = 5/(-5)\cdot(\text{up to sign}) = -1$ — the standard Lucas-Fibonacci identity.)

Then

$$Q \;=\; \frac{P + \sqrt{5P^2 + 20\cdot(-1)^n}}{2} \;=\; \frac{P + \sqrt{5P^2 \pm 20}}{2}$$

(positive sign for even $n$, negative for odd). At $n = 4$, $P = 11$, so $Q = (11 + \sqrt{5\cdot 121 + 20})/2 = (11 + \sqrt{625})/2 = (11 + 25)/2 = 18$. ✓

Doubled-index formula: $X_{2n} = (-4P^2 + 6PQ - Q^2)/5$. At $n = 4$, $P = 11, Q = 18$: $X_8 = (-484 + 1188 - 324)/5 = 380/5 = 76$. ✓ (The 9th Lucas-like term in $1, 3, 4, 7, 11, 18, 29, 47, 76, \ldots$.)

Also $Q^2 = (3P^2 + 10 + P\sqrt{5P^2 \pm 20})/2$ and $X_{2n} = (-P^2 + 2 + P\sqrt{5P^2 \pm 20})/2$ — Euler gives both.

## Notable points

- **The §227 identity is the determinant of a Casorati-like matrix.** Modern phrasing: $UV = -(B^2 - \alpha AB + \beta A^2)/(p - q)^2$ is the determinant of the matrix $\begin{pmatrix} 1 & 1 \\ p & q\end{pmatrix}^{-1}\begin{pmatrix} A \\ B\end{pmatrix}\bigl(\text{transposed product}\bigr)$. Euler arrives at it by direct multiplication.
- **The "irrationality is illusory" phenomenon.** §227's square-root formula is conceptually striking: a rational sequence is computable from one predecessor only via an apparently irrational operation, yet the irrational part always cancels. The same phenomenon recurs in modern treatments of Lucas sequences — e.g. Fibonacci's $F_{n+1} = (F_n + \sqrt{5F_n^2 + 4(-1)^n})/2$ is the same formula in different signs.
- **The doubling formula generalizes.** §229 derives both $X_{2n}$ and $X_{2n+1}$ from $(X_n, X_{n+1})$. Iterating gives "Lucas's doubling" — modern fast Fibonacci computation in $O(\log n)$ operations is exactly this scheme.
- **§230 hints at the cubic generalization.** For a three-member scale, the analogous formula is a *cubic* in the next term given the two predecessors — Euler writes the cubic but does not solve it. The pattern continues: a $k$-member scale gives a degree-$k$ algebraic relation.

## Why this matters

The two-term scale closed form is the *Binet formula* in full generality. It compresses an arbitrary linear two-term recurrence into a single algebraic expression, with a discriminant-like invariant ($B^2 - \alpha AB + \beta A^2$) that controls when the sequence is rational vs. integral. Euler's §227 identity is the source of the modern theory of *Lucas sequences* developed in the 19th century.

## Dominant-root limit (Chapter 17)

Because $X_n = U p^n + V q^n$ with $|p| > |q|$, the ratio of consecutive terms converges to $p$:

$$\frac{X_{n+1}}{X_n} \;\to\; p \;=\; \frac{\alpha + \sqrt{\alpha^2 + 4\beta}}{2}$$

(in the $+\beta$ sign convention; equivalently, the larger root of $1 - \alpha z - \beta z^2$). This is the simplest instance of [[bernoullis-method-for-roots|Daniel Bernoulli's method]]: the [[chapter-17-using-recurrent-series-to-find-roots-of-equations|Chapter 17]] Example I uses $x^2 - 3x - 1 = 0$ with series $1, 2, 7, 23, 76, 251, 829, 2738$ and quotient $2738/829 = 3.3027744$, matching $(3+\sqrt{13})/2$ to six digits. The closed-form general term $Up^n + Vq^n$ explains *why* the ratio converges, and how fast — the convergence is geometric with ratio $|q/p|$.

## Related pages

- [[recurrent-series]]
- [[scale-of-the-relation]]
- [[general-term-of-recurrent-series]]
- [[sum-of-recurrent-series]]
- [[partial-fraction-decomposition]]
- [[chapter-13-on-recurrent-series]]
- [[bernoullis-method-for-roots]]
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]]
