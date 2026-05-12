# Infinitesimal and Infinite Numbers

**Summary**: Euler's working device throughout Chapter 7 (and most of Book I from this point on): introduce an *infinitely small* positive number $\omega$ and an *infinitely large* number $j$, linked by $j\omega = z$ for some finite $z$. Coefficients of the form $(j - m)/(nj)$ with $m, n$ finite are then treated as the algebraic identity $1/n$, since $j - m = j$ when $j$ is infinite. This collapses binomial expansions of $(1 + k\omega)^j = (1 + kz/j)^j$ into power series for $a^z$ and $\log(1+x)$.

**Sources**: chapter7 (§114–§125)

**Last updated**: 2026-04-26

---

## The setup

In §114 Euler writes:

> Let $\omega$ be an infinitely small number, or a fraction so small that, although not equal to zero, still $a^\omega = 1 + \psi$, where $\psi$ is also an infinitely small number.

and proceeds to set $\psi = k\omega$ — i.e. he treats two infinitely small quantities as commensurable, with a finite ratio $k$ depending on $a$.

The companion device is the *infinitely large* number. In §115 he raises $a^\omega = 1 + k\omega$ to a power $j$:

$$a^{j\omega} = (1 + k\omega)^j$$

and then sets $j = z/\omega$. Since $\omega$ is infinitely small and $z$ is finite, $j = z/\omega$ is *infinitely large*. The product $j\omega = z$ is a finite, ordinary real number.

So the recipe has three actors:

| Symbol | Status | Role |
|:--|:--|:--|
| $\omega$ | infinitely small ($> 0$) | step size |
| $j$ | infinitely large | repetition count |
| $z = j\omega$ | finite | the variable of interest |

The whole of Chapter 7 manipulates this triple.

## The key algebraic move

When $j$ is infinitely large and $m, n$ are finite,

$$\frac{j - m}{nj} = \frac{1}{n}.$$

Euler defends this in §116:

> Since $j$ is infinitely large, $(j-1)/j = 1$, and the larger the number we substitute for $j$, the closer the value of the fraction $(j-1)/j$ comes to 1. Therefore, if $j$ is a number larger than any assignable number, then $(j-1)/j$ is equal to 1. For the same reason $(j-2)/j = 1$, $(j-3)/j = 1$, and so forth.

This is treated as an *equality*, not a limit relation. Inside any binomial coefficient, every $(j - m)/j$ collapses to 1 and every $(j - m)/(nj)$ collapses to $1/n$.

## Why this collapses series

Apply the binomial theorem ([[binomial-series]]) to $(1 + kz/j)^j$:

$$(1 + kz/j)^j = 1 + \frac{j}{1}\cdot\frac{kz}{j} + \frac{j(j-1)}{1\cdot 2}\cdot\frac{k^2z^2}{j^2} + \frac{j(j-1)(j-2)}{1\cdot 2\cdot 3}\cdot\frac{k^3z^3}{j^3} + \cdots$$

Group the $j$'s. The $n$-th term is

$$\frac{j(j-1)(j-2)\cdots(j-n+1)}{n!}\cdot\frac{k^n z^n}{j^n} = \frac{k^n z^n}{n!}\cdot\frac{j}{j}\cdot\frac{j-1}{j}\cdot\frac{j-2}{j}\cdots\frac{j-n+1}{j}.$$

By the §116 collapse, every factor $(j - m)/j$ equals 1 for finite $m$. So the $n$-th term reduces to $k^n z^n/n!$, and

$$a^z = \sum_{n=0}^{\infty} \frac{(kz)^n}{n!}.$$

This is the [[exponential-series]]. The same collapse, applied to the binomial expansion of $(1+x)^{1/j}$, produces the [[logarithmic-series]] in §119.

## What status does this argument have?

Euler is comfortable treating $\omega$, $j$, and the collapse $(j - m)/j = 1$ as legitimate algebraic operations, not as approximations. He distinguishes:

- *Infinitely small* — smaller than any assignable positive quantity, but not zero. So $\omega \neq 0$ and division by $\omega$ is permitted.
- *Infinitely large* — larger than any assignable number; the reciprocal of an infinitely small. The product $j\omega$ can be finite, infinite, or infinitely small depending on the relationship between them.
- *Finite* — an ordinary real number, possibly the product $j\omega$ when $j$ and $\omega$ are inversely commensurable.

These are not the modern $\varepsilon$–$\delta$ concepts. They behave as a separate algebraic system, in which the rules "$j - m = j$" and "$j\omega = z$ is finite when $z$ is finite" are postulates one accepts as part of how the calculus operates. (A rigorous reconstruction is the modern *non-standard analysis* of Robinson, but Euler does not need it: his series have all the right coefficients, which is what counts.)

## A second use: defining $e$ as a limit (§125)

The same machinery represents the exponential as a "power":

$$e^z = \left(1 + \frac{z}{j}\right)^j, \qquad a^y = \left(1 + \frac{y \log a}{j}\right)^j$$

with $j$ infinitely large (source: chapter7, §125). In modern notation this is the limit definition $e^z = \lim_{n \to \infty}(1 + z/n)^n$, but for Euler it is an equality between an infinite-$j$ power and the corresponding series.

## Where else this appears

The technique is reused throughout Book I:

- Chapter 7 itself uses it for both $a^z$ (§115) and $\log(1+x)$ (§119), and for the closed-form $e^z = (1 + z/j)^j$ (§125).
- Chapter 8 will reuse it with imaginary increments to derive the trigonometric series and the formula $e^{ix} = \cos x + i \sin x$.
- Later chapters apply it to angle multiplication, partial fractions of $\sin$ and $\cos$, and the product expansions for $\sin x$ and $\cos x$.

## Caveats

- The argument that $\omega$ being infinitely small *forces* $\psi = a^\omega - 1$ to be infinitely small (§114) is not proved; Euler appeals to continuity from Chapter 6. In modern terms it is the continuity of $a^z$ at $z = 0$.
- The collapse $(j - m)/j = 1$ is uniform in the position $m$ within a fixed term, but Euler implicitly applies it *across all terms simultaneously* — equivalent to swapping a limit with an infinite sum. This is where modern analysis would demand a uniform-convergence justification. The series produced are nonetheless correct.
- Different choices of how $\omega$ and $j$ go to their limits — i.e. different orders or rates — would in general produce different answers in modern analysis. Euler tacitly chooses the rate $j\omega = z$ (constant), which is the choice that produces the analytic series.

## Related pages

- [[exponential-series]]
- [[logarithmic-series]]
- [[eulers-number]]
- [[binomial-series]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
