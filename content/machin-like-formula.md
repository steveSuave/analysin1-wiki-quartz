# Machin-like Formula

**Summary**: §142 of Chapter 8. To compute $\pi$ rapidly without irrational denominators, Euler decomposes $\pi/4$ as a sum of two arctangents of small rational numbers:

$$\frac{\pi}{4} = \arctan\frac{1}{2} + \arctan\frac{1}{3}.$$

Combining with the [[arctangent-series|arctangent series]] gives

$$\pi = 4\left(\frac{1}{1\cdot 2} - \frac{1}{3\cdot 2^3} + \frac{1}{5\cdot 2^5} - \cdots\right) + 4\left(\frac{1}{1\cdot 3} - \frac{1}{3\cdot 3^3} + \frac{1}{5\cdot 3^5} - \cdots\right),$$

two rational geometric-rate series, "with much more ease than with the series mentioned before."

**Sources**: chapter8 (§142)

**Last updated**: 2026-04-27

---

## The decomposition

Suppose $a + b = \pi/4$, so $\tan(a + b) = 1$. The §128 addition formula gives

$$\tan(a + b) = \frac{\tan a + \tan b}{1 - \tan a\tan b} = 1\quad\Longrightarrow\quad 1 - \tan a\tan b = \tan a + \tan b,$$

$$\tan b = \frac{1 - \tan a}{1 + \tan a}.$$

(source: chapter8, §142). Choose $\tan a = 1/2$. Then

$$\tan b = \frac{1 - 1/2}{1 + 1/2} = \frac{1/2}{3/2} = \frac{1}{3}.$$

Hence

$$\frac{\pi}{4} = \arctan\frac{1}{2} + \arctan\frac{1}{3}.$$

## The two series

Substituting $t = 1/2$ in $\arctan t = t - t^3/3 + t^5/5 - \cdots$:

$$\arctan\frac{1}{2} = \frac{1}{2} - \frac{1}{3\cdot 2^3} + \frac{1}{5\cdot 2^5} - \frac{1}{7\cdot 2^7} + \cdots$$

Substituting $t = 1/3$:

$$\arctan\frac{1}{3} = \frac{1}{3} - \frac{1}{3\cdot 3^3} + \frac{1}{5\cdot 3^5} - \frac{1}{7\cdot 3^7} + \cdots$$

Therefore

$$\pi = 4\left(\frac{1}{1\cdot 2} - \frac{1}{3\cdot 2^3} + \frac{1}{5\cdot 2^5} - \frac{1}{7\cdot 2^7} + \frac{1}{9\cdot 2^9} - \cdots\right) + 4\left(\frac{1}{1\cdot 3} - \frac{1}{3\cdot 3^3} + \frac{1}{5\cdot 3^5} - \frac{1}{7\cdot 3^7} + \frac{1}{9\cdot 3^9} - \cdots\right).$$

(source: chapter8, §142). Both series have only *rational* terms, decay geometrically at rate $1/4$ and $1/9$ respectively, and avoid the $\sqrt 3$ that complicates the [[arctangent-series|§141]] series.

## Convergence rate

Per term in the $\arctan(1/2)$ series, the magnitude shrinks roughly by $1/4$. In the $\arctan(1/3)$ series, by $1/9$. So:

| Terms used | Approximate digits of $\pi$ |
|:--:|:--:|
| 5 | 4 |
| 10 | 8 |
| 15 | 12 |
| 20 | 16 |

This is a dramatic improvement over Leibniz ($t = 1$, no convergence in any practical sense) and a significant improvement over §141's $t = 1/\sqrt 3$ series (irrational terms, factor $\sim 1/3$ per step).

## Naming and history

Euler attributes this style of identity to no-one in §142 — he simply derives it. The general technique is named after John Machin, who in 1706 used the identity

$$\frac{\pi}{4} = 4\arctan\frac{1}{5} - \arctan\frac{1}{239}$$

to compute $\pi$ to 100 digits — the first 100-digit computation of $\pi$ in history. Euler's $\arctan(1/2) + \arctan(1/3)$ identity is a simpler cousin in the same family. Both rely on the same algebraic manipulation: choose $\tan a$ rational with small denominator, solve $\tan b = (1 - \tan a)/(1 + \tan a)$ for the complementary arc, and check that $\tan b$ is also rational with small denominator.

The general "Machin-like formula" pattern $\pi/4 = \sum c_k \arctan(p_k/q_k)$ with $c_k$ integers and $p_k/q_k$ rational is, after this section, the canonical method for computing $\pi$ to high precision. It dominated $\pi$ computation from the 18th into the early 20th century, when iterative methods (Gauss–Brent–Salamin, etc.) finally surpassed it.

## Pattern: combining arctangents

The §142 derivation generalizes. From $\tan(a + b) = (\tan a + \tan b)/(1 - \tan a\tan b)$:

$$\arctan p + \arctan q = \arctan\frac{p + q}{1 - pq}\qquad (\text{when } pq < 1).$$

Picking $p, q$ small and rational so that $(p+q)/(1 - pq)$ also lands at a useful arc — e.g., 1 (giving $\pi/4$), $\tan(\pi/3) = \sqrt 3$, etc. — produces an unending family of identities. The §142 choice $p = 1/2$, $q = 1/3$ gives $(p+q)/(1-pq) = (5/6)/(5/6) = 1$, exactly the value at which $\arctan = \pi/4$.

## Why Euler stops here

The chapter ends at §142, with the Machin-style formula as the final word on rapid computation of $\pi$. No further arctangent decompositions are explored, and the *Introductio*'s treatment of $\pi$ pauses here. Later chapters and other works return to the topic — Euler himself derived several improved Machin-like formulas in subsequent papers — but in the *Introductio* the §142 identity stands as the definitive practical tool.

## Related pages

- [[arctangent-series]]
- [[pi]]
- [[trigonometric-addition-formulas]]
- [[eulers-formula]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
