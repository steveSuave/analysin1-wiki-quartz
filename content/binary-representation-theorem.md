# Binary Representation Theorem

**Summary**: Euler's algebraic proof (§328–§329) that every non-negative integer has a unique representation as a sum of distinct powers of $2$. The identity $\prod_{k\geq 0}(1 + x^{2^k}) = 1/(1 - x)$ shows that the generating function for partitions into distinct powers of $2$ is exactly the geometric series — so each $x^n$ appears with coefficient $1$. Application: weighing with binary weights $1, 2, 4, 8, \ldots$ on a one-pan scale.

**Sources**: chapter16

**Last updated**: 2026-05-11

---

## Statement

$$\prod_{k\geq 0}(1 + x^{2^k}) = (1 + x)(1 + x^2)(1 + x^4)(1 + x^8)(1 + x^{16})\cdots = \sum_{n\geq 0} x^n = \frac{1}{1 - x}.$$

Equivalently, every non-negative integer $n$ admits a unique representation

$$n = \sum_{i\in S} 2^i,\qquad S\subset \{0, 1, 2, \ldots\}\text{ finite}.$$

(Source: chapter16, §329.)

## Euler's proof (§328)

Let $P = \prod_{k\geq 0}(1 + x^{2^k})$ and write its expansion as

$$P = 1 + \alpha x + \beta x^2 + \gamma x^3 + \delta x^4 + \epsilon x^5 + \zeta x^6 + \eta x^7 + \theta x^8 + \cdots.$$

Substituting $x^2$ for $x$ drops the $k = 0$ factor:

$$\prod_{k\geq 1}(1 + x^{2^k}) = \frac{P}{1 + x},$$

and the left side is $P(x^2) = 1 + \alpha x^2 + \beta x^4 + \gamma x^6 + \delta x^8 + \cdots$. Hence

$$\frac{P}{1 + x} = 1 + \alpha x^2 + \beta x^4 + \gamma x^6 + \delta x^8 + \cdots,$$

and multiplying by $1 + x$:

$$P = 1 + x + \alpha x^2 + \alpha x^3 + \beta x^4 + \beta x^5 + \gamma x^6 + \gamma x^7 + \delta x^8 + \delta x^9 + \cdots.$$

Comparing term-by-term with the original expansion of $P$:

$$\alpha = 1,\quad \beta = \alpha,\quad \gamma = \alpha,\quad \delta = \beta,\quad \epsilon = \beta,\quad \zeta = \gamma,\quad \eta = \gamma,\quad \theta = \delta,\ldots$$

so **all coefficients are equal to $1$**. Therefore

$$P = 1 + x + x^2 + x^3 + x^4 + \cdots = \frac{1}{1 - x}.$$

## Combinatorial interpretation (§329)

Expanding $\prod(1 + x^{2^k})$ as a sum over choices of one term from each factor:

$$P = \sum_{S \subset \{0, 1, 2, \ldots\}}^{\text{finite}} x^{\sum_{k\in S}2^k}.$$

The coefficient of $x^n$ is the number of subsets $S$ with $\sum_{k\in S} 2^k = n$. Euler's identity shows this is always $1$ — every $n$ has **exactly one** such subset.

## Application: weighing with binary weights (§329)

A set of weights $1, 2, 4, 8, 16, 32, \ldots$ pounds suffices to weigh any whole-number weight on a one-pan scale, with each weight used at most once. With $n$ weights ($1, 2, 4, \ldots, 2^{n-1}$, totalling $2^n - 1$), any integer up to $2^n - 1$ pounds can be weighed:

> "With only the ten weights, 1 lb., 2 lb., 4 lb., 8 lb., 16 lb., 32 lb., 64 lb., 128 lb., 256 lb., 512 lb., anything up to 1024 lb. can be weighed. Indeed, if an eleventh weight weighing 1024 lb. is added to the set, then anything up to 2048 lb. can be weighed." (§329)

This is Euler's earliest published application of binary representation to practical computation. It anticipates by two centuries the use of binary in digital computation.

## Generalization

The same fixed-point argument applies to any sequence $a_0 < a_1 < a_2 < \ldots$ of integers with $a_{k+1} = ba_k$ for some integer $b$, leading to a unique base-$b$ representation. Euler immediately specializes to **balanced ternary** in §330–§331 — see [[balanced-ternary-representation]].

## Modern reading

This is the simplest **non-trivial generating-function identity for representation uniqueness**, and the prototype for a long tradition of representation theorems: Cantor's mixed-radix, Zeckendorf's Fibonacci representation, Ostrowski numeration, etc. The fixed-point trick — substitute $x \to x^b$, get a functional equation, conclude all coefficients agree — is the simplest of its kind.

Note also that the identity $\prod(1 + x^{2^k}) = 1/(1-x)$ is **dual** to Euler's [[distinct-parts-equals-odd-parts|distinct = odd]] theorem: there the distinct-part product equals an *odd*-restricted reciprocal product; here it equals the *unrestricted* geometric series.

## Related pages

- [[chapter-16-on-the-partition-of-numbers]]
- [[partition-of-numbers]]
- [[partition-generating-functions]]
- [[balanced-ternary-representation]]
- [[distinct-parts-equals-odd-parts]]
- [[geometric-series]]
