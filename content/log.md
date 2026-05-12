# Log

Append-only record of wiki operations.

---

## 2026-04-23 — Ingested chapter1.pdf

Source: `raw/chapter1.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 1: "On Functions in General").

Created:

- `wiki/index.md` — table of contents.
- `wiki/log.md` — this file.
- `wiki/chapter-1-on-functions-in-general.md` — chapter summary.
- `wiki/function.md` — Euler's definition of a function.
- `wiki/variable-and-constant.md` — notational convention and scope of a variable.
- `wiki/classification-of-functions.md` — algebraic/transcendental tree.
- `wiki/single-valued-and-multi-valued-functions.md` — n-valued functions, Vieta relations.
- `wiki/even-and-odd-functions.md` — parity and multiplicative rules.
- `wiki/similar-functions.md` — Euler's "similar function" notion.

## 2026-04-23 — Converted math to LaTeX

Updated all wiki pages to use LaTeX syntax for mathematical expressions and variables, as per project rules.

Modified:
- `wiki/chapter-1-on-functions-in-general.md`
- `wiki/classification-of-functions.md`
- `wiki/even-and-odd-functions.md`
- `wiki/function.md`
- `wiki/similar-functions.md`
- `wiki/single-valued-and-multi-valued-functions.md`
- `wiki/variable-and-constant.md`

## 2026-04-23 — Ingested chapter2.pdf

Source: `raw/chapter2.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 2: "On the Transformation of Functions").

Created:

- `wiki/chapter-2-on-the-transformation-of-functions.md` — chapter summary.
- `wiki/factoring-polynomials.md` — linear/quadratic factors, roots, §28–§29.
- `wiki/fundamental-theorem-of-algebra.md` — Euler's §32 statement and its gap.
- `wiki/complex-conjugate-factors.md` — §30–§31 pairing of complex factors into real quadratics.
- `wiki/intermediate-value-property.md` — §33 IVT-like property.
- `wiki/real-roots-by-degree-parity.md` — §34–§37 corollaries for odd/even degree.
- `wiki/improper-rational-function.md` — §38 polynomial-part split.
- `wiki/partial-fraction-decomposition.md` — §39–§46 algorithm with worked example.

Modified:

- `wiki/index.md` — added chapter-2 summary and concept links, split concepts by chapter.

## 2026-04-23 — Ingested chapter3.pdf

Source: `raw/chapter3.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 3: "On the Transformation of Functions by Substitution", §46–§58).

Created:

- `wiki/chapter-3-on-the-transformation-of-functions-by-substitution.md` — chapter summary.
- `wiki/substitution.md` — the technique of introducing a new variable to define both $y$ and $z$.
- `wiki/rationalizing-substitutions.md` — §47–§51 catalog of radical-removing substitutions.
- `wiki/rational-parametrization-of-the-circle.md` — the §46/§50 half-angle parametrization.
- `wiki/homogeneous-substitution.md` — §52–§58 $y = xz$ / $y = x^m z^n$ trick.
- `wiki/folium-of-descartes.md` — §52 worked example: $y^3 + z^3 - cyz = 0$.

Modified:

- `wiki/index.md` — added chapter-3 summary and new concept links.

## 2026-04-23 — Ingested chapter4.pdf

Source: `raw/chapter4.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 4: "On the Development of Functions in Infinite Series", §59–§76).

Created:

- `wiki/chapter-4-on-the-development-of-functions-in-infinite-series.md` — chapter summary.
- `wiki/geometric-series.md` — §60: the series for $a/(\alpha + \beta z)$.
- `wiki/method-of-undetermined-coefficients.md` — §60–§61: match-powers-of-$z$ technique.
- `wiki/recurrent-series.md` — §62–§70: De Moivre's recurrent series; law read off the denominator; Laurent case; non-uniqueness.
- `wiki/higher-order-arithmetic-progressions.md` — §64–§67: $(1-z)^{k+1}$-recurrent progressions with constant $k$-th differences.
- `wiki/binomial-series.md` — §71–§76: Newton's $(P+Q)^{m/n}$ and its recurrent form when $Z$ is a polynomial in $z$.

Modified:

- `wiki/index.md` — added chapter-4 summary and five new concept links.

## 2026-04-23 — Ingested chapter5.pdf

Source: `raw/chapter5.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 5: "Concerning Functions of Two or More Variables", §77–§95).

Created:

- `wiki/chapter-5-on-functions-of-two-or-more-variables.md` — chapter summary.
- `wiki/functions-of-several-variables.md` — §77–§82: independent variables; Ch.1 classification carried over; implicit-function / equation-counting remark.
- `wiki/homogeneous-function.md` — §83–§91: degree for polynomial, rational, irrational, and implicit cases; the §88 reduction $V = z^n f(y/z)$; linear factorization of bivariate homogeneous polynomials.
- `wiki/heterogeneous-function.md` — §92–§93: bifid, trifid, reduction to homogeneity by substitution.
- `wiki/reducible-polynomial.md` — §94–§95: order of a polynomial, reducibility into non-irrational factors.

Modified:

- `wiki/homogeneous-substitution.md` — added a "Theoretical justification" section linking the §52–§58 trick to the §88 reduction theorem.
- `wiki/classification-of-functions.md` — added "Extension to several variables" section noting §79–§80 carry the tree over verbatim.
- `wiki/index.md` — added chapter-5 summary line and a "From Chapter 5" concept section with four entries.

## 2026-04-24 — Lint fixes

Created:

- `wiki/implicit-function-and-equation-counting.md` — §82 heuristic that relations define variables implicitly and each independent equation reduces freedom by one.
- `wiki/order-of-a-polynomial.md` — §94 definition of polynomial order and its geometric use.

Modified:

- `wiki/chapter-3-on-the-transformation-of-functions-by-substitution.md` — removed stray front matter to match wiki page format.
- `wiki/folium-of-descartes.md` — removed stray front matter to match wiki page format.
- `wiki/functions-of-several-variables.md` — removed stray front matter and linked the §82 heuristic to its own concept page.
- `wiki/heterogeneous-function.md` — removed stray front matter to match wiki page format.
- `wiki/homogeneous-function.md` — removed stray front matter and corrected the ternary quadratic example in the three-variable non-factorization remark.
- `wiki/homogeneous-substitution.md` — removed stray front matter to match wiki page format.
- `wiki/improper-rational-function.md` — fixed the case-mismatched link to `partial-fraction-decomposition`.
- `wiki/rational-parametrization-of-the-circle.md` — removed stray front matter to match wiki page format.
- `wiki/rationalizing-substitutions.md` — removed stray front matter to match wiki page format.
- `wiki/reducible-polynomial.md` — removed stray front matter and linked "order" to its own concept page.
- `wiki/substitution.md` — removed stray front matter to match wiki page format.
- `wiki/chapter-5-on-functions-of-two-or-more-variables.md` — linked the implicit-function heuristic and polynomial order to dedicated concept pages.
- `wiki/index.md` — added the two new Chapter 5 concept pages.

## 2026-04-25 — Clarified 'solution of equations' operation

Modified:

- `wiki/function.md` — elaborated on the "solution of equations" operation to explain its role in defining implicit functions.
- `wiki/classification-of-functions.md` — explicitly linked the "solution of equations" operation to the definition of implicit irrational functions.

## 2026-04-26 — Ingested chapter6.pdf

Source: `raw/chapter6.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 6: "On Exponentials and Logarithms", §96–§113).

Created:

- `wiki/chapter-6-on-exponentials-and-logarithms.md` — chapter summary.
- `wiki/exponential-function.md` — §96–§101: $a^z$, definition by extension, case-split on $a$, canonical case $a > 1$.
- `wiki/logarithm.md` — §102–§104: inverse of $a^z$, when real, the four algebraic rules.
- `wiki/transcendence-of-logarithms.md` — §105: dichotomy showing $\log b$ is transcendental unless $b$ is a rational power of the base.
- `wiki/geometric-mean-method-for-logarithms.md` — §106: iterated $\sqrt{AB}$ algorithm with the worked $\log_{10} 5$ table; historical note on Briggs and Vlacq.
- `wiki/change-of-base.md` — §107–§108: ratio invariance, conversion factor $1/\log_a b$, the §109 prime-tabulation reduction.
- `wiki/common-logarithm.md` — §112: base 10 and its decimal advantage.
- `wiki/characteristic-and-mantissa.md` — §112–§113: integer/fractional split, digit count from characteristic, digit string from mantissa, $2^{16777216}$ closing example.

Modified:

- `wiki/index.md` — added chapter-6 summary line and a "From Chapter 6" concept section with seven entries.

## 2026-04-26 — Ingested chapter7.pdf

Source: `raw/chapter7.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 7: "Exponentials and Logarithms Expressed through Series", §114–§125).

Created:

- `wiki/chapter-7-on-exponentials-and-logarithms-expressed-through-series.md` — chapter summary.
- `wiki/infinitesimal-and-infinite-numbers.md` — Euler's working device of $\omega$ infinitely small and $j = z/\omega$ infinitely large; the algebraic identity $(j - m)/(nj) = 1/n$ that collapses binomial expansions into power series.
- `wiki/exponential-series.md` — §115–§117: derivation of $a^z = \sum (kz)^n/n!$ from $(1 + kz/j)^j$; the implicit relation $a = \sum k^n/n!$; the general $b^z$ formula via $\log b$.
- `wiki/logarithmic-series.md` — §118–§121: the boxed $\log(1+x) = (1/k)\sum(-1)^{n+1}x^n/n$; the divergence paradox at $a = 10$; the fast-converging $\log\frac{1+x}{1-x} = (2/k)\sum x^{2n+1}/(2n+1)$ with $x = (a-1)/(a+1)$.
- `wiki/eulers-number.md` — §122: choosing the base so $k = 1$ gives $e = \sum 1/n! = 2.71828\ldots$; first appearance of the symbol $e$.
- `wiki/natural-logarithm.md` — §123–§125: defining property $\log(1+\omega) = \omega$; the three master series in base $e$; the twenty-digit table $\log 1, \ldots, \log 10$ with the $\log 7$ trick via $x = 1/99$; identification $k = \log_e a$ recovering [[change-of-base]] from a different angle.

Modified:

- `wiki/index.md` — added chapter-7 summary line and a "From Chapter 7" concept section with five entries.

## 2026-04-27 — Ingested chapter8.pdf

Source: `raw/chapter8.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 8: "On Transcendental Quantities Which Arise from the Circle", §126–§142).

Created:

- `wiki/chapter-8-on-transcendental-quantities-which-arise-from-the-circle.md` — chapter summary.
- `wiki/pi.md` — §126: Euler's adoption of the symbol $\pi$; the 113-digit decimal expansion; unit-circle convention.
- `wiki/sine-and-cosine.md` — §127: definitions on the unit circle; special values; Pythagorean identity; co-function relations; tangent/cotangent.
- `wiki/trigonometric-addition-formulas.md` — §128, §130, §131: the four sum/difference identities, the periodicity catalog $\sin\bigl((4n+k)\pi/2 \pm z\bigr)$, product-to-sum, sum-to-product, half-angle, derived ratios.
- `wiki/trigonometric-recurrent-progression.md` — §129: sines and cosines of arithmetic-progression arcs as a recurrent series with denominator $1 - 2\cos y\cdot Z + Z^2$.
- `wiki/de-moivre-formula.md` — §132–§133: complex factorization of unity, the multiplicative law, De Moivre $(\cos z \pm i\sin z)^n = \cos nz \pm i\sin nz$, binomial expansions of $\cos nz$ and $\sin nz$.
- `wiki/sine-and-cosine-series.md` — §134: derivation of $\cos v = 1 - v^2/2! + \cdots$ and $\sin v = v - v^3/3! + \cdots$ from De Moivre by $z$ infinitesimal, $n$ infinite, $nz = v$ finite; the 28-digit numerical series for $\sin(m\pi/(2n))$ and $\cos(m\pi/(2n))$.
- `wiki/eulers-formula.md` — §138: derivation of $e^{iv} = \cos v + i\sin v$, $\cos v = (e^{iv} + e^{-iv})/2$, $\sin v = (e^{iv} - e^{-iv})/(2i)$.
- `wiki/arctangent-series.md` — §139–§141: $z = (1/2i)\log\frac{\cos z + i\sin z}{\cos z - i\sin z}$, $\arctan t = t - t^3/3 + t^5/5 - \cdots$, Leibniz's $\pi/4$, the $\arctan(1/\sqrt 3)$ series.
- `wiki/machin-like-formula.md` — §142: decomposition $\pi/4 = \arctan(1/2) + \arctan(1/3)$ and the resulting rational geometric-rate series for $\pi$.

Modified:

- `wiki/index.md` — added chapter-8 summary line and a "From Chapter 8" concept section with nine entries.

## 2026-04-29 — Ingested chapter9.pdf

Source: `raw/chapter9.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 9: "On Trinomial Factors", §143–§164).

Created:

- `wiki/chapter-9-on-trinomial-factors.md` — chapter summary.
- `wiki/trinomial-factor.md` — §144–§146: canonical form $p^2 - 2pqz\cos\phi + q^2z^2$, the §148 two-equation extraction algorithm, §149 generalization.
- `wiki/factorization-of-an-plus-minus-zn.md` — §150–§153: cyclotomic factorization of $a^n + z^n$ via $(2k+1)\pi/n$, $a^n - z^n$ via $2k\pi/n$, and the master formula for $a^{2n} - 2a^n z^n\cos g + z^{2n}$.
- `wiki/exponential-infinite-product.md` — §155–§157: $e^x - 1$, $(e^x - e^{-x})/2 = \sinh$, $(e^x + e^{-x})/2 = \cosh$ as infinite products from $(1 + x/j)^j$.
- `wiki/sine-infinite-product.md` — §158: $\sin z = z\prod(1 - z^2/k^2\pi^2)$ via $x = iz$; bridge to the Basel problem.
- `wiki/cosine-infinite-product.md` — §158: $\cos z = \prod(1 - 4z^2/(2k+1)^2\pi^2)$; sum of reciprocal odd squares = $\pi^2/8$.

Modified:

- `wiki/index.md` — added chapter-9 summary line and a "From Chapter 9" concept section with five entries.

## 2026-04-30 — Ingested chapter10.pdf

Source: `raw/chapter10.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 10: "On the Use of the Discovered Factors to Sum Infinite Series", §165–§183).

Created:

- `wiki/chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series.md` — chapter summary covering the four movements: Newton's identities, even-zeta evaluation, arc-form character series, partial-fraction expansions.
- `wiki/newtons-identities.md` — §165–§166: the elementary-symmetric ↔ power-sum recurrence $P = A$, $Q = AP - 2B$, $R = AQ - BP + 3C$, etc.
- `wiki/basel-problem.md` — §167: derivation of $\sum 1/k^2 = \pi^2/6$ from the sinh product via Newton's identities, plus the higher-power $\zeta(2k)$ values.
- `wiki/zeta-at-even-integers.md` — §168: the tabulated rational coefficients of $\zeta(2k)/\pi^{2k}$ through $\zeta(26)$; modern footnote linking Euler's $c_k$ to Bernoulli numbers $B_{2k}$.
- `wiki/odd-and-alternating-zeta-decomposition.md` — §170: the $M$, $M/2^n$, $M - M/2^n$, $M - 2M/2^n$ algebra splitting any zeta sum into even, odd, alternating restrictions.
- `wiki/circular-arc-series.md` — §171–§180: Newton's identities applied to the §164 products $\cos(v/2) + \tan(g/2)\sin(v/2)$ with $v = \pi x/n$, $g = m\pi/n$; the family of character-style series including Leibniz's $\pi/4$ and $\sqrt{2}, \sqrt{3}$ analogues.
- `wiki/cotangent-partial-fraction.md` — §181–§183: partial-fraction expansions of $\pi\cot(\pi\sqrt a)$, $\pi/\sin(\pi\sqrt a)$ from combining §172 and §174 in pairs; hyperbolic versions for $a = -b$ via Euler's formula.

Modified:

- `wiki/index.md` — added chapter-10 summary line and a "From Chapter 10" concept section with six entries.
- `wiki/exponential-infinite-product.md` — linked the chapter-10 follow-up (Newton's identities, Basel, zeta tables) and updated related-pages list.
- `wiki/sine-infinite-product.md` — linked the chapter-10 derivation in the Basel teaser and updated related-pages list.
- `wiki/cosine-infinite-product.md` — extended related-pages list to chapter-10 concepts.
- `wiki/arctangent-series.md` — noted that chapter 10 re-derives Leibniz's $\pi/4$ as a special case of `circular-arc-series`; updated related-pages list.
- `wiki/chapter-9-on-trinomial-factors.md` — linked the Basel-problem comparison and chapter-10 follow-ups; extended related-pages list.

## 2026-05-01 — Ingested chapter11.pdf

Source: `raw/chapter11.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 11: "On Other Infinite Expressions for Arcs and Sines", §184–§198).

Created:

- `wiki/chapter-11-on-other-infinite-expressions-for-arcs-and-sines.md` — chapter summary covering the four movements: linear-factor split, Wallis product, log $\pi$ via transposition, log sin/cos and fast tan/cot via the same transposition.
- `wiki/linear-factors-of-sine-cosine.md` — §184: the [[sine-infinite-product|§158]] products at $z = m\pi/(2n)$ rationalize each quadratic factor into two linear factors; co-function identity gives a second expression per function.
- `wiki/wallis-product.md` — §185: $\pi/2 = (2\cdot 2\cdot 4\cdot 4\cdots)/(1\cdot 3\cdot 3\cdot 5\cdots)$ from dividing the two §184 expressions; parametric variants for $\sqrt 2$ etc.; convergence note.
- `wiki/trig-infinite-products.md` — §186–§187: $\tan, \cot, \sec, \csc$ as quotients of the §184 products; ratio formulas in §187.
- `wiki/log-pi-via-products.md` — §188–§190: take log of $\pi = 4\prod(1 - 1/(2k+1)^2)$, expand each factor by the [[logarithmic-series|§118 series]], transpose to get $\log\pi = \log 4 - (A-1) - (B-1)/2 - \cdots$ in odd-square sums; numerical $\log_e\pi = 1.144729\ldots$.
- `wiki/log-sine-via-products.md` — §191–§198: same transposition trick for $\log\sin$ and $\log\cos$, with column sums $A, B, C, \ldots$ (odd integers) and $\alpha, \beta, \gamma, \ldots$ (even integers); §197 partial-fraction route to $\tan, \cot$.

Modified:

- `wiki/index.md` — added chapter-11 summary line and a "From Chapter 11" concept section with five entries.

## 2026-05-04 — Ingested chapter12.pdf

Source: `raw/chapter12.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 12: "On the Development of Real Rational Functions", §199–§210).

Created:

- `wiki/chapter-12-on-the-development-of-real-rational-functions.md` — chapter summary covering the two movements: closed-form coefficients $P, Q$ for distinct quadratic factors (§199–§205) and the iterative tower for repeated quadratic factors (§206–§210).
- `wiki/real-partial-fraction-decomposition.md` — §199–§210: derivation of the $P, Q$ formula from substituting the [[trinomial-factor|trinomial]]'s complex roots via [[de-moivre-formula|De Moivre]]; the §204 streamlining that reduces to four scalars; iterative procedure for $(p^2 - 2pqz\cos\phi + q^2z^2)^k$; worked Examples I, III from §203 and the §209 repeated-factor example $\frac{z - z^3}{(1+z^2)^4(1+z^4)}$; §210 observation that the iteration's leftover polynomial is the numerator of the complementary fraction for free.

Modified:

- `wiki/partial-fraction-decomposition.md` — replaced the "quadratic factors handled later" note with an explicit forward link to `real-partial-fraction-decomposition`; added the new page and `trinomial-factor` to related pages.
- `wiki/index.md` — added chapter-12 summary line and a "From Chapter 12" concept section with the new entry.

## 2026-05-10 — Ingested chapter14.pdf

Source: `raw/chapter14.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 14: "On the Multiplication and Division of Angles", §234–§258).

Created:

- `wiki/chapter-14-on-the-multiplication-and-division-of-angles.md` — chapter summary covering the five movements: multiple-angle polynomials, roots at equally-spaced angles, factored products for sin/cos, partial-fraction sums for all six trig functions, and sum of trig functions in AP.
- `wiki/multiple-angle-polynomials.md` — §234–§238, §243: recurrence-generated tables and general formulas for $\sin nz$ and $\cos nz$ as polynomials in $\sin z$ and $\cos z$; odd/even $n$ cases; Chebyshev polynomials.
- `wiki/trig-values-as-roots.md` — §235–§256: the $n$ roots of the multiple-angle polynomial are trig values at equally-spaced angles; Vieta's formulas generating all product and sum identities of the chapter.
- `wiki/sine-cosine-factored-products.md` — §237, §240–§245: the $2^{n-1}$ product formula for $\sin nz$ and $\cos nz$; unified formula covering odd and even $n$; discrete Fourier zero-sum.
- `wiki/trig-multiple-angle-partial-fractions.md` — §237, §246–§256: finite-$n$ partial-fraction sums for csc, sec, cot, tan at shifted equally-spaced angles; product of tangents; connection to Chapter 10 Mittag-Leffler formulas.
- `wiki/sum-of-trig-in-ap.md` — §258: generating-function evaluation at $z = 1$ gives $(\sin a - \sin(a-b))/(2-2\cos b)$ for the infinite sum of sines in arithmetic progression.

Modified:

- `wiki/de-moivre-formula.md` — added "Extension in Chapter 14" section noting the §249 tangent derivation; expanded related-pages list.
- `wiki/cotangent-partial-fraction.md` — added "Finite analogue in Chapter 14" section noting the $n\cot nz$ finite sum; expanded related-pages list.
- `wiki/trigonometric-recurrent-progression.md` — added "Application in Chapter 14" section linking §234 multiple-angle table and §258 sum; expanded related-pages list.
- `wiki/index.md` — added chapter-14 summary line and a "From Chapter 14" concept section with five entries.

## 2026-05-07 — Ingested chapter13.pdf

Source: `raw/chapter13.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 13: "On Recurrent Series", §211–§233).

Created:

- `wiki/chapter-13-on-recurrent-series.md` — chapter summary covering the three movements: closed-form general term via real partial fractions (§211–§223), inverse problem and De Moivre's "scale of the relation" (§224–§230), and infinite/partial sums (§231–§233).
- `wiki/general-term-of-recurrent-series.md` — §215–§223: closed-form coefficient of $z^n$ from the partial-fraction decomposition; linear-factor brick $A/(1-pz)^k$ gives binomial-times-$p^n$, quadratic-factor brick $(A+Bpz)/(1-2pz\cos\phi+p^2 z^2)^k$ gives $\sin(n+1)\phi/\sin\phi$ (for $k=1$) and increasingly complicated trigonometric polynomials for $k=2,3,4$; Examples I–V of §216 plus §223's mod-6 partition example $1/((1-z)(1-z^2)(1-z^3))$ and mod-4 example.
- `wiki/scale-of-the-relation.md` — §224: De Moivre's terminology for the recurrence multipliers $\alpha, \beta, \gamma, \ldots$; equivalence with the (sign-flipped) denominator of the generating rational function; §225 procedure for recovering closed-form general term from the scale.
- `wiki/closed-form-two-term-recurrence.md` — §226–§229: Binet-type formula $X_n = Up^n + Vq^n$ for two-member scales; the principal invariant $UV = (B^2 - \alpha AB + \beta A^2)/(4\beta - \alpha^2)$; term-from-single-predecessor formula with apparent square root that is always rational; doubling formula $X_{2n}, X_{2n+1}$; Lucas-numbers worked example.
- `wiki/sum-of-recurrent-series.md` — §231–§233: infinite sum equals the rational function; partial sum has closed-form rational expression; for two-member scales the partial sum collapses to first/last terms only; Lucas example $1+3+4+7+11+\cdots+P = (3P-6+\sqrt{5P^2+20})/2$.

Modified:

- `wiki/recurrent-series.md` — added a "Closed-form theory (Chapter 13)" section with forward links to the four new Chapter 13 pages; updated summary to note Chapter 13 develops the closed form, inverse problem, and sum; added `chapter13.pdf` to sources; expanded related-pages list.
- `wiki/index.md` — added chapter-13 summary line and a "From Chapter 13" concept section with the four new entries.

## 2026-05-11 — Extended chapter14.pdf ingestion to §259–§263

The earlier pass on chapter14.pdf stopped at §258. Re-read §259–§263 and extended the wiki to cover the finite arithmetic-progression sum and the powers-of-trig inversion that close the chapter.

Created:

- `wiki/powers-of-sine-and-cosine.md` — §261–§263: $(\sin z)^n$ and $(\cos z)^n$ as binomial-weighted finite sums of $\sin kz$ / $\cos kz$; derivation from the four product-to-sum lemmas of §262; tables through $n = 9$ for sine and $n = 7$ for cosine; modern derivation from [[eulers-formula]].

Modified:

- `wiki/sum-of-trig-in-ap.md` — added §259–§260 finite-sum section deriving $\sum_{k=0}^n\sin(a+kb) = \sin(a + nb/2)\sin((n+1)b/2)/\sin(b/2)$ by subtracting the tail of the infinite series; updated section range and summary.
- `wiki/chapter-14-on-the-multiplication-and-division-of-angles.md` — extended section range to §234–§263; expanded Movement 5 to include the finite-AP sums of §259–§260; added Movement 6 for the §261–§263 powers-of-sin/cos inversion.
- `wiki/index.md` — extended the chapter-14 one-liner; updated the `sum-of-trig-in-ap` entry to §258–§260; added `powers-of-sine-and-cosine` to the "From Chapter 14" section.

## 2026-05-11 — Cross-linked chapter 13 §222 with chapter 14 powers-of-sine-and-cosine

Re-read chapter13.pdf to verify coverage after noticing the log entries were out of chronological order (chapter 13 was ingested 2026-05-07 but logged after chapter 14, which was ingested 2026-05-10). Coverage of §211–§233 is complete, but the §222 odd-power identities ($16\sin^5\phi = 10\sin\phi - 5\sin 3\phi + \sin 5\phi$, etc.) — invoked in chapter 13 to convert the complex $k=3,4$ general-term derivations to real form — are exactly the table derived in chapter 14 §262, and neither side referenced the other.

Modified:

- `wiki/chapter-13-on-recurrent-series.md` — noted that the §222 identities are systematically derived in chapter 14 §262; added `powers-of-sine-and-cosine` and `chapter-14-on-the-multiplication-and-division-of-angles` to related pages.
- `wiki/general-term-of-recurrent-series.md` — forward link from the §222 identity listing to `powers-of-sine-and-cosine`; added to related pages.
- `wiki/powers-of-sine-and-cosine.md` — added "Earlier use in Chapter 13 §222" section explaining that this is where Euler first invokes (unproven) the odd-power identities; added `general-term-of-recurrent-series` and `chapter-13-on-recurrent-series` to related pages.

## 2026-05-11 — Ingested chapter15.pdf

Source: `raw/chapter15.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 15: "On Series Which Arise From Products", §264–§296).

Created:

- `wiki/chapter-15-on-series-which-arise-from-products.md` — chapter summary covering five movements: symmetric-coefficient series from $\prod(1+\alpha_i z)$; reciprocal products and the Euler product; logarithms and divergence of $\sum 1/p$; sieve derivation of the Euler product; prime-classified series for $\pi$.
- `wiki/euler-product-formula.md` — §270–§277, §283–§284: the central identity $\sum 1/k^n = \prod_p (1-1/p^n)^{-1}$ derived two ways (reciprocal-product expansion via unique factorisation; sieve of Eratosthenes on the series); the Möbius-dual relation; the alternating-character variant for $\pi/4$.
- `wiki/squarefree-and-mobius-series.md` — §267–§269: $\prod(1+1/p^n)$ as squarefree-supported sum; $\prod(1-1/p^n) = \sum \mu(k)/k^n$; numerical examples $6/\pi^2$ and $90/\pi^4$.
- `wiki/divergence-of-prime-reciprocals.md` — §278–§280: derivation of $\sum 1/p = \infty$ via $\log\zeta$ transposed to a double sum; comparison with Euclid; comparison with Mertens; the $n = 2, 4$ closed forms.
- `wiki/prime-zeta-values.md` — §281–§282: Euler's 12-digit table of $\sum 1/p^n$ for $n = 2, 4, \ldots, 36$; bootstrap-from-large-$n$ method using closed-form $\zeta(2k)$; explanation of why no closed form exists for the prime-zeta values.
- `wiki/prime-sign-series-for-pi.md` — §285–§296: catalogue of identities expressing $\pi/4$, $\pi/2$, $\pi^3/32$, $\pi/(3\sqrt 3)$, $\pi/(2\sqrt 2)$ as Euler-product-form Dirichlet $L$-functions with primes classified mod 4, mod 6, mod 8; the §285 sieve derivation worked through in detail; modern dictionary linking Euler's four examples to characters $\chi_{-4}, \chi_{-3}, \chi_8$.

Modified:

- `wiki/index.md` — added chapter-15 summary line and "From Chapter 15" concept section with five entries.
- `wiki/arctangent-series.md` — noted that Chapter 15 sieves Leibniz's $\pi/4$ series into Euler-product form; expanded related-pages list.
- `wiki/basel-problem.md` — added "Re-derivation via primes (Chapter 15)" section with the prime-only product $\pi^2/6 = \prod p^2/(p^2-1)$; expanded related-pages list.
- `wiki/circular-arc-series.md` — added the chapter-15 prime-classified forms to related-pages list.
- `wiki/zeta-at-even-integers.md` — added "Re-derivation via primes (Chapter 15)" section noting that closed-form $\zeta(2k)$ values feed the §281 prime-zeta inversion; expanded related-pages list.
- `wiki/wallis-product.md` — added chapter-15 prime-only Wallis-style products to related-pages list.
- `wiki/logarithmic-series.md` — added chapter-15 and divergence-of-prime-reciprocals to related-pages list (logarithmic series is the engine of the §278 transposition).

## 2026-05-11 — Ingested chapter16.pdf

Source: `raw/chapter16.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 16: "On the Partition of Numbers", §297–§331).

Created:

- `wiki/chapter-16-on-the-partition-of-numbers.md` — chapter summary covering nine movements: distinct-part product, unrestricted reciprocal product, closed-form recurrent series for $P_m$ via functional equation $Z(x, xz) = Z/(1+xz)$, Pascal-like recurrence $p_m(n) = p_{m-1}(n) + p_m(n-m)$, figurate-number structure of the columns, pentagonal number theorem, distinct = odd, binary and balanced-ternary uniqueness, partition table.
- `wiki/partition-of-numbers.md` — core concept page: definitions, $p(n)$/$p_m(n)$/$q(n)$/$q_m(n)$ notation, Euler's six enumerated examples ($p(6) = 11$, $q(8) = 6$, $q_7(35) = 15$, $p_5(13) = 18$, $p(7) = 15$, $q(9) = 8$), index of the chapter's six theorems.
- `wiki/partition-generating-functions.md` — §297–§315: bivariate products as enumerators by integer-size $x$ and part-count $z$; functional-equation derivation of $P_m = x^{m(m+1)/2}/\prod_{k=1}^m(1-x^k)$ and the unrestricted analogue; the staircase bijection in both forms.
- `wiki/partitions-into-distinct-parts.md` — §299–§315: $q_m(n)$ generating function, the five closed forms $P, Q, R, S, T$ with triangular-number numerators, bijective interpretation of the staircase, $q(50)$ from the table, derivation of $q(n)$ from $p(n)$ via the pentagonal expansion.
- `wiki/partition-recurrence.md` — §316–§318: combinatorial and algebraic derivations of $p_m(n) = p_{m-1}(n) + p_m(n-m)$; sample entries from Euler's table; faster pentagonal-number recurrence for the unrestricted partition function.
- `wiki/eulers-pentagonal-number-theorem.md` — §323–§324: the identity $\prod(1-x^k) = \sum_{n\in\mathbb Z}(-1)^n x^{n(3n-1)/2}$; Euler's empirical discovery (no proof in the *Introductio*); induced $O(\sqrt n)$-term recurrence for $p(n)$ worked through $p(7), p(10), p(15)$; the partition function's [[scale-of-the-relation|scale of the relation]] is infinite but sparsely supported on the pentagonal-number lattice; connection to the Dedekind $\eta$-function.
- `wiki/distinct-parts-equals-odd-parts.md` — §326: one-line proof $\prod(1+x^k) = 1/\prod(1-x^{2k-1})$ via $PQ = \prod(1-x^{2k})$; $q(9) = 8$ as worked example with both enumerations; §327 derivation of $q(n)$ from $p(n)$; Glaisher's bijection (anachronistic).
- `wiki/binary-representation-theorem.md` — §328–§329: $\prod(1+x^{2^k}) = 1/(1-x)$ by the substitution $x \mapsto x^2$ and fixed-point analysis; uniqueness of binary; weighing with $1, 2, 4, \ldots$-pound weights.
- `wiki/balanced-ternary-representation.md` — §330–§331: $\prod(x^{-3^k}+1+x^{3^k}) = \sum_{n\in\mathbb Z}x^n$ by the substitution $x \mapsto x^3$; every integer is uniquely a signed sum of distinct powers of $3$ with digits $\{-1, 0, +1\}$; two-pan balance weighing; comparison with binary.

Modified:

- `wiki/index.md` — added chapter-16 summary line; added "From Chapter 16" concept section with eight entries.
- `wiki/recurrent-series.md` — added note that Chapter 16 uses recurrent series with denominator $\prod_{k=1}^m(1-x^k)$ to enumerate partitions by largest-part bound, and that the partition function's recurrence (from the pentagonal theorem) is a recurrent-series scale supported on the pentagonal lattice; expanded related-pages list.
- `wiki/scale-of-the-relation.md` — added note that the partition function has a famous *sparse* scale (entries at the pentagonal numbers, signs $(-1)^n$), Euler's first example of a series whose scale is infinite but whose effective recurrence uses only $O(\sqrt n)$ predecessors; expanded related-pages list.
- `wiki/higher-order-arithmetic-progressions.md` — added "Use in Chapter 16" note explaining how the column generating functions $1/\prod_{k=1}^m(1-x^k)$ produce the triangular, tetrahedral, … numbers as leading-column entries; expanded related-pages list.
- `wiki/geometric-series.md` — added a "Used in Chapter 16" note that the partition generating functions are built from geometric series factor by factor, and that the binary identity $\prod(1+x^{2^k}) = 1/(1-x)$ is the simplest non-trivial product equal to a geometric series; expanded related-pages list.

## 2026-05-11 — Ingested chapter17.pdf

Source: `raw/chapter17.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 17: "Using Recurrent Series to Find Roots of Equations", §332–§355).

Created:

- `wiki/chapter-17-using-recurrent-series-to-find-roots-of-equations.md` — chapter summary covering eight movements: basic correspondence (Q/P → largest root), failure modes, numerator choice, repeated real factors, dominant complex factor, repeated trinomial factors with substitution rescue, geometric-progression theoretical justification (§354), and partial application to transcendental equations (§355).
- `wiki/bernoullis-method-for-roots.md` — §332–§347, §354–§355: the core method for distinct real roots (Q/P → p, the largest); failure modes (close roots remedied by substitution shift $x = y + k$, the ±p case where alternate ratios converge to $p^2$); numerator choice (safe default = 1); repeated real factors with their slow $1 + O(1/n)$ excess; §354 geometric-progression justification; §355 application to $\sin z = 1/2$ recovering $\pi/6 = 0.52356$ to four digits.
- `wiki/trinomial-factor-from-recurrent-series.md` — §348–§353: the complex-roots analogue. When a dominant trinomial factor $1 - 2pz\cos\phi + p^2z^2$ is in the denominator, $Q/P$ oscillates; from $Pp^2 + R = 2Qp\cos\phi$ and the shifted version, Euler eliminates the amplitudes and the index $n$ to obtain $p = \sqrt{(R^2 - QS)/(Q^2 - PR)}$ and $\cos\phi = (QR - PS)/(2\sqrt{(Q^2-PR)(R^2-QS)})$; the §353 substitution rescue for repeated trinomial factors.

Modified:

- `wiki/recurrent-series.md` — added an "Inverse use in Chapter 17" section describing Bernoulli's method as the reverse direction of chapter-13 closed forms; updated summary and sources; expanded related-pages list.
- `wiki/scale-of-the-relation.md` — extended the "same data, three views" note to call out that the characteristic-equation view is what Chapter 17 exploits; updated summary and sources; expanded related-pages list.
- `wiki/general-term-of-recurrent-series.md` — added a "Dominant term and Bernoulli's method (Chapter 17)" section deriving $Q/P \to p$ from the §215 linear-factor brick; updated summary and sources; expanded related-pages list.
- `wiki/chapter-13-on-recurrent-series.md` — added an "Inverse application in Chapter 17" section; expanded related-pages list.
- `wiki/closed-form-two-term-recurrence.md` — added a "Dominant-root limit (Chapter 17)" section deriving the $X_{n+1}/X_n \to p$ limit directly from the Binet form, with the §338 Example I worked through; updated sources; expanded related-pages list.
- `wiki/trinomial-factor.md` — added a "Recovery from a recurrent series (Chapter 17)" section stating the §348–§352 closed form; updated sources; expanded related-pages list.
- `wiki/index.md` — added chapter-17 summary line and "From Chapter 17" concept section with the two new entries.

## 2026-05-11 — Ingested chapter18.pdf (final chapter of Book I)

Source: `raw/chapter18.pdf` (Euler, *Introductio in analysin infinitorum*, Book I, Chapter 18: "On Continued Fractions", §356–§382). Closes Book I — Euler's last sentence in the book is "END OF THE FIRST BOOK" following the Gregorian-calendar calculation.

Created:

- `wiki/chapter-18-on-continued-fractions.md` — chapter summary covering eight movements: definitions; convergent recurrence and alternation; continued fraction → alternating series; alternating series → continued fraction with templates and famous examples; failure of the converse; periodic CFs and quadratic irrationals; quadratic-equation roots; rational CFs = Euclidean algorithm; best rational approximations.
- `wiki/continued-fraction.md` — §357: the two forms (simple, with numerators $1$; generalised, with arbitrary numerators); positioning as the "third kind of infinite expression" alongside series and products; Euler's §356 prediction of expanded future use.
- `wiki/convergents-of-a-continued-fraction.md` — §358–§362: the truncation table; three-term recurrence $N_k = b_k N_{k-1} + \beta_k N_{k-2}$ for numerators and denominators with the $1/0$ prefix; alternation of convergents around the true value; §363 differences identity.
- `wiki/continued-fraction-series-equivalence.md` — §363–§373: telescoping convergent-differences gives $z = a + \alpha/P - \alpha\beta/(PQ) + \alpha\beta\gamma/(QR) - \cdots$ (§363); inverse problem solved by free choice of partial denominators (§365–§367); four named templates (§368, §369, §370, §371–§373) yielding integer-, reciprocal-, product-, and power-series-form CFs; §374–§375 asymmetry note.
- `wiki/brouncker-formula.md` — §369 Example II: derivation of $4/\pi = 1 + 1/(2 + 9/(2 + 25/(2 + \cdots)))$ from the Leibniz series via Template II; Euler's explicit attribution to Brouncker; historical note on the 1655 communication to Wallis; convergence comparison with Machin's formula.
- `wiki/continued-fraction-for-log-2.md` — §369 Example I: $\log 2 = 1/(1 + 1/(1 + 4/(1 + 9/(1 + \cdots))))$ derived from the alternating-harmonic series via Template II; partial numerators $1, 1, 4, 9, 16, 25, \ldots$
- `wiki/continued-fraction-for-e.md` — §381 Example III: Euler's empirical discovery that $(e - 1)/2 = [0; 1, 6, 10, 14, 18, 22, 26, 30, 34, \ldots]$ has partial quotients in arithmetic progression; the more familiar modern interleaved form $e = [2; 1, 2, 1, 1, 4, 1, 1, 6, 1, \ldots]$; significance for irrationality and the empirical-then-analytic style of Euler.
- `wiki/periodic-continued-fractions.md` — §376–§379: periodic CFs = quadratic irrationals (one direction of Lagrange's theorem before Lagrange); single-letter period gives $\sqrt{a^2 + 4}$ catalog $\sqrt 5, \sqrt 2, \sqrt{13}, \sqrt 5, \sqrt{29}, \sqrt{10}, \sqrt{53}$; two-letter period extends to all square roots ($\sqrt 7 \approx 2024/765$ with error $< 3/10^7$); three- and four-letter periods reduce back to two-letter.
- `wiki/euclidean-algorithm-continued-fraction.md` — §381: rational $A/B$'s continued fraction = Euclidean-algorithm quotients; finite iff input is rational; worked example $1461/59 = [24; 1, 3, 4, 1, 2]$; algorithm applied to decimals recovers $\sqrt 2 = [1; 2, 2, 2, \ldots]$ (Example II) and discovers AP pattern for $(e-1)/2$ (Example III).
- `wiki/best-rational-approximations.md` — §382: Wallis's principle that convergents are best rationals with bounded denominator; $\pi$'s convergents $3/1, 22/7, 333/106, 355/113, 103993/33102$ (Archimedean, Metian); solar-year convergents $1/4, 7/29, 8/33, \ldots, 181/747$ giving the Julian rule and motivating the Gregorian compromise $97/400$. Book closes.

Modified:

- `wiki/index.md` — added chapter-18 summary line and "From Chapter 18" concept section with nine entries.

## 2026-05-11 — Lint fixes

Created:

- `wiki/vietas-formulas.md` — concept page for the coefficient ↔ elementary-symmetric-function dictionary. The recurring tool that Euler uses (without naming Vieta) across Chapters 1, 9, 10, and 14. Previously a load-bearing concept with no dedicated page.

Modified:

- `wiki/basel-problem.md` — added `chapter15.pdf` to Sources (the "Re-derivation via primes (Chapter 15)" section was already there); bumped Last updated to 2026-05-11.
- `wiki/zeta-at-even-integers.md` — added `chapter15.pdf` to Sources (the "Re-derivation via primes (Chapter 15)" section was already there); bumped Last updated to 2026-05-11.
- `wiki/chapter-13-on-recurrent-series.md` — added `chapter17.pdf` to Sources (the "Inverse application in Chapter 17" section was already there); bumped Last updated to 2026-05-11.
- `wiki/arctangent-series.md`, `wiki/circular-arc-series.md`, `wiki/wallis-product.md`, `wiki/logarithmic-series.md` — bumped Last updated to 2026-05-11 to reflect chapter-15 cross-link additions.
- `wiki/single-valued-and-multi-valued-functions.md`, `wiki/trig-values-as-roots.md`, `wiki/multiple-angle-polynomials.md`, `wiki/sine-cosine-factored-products.md`, `wiki/trig-multiple-angle-partial-fractions.md`, `wiki/de-moivre-formula.md` — linked existing "Vieta" mentions to `vietas-formulas`; added to related-pages list where appropriate.
- `wiki/index.md` — added `vietas-formulas` under "From Chapter 1".
