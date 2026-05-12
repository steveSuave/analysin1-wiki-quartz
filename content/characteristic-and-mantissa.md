# Characteristic and Mantissa

**Summary**: §112–§113 of Chapter 6: the integer–fractional split of a base-10 logarithm. The integer part — the *characteristic* — equals one less than the digit count of the number. The fractional part — the *mantissa* — depends only on the digit pattern of the number, not on where the decimal point sits. Two numbers with the same mantissa share digits and differ only by a power of 10.

**Sources**: chapter6.pdf (§112–§113)

**Last updated**: 2026-04-26

---

## The split

For $N > 0$, write the [[common-logarithm]]

$$\log_{10} N = c + m, \qquad c \in \mathbb{Z}, \quad m \in [0, 1).$$

- $c$ is the **characteristic**.
- $m$ is the **mantissa**.

This decomposition is unique (source: chapter6.pdf, §112).

## The characteristic counts digits

For $N \ge 1$ with $k$ digits in its integer part, $10^{k-1} \le N < 10^k$, so $\log N \in [k-1, k)$ and hence $c = k - 1$.

> The characteristic of a number is one less than the number of digits which express the number.

(source: chapter6.pdf, §112)

Examples:

| $N$ | Digits | Characteristic |
|:--|:--|:--|
| $1$ | 1 | 0 |
| $78509$ | 5 | 4 |
| $1{,}000{,}000$ | 7 | 6 |

Conversely, from a tabulated $\log N = 7.5804631$, one reads off characteristic $7$, hence $N$ has 8 integer digits — without computing $N$ itself (source: chapter6.pdf, §112).

For $0 < N < 1$ the characteristic is negative.

## The mantissa is invariant under $\times 10^k$

Multiplying $N$ by $10^k$ adds $k$ to $\log N$ — i.e. it changes the *characteristic* by $k$ and leaves the *mantissa* unchanged. So *the mantissa encodes only the digit string of $N$*, independent of decimal placement (source: chapter6.pdf, §113):

| $\log N$ | $N$ |
|:--|:--|
| $4.9130187$ | $81850$ |
| $6.9130187$ | $8{,}185{,}000$ |
| $3.9130187$ | $8185$ |
| $0.9130187$ | $8.185$ |

Same mantissa $0.9130187 \Rightarrow$ same digit string $8185$, with the decimal point shifted according to the characteristic. From $\log N = 2.7603429$, the mantissa $0.7603429$ gives the digit string $5758945$, and the characteristic 2 says the integer part has 3 digits, giving $N = 575.8945$ (source: chapter6.pdf, §113).

## Negative characteristics by convention

A logarithm like $\log 0.5758945 = -1 + 0.7603429$ has *integer part* $-1$ and *fractional part* $0.7603429$. To preserve the digit-pattern reading of the mantissa, tables write this as

$$\log 0.5758945 = 9.7603429 - 10$$

— i.e. with characteristic $9$ "diminished by 10." Likewise $-2$ is written as $8 - 10$, $-3$ as $7 - 10$, etc. (source: chapter6.pdf, §113). This convention keeps the mantissa in $[0, 1)$ and the table lookup unchanged.

## Why this is useful

The split is what makes a printed log table small enough to be portable. The **mantissa table** lists, for every digit pattern from 1 to (typically) 100,000, the seven-place mantissa. The **characteristic** is computed by inspection of the number itself. Together:

- For multiplication: add logs, separately combining characteristics and mantissas; carry from the mantissa to the characteristic on overflow.
- For finding a number from its log: read the mantissa table backward to recover the digit string; the characteristic positions the decimal point.

## §113's closing example: $2^{16777216}$

To find the digit count of the 25th term of the progression $2, 4, 16, 256, \ldots$ (each term the square of its predecessor):

1. The terms are $2, 2^2, 2^4, 2^8, \ldots, 2^{2^{n-1}}$. The 25th term is $2^{2^{24}} = 2^{16777216}$.
2. $\log 2 = 0.301029995663981195$.
3. $\log_{10}(2^{16777216}) = 16777216 \cdot 0.301029995663981195 = 5050445.25973367$.
4. **Characteristic 5050445** ⇒ the number has *5,050,446 digits*.
5. **Mantissa $0.25973367$** ⇒ the leading digits are $181858\ldots$; pushing to more decimal places of $\log 2$, Euler reports the eleven leading digits as $18185852986$ (source: chapter6.pdf, §113).

The actual 5,050,446-digit number is uncomputable in any direct sense at the time — but its digit count and leading digits drop out of one multiplication and a table lookup. This is the kind of computation Chapter 6's machinery makes routine.

## Related pages

- [[common-logarithm]]
- [[logarithm]]
- [[change-of-base]]
- [[geometric-mean-method-for-logarithms]]
- [[chapter-6-on-exponentials-and-logarithms]]
