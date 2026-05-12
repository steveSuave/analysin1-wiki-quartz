# Geometric-Mean Method for Logarithms

**Summary**: Euler's §106 algorithm for computing a [[logarithm]] to arbitrary precision using only square roots and bisection. Bracket the target between two numbers whose logs are known, replace one bound by the geometric mean (whose log is the arithmetic mean of the two known logs), and iterate. This is how Briggs and Vlacq computed the historical tables of common logarithms.

**Sources**: chapter6 (§106)

**Last updated**: 2026-04-26

---

## The principle

If $\log y = z$ and $\log v = x$, then

$$\log \sqrt{vy} = \frac{x + z}{2}.$$

That is, *the logarithm of the geometric mean is the arithmetic mean of the logarithms* (source: chapter6, §106). Combined with bracketing, this gives a binary-search-like algorithm: each square root halves the bracket containing the target.

## The algorithm

To find $\log b$:

1. Choose two anchors $A < B$ with known logs $\log A, \log B$ such that $A < b < B$.
2. Compute the geometric mean $C = \sqrt{AB}$, with $\log C = (\log A + \log B)/2$.
3. Compare $b$ to $C$. Replace whichever of $A, B$ is on the *wrong* side of $b$ with $C$, so the new bracket still encloses $b$.
4. Repeat until the geometric mean equals $b$ to the desired number of decimal places.

Each iteration costs one square root and one comparison.

## Worked example: $\log_{10} 5$

Take base $a = 10$. Bracket: $1 < 5 < 10$, so $A = 1$, $\log A = 0$ and $B = 10$, $\log B = 1$ (source: chapter6, §106 example).

| Step | New value | Definition | Log |
|:--|:--|:--|:--|
| $A$ | $1.000000$ | | $0.0000000$ |
| $B$ | $10.000000$ | | $1.0000000$ |
| $C$ | $3.162277$ | $\sqrt{AB}$ | $0.5000000$ |
| $D$ | $5.623413$ | $\sqrt{BC}$ | $0.7500000$ |
| $E$ | $4.216964$ | $\sqrt{CD}$ | $0.6250000$ |
| $F$ | $4.869674$ | $\sqrt{DE}$ | $0.6875000$ |
| $G$ | $5.232991$ | $\sqrt{DF}$ | $0.7187500$ |
| $H$ | $5.048065$ | $\sqrt{FG}$ | $0.7031250$ |
| $I$ | $4.958069$ | $\sqrt{FH}$ | $0.6953125$ |
| $K$ | $5.002865$ | $\sqrt{HI}$ | $0.6992187$ |
| $L$ | $4.980416$ | $\sqrt{IK}$ | $0.6972656$ |
| ... | ... | ... | ... |
| $Z$ | $5.000000$ | (stable) | $0.6989700$ |

After roughly 26 iterations the geometric mean has stabilized at $5.000000$, giving $\log_{10} 5 \approx 0.6989700$, equivalently $10^{0.6989700} \approx 5$.

## Convergence

Each step halves the *log-bracket* — the interval $[\log A, \log B]$. After $n$ steps the bracket has length $2^{-n}$, so $n \approx 3.32\, d$ steps suffice for $d$ decimal places of $\log b$. The corresponding bracket for $b$ itself does not halve linearly (it depends on the local slope of $a^z$), but it shrinks geometrically.

## Why only square roots are needed

The four log-rules of §104 say $\log(\text{geometric mean}) = $ arithmetic mean. This is the *only* nontrivial operation needed: with bracketing and geometric means, one can compute $\log b$ to any precision — and inversely, given $\log b$ as a binary expansion, one can recover $b$ by the same iteration in reverse.

## Historical role

Euler notes this is the method by which **Briggs** and **Vlacq** computed the original tables of common logarithms in the seventeenth century (source: chapter6, §106). Their tables of $\log p$ for prime $p$ then generated, via §109, the logarithms of all integers — and ultimately of every rational, by addition and subtraction.

Faster series-based methods were available by Euler's time and are introduced in subsequent chapters; the geometric-mean method survives as the conceptually simplest derivation.

## Related pages

- [[logarithm]]
- [[transcendence-of-logarithms]]
- [[common-logarithm]]
- [[change-of-base]]
- [[chapter-6-on-exponentials-and-logarithms]]
