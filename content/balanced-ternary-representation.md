# Balanced Ternary Representation

**Summary**: Euler's theorem (§330–§331): every integer — positive, negative, or zero — has a unique representation as $\sum_k c_k\,3^k$ with digits $c_k \in \{-1, 0, +1\}$. The proof mirrors the binary case: the formal Laurent product $\prod_{k\geq 0}(x^{-3^k} + 1 + x^{3^k})$ has every coefficient equal to $1$ at every power of $x$, positive or negative. Application: weighing on a two-pan balance with weights $1, 3, 9, 27, 81, \ldots$ pounds.

**Sources**: chapter16.pdf

**Last updated**: 2026-05-11

---

## Statement

$$\prod_{k\geq 0}(x^{-3^k} + 1 + x^{3^k}) = \sum_{n\in\mathbb Z} x^n.$$

Equivalently, every integer $n \in \mathbb Z$ has a unique representation

$$n = \sum_{k\geq 0} c_k\,3^k,\qquad c_k \in \{-1, 0, +1\}.$$

(Source: chapter16.pdf, §331.)

## Euler's proof (§331)

Let

$$P = \prod_{k\geq 0}(x^{-3^k} + 1 + x^{3^k}) = \cdots + cx^{-3} + bx^{-2} + ax^{-1} + 1 + \alpha x + \beta x^2 + \gamma x^3 + \delta x^4 + \epsilon x^5 + \cdots.$$

The product is a **formal Laurent series** — both positive and negative powers of $x$ appear because of the $x^{-3^k}$ terms.

Substituting $x^3$ for $x$ drops the $k = 0$ factor:

$$\prod_{k\geq 1}(x^{-3^k} + 1 + x^{3^k}) = \frac{P}{x^{-1} + 1 + x}.$$

The left side is

$$P(x^3) = \cdots + cx^{-9} + bx^{-6} + ax^{-3} + 1 + \alpha x^3 + \beta x^6 + \gamma x^9 + \cdots.$$

Hence

$$P = (x^{-1} + 1 + x)\cdot P(x^3) = \cdots + ax^{-4} + ax^{-3} + ax^{-2} + bx^{-1}\cdot(\ldots)\cdot\ldots + 1 + x + \alpha x^2 + \alpha x^3 + \alpha x^4 + \beta x^5 + \beta x^6 + \beta x^7 + \gamma x^8 + \gamma x^9 + \gamma x^{10} + \cdots,$$

after multiplying the three-term factor through. Comparing with the original expansion of $P$ term by term:

$$\alpha = 1,\quad \beta = \alpha,\quad \gamma = \alpha,\quad \delta = \alpha,\quad \epsilon = \beta,\quad \zeta = \beta,\ldots\quad\text{and}\quad a = 1,\quad b = a,\quad c = a,\ldots$$

All coefficients (positive and negative powers) equal $1$. Therefore

$$P = \sum_{n\in\mathbb Z} x^n = \cdots + x^{-3} + x^{-2} + x^{-1} + 1 + x + x^2 + x^3 + \cdots.$$

## Combinatorial interpretation

Expanding $\prod(x^{-3^k} + 1 + x^{3^k})$ as a sum over choices of one of three terms from each factor:

$$P = \sum_{\substack{(c_k)_{k\geq 0}\\c_k \in \{-1, 0, +1\}}} x^{\sum_k c_k\,3^k}.$$

The coefficient of $x^n$ is the number of sequences $(c_k)$ with $\sum c_k 3^k = n$. Euler's identity says this count is **always $1$** — every integer has a unique balanced-ternary representation.

## Application: weighing with ternary weights on a two-pan balance (§330)

A set of weights $1, 3, 9, 27, 81, \ldots$ pounds suffices to weigh any whole number of pounds on a **two-pan balance**: each weight goes either on the opposite pan from the goods (digit $+1$), on the same pan as the goods (digit $-1$), or off the scale (digit $0$). Euler's examples (§330):

$$1 = 1\quad 2 = 3 - 1\quad 3 = 3\quad 4 = 3 + 1\quad 5 = 9 - 3 - 1\quad 6 = 9 - 3\quad 7 = 9 - 3 + 1\quad 8 = 9 - 1\quad 9 = 9$$

$$10 = 9 + 1\quad 11 = 9 + 3 - 1\quad 12 = 9 + 3.$$

With $n$ weights ($1, 3, \ldots, 3^{n-1}$, total $(3^n - 1)/2$), any integer up to $(3^n - 1)/2$ can be weighed — a much faster growth than binary's $2^n - 1$. Six ternary weights ($1, 3, 9, 27, 81, 243$, total $364$) reach $364$; six binary weights reach only $63$.

## Comparison to binary (§329 vs §331)

|                       | Binary                              | Balanced ternary                                      |
|-----------------------|-------------------------------------|-------------------------------------------------------|
| Identity              | $\prod(1 + x^{2^k}) = 1/(1 - x)$    | $\prod(x^{-3^k} + 1 + x^{3^k}) = \sum_{n\in\mathbb Z}x^n$ |
| Digits                | $\{0, 1\}$                          | $\{-1, 0, +1\}$                                       |
| Range with $n$ weights | $0$ to $2^n - 1$                   | $-(3^n - 1)/2$ to $(3^n - 1)/2$                       |
| Physical              | one-pan scale                       | two-pan scale                                         |

## Modern reading

The trick — make a *symmetric* digit set $\{-1, 0, +1\}$ so that the product covers all integers, not just non-negative ones — is exactly the modern notion of **balanced ternary** (also called signed-digit ternary). It is used in some digital-arithmetic algorithms (Booth multiplier, non-adjacent form for elliptic-curve scalar multiplication) precisely because the symmetric digit set eliminates the need for a separate sign bit. Euler's two pages (§330–§331) are the earliest known appearance of the system.

## Related pages

- [[chapter-16-on-the-partition-of-numbers]]
- [[partition-of-numbers]]
- [[partition-generating-functions]]
- [[binary-representation-theorem]]
- [[geometric-series]]
