# Real Partial Fraction Decomposition

**Summary**: Euler's method (§199–§210) for resolving a real proper rational function into a sum of real partial fractions whose denominators are real linear factors or real quadratic [[trinomial-factor|trinomial factors]] $p^2 - 2pqz\cos\phi + q^2z^2$. Extends [[partial-fraction-decomposition|the §39–§46 algorithm]] to handle the complex-root case without introducing complex numerators.

**Sources**: chapter12

**Last updated**: 2026-05-04

---

## Setup

Let $M/N$ be a *proper* real rational function (see [[improper-rational-function]] if it is improper). By [[factoring-polynomials|the §28–§32 theorem]] (the [[fundamental-theorem-of-algebra]]), $N$ factors over $\mathbb{R}$ into real linear factors and real quadratic factors. Each *real linear* factor is handled by the [[partial-fraction-decomposition|Chapter 2 algorithm]]. Each *real quadratic* factor — the case Chapter 12 addresses — is normalized to the [[trinomial-factor|canonical form]]

$$p^2 - 2pqz\cos\phi + q^2z^2$$

with complex roots $z = (p/q)(\cos\phi \pm i\sin\phi)$ (source: chapter12, §200).

## Distinct quadratic factors (§200–§205)

For one such factor of $N$, the corresponding partial fraction has the form

$$\frac{P + Qz}{p^2 - 2pqz\cos\phi + q^2z^2}$$

with two unknown real coefficients $P$ and $Q$. The numerator is exactly first degree: a higher degree would leave behind a polynomial part (which should already have been removed) (source: chapter12, §200).

### Derivation (§201)

Write $N = (p^2 - 2pqz\cos\phi + q^2z^2)\,Z$. Subtracting $(P + Qz)/(\text{trinomial})$ from $M/N$ leaves a fraction whose numerator $M - PZ - QZz$ must be divisible by the trinomial — i.e. it must vanish at the trinomial's two roots. Setting $f = p/q$, [[de-moivre-formula|De Moivre]] gives at the roots

$$z^n = f^n(\cos n\phi \pm i\sin n\phi).$$

(source: chapter12, §201).

### Two real equations (§202)

Substituting both roots into $M = PZ + QZz$ and expanding the cosines/sines gives, in the abbreviations

$$
\begin{aligned}
R &= A + Bf\cos\phi + Cf^2\cos 2\phi + Df^3\cos 3\phi + \cdots,\\
r &= Bf\sin\phi + Cf^2\sin 2\phi + Df^3\sin 3\phi + \cdots,\\
S &= \alpha + \beta f\cos\phi + \gamma f^2\cos 2\phi + \delta f^3\cos 3\phi + \cdots,\\
s &= \beta f\sin\phi + \gamma f^2\sin 2\phi + \delta f^3\sin 3\phi + \cdots,\\
T &= \alpha f\cos\phi + \beta f^2\cos 2\phi + \gamma f^3\cos 3\phi + \cdots,\\
t &= \alpha f\sin\phi + \beta f^2\sin 2\phi + \gamma f^3\sin 3\phi + \cdots,
\end{aligned}
$$

the single complex equation $R \pm ri = (PS \pm Psi) + (QT \pm Qti)$. Separating real and imaginary parts:

$$R = PS + QT,\qquad r = Ps + Qt.$$

(source: chapter12, §202–§203). Notice the pattern: $R, r$ come from substituting $z^n \to f^n\cos n\phi$ (resp. $f^n\sin n\phi$) in $M$; $S, s$ come from the same substitution in $Z$; $T, t$ from the same substitution in $Zz$ (which shifts every exponent by one).

### Closed-form solution (§203)

The two-equation system gives

$$\boxed{\;P = \frac{Rt - rT}{St - sT},\qquad Q = \frac{Rs - rS}{sT - St}.\;}$$

Once $P$ and $Q$ are computed, the partial fraction $(P + Qz)/(p^2 - 2pqz\cos\phi + q^2z^2)$ is determined. Subtracting it from $M/N$ leaves a "complementary fraction" whose denominator is $Z$, which can be decomposed by the same rule applied to its own quadratic factors (and by the [[partial-fraction-decomposition|Chapter 2 algorithm]] for any linear factors).

### Streamlined formula (§204–§205)

A direct calculation from the definitions gives

$$T = f(S\cos\phi - s\sin\phi),\qquad t = f(S\sin\phi + s\cos\phi),$$

so $T$ and $t$ are *not* independent computations — they are determined by $S, s$. Substituting into the §203 system yields

$$St - sT = (S^2 + s^2)\,f\sin\phi,$$

$$Rt - rT = (RS + rs)\,f\sin\phi + (Rs - rS)\,f\cos\phi.$$

Plugging back gives the compact form

$$\frac{P + Qz}{p^2 - 2pqz\cos\phi + q^2z^2} = \frac{(RS + rs)\,p\sin\phi + (Rs - rS)(p\cos\phi - qz)}{(p^2 - 2pqz\cos\phi + q^2z^2)\,(S^2 + s^2)\,p\sin\phi}.$$

Only the four scalars $R, r, S, s$ are needed — half the trigonometric multiples of §203 (source: chapter12, §204–§205).

### Worked Example I (§203)

Decompose $\dfrac{z^2}{(1 - z + z^2)(1 + z^4)}$ using the factor $1 - z + z^2$.

Compare $1 - z + z^2$ to $p^2 - 2pqz\cos\phi + q^2z^2$: $p = 1$, $q = 1$, $\cos\phi = 1/2$, hence $\phi = \pi/3$. Here $M = z^2$ and $Z = 1 + z^4$, $f = 1$.

- **From $M = z^2$:** only the $z^2$-coefficient $C = 1$ contributes. $R = \cos(2\pi/3) = -1/2$, $r = \sin(2\pi/3) = \sqrt 3/2$.
- **From $Z = 1 + z^4$:** the $z^0$-coefficient $\alpha = 1$ and the $z^4$-coefficient $\epsilon = 1$ contribute. $S = 1 + \cos(4\pi/3) = 1/2$, $s = \sin(4\pi/3) = -\sqrt 3/2$.
- **From $Zz$:** $T = \cos(\pi/3) + \cos(5\pi/3) = 1/2 + 1/2 = 1$, $t = \sin(\pi/3) + \sin(5\pi/3) = \sqrt 3/2 - \sqrt 3/2 = 0$.

Then $P = (Rt - rT)/(St - sT) = (0 - \sqrt 3/2)/(0 - (-\sqrt 3/2)) = -1$ and $Q = 0$. The partial fraction is

$$\frac{-1}{1 - z + z^2}.$$

Subtracting from the original gives the complementary fraction $(1 + z + z^2)/(1 + z^4)$ (using $1 + z^2 + z^4 = (1 + z + z^2)(1 - z + z^2)$). The complement still has denominator $1 + z^4 = (1 + \sqrt 2\,z + z^2)(1 - \sqrt 2\,z + z^2)$, two more trinomial factors with $\phi = \pi/4$, decomposed identically in Example II (source: chapter12, §203).

### Worked Example III (§203, abridged)

Decompose $\dfrac{1 + 2z + z^2}{(1 - \tfrac{8}{5}z + z^2)(1 + 2z + 3z^2)}$. The factor $1 - \tfrac{8}{5}z + z^2$ has $p = 1$, $q = 1$, $\cos\phi = 4/5$. This is *not* a fractional part of a right angle, so $\sin\phi$, $\cos 2\phi, \sin 2\phi, \cos 3\phi, \sin 3\phi$ must be computed by [[trigonometric-addition-formulas|the addition formulas]]: $\sin\phi = 3/5$, $\cos 2\phi = 7/25$, $\sin 2\phi = 24/25$, $\cos 3\phi = -44/125$, $\sin 3\phi = 117/125$. With $M = 1 + 2z + z^2$ and $Z = 1 + 2z + 3z^2$ (and $f = 1$), the formulas give $R = 72/25$, $r = 54/25$, $S = 86/25$, $s = 102/25$, $T = 38/125$, $t = 666/125$, and finally $P = 153/178$, $Q = -45/178$. The partial fraction is

$$\frac{9(17 - 5z)/178}{1 - \tfrac{8}{5}z + z^2}.$$

A symmetric computation for the other factor $1 + 2z + 3z^2$ (now $f = -1/\sqrt 3$, $\cos\phi = 1/\sqrt 3$) yields $\dfrac{5(5 + 27z)/178}{1 + 2z + 3z^2}$ (source: chapter12, §203).

## Repeated quadratic factors (§206–§210)

If $(p^2 - 2pqz\cos\phi + q^2z^2)^k$ divides $N$, the algorithm above degenerates: after substituting the trinomial's roots, both $M - PZ - QZz$ *and* $Z$ vanish, and the §203 system becomes $0 = 0$ (source: chapter12, §206). A separate iterative procedure is needed.

### Tower of partial fractions (§206)

Write $N = (p^2 - 2pqz\cos\phi + q^2z^2)^k Z$ where $Z$ contains *no* further power of this trinomial. The contribution to the partial-fraction decomposition is the tower

$$\frac{U + uz}{(p^2 - 2pqz\cos\phi + q^2z^2)^k} + \frac{V + vz}{(p^2 - 2pqz\cos\phi + q^2z^2)^{k-1}} + \cdots + \frac{X + xz}{p^2 - 2pqz\cos\phi + q^2z^2}.$$

(source: chapter12, §209). Each numerator pair has two unknowns; together there are $2k$ unknowns to determine.

### One step at a time (§207–§209)

Each numerator pair is found by a single application of a fixed formula. For the *top* numerator $(U + uz)$:

- Substitute $z^n \to (p/q)^n\cos n\phi$ in $M$ to obtain the scalar $Y$, and in $Z$ to obtain $N$.
- Substitute $z^n \to (p/q)^n\sin n\phi$ in $M$ to obtain $y$, and in $Z$ to obtain $n$.
- Then

$$U = \frac{YN + yn}{N^2 + n^2} + \frac{Yn - yN}{N^2 + n^2}\cdot\frac{\cos\phi}{\sin\phi},\qquad u = -\frac{Yn - yN}{N^2 + n^2}\cdot\frac{q}{p\sin\phi}.$$

(source: chapter12, §207). After $U, u$ are known, define the next polynomial

$$F = \frac{M - (U + uz)\,Z}{p^2 - 2pqz\cos\phi + q^2z^2}.$$

The numerator is divisible by the trinomial (this is what the formulas for $U, u$ guarantee), so $F$ is a polynomial. Apply the *same* formula to $F$ in place of $M$: new substituted values $P, p$ (real and imaginary substitutions of $F$) replace $Y, y$; the values $N, n$ are unchanged because $Z$ has not changed. This produces $V, v$. Then $G = (F - (V + vz)Z)/(\text{trinomial})$, then $W, w$, then $H, X, x$, and so on for $k$ rounds (source: chapter12, §208–§209).

### Complementary fraction (§210)

The sequence of polynomials $F, G, H, I, K, \ldots$ produced in the iteration is exactly what is needed for the *complementary* fraction with denominator $Z$. After all $k$ numerators in the tower have been extracted, the *next* polynomial in the sequence (call it the last one) is the numerator of the complement: for $k = 1$, $F/Z$; for $k = 2$, $G/Z$; for $k = 3$, $H/Z$; and so on. The complement, having denominator $Z$ which contains no further power of *this* trinomial, can itself be expressed in partial fractions by the §200–§205 rule applied to its own quadratic factors (source: chapter12, §210).

### Worked example (§209)

Decompose $\dfrac{z - z^3}{(1 + z^2)^4(1 + z^4)}$. The repeated factor $(1 + z^2)^4$ has $p = 1$, $q = 1$, $\cos\phi = 0$, $\phi = \pi/2$, $\sin\phi = 1$, $f = 1$. Take $M = z - z^3$, $Z = 1 + z^4$.

- **At $z = i$**: $M$ evaluates to $i - i^3 = 2i$, so $Y = 0$, $y = 2$. $Z$ evaluates to $1 + i^4 = 2$, so $N = 2$, $n = 0$.
- $U = (YN + yn)/(N^2 + n^2) + (Yn - yN)\cos\phi/((N^2 + n^2)\sin\phi) = 0 + 0 = 0$.
- $u = -(Yn - yN)\cdot q/((N^2+n^2)p\sin\phi) = -(-4)/(4\cdot 1\cdot 1) = 1$.

So $U + uz = z$. The first partial fraction is $\dfrac{z}{(1 + z^2)^4}$.

Compute $F = (z - z^3 - z(1 + z^4))/(1 + z^2) = -z^3$.

Repeat with $F = -z^3$: at $z = i$, $-i^3 = i$, so the new $Y = 0$, new $y = 1$. $N, n$ unchanged ($N = 2, n = 0$). Then $V = 0$, $v = -(0 - 2)/(4) = 1/2$, so $V + vz = z/2$ and the second partial fraction is $\dfrac{z}{2(1 + z^2)^3}$.

Compute $G = (-z^3 - (z/2)(1 + z^2))/(1 + z^2) = -z/2 - z^3/2 \cdot$ wait — $G = (-z^3 - z/2 - z^5/2)/(1 + z^2) = -z/2 - z^3/2$.

Repeat: at $z = i$, $G = -i/2 - i^3/2 = -i/2 + i/2 = 0$, so $W = w = 0$. Third partial fraction is $0$.

Compute $H = (G - 0)/(1 + z^2) = (-z/2 - z^3/2)/(1 + z^2) = -z/2$.

Repeat: at $z = i$, $H = -i/2$, so the substituted values from $H$ are $0$ (real) and $-1/2$ (imaginary). Then $X = 0 + (0\cdot 0 - (-1/2)\cdot 2)\cdot 0/(4\cdot 1) = 0$ and $x = -(0\cdot 0 - (-1/2)\cdot 2)\cdot 1/(4\cdot 1\cdot 1) = -1/4$. Fourth partial fraction is $-\dfrac{z}{4(1 + z^2)}$ (source: chapter12, §209).

The complementary fraction has numerator $I = (H - (X + xz)Z)/(1 + z^2) = -z/4 + z^3/4$, divided by $1 + z^4$:

$$\frac{-z + z^3}{4(1 + z^4)}.$$

Putting everything together (source: chapter12, §209):

$$\frac{z - z^3}{(1 + z^2)^4(1 + z^4)} = \frac{z}{(1 + z^2)^4} + \frac{z}{2(1 + z^2)^3} - \frac{z}{4(1 + z^2)} + \frac{-z + z^3}{4(1 + z^4)}.$$

The remaining $1/(1 + z^4)$ piece could itself be decomposed into trinomial fractions by the §200–§205 rule (Example II of §203 does exactly this for the cousin denominator $(1 + \sqrt 2 z + z^2)(1 - \sqrt 2 z + z^2)$).

## General procedure

To decompose an arbitrary real proper rational function $M/N$:

1. If $M/N$ is improper, extract the polynomial part by division; see [[improper-rational-function]].
2. Factor $N$ over $\mathbb{R}$ into real linear and real quadratic factors (see [[chapter-9-on-trinomial-factors|Chapter 9]]).
3. For each real linear factor (distinct or repeated), use the [[partial-fraction-decomposition|Chapter 2 algorithm]].
4. For each *distinct* real quadratic [[trinomial-factor|trinomial factor]], use §200–§205 to produce a single partial fraction $(P + Qz)/(\text{trinomial})$.
5. For each *repeated* real quadratic factor $(\text{trinomial})^k$, use the §207–§209 iterative algorithm to produce the tower of $k$ partial fractions; the iteration's last polynomial is the numerator of the complementary fraction.
6. Sum all partial fractions (plus the polynomial part, if any). The result equals $M/N$ in fully real partial-fraction form.

## Why this matters

A *real* partial-fraction decomposition is what makes rational functions tractable when working over $\mathbb{R}$:

- **Integration.** Real linear pieces $A/(p - qz)$ integrate to logarithms; real quadratic pieces $(P + Qz)/(p^2 - 2pqz\cos\phi + q^2z^2)$ integrate to a logarithm plus an arctangent (after completing the square). Without §200–§205, one would either work with complex partial fractions (and then re-pair them at the end) or simply not have a method.
- **Series expansion.** Each real quadratic piece is, by [[recurrent-series|the §62–§70 recurrent-series machinery]], a power series whose coefficients satisfy a [[trigonometric-recurrent-progression|trigonometric recurrence]] $a_{n+2} = 2(\cos\phi)\,a_{n+1} - a_n$. Real partial fractions therefore expose the trigonometric content of any real rational function's series expansion.

## Related pages

- [[partial-fraction-decomposition]]
- [[improper-rational-function]]
- [[trinomial-factor]]
- [[factoring-polynomials]]
- [[fundamental-theorem-of-algebra]]
- [[de-moivre-formula]]
- [[trigonometric-addition-formulas]]
- [[trigonometric-recurrent-progression]]
- [[recurrent-series]]
- [[chapter-2-on-the-transformation-of-functions]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-12-on-the-development-of-real-rational-functions]]
