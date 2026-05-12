# Complex Conjugate Factors

**Summary**: Euler's argument (§30–§31) that complex linear factors of a real polynomial come in pairs whose product is a real quadratic factor.

**Sources**: chapter2.pdf

**Last updated**: 2026-04-23

---

## Even count of complex factors

"In every equation the number of complex roots is even, so that the function $Z$ has either no complex factor, or it has two or four or six, etc." (source: chapter2.pdf, §30). If $P$ is the product of the real linear factors of $Z$, then $Z/P$ must be real, so the remaining complex factors must combine into a real product.

## Two complex factors → one real quadratic

If $Z$ has exactly two complex linear factors, their product is a real quadratic, since removing the real factors from a real polynomial leaves a real quotient (source: chapter2.pdf, §30).

## Four complex factors → two real quadratics (§31)

Euler considers a real polynomial
$$ Q = z^4 + A z^3 + B z^2 + C z + D $$
that does not split into two real quadratic factors. He writes it as the product of two complex quadratics in conjugate form:

$$ Q = \big(z^2 - 2(p + q i) z + r + s i\big) \big(z^2 - 2(p - q i) z + r - s i\big). $$

Expanding and solving gives four complex linear factors. Pairing the first with the third (and the second with the fourth), and letting $t = p^2 - q^2 - r$ and $u = 2 p q - s$, each paired product turns out to be

$$ z^2 - \left(2p \mp \sqrt{2 t + 2 \sqrt{t^2 + u^2}}\right) z + p^2 + q^2 \mp p \sqrt{2 t + 2 \sqrt{t^2 + u^2}} + \sqrt{t^2 + u^2} + q \sqrt{-2 t + 2 \sqrt{t^2 + u^2}}, $$

which Euler observes is real. Thus $Q$, assumed not to split into two real quadratic factors, in fact does. By contradiction, every real quartic splits into two real quadratic factors.

## Beyond degree four

Euler admits the same explicit construction does not go through in higher degree:

> Although the same method of proof is not valid for higher powers, nevertheless, there is no doubt that the same property holds for any number of complex factors. (source: chapter2.pdf, §32)

The general case is taken as a working hypothesis and used to justify the §32 decomposition of any real polynomial into real linear and quadratic factors. See [[fundamental-theorem-of-algebra]].

## Related pages

- [[factoring-polynomials]]
- [[fundamental-theorem-of-algebra]]
- [[chapter-2-on-the-transformation-of-functions]]
