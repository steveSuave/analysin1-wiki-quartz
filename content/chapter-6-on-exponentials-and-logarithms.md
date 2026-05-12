# Chapter 6: On Exponentials and Logarithms

**Summary**: Euler's first transcendental chapter. He develops the [[exponential-function]] $y = a^z$ informally — extending from integer to fractional to irrational exponents — and then introduces its inverse, the [[logarithm]]. Most logarithms are transcendental (§105); they are computed in practice by iterated geometric means (§106), tabulated for primes (§109), and converted between bases by a single multiplicative constant (§107–§108). The chapter closes with the working machinery of common (base-10) logarithms: [[characteristic-and-mantissa]].

**Sources**: chapter6

**Last updated**: 2026-04-26

---

## Overview

Up to Chapter 5 every function was *algebraic* — built from the four arithmetic operations and root extraction (see [[classification-of-functions]]). Chapter 6 takes the first step into transcendental territory. Euler concedes that a fully rigorous theory needs integral calculus, but two species of transcendental function — exponentials and their inverse logarithms — can already be developed by elementary means, and they "open the door to further investigations" (source: chapter6, §96).

The chapter has three movements:

1. **§96–§101 — the exponential.** Define $y = a^z$ for variable exponent. Walk through integer, fractional, irrational $z$ to make plausible that the function is single-valued and continuous. Case-split on $a$ to settle on $a > 1$ as the canonical setting.
2. **§102–§109 — the logarithm.** Invert: $\log y$ is the exponent that produces $y$. Derive the algebraic rules. Show (§105) that logarithms of "generic" numbers are *transcendental*. Sketch the computational machinery: compute by iterated geometric means (§106), change base by a single multiplier (§107–§108), and reduce all tabulation to the primes (§109).
3. **§110–§113 — applications and decimal logarithms.** Use logarithms to compute complicated expressions and solve $a^x = b$; work out four word problems on population growth and compound interest. Then define [[common-logarithm|common logarithms]] (base 10) and their split into [[characteristic-and-mantissa|characteristic and mantissa]].

See also: [[exponential-function]], [[logarithm]], [[transcendence-of-logarithms]], [[geometric-mean-method-for-logarithms]], [[change-of-base]], [[common-logarithm]], [[characteristic-and-mantissa]].

## Structure of the chapter

### §96 — Why exponentials are not algebraic

A *power with variable exponent* — $a^z$, $y^z$, $a^{a^z}$, $a^{y^z}$, $y^{x^z}$, $x^{y^z}$ — is not an algebraic function, since algebraic functions require the exponents to be constants (source: chapter6, §96). Euler absorbs all the variant forms into a single representative $a^z$: the analysis of one settles the others.

### §97 — Defining $a^z$ on $\mathbb{Q}$

For positive integer $z$, $a^z$ has the obvious meaning. For $z = 0$, set $a^0 = 1$. For negative integer $z$, $a^{-n} = 1/a^n$. For rational $z = p/q$, $a^{p/q} = \sqrt[q]{a^p}$, which is in general multivalued, but Euler restricts to the *primary positive real value* so that $a^z$ is single-valued (source: chapter6, §97). This places, e.g., $a^{5/2}$ between $a^2$ and $a^3$. Irrational $z$ is handled by interpolation: $a^{\sqrt{7}}$ lies between $a^2$ and $a^3$. See [[exponential-function]].

### §98–§99 — Case analysis on the base

The behavior of $a^z$ depends on $a$ (source: chapter6, §98):

- $a = 1$: constant 1.
- $a > 1$: $a^z$ strictly increases; $a^z \to \infty$ as $z \to \infty$ and $a^z \to 0$ as $z \to -\infty$.
- $0 < a < 1$: write $1/a = b > 1$ to get $a^z = b^{-z}$ — the $a > 1$ case, reflected.
- $a = 0$: discontinuity at $z = 0$. For $z > 0$, $a^z = 0$; for $z = 0$, $a^0 = 1$; for $z < 0$, $a^{-n} = 1/0^n$ "is infinite" (source: chapter6, §99).
- $a < 0$: integer exponents alternate sign; rational exponents may produce real or pure-imaginary values ($(-2)^{1/2} = \sqrt{-2}$ vs. $(-2)^{1/3} = -\sqrt[3]{2}$); irrational exponents are unpredictable.

§100 distills the conclusion: take $a > 1$; the case $0 < a < 1$ then follows by reflection, and the others are pathological.

### §101 — Algebraic rules and the example $a = 10$

With $y = a^z$: $y^n = a^{nz}$, $y^{1/n} = a^{z/n}$, $1/y = a^{-z}$; if $v = a^x$ then $vy = a^{x+z}$ and $v/y = a^{x-z}$ (source: chapter6, §101). Worked example for $a = 10$: $10^1 = 10$, $10^2 = 100$, $10^{-1} = 0.1$, $10^{1/2} = \sqrt{10} \approx 3.162277$, etc.

### §102 — Logarithm as inverse exponent

For each $y > 0$ there is a unique real $z$ with $a^z = y$; this $z$ is called the *logarithm* of $y$ to the base $a$, written $z = \log y$. The base $a$ must be specified for the symbol to be unambiguous, and Euler assumes $a > 1$ throughout (source: chapter6, §102). See [[logarithm]].

### §103 — First values of $\log$

$\log 1 = 0$ regardless of base; $\log a = 1$, $\log a^2 = 2$, $\log a^3 = 3$, etc.; $\log(1/a^n) = -n$ (source: chapter6, §103). Numbers $> 1$ have positive logs; numbers in $(0, 1)$ have negative logs; the "logarithm" of a negative number is complex.

### §104 — The algebraic rules of logarithms

From $\log y^n = n \log y$, one gets $\log \sqrt{y} = \tfrac{1}{2} \log y$, $\log(1/\sqrt{y}) = -\tfrac{1}{2} \log y$, etc. From $vy = a^{x+z}$ one gets $\log(vy) = \log v + \log y$ and $\log(v/y) = \log v - \log y$ (source: chapter6, §104). These four rules — log of a power, log of a root, log of a product, log of a quotient — are the entire algebra of logarithms.

### §105 — Logarithms are transcendental

Suppose $\log b$ is rational, say $\log b = m/n$. Then $a^{m/n} = b$, i.e. $a^m = b^n$; if both $a$ and $b$ are rational this forces $b$ to be a rational power of $a$. Suppose instead $\log b$ is irrational, say $\log b = \sqrt{n}$. Then $a^{\sqrt{n}} = b$ — impossible if $a, b$ are rational (source: chapter6, §105). Conclusion: unless $b$ is exactly a power of $a$, $\log b$ is *neither rational nor irrational algebraic* — Euler labels such quantities *transcendental*, and so logarithms in general are transcendental. See [[transcendence-of-logarithms]].

### §106 — Computing logarithms by geometric means

A transcendental logarithm can be approximated to arbitrary decimal precision by an algorithm using only square roots. The principle: if $\log y = z$ and $\log v = x$, then $\log\sqrt{vy} = (x+z)/2$ — the log of the geometric mean is the arithmetic mean of the logs (source: chapter6, §106).

To find $\log_{10} 5$: 5 lies between $A = 1$ ($\log A = 0$) and $B = 10$ ($\log B = 1$). Set $C = \sqrt{AB} = 3.162277$, $\log C = 0.5$. Now 5 lies between $C$ and $B$; take $D = \sqrt{BC}$, etc. The bounds halve at each step. After ~26 iterations the geometric mean stabilizes to $5.000000$ with $\log = 0.6989700$.

This is how Briggs and Vlacq computed the original tables of common logarithms (source: chapter6, §106 example). See [[geometric-mean-method-for-logarithms]].

### §107–§108 — Change of base

Different bases give different logarithm systems, but they are all proportional. If $\log_a n = p$ and $\log_b n = q$, then $a^p = n = b^q$, so $a = b^{q/p}$, and *the ratio $p/q$ is the same for every $n$* (source: chapter6, §107). Thus a single multiplier converts one full table into another: e.g. base-10 to base-2 by multiplying every common log by $1/\log_{10} 2 = 1/0.3010300 = 3.3219277$.

§108 strengthens this with a base-free formulation: for any two numbers $M, N$ in the same system, the *ratio of their logarithms* is base-independent. From $M = N^{m/n}$ in base $a$ and $M = N^{\mu/\nu}$ in base $b$, both ratios equal — they record the algebraic relationship between $M$ and $N$, not the choice of base. See [[change-of-base]].

### §109 — Tables built from primes

The product rule reduces tabulation to *prime* logs: $\log 15 = \log 3 + \log 5$, $\log 4 = 2 \log 2$, etc. Once $\log 2 = 0.3010300$ and $\log 5 = 0.6989700$ are computed, every number whose only prime factors are 2 and 5 (i.e. every terminating decimal multiplied by a power of 10) follows by addition (source: chapter6, §109). Note also that $\log 2 = \log 10 - \log 5 = 1 - 0.6989700$, so a single root extraction (for $\log 5$) suffices for both.

### §110–§111 — Applications

§110 uses logs to evaluate complicated algebraic expressions: e.g. $\log\left(\frac{c^2 d \sqrt{e}}{f (gh)^{1/3}}\right) = 2\log c + \log d + \tfrac{1}{2}\log e - \log f - \tfrac{1}{3}\log g - \tfrac{1}{3}\log h$. Numerical roots are found this way without explicit root extraction.

§111 turns to the most important application: solving equations with the unknown in the exponent. From $a^x = b$, $x = \log b / \log a$ — the choice of base is irrelevant since the ratio is invariant (§107–§108). Worked examples:

- *Population growth.* If a population grows by $1/30$ per year, after 100 years it is multiplied by $(31/30)^{100}$. Working in common logs, $100 \log(31/30) = 1.4240439$, so the population grows by a factor of $\approx 26.5$ (Example II, §110).
- *Bible-flood example.* Starting from 6 people after the Flood and reaching 1,000,000 after 200 years requires an annual growth rate of about $1/16$; "the same rate over 400 years gives 166 billion — but the earth could not sustain it" (Example III, §110).
- *Doubling per century.* Annual rate is then $1/144$ (Example IV, §110).
- *Time to a tenfold population.* At rate $1/100$ per year, $x = \log 10 / (\log 101 - \log 100) \approx 231$ years (Example I, §111).
- *Compound debt.* A loan of 400,000 florins at 5% per annum, repaid 25,000 per year, is settled in just under 33 years — the creditor in fact owes the debtor 318.8 florins after 33 years (Example II, §111).

### §112–§113 — Common logarithms: characteristic and mantissa

Base 10 is special because our arithmetic is decimal. A common logarithm splits into:

- *Characteristic*: the integer part. Equal to (number of digits in the integer part) $- 1$. So $\log 78509$ has characteristic 4; reading the characteristic of any $\log$, one knows the number's digit count (source: chapter6, §112).
- *Mantissa*: the decimal fractional part. Encodes the digit string of the number, independent of decimal placement (source: chapter6, §113).

Two numbers whose logs share a mantissa differ only by a power of 10 — same digits, decimal point shifted. Negative characteristics are conventionally shifted upward by 10 (writing 9, 8, 7, ... for $-1, -2, -3$ and noting "diminished by 10"). See [[characteristic-and-mantissa]] and [[common-logarithm]].

The closing example: in the progression $2, 4, 16, 256, \ldots$ where each term is the square of the previous, the 25th term is $2^{2^{24}} = 2^{16777216}$, whose common logarithm is $16777216 \cdot \log 2 = 5050445.25973367$. The characteristic 5050445 says the number has *5,050,446 digits*, and the mantissa locates its leading digits — Euler reports the eleven leading digits as $18185852986$.

## Notable points

- **First definition of "transcendental" applied to a number, not a function.** §105 names logarithms transcendental — extending the algebraic/transcendental distinction from [[classification-of-functions]] from *expressions* to *quantities*. The argument is a clean dichotomy: either rational (force on $b$) or impossible.
- **The geometric-mean algorithm (§106) is striking.** It computes a transcendental quantity from purely algebraic operations (square roots and bisection of brackets). This anticipates the quadrature-style computations of subsequent chapters and is conceptually parallel to how $e$ and $\pi$ will be approached later.
- **Change of base (§107–§108) reduces "infinitely many systems of logarithms" to one.** Logarithms are intrinsically a single one-parameter family — the only base-dependent thing is a multiplicative constant. The base-free §108 formulation ($\log M : \log N$ is base-invariant) is the proportionality principle that ties all the systems together.
- **The Bible-flood example (§110, Example III) is unusual.** Most of Euler's worked examples are abstract; this one is socio-theological. He uses it to defend the plausibility of biblical population numbers — a 1/16 annual growth rate is enough to take the post-Flood population from 6 to 1,000,000 in 200 years.
- **§113's last example is a flex.** Computing the digit count of $2^{16777216}$ shows logarithms doing work no other tool can do at the time — the number itself is uncomputable in any direct sense.
- **No mention of $e$ yet.** Euler is careful: the special role of base $e$ requires the limit $\lim_n (1 + 1/n)^n$, which belongs to Chapter 7. Here every base is on equal footing.

## Why this chapter matters

Chapter 6 introduces the first transcendental functions and the first numerical constants outside the algebraic realm. The algebraic theory of Chapters 1–5 was self-contained but bounded: rational functions, polynomial roots, partial fractions, homogeneous reductions. Now Euler crosses into a class of functions whose values cannot in general be expressed by finite algebraic formulas — and supplies, through §106 and §107–§109, exactly the computational scaffolding (geometric means, change of base, prime tables, characteristic/mantissa) that makes such functions usable in practice.

The chapter is also a setup. Chapter 7 will return to $a^z$, expand it as a power series via the limit $\lim_n (1 + z/n)^n$, identify the privileged base $e$ for which the series is simplest, and so launch the analytic theory of exponentials and logarithms that the rest of Book I depends on.

## Related pages

- [[exponential-function]]
- [[logarithm]]
- [[transcendence-of-logarithms]]
- [[geometric-mean-method-for-logarithms]]
- [[change-of-base]]
- [[common-logarithm]]
- [[characteristic-and-mantissa]]
- [[classification-of-functions]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
