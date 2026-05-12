# Partition of Numbers

**Summary**: A **partition** of a positive integer $n$ is an unordered way of writing $n$ as a sum of positive integers. Chapter 16 of Euler's *Introductio* is the first systematic study, distinguishing distinct-part from unrestricted partitions, counting them by number of parts and by largest part, and proving the foundational identities (pentagonal number theorem, distinct = odd, Pascal-like recurrence, binary/balanced-ternary uniqueness).

**Sources**: chapter16

**Last updated**: 2026-05-11

---

## Definitions

A **partition** of $n$ is an unordered tuple of positive integers $(a_1, a_2, \ldots, a_m)$ with $a_1 + a_2 + \cdots + a_m = n$. The integers $a_i$ are the **parts**; $m$ is the **number of parts**. Euler distinguishes two cases (source: chapter16, §297, §302):

- **Distinct (unequal) parts**: all $a_i$ different.
- **Unrestricted parts** ("either equal or unequal"): repetition allowed.

He also allows the parts to be drawn from a prescribed sequence $\{\alpha, \beta, \gamma, \delta, \ldots\}$ of positive integers (§297). The default sequence is $1, 2, 3, 4, 5, \ldots$, but the framework is general.

## Counting notation

Following modern usage:

- $p(n)$ — number of partitions of $n$ (unrestricted, any number of parts). E.g. $p(6) = 11$ (§305 enumeration: $6, 5+1, 4+2, 4+1+1, 3+3, 3+2+1, 3+1+1+1, 2+2+2, 2+2+1+1, 2+1+1+1+1, 1+1+1+1+1+1$).
- $p_m(n)$ — number of partitions of $n$ into parts $\leq m$ (equivalently — by Euler's §315 bijection — into at most $m$ parts). E.g. $p_5(13) = 18$ (§304).
- $q(n)$ — number of partitions of $n$ into distinct parts. E.g. $q(8) = 6$: $8, 7+1, 6+2, 5+3, 5+2+1, 4+3+1$ (§301).
- $q_m(n)$ — number of partitions of $n$ into exactly $m$ distinct parts. E.g. $q_7(35) = 15$ (§300).

The two functions are linked by the **staircase bijection** $q_m(n) = p_m(n - m(m-1)/2)$ (§315). See [[partitions-into-distinct-parts]].

## Worked enumerations from Chapter 16

- §300: $35$ as a sum of $7$ distinct positive integers — $15$ ways.
- §301: $8$ as a sum of distinct positive integers — $6$ ways (above).
- §304: $13$ as a sum of $5$ positive integers (equal or unequal) — $18$ ways.
- §305: $6$ as a sum of positive integers (equal or unequal) — $11$ ways (above).
- §324: $7$ as a sum of positive integers — $15$ ways.
- §325: $9$ as a sum of distinct positive integers — $8$ ways: $9, 6+2+1, 8+1, 5+4, 7+2, 5+3+1, 6+3, 4+3+2$.

## Generating functions (§297, §302)

$$\sum_{n,m\geq 0} q_m(n) x^n z^m = \prod_{k\geq 1}(1 + x^k z),\qquad \sum_{n,m\geq 0} p_m(n) x^n z^m = \frac{1}{\prod_{k\geq 1}(1 - x^k z)}.$$

Setting $z = 1$:

$$\sum_n q(n) x^n = \prod_{k\geq 1}(1 + x^k),\qquad \sum_n p(n) x^n = \frac{1}{\prod_{k\geq 1}(1 - x^k)}.$$

The auxiliary variable $z$ tracks the **number of parts**; the variable $x$ tracks the **integer being partitioned**. See [[partition-generating-functions]].

## Key theorems (Chapter 16)

1. **Pentagonal number theorem** (§323–§324):

$$\prod_{k\geq 1}(1 - x^k) = \sum_{n\in\mathbb Z}(-1)^n x^{n(3n-1)/2}.$$

See [[eulers-pentagonal-number-theorem]].

2. **Distinct = odd** (§326):

$$\prod_{k\geq 1}(1 + x^k) = \prod_{k\geq 1}\frac{1}{1 - x^{2k - 1}}.$$

See [[distinct-parts-equals-odd-parts]].

3. **Staircase bijection** (§315): $q_m(n) = p_m(n - m(m-1)/2)$.

4. **Pascal-like recurrence** (§318): $p_m(n) = p_{m-1}(n) + p_m(n - m)$. See [[partition-recurrence]].

5. **Binary uniqueness** (§329): $\prod_{k\geq 0}(1 + x^{2^k}) = 1/(1 - x)$. See [[binary-representation-theorem]].

6. **Balanced-ternary uniqueness** (§331): every integer is uniquely a signed sum of distinct powers of $3$. See [[balanced-ternary-representation]].

## Why partitions matter

- **Additive number theory** begins here. Euler's identities are still the foundation of partition theory.
- **The partition function** $p(n)$ is the gateway to deeper objects: Ramanujan's congruences, the Hardy–Ramanujan circle method, modular forms.
- **Generating-function combinatorics** as a general method — products counting unordered choices, reciprocal products counting choices-with-repetition — is born in this chapter.

## Related pages

- [[chapter-16-on-the-partition-of-numbers]]
- [[partition-generating-functions]]
- [[partitions-into-distinct-parts]]
- [[partition-recurrence]]
- [[eulers-pentagonal-number-theorem]]
- [[distinct-parts-equals-odd-parts]]
- [[binary-representation-theorem]]
- [[balanced-ternary-representation]]
