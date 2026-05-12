# Function

**Summary**: In Euler's *Introductio*, a function of a variable is an analytic expression built in any way from that variable together with numbers or constants.

**Sources**: chapter1.pdf

**Last updated**: 2026-04-23

---

## Euler's definition

> A function of a variable quantity is an analytic expression composed in any way whatsoever of the variable quantity and numbers or constant quantities. (source: chapter1.pdf, §4)

Under this definition, every analytic expression whose only non-constant ingredient is the variable $z$ is a function of $z$. Euler's examples include:

- $a + 3z$
- $az - 4z^2$
- $az + b \sqrt{a^2 - z^2}$
- $e^z$

See [[variable-and-constant]] for the underlying notion of a variable.

## A function is itself a variable

Since any value may be substituted for the variable, the function takes on infinitely many values. No value is excluded, because the variable admits complex values as well as real (source: chapter1.pdf, §5). The function $\sqrt{9 - z^2}$ is bounded by $3$ on real inputs but attains any prescribed value on complex inputs; for example at $z = 5i$ it equals $\sqrt{34}$ in the real direction Euler uses in the text.

## Apparent functions

Some expressions look like functions of $z$ but are in fact constants. Euler lists three:

- $z^0 = 1$
- $1^z = 1$
- $\frac{a^2 - az}{a - z} = a$ (away from $z = a$)

(source: chapter1.pdf, §5)

## Operations that build functions

The fundamental operations are (source: chapter1.pdf, §6):

1. addition
2. subtraction
3. multiplication
4. division
5. raising to a power
6. extraction of roots
7. solution of equations

These seven are algebraic. Beyond them come transcendental operations such as exponentials, logarithms, and those supplied by the integral calculus.

### Solution of equations as an operation

Euler includes the "solution of equations" as a primary operation to account for quantities that are determined by a variable but cannot be expressed through the first six operations alone. For example, if $Z$ is defined by $Z^5 = az^2 Z^3 - bz^4 Z^2 + cz^3 Z - 1$, then $Z$ is a function of $z$ because its value is determined by the value of $z$, even if "common algebra" lacks the means to solve for $Z$ explicitly using radicals (source: chapter1.pdf, §8). This allows Euler to classify such quantities as algebraic functions rather than transcendental.

## Reciprocity

If $y$ is a function of $z$, then by rearranging the defining equation, $z$ is a function of $y$ (source: chapter1.pdf, §16). The number of values each takes in terms of the other can differ: if $y^3 = ayz - bz^2$, then $y$ is a three-valued function of $z$ while $z$ is a two-valued function of $y$.

If $y$ and $x$ are both functions of $z$, eliminating $z$ from the two defining equations expresses each as a function of the other (source: chapter1.pdf, §17).

## Historical note

This "analytic expression" definition was standard in the 18th century. It differs from the modern set-theoretic definition of a function as an arbitrary rule or mapping; Euler's notion requires that the rule be given by a formula. The later controversy over vibrating strings and arbitrary functions (d'Alembert, Euler, Daniel Bernoulli) eventually led Euler himself to broaden the concept in later writings.

## Related pages

- [[variable-and-constant]]
- [[classification-of-functions]]
- [[single-valued-and-multi-valued-functions]]
- [[even-and-odd-functions]]
- [[similar-functions]]
- [[chapter-1-on-functions-in-general]]
