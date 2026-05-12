# Similar Functions

**Summary**: $Y$ and $Z$ are similar functions of $y$ and $z$ when both are built from their respective variables by the same formal expression. Euler introduces this as a bookkeeping notion used throughout the *Introductio*.

**Sources**: chapter1

**Last updated**: 2026-04-23

---

## Definition

> If $Z$ is a function of $z$ and $Y$ a function of $y$ such that $Y$ is defined through $y$ and constants, in the same way as $Z$ is defined through $z$ and constants, then the functions $Y$ and $Z$ are said to be similar functions of $y$ and $z$ respectively. (source: chapter1, §26)

Operationally: replacing $z$ by $y$ in the expression for $Z$ yields the expression for $Y$.

## Example

If $Z = a + b z + c z^2$ and $Y = a + b y + c y^2$, then $Z$ and $Y$ are similar functions (source: chapter1, §26).

A common idiom is "$Y$ is such a function of $y$ as $Z$ is of $z$."

## Use under substitution

Similarity is used even when the two variables are related. For instance, with $z = y + n$:

- "Such a function of $y$ as $a y + b y^3$" is similar to the function $a(y+n) + b(y+n)^3$ of $y + n$.

And with $y = 1/z$:

- $\frac{a + b z + c z^2}{\alpha + \beta z + \gamma z^2}$ as a function of $z$ is similar to $\frac{a z^2 + b z + c}{\alpha z^2 + \beta z + \gamma}$ as a function of $1/z$ — after clearing, this is the same expression written in $1/z$.

## Why this matters

The similar-function concept is the 18th-century precursor of a formula template or an abstract function symbol. It lets Euler talk about "the same function applied to different arguments" without the modern notation $f(\dots)$. He says it "is fruitfully used throughout all of higher analysis" (source: chapter1, §26).

## Related pages

- [[function]]
- [[chapter-1-on-functions-in-general]]
