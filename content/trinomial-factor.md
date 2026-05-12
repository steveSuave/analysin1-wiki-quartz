# Trinomial Factor

**Summary**: §144–§146: a real quadratic of the form $p^2 - 2pqz\cos\phi + q^2z^2$ obtained as the product of a complex linear factor $qz - p(\cos\phi + i\sin\phi)$ and its conjugate. Every irreducible real quadratic factor of a polynomial can be written this way.

**Sources**: chapter9, chapter17

**Last updated**: 2026-05-11

---

## Why "trinomial"?

Chapter 2 established that every real polynomial decomposes into real linear factors and real quadratic factors (see [[factoring-polynomials]], [[complex-conjugate-factors]]). But finding the *complex* linear factors is hard, and Euler proposes a different route: search directly for the *real quadratic* factor in a normalized form, then read off the two complex linear factors from it.

A real quadratic $p - qz + rz^2$ has *complex* linear factors precisely when $4pr > q^2$, i.e. when

$$\frac{q}{2\sqrt{pr}} < 1.$$

Since this dimensionless quantity lies in $(-1, 1)$, Euler sets

$$\frac{q}{2\sqrt{pr}} = \cos\phi,\qquad q = 2\sqrt{pr}\cos\phi$$

(source: chapter9, §145). To avoid the awkward $\sqrt{pr}$, he absorbs it: rename $p \to p^2$ and $r \to q^2$. The trinomial factor takes the canonical form

$$\boxed{\;p^2 - 2pqz\cos\phi + q^2 z^2\;}$$

and its two (complex) linear factors are

$$qz - p(\cos\phi + i\sin\phi),\qquad qz - p(\cos\phi - i\sin\phi).$$

When $\cos\phi = \pm 1$, $\sin\phi = 0$ and both linear factors coincide and are real (source: chapter9, §145).

## How to find $p$, $q$, $\phi$ (§146–§149)

If $p^2 - 2pqz\cos\phi + q^2z^2$ divides a polynomial $\alpha + \beta z + \gamma z^2 + \delta z^3 + \cdots$, then the polynomial vanishes at both $z = (p/q)(\cos\phi + i\sin\phi)$ and $z = (p/q)(\cos\phi - i\sin\phi)$. Substitute and use [[de-moivre-formula|De Moivre]]: $z^n = (p/q)^n (\cos n\phi \pm i\sin n\phi)$. Writing $r = p/q$, the two substitutions give

$$0 = \alpha + \beta r\cos\phi + \gamma r^2\cos 2\phi + \delta r^3\cos 3\phi + \cdots \pm i(\beta r\sin\phi + \gamma r^2\sin 2\phi + \delta r^3\sin 3\phi + \cdots).$$

Adding and subtracting (and dividing the imaginary equation by $2i$) yields **two real equations**:

$$0 = \alpha + \beta r\cos\phi + \gamma r^2\cos 2\phi + \delta r^3\cos 3\phi + \cdots,$$

$$0 = \beta r\sin\phi + \gamma r^2\sin 2\phi + \delta r^3\sin 3\phi + \cdots.$$

(source: chapter9, §148). Two equations in two unknowns $r, \phi$. Each solution gives one trinomial factor; multiple solutions give multiple trinomial factors, and Euler claims they exhaust all of them (source: chapter9, §149).

The rule for any term: $z^n$ contributes $r^n\cos n\phi$ to the first equation and $r^n\sin n\phi$ to the second. Recall $\sin 0 = 0$, $\cos 0 = 1$, so a constant term $\alpha = \alpha z^0$ contributes $\alpha$ to the first equation and $0$ to the second.

§149 gives a useful generalization: multiplying the first equation by $\cos m\phi$ and the second by $\sin m\phi$ and combining produces

$$0 = \alpha\cos m\phi + \beta r\cos(m-1)\phi + \gamma r^2\cos(m-2)\phi + \cdots,$$

$$0 = \alpha\cos m\phi + \beta r\cos(m+1)\phi + \gamma r^2\cos(m+2)\phi + \cdots,$$

— any pair of these determines $r$ and $\phi$.

## Why this is a useful normalization

- The form makes the discriminant condition transparent: complex factors $\iff |\cos\phi| < 1$, real factors $\iff \cos\phi = \pm 1$.
- The arc $\phi$ is the *argument* of the complex root $(p/q)(\cos\phi + i\sin\phi)$ and $r = p/q$ is its modulus. The trinomial factor is therefore exactly $q^2(z - re^{i\phi})(z - re^{-i\phi})$ in modern notation, but Euler avoids invoking $e^{i\phi}$ here even though [[eulers-formula]] is already in his toolbox.
- The form interlocks with [[de-moivre-formula]] and the [[sine-and-cosine-series|trig power series]] cleanly: $z^n$ becomes a closed-form polynomial in $\cos\phi$ and $\sin\phi$.

This normalization is the engine of every result in Chapter 9 — from the closed-form factorization of $a^n \pm z^n$ (see [[factorization-of-an-plus-minus-zn]]) to the [[sine-infinite-product|infinite product]] for $\sin z$.

## Recovery from a recurrent series (Chapter 17)

[[chapter-17-using-recurrent-series-to-find-roots-of-equations|Chapter 17 §348–§352]] gives the reverse computation: when an algebraic equation has a dominant trinomial factor $1 - 2pz\cos\phi + p^2 z^2$ in its associated rational function, four consecutive terms $P, Q, R, S$ of a recurrent series with the equation's [[scale-of-the-relation|scale]] determine both $p$ and $\cos\phi$ in closed form:

$$p = \sqrt{\frac{R^2 - QS}{Q^2 - PR}},\qquad \cos\phi = \frac{QR - PS}{2\sqrt{(Q^2 - PR)(R^2 - QS)}}.$$

This is the complex-roots analogue of [[bernoullis-method-for-roots|Bernoulli's method]] — see [[trinomial-factor-from-recurrent-series]].

## Related pages

- [[factoring-polynomials]]
- [[complex-conjugate-factors]]
- [[fundamental-theorem-of-algebra]]
- [[de-moivre-formula]]
- [[factorization-of-an-plus-minus-zn]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[chapter-9-on-trinomial-factors]]
- [[trinomial-factor-from-recurrent-series]]
- [[bernoullis-method-for-roots]]
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]]
