# Sum of a Recurrent Series

**Summary**: Euler (§231–§233) computes the sum of a [[recurrent-series|recurrent series]], finite or infinite. The infinite sum equals the generating rational function (when convergent). The partial sum up to $Pz^n$ is the rational function minus a "tail" rational function with shifted numerator. For a two-member [[scale-of-the-relation|scale]], the partial sum collapses to a remarkably clean closed form involving only the last two terms of the partial sum.

**Sources**: chapter13.pdf

**Last updated**: 2026-05-07

---

## Infinite sum (§231)

For a [[recurrent-series|recurrent series]]

$$A + Bz + Cz^2 + Dz^3 + \cdots,$$

with [[scale-of-the-relation|scale]] $\alpha, -\beta, \gamma, -\delta$ — denominator $1 - \alpha z + \beta z^2 - \gamma z^3 + \delta z^4$ — the sum equals the generating rational function

$$\frac{a + bz + cz^2 + dz^3}{1 - \alpha z + \beta z^2 - \gamma z^3 + \delta z^4},$$

where the numerator is determined by matching power-series coefficients to $A, B, C, D$:

$$a = A,\quad b = B - \alpha A,\quad c = C - \alpha B + \beta A,\quad d = D - \alpha C + \beta B - \gamma A$$

(source: chapter13.pdf, §231–§232). The numerator degree is one less than the denominator.

This is consistent with [[recurrent-series|§63's]] derivation: the recurrence becomes homogeneous from the $(k+1)$-th coefficient onward, where $k$ is the scale length, so the numerator stops at degree $k - 1$.

## Partial sum (§232)

To find $S = A + Bz + Cz^2 + \cdots + Pz^n$, write

$$S = (\text{full infinite sum}) - (\text{tail starting at }Qz^{n+1}).$$

The tail $t = Qz^{n+1} + Rz^{n+2} + Sz^{n+3} + \cdots$ is itself a recurrent series with the *same* scale, so dividing by $z^{n+1}$ produces another recurrent series. Hence

$$t \;=\; \frac{Qz^{n+1} + (R - \alpha Q)z^{n+2} + (S - \alpha R + \beta Q)z^{n+3} + (T - \alpha S + \beta R - \gamma Q)z^{n+4}}{1 - \alpha z + \beta z^2 - \gamma z^3 + \delta z^4}$$

(source: chapter13.pdf, §232). Subtracting from the infinite sum:

$$S \;=\; \frac{a + bz + cz^2 + dz^3 - (R - \alpha Q)z^{n+2} - (S - \alpha R + \beta Q)z^{n+3} - (T - \alpha S + \beta R - \gamma Q)z^{n+4} - Qz^{n+1}}{1 - \alpha z + \beta z^2 - \gamma z^3 + \delta z^4}.$$

(Euler's signs are consolidated in the final expression at §232.)

## Two-member scale collapses cleanly (§233)

When the scale has only two members $\alpha, -\beta$, the tail formula simplifies dramatically. Using the recurrence $R = \alpha Q - \beta P$ to eliminate $R$:

$$\boxed{\,A + Bz + Cz^2 + \cdots + Pz^n \;=\; \frac{A + (B - \alpha A)z - Qz^{n+1} + \beta P z^{n+2}}{1 - \alpha z + \beta z^2}.\,}$$

(source: chapter13.pdf, §233). Only the *last two* terms $P, Q$ of the partial sum (and the first two $A, B$) enter the formula — every middle term has cancelled out.

## Worked Lucas example (§233)

For $1 + 3z + 4z^2 + 7z^3 + 11z^4 + \cdots + Pz^n$ with $\alpha = 1, \beta = -1, A = 1, B = 3$:

$$\sum_{k=0}^{n} L_k z^k \;=\; \frac{1 + 2z - Qz^{n+1} - Pz^{n+2}}{1 - z - z^2}.$$

At $z = 1$ (substituting numerically into the partial sum identity, *not* the rational function which diverges there):

$$1 + 3 + 4 + 7 + 11 + \cdots + P \;=\; P + Q - 3,$$

where $Q$ is the next Lucas-like number. Using §227's $Q = (P + \sqrt{5P^2 + 20})/2$ (sign by parity), the partial sum is

$$1 + 3 + 4 + 7 + 11 + \cdots + P \;=\; \frac{3P - 6 + \sqrt{5P^2 + 20}}{2}.$$

The partial sum is determined by the *last term alone* (source: chapter13.pdf, §233 Example).

Spot-check: $P = 11$ gives $(33 - 6 + \sqrt{605 + 20})/2 = (27 + 25)/2 = 26$. And $1 + 3 + 4 + 7 + 11 = 26$. ✓

## Notable points

- **The cancellation is structural, not accidental.** The recurrence $X_{n+2} = \alpha X_{n+1} - \beta X_n$ means that from the third term onward, every coefficient is a $\mathbb Z$-linear combination of the previous two. So the partial sum, telescoped against the rational function, collapses to a polynomial whose only surviving terms are at the boundaries.
- **§231 needs convergence to be a numerical statement.** As an *identity of formal power series*, the sum-equals-rational-function statement holds always. As a numerical equality — with $z$ given a specific value — it requires $|z| < \min|p|^{-1}$ where $p$ runs over roots of the denominator. Euler does not flag this; it is implicit in his manipulation.
- **The partial sum lets one evaluate at $z = 1$.** Even when the infinite sum diverges (as in the Lucas example), the *partial* sum at $z = 1$ is a finite expression, and the §233 formula still applies. This converts the partial-sum problem into evaluating a specific algebraic expression in the last term — a substantial simplification over summing the recurrence directly.
- **The formula generalizes upward in scale length.** §232 writes out the $k = 4$ scale in full; the same telescoping mechanism gives a closed-form partial sum for any scale length, with the boundary terms involving the first $k$ and last $k$ series coefficients.

## Why this matters

For finite sums of linear-recurrence sequences, §233 gives a *single arithmetic step* from any one term to the partial sum up to that term. For Fibonacci, Lucas, Pell, and more general two-member-scale sequences, this is a one-line formula — historically the first such systematic treatment.

For *generating function* purposes the §231 identity is the foundation: it says the rational function is *the* sum, not just a formal device. This is the basis for residue-style asymptotic analysis of recurrence solutions, in which one extracts coefficient asymptotics from the poles of the generating rational function.

## Related pages

- [[recurrent-series]]
- [[general-term-of-recurrent-series]]
- [[scale-of-the-relation]]
- [[closed-form-two-term-recurrence]]
- [[partial-fraction-decomposition]]
- [[chapter-13-on-recurrent-series]]
