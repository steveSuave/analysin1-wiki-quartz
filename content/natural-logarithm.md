# Natural Logarithm

**Summary**: §123–§125 of Chapter 7. The *natural* (or *hyperbolic*) logarithm is $\log$ in the base $a = e$ of [[eulers-number]] — the unique base for which $\log(1 + \omega) = \omega$ for infinitely small $\omega$ (equivalently, the constant $k = 1$ in [[exponential-series|§116]]). Euler tabulates $\log_e n$ for $n = 1, \ldots, 10$ to twenty decimal places using the [[logarithmic-series|fast-converging series]] $\log\frac{1+x}{1-x} = 2(x + x^3/3 + x^5/5 + \cdots)$, then shows that for any other base $a$, $k = \log_e a$ is the conversion factor — so a single table of natural logs supplies every other system by one multiplication, recovering [[change-of-base|§107–§108]] from a different angle.

**Sources**: chapter7 (§123–§125)

**Last updated**: 2026-04-26

---

## Defining property (§123)

> Natural logarithms have the property that the logarithm of $1 + \omega$ is equal to $\omega$, where $\omega$ is an infinitely small quantity.

(source: chapter7, §123). This is exactly the condition $k = 1$ from [[exponential-series|§114]] — and it picks out the base $a = e$ uniquely. Equivalently:

- $a^\omega = 1 + \omega$ for infinitely small $\omega$ — the exponential is "tangent to $1 + z$ at $z = 0$" in modern language;
- the [[exponential-series|exponential series]] is $e^z = 1 + z + z^2/2 + z^3/6 + \cdots$ with no extra factor;
- the [[logarithmic-series|log series]] is $\log(1+x) = x - x^2/2 + x^3/3 - \cdots$ with no extra factor.

## The three master series in base $e$

With $k = 1$ the series of [[exponential-series|§116]] and [[logarithmic-series|§119, §121]] take their cleanest forms (source: chapter7, §123):

$$e^z = 1 + \frac{z}{1} + \frac{z^2}{1\cdot 2} + \frac{z^3}{1\cdot 2\cdot 3} + \frac{z^4}{1\cdot 2\cdot 3\cdot 4} + \cdots$$

$$\log(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \frac{x^5}{5} - \frac{x^6}{6} + \cdots$$

$$\log\frac{1+x}{1-x} = \frac{2x}{1} + \frac{2x^3}{3} + \frac{2x^5}{5} + \frac{2x^7}{7} + \frac{2x^9}{9} + \cdots$$

The third series is "strongly convergent if we substitute an extremely small fraction for $x$" (source: chapter7, §123) and is the workhorse for the table below.

## The integer table (§123)

Using $x = 1/5, 1/7, 1/9$ in $\log\frac{1+x}{1-x}$:

$$\log\frac{6}{4} = \log\frac{3}{2} = \frac{2}{1\cdot 5} + \frac{2}{3\cdot 5^3} + \frac{2}{5\cdot 5^5} + \frac{2}{7\cdot 5^7} + \cdots$$

$$\log\frac{4}{3} = \frac{2}{1\cdot 7} + \frac{2}{3\cdot 7^3} + \frac{2}{5\cdot 7^5} + \frac{2}{7\cdot 7^7} + \cdots$$

$$\log\frac{5}{4} = \frac{2}{1\cdot 9} + \frac{2}{3\cdot 9^3} + \frac{2}{5\cdot 9^5} + \frac{2}{7\cdot 9^7} + \cdots$$

Combining via the [[logarithm|algebraic rules]]:

$$\log\tfrac{3}{2} + \log\tfrac{4}{3} = \log 2, \qquad \log\tfrac{3}{2} + \log 2 = \log 3, \qquad 2\log 2 = \log 4, \qquad \log\tfrac{5}{4} + \log 4 = \log 5,$$

$$\log 2 + \log 3 = \log 6, \qquad 3\log 2 = \log 8, \qquad 2\log 3 = \log 9, \qquad \log 2 + \log 5 = \log 10.$$

For $\log 7$, $x = 1/99$ gives $\log(100/98) = \log(50/49) = 0.02020\,27073\,17519\,44840\,78230$. Subtracting from $\log 50 = 2\log 5 + \log 2 = 3.91202\,30054\,28146\,05861\,87508$ gives $\log 49$, and $\log 7 = \tfrac{1}{2}\log 49$.

The resulting table (source: chapter7, §123 example), to twenty digits:

| $n$ | $\log n = \ln n$ |
|:--|:--|
| 1 | $0.00000\,00000\,00000\,00000\,00000$ |
| 2 | $0.69314\,71805\,59945\,30941\,72321$ |
| 3 | $1.09861\,22886\,68109\,69139\,52452$ |
| 4 | $1.38629\,43611\,19890\,61883\,44642$ |
| 5 | $1.60943\,79124\,34100\,37460\,07593$ |
| 6 | $1.79175\,94692\,28055\,00081\,24773$ |
| 7 | $1.94591\,01490\,55313\,30510\,54639$ |
| 8 | $2.07944\,15416\,79835\,92825\,16964$ |
| 9 | $2.19722\,45773\,36219\,38279\,04905$ |
| 10 | $2.30258\,50929\,94045\,68401\,79914$ |

These are the *natural logarithms* — the modern $\ln 1, \ln 2, \ldots, \ln 10$.

## $k = \log_e a$ as the change-of-base factor (§124)

Suppose the natural log of $1 + x$ is $y$. By [[logarithmic-series|§123]],

$$y = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots$$

If $v$ is the logarithm of the *same* $1 + x$ in base $a$, then by [[logarithmic-series|§119]],

$$v = \frac{1}{k}\left(x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots\right) = \frac{y}{k}.$$

So $k = y/v$. Setting $1 + x = a$ makes $v = \log_a a = 1$ and $y = \log_e a$:

$$\boxed{\;k = \log_e a.\;}$$

This is "the most convenient method of calculating the value of $k$ corresponding to the base $a$" (source: chapter7, §124). For $a = 10$:

$$k = \log_e 10 = 2.30258\,50929\,94045\,68401\,79914,$$

the same value computed in [[exponential-series|§114]] from the table and in [[logarithmic-series|§121]] from the fast-converging series.

The reciprocal,

$$\frac{1}{k} = \log_{10} e = 0.43429\,44819\,03251\,82765\,11289,$$

multiplies a natural log to produce a common log, and is the famous *"modulus" of common logarithms*.

## $a^y = e^{y \log a}$ (§125)

Substituting $a^y = e^z$ with $z = y \log a$ (since $\log e = 1$ implies $\log a^y = y \log a$ in natural logs) into $e^z = \sum z^n/n!$:

$$a^y = 1 + \frac{y \log a}{1} + \frac{y^2 (\log a)^2}{1 \cdot 2} + \frac{y^3 (\log a)^3}{1\cdot 2 \cdot 3} + \cdots$$

— the [[exponential-series|§117]] formula in disguise, with $k = 1$ absorbed and $\log = \log_e$ everywhere (source: chapter7, §125).

The two infinite-power forms recap:

$$e^z = \left(1 + \frac{z}{j}\right)^j, \qquad a^y = \left(1 + \frac{y \log a}{j}\right)^j, \qquad \log(1+x) = j\bigl((1+x)^{1/j} - 1\bigr),$$

with $j$ infinitely large — see [[infinitesimal-and-infinite-numbers]].

## Why "natural" is the right word

Two clean facts pick out base $e$:

- **Tangency at the identity:** $\log(1+\omega) = \omega$ for infinitely small $\omega$ — the natural log is the only one whose graph has slope 1 at $1$. (Modern: $(d/dx) \log_a x|_{x=1} = 1$ iff $a = e$.)
- **Inverse with itself:** $e^z$ and $\log_e$ are the unique base-pair for which both the exponential and logarithm series have unit leading coefficient.

Every other base introduces the multiplicative constant $k$, $1/k$, or $\log a$ somewhere. Natural logs are "natural" in the sense of being unweighted.

## Related pages

- [[eulers-number]]
- [[exponential-series]]
- [[logarithmic-series]]
- [[infinitesimal-and-infinite-numbers]]
- [[exponential-function]]
- [[logarithm]]
- [[change-of-base]]
- [[common-logarithm]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
