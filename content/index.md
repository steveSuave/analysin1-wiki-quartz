# Wiki Index

Table of contents for the *Introductio in analysin infinitorum* wiki.

## Chapter summaries

- [[chapter-1-on-functions-in-general]] — Euler's definitional chapter: variables, functions, and their classification.
- [[chapter-2-on-the-transformation-of-functions]] — factoring polynomials and partial-fraction decomposition.
- [[chapter-3-on-the-transformation-of-functions-by-substitution]] — removing radicals, and rational parametrizations via $y = xz$.
- [[chapter-4-on-the-development-of-functions-in-infinite-series]] — expansion of rational and irrational functions as infinite series.
- [[chapter-5-on-functions-of-two-or-more-variables]] — several independent variables; homogeneous functions and the $y = uz$ reduction.
- [[chapter-6-on-exponentials-and-logarithms]] — first transcendental functions: $a^z$, $\log y$, transcendence of logs, geometric-mean tables, characteristic and mantissa.
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]] — power series for $a^z$ and $\log(1+x)$ via $\omega$ infinitesimal and $j$ infinite; definition of $e$.
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]] — sine/cosine on the unit circle, De Moivre, the trig power series, $e^{iv} = \cos v + i\sin v$, the arctangent series, fast computation of $\pi$.
- [[chapter-9-on-trinomial-factors]] — constructive real factorization via $p^2 - 2pqz\cos\phi + q^2z^2$; cyclotomic factorization of $a^n \pm z^n$; infinite products for $\sin z$, $\cos z$, $e^x \pm e^{-x}$.
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]] — Newton's identities applied to the Chapter 9 products: Basel problem, even-zeta values, character-style series, partial-fraction expansions of cot, csc, coth, csch.
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]] — linear-factor sine/cosine products at rational angles; Wallis product; log $\pi$ and log sin/cos by transposing double sums whose columns are even-zeta values.
- [[chapter-12-on-the-development-of-real-rational-functions]] — extension of partial-fraction decomposition to real quadratic ([[trinomial-factor]]) denominators; iterative algorithm for repeated quadratic factors.
- [[chapter-13-on-recurrent-series]] — closed-form general term and sum of any [[recurrent-series|recurrent series]] from real partial fractions; De Moivre's [[scale-of-the-relation|scale of the relation]] and its inversion.
- [[chapter-14-on-the-multiplication-and-division-of-angles]] — multiple-angle polynomials for sin/cos; factored products $\sin nz = 2^{n-1}\sin z\cdots$; partial-fraction sums for csc, sec, cot, tan at equally-spaced angles; tangent of multiple angles via De Moivre; sums of trig functions in arithmetic progression (infinite and finite); inversion to powers of sin/cos as multiple-angle sums.
- [[chapter-15-on-series-which-arise-from-products]] — products $\prod(1\pm\alpha_i z)^{\pm 1}$ over primes give squarefree, Möbius, and Euler-product series; $\sum 1/p = \infty$ via logs at $n=1$; numerical table of $\sum 1/p^n$; prime-classified series for $\pi/4$, $\pi/2$, $\pi/(2\sqrt 2)$, $\pi/(3\sqrt 3)$ via the sieve of Eratosthenes lifted to series level.
- [[chapter-16-on-the-partition-of-numbers]] — partitions of integers via the products $\prod(1+x^{\alpha_i}z)$ (distinct parts) and $1/\prod(1-x^{\alpha_i}z)$ (with repetition); recurrent series for the column generating functions with triangular numerators; the Pascal-like recurrence $p_m(n) = p_{m-1}(n) + p_m(n-m)$ for the partition table; Euler's pentagonal number theorem $\prod(1-x^k) = \sum(-1)^n x^{n(3n-1)/2}$; distinct = odd identity; uniqueness of binary and balanced-ternary representations.
- [[chapter-17-using-recurrent-series-to-find-roots-of-equations]] — Daniel Bernoulli's method: from $x^m - \alpha x^{m-1} - \beta x^{m-2} - \cdots = 0$, run a recurrent series with [[scale-of-the-relation|scale]] $\alpha, \beta, \gamma, \ldots$; the ratio $Q/P$ converges to the largest root in absolute value. Substitution shift $x = y + k$ makes the method universal; failure modes (close roots, $\pm p$ pairs, repeated roots); §348–§352 closed-form recovery of modulus and argument of a dominant complex pair from four consecutive coefficients; §354 geometric-progression interpretation; §355 partial application to transcendental equations.
- [[chapter-18-on-continued-fractions]] — the third kind of infinite expression; convergent three-term recurrence and alternation; bidirectional dictionary with alternating series giving Brouncker's $4/\pi$, a CF for $\log 2$, and the celebrated $(e-1)/2 = [0; 1, 6, 10, 14, 18, \ldots]$ with arithmetic-progression quotients; periodic CFs = quadratic irrationals; rational CFs = Euclidean algorithm; best-rational-approximation principle applied to $\pi \approx 355/113$ and to the Gregorian leap-year rule.

## Concepts

### From Chapter 1

- [[function]] — Euler's "analytic expression" definition.
- [[variable-and-constant]] — notation and the scope of a variable (including complex numbers).
- [[classification-of-functions]] — algebraic vs. transcendental, polynomial/rational/irrational.
- [[single-valued-and-multi-valued-functions]] — n-valued functions and Vieta-style relations.
- [[vietas-formulas]] — coefficient ↔ elementary-symmetric-function dictionary; the workhorse identification used in Chapters 1, 9, 10, 14.
- [[even-and-odd-functions]] — parity and its multiplicative rules.
- [[similar-functions]] — Euler's template notion of "the same function of different variables."

### From Chapter 2

- [[factoring-polynomials]] — linear/quadratic factors, roots, leading-coefficient form.
- [[fundamental-theorem-of-algebra]] — Euler's §32 claim that every real polynomial factors into real linear and quadratic factors.
- [[complex-conjugate-factors]] — pairing complex linear factors into real quadratics.
- [[intermediate-value-property]] — Euler's informal IVT for polynomials.
- [[real-roots-by-degree-parity]] — existence of real roots from degree parity and constant-term sign.
- [[improper-rational-function]] — polynomial-part-plus-proper-remainder split.
- [[partial-fraction-decomposition]] — the §39–§46 algorithm, with the cover-up shortcut and repeated-factor tower.

### From Chapter 3

- [[substitution]] — the technique: introduce a new variable $x$ defining both $y$ and $z$.
- [[rationalizing-substitutions]] — §47–§51 catalog of substitutions that remove radicals.
- [[rational-parametrization-of-the-circle]] — the §46/§50 half-angle parametrization.
- [[homogeneous-substitution]] — the §52–§58 $y = xz$ (or $y = x^m z^n$) trick.
- [[folium-of-descartes]] — Euler's §52 worked example: $y^3 + z^3 = cyz$ parametrized rationally.

### From Chapter 4

- [[geometric-series]] — §60: the series for $a/(\alpha + \beta z)$.
- [[method-of-undetermined-coefficients]] — §60–§61: positing a series and matching powers of $z$.
- [[recurrent-series]] — §62–§70: De Moivre's recurrent series, law read off the denominator.
- [[higher-order-arithmetic-progressions]] — §64–§67: progressions with constant $k$-th differences as $(1-z)^{k+1}$-recurrent series.
- [[binomial-series]] — §71–§76: Newton's $(P + Q)^{m/n}$ theorem and its recurrent form.

### From Chapter 5

- [[functions-of-several-variables]] — §77–§82: independent variables, the old classification carried over, the equation-counting rule.
- [[implicit-function-and-equation-counting]] — §82: relations define variables implicitly; each independent equation removes one degree of freedom.
- [[homogeneous-function]] — §83–§91: degree of multivariate functions; Euler's $y = uz$ reduction $V = z^n f(u)$; linear factorization of bivariate homogeneous polynomials.
- [[heterogeneous-function]] — §92–§93: bifid, trifid, and reduction to homogeneity by substitution.
- [[order-of-a-polynomial]] — §94: the greatest degree of any term, used to classify algebraic curves.
- [[reducible-polynomial]] — §94–§95: order of a polynomial and reducibility into non-irrational factors.

### From Chapter 6

- [[exponential-function]] — §96–§101: $a^z$ defined by extension from integers to reals; canonical case $a > 1$.
- [[logarithm]] — §102–§104: inverse of $a^z$; the four algebraic rules.
- [[transcendence-of-logarithms]] — §105: logs of "generic" rationals are transcendental.
- [[geometric-mean-method-for-logarithms]] — §106: iterated $\sqrt{AB}$ algorithm used by Briggs and Vlacq.
- [[change-of-base]] — §107–§108: a single multiplicative constant converts any log table to any other base.
- [[common-logarithm]] — §112: base-10 logs and their special role in decimal computation.
- [[characteristic-and-mantissa]] — §112–§113: integer/fractional split of base-10 logs; digit count from characteristic, digit string from mantissa.

### From Chapter 7

- [[infinitesimal-and-infinite-numbers]] — Euler's working device: $\omega$ infinitely small, $j$ infinitely large, $j\omega = z$ finite; the collapse $(j-m)/(nj) = 1/n$.
- [[exponential-series]] — §115–§117: $a^z = \sum (kz)^n/n!$ from $(1 + kz/j)^j$; the general $b^z$ via $\log b$.
- [[logarithmic-series]] — §118–§121: $\log(1+x) = (1/k)(x - x^2/2 + \cdots)$, the §120 divergence paradox at $a = 10$, and the fast-converging $\log\frac{1+x}{1-x}$ variant.
- [[eulers-number]] — §122: the base for which $k = 1$, giving $e = \sum 1/n! = 2.71828\ldots$ — first appearance of the symbol $e$.
- [[natural-logarithm]] — §123–§125: $\log_e$, the integer table to twenty digits, and $k = \log_e a$ as the universal change-of-base factor.

### From Chapter 8

- [[pi]] — §126: the symbol $\pi$ enters notation; 113-digit decimal of half the unit circumference.
- [[sine-and-cosine]] — §127: definitions on the unit circle, special values, Pythagorean identity, co-function relations, tangent and cotangent.
- [[trigonometric-addition-formulas]] — §128, §130, §131: sum/difference, periodicity catalog, product-to-sum, sum-to-product, half-angle.
- [[trigonometric-recurrent-progression]] — §129: arcs in arithmetic progression have sines and cosines forming a recurrent series with denominator $1 - 2\cos y\cdot Z + Z^2$.
- [[de-moivre-formula]] — §132–§133: $(\cos z \pm i\sin z)^n = \cos nz \pm i\sin nz$; binomial expansions of $\cos nz$ and $\sin nz$.
- [[sine-and-cosine-series]] — §134: $\cos v = \sum (-1)^k v^{2k}/(2k)!$, $\sin v = \sum (-1)^k v^{2k+1}/(2k+1)!$ from De Moivre under $z$ infinitesimal, $n$ infinite, $nz = v$ finite.
- [[eulers-formula]] — §138: $e^{iv} = \cos v + i\sin v$; sines and cosines as complex exponentials.
- [[arctangent-series]] — §139–§141: $z = (1/2i)\log\frac{1+i\tan z}{1-i\tan z}$, $\arctan t = t - t^3/3 + t^5/5 - \cdots$, Leibniz $\pi/4$, $\pi$ from $\arctan(1/\sqrt 3)$.
- [[machin-like-formula]] — §142: $\pi/4 = \arctan(1/2) + \arctan(1/3)$ for fast rational computation of $\pi$.

### From Chapter 9

- [[trinomial-factor]] — §144–§146: real quadratic factor $p^2 - 2pqz\cos\phi + q^2z^2$ from a complex linear conjugate pair.
- [[factorization-of-an-plus-minus-zn]] — §150–§153: cyclotomic factorization of $a^n + z^n$, $a^n - z^n$, and $a^{2n} - 2a^n z^n\cos g + z^{2n}$.
- [[exponential-infinite-product]] — §155–§157: infinite products for $e^x - 1$, $(e^x - e^{-x})/2$, $(e^x + e^{-x})/2$ from $(1 + x/j)^j$.
- [[sine-infinite-product]] — §158: $\sin z = z\prod(1 - z^2/k^2\pi^2)$ from $x = iz$ in the §156 product.
- [[cosine-infinite-product]] — §158: $\cos z = \prod(1 - 4z^2/(2k+1)^2\pi^2)$ from $x = iz$ in the §157 product.

### From Chapter 10

- [[newtons-identities]] — §165–§166: the recurrence $P = A$, $Q = AP - 2B$, $R = AQ - BP + 3C$, $\ldots$ converting elementary symmetric coefficients into power sums.
- [[basel-problem]] — §167: $\sum 1/k^2 = \pi^2/6$ via the [[exponential-infinite-product|sinh product]] and Newton's identities.
- [[zeta-at-even-integers]] — §167–§169: tabulation of $\zeta(2k)$ as a rational multiple of $\pi^{2k}$ through $\zeta(26)$; sums over odd squares from the [[cosine-infinite-product|cosh product]].
- [[odd-and-alternating-zeta-decomposition]] — §170: $M$, $M/2^n$, $M - M/2^n$, $M - 2M/2^n$ — the elementary algebra giving even, odd, and alternating restrictions.
- [[circular-arc-series]] — §171–§180: applying Newton's identities to the [[chapter-9-on-trinomial-factors|§164]] arc-form products yields the Leibniz $\pi/4$ family and a vast catalog of character-style sums.
- [[cotangent-partial-fraction]] — §181–§183: partial-fraction expansions of $\pi\cot(\pi\sqrt a)$, $\pi/\sin(\pi\sqrt a)$ and their hyperbolic counterparts.

### From Chapter 11

- [[linear-factors-of-sine-cosine]] — §184: the §158 sine/cosine products at $z = m\pi/(2n)$ split each quadratic factor as $(kn-m)/kn\cdot(kn+m)/kn$; co-function identity gives a second product per function.
- [[wallis-product]] — §185: $\pi/2 = (2\cdot 2\cdot 4\cdot 4\cdot 6\cdot 6\cdots)/(1\cdot 3\cdot 3\cdot 5\cdot 5\cdot 7\cdots)$ from dividing the two §184 expressions, plus parametric variants for $\sqrt 2$ and others.
- [[trig-infinite-products]] — §186–§187: linear-factor infinite products for $\tan, \cot, \sec, \csc$ as quotients; ratio formulas for $\sin(m\pi/2n)/\sin(k\pi/2n)$.
- [[log-pi-via-products]] — §188–§190: $\log\pi = \log 4 - (A-1) - (B-1)/2 - \cdots$ via taking logs of the Wallis product, expanding by [[logarithmic-series|§118]], and transposing.
- [[log-sine-via-products]] — §191–§198: $\log\sin(m\pi/2n)$ and $\log\cos(m\pi/2n)$ by the same transposition, sharing the table $A, B, C, \ldots$ and $\alpha, \beta, \gamma, \ldots$ with $\log\pi$; §197 fast tan/cot via the [[cotangent-partial-fraction|§181 partial fraction]].

### From Chapter 12

- [[real-partial-fraction-decomposition]] — §199–§210: real partial fractions for a rational function with real quadratic factors $p^2 - 2pqz\cos\phi + q^2z^2$ in the denominator; closed-form coefficients via [[de-moivre-formula|De Moivre]] substitution at the complex roots; iterative tower for repeated quadratic factors.

### From Chapter 13

- [[general-term-of-recurrent-series]] — §211–§223: closed-form coefficient of $z^n$ via real partial fractions; linear-factor brick $A/(1-pz)^k$ gives binomial-times-power, quadratic-factor brick gives $\sin(n+1)\phi/\sin\phi$.
- [[scale-of-the-relation]] — §224: De Moivre's name for the recurrence multipliers $\alpha, \beta, \gamma, \ldots$; equivalent to the (sign-flipped) denominator of the generating rational function.
- [[closed-form-two-term-recurrence]] — §226–§229: Binet-type $X_n = Up^n + Vq^n$ for two-member scales; the invariant $UV = (B^2 - \alpha AB + \beta A^2)/(4\beta - \alpha^2)$; term from a single predecessor by an "illusory" square root.
- [[sum-of-recurrent-series]] — §231–§233: infinite sum equals the generating rational function; partial sum collapses to first/last terms only for two-member scales.

### From Chapter 14

- [[multiple-angle-polynomials]] — §234–§238, §243: recurrence-generated tables for $\sin nz$ and $\cos nz$; pure polynomial in $\sin z$ for odd $n$; residual $\sqrt{1-x^2}$ factor for even $n$; Chebyshev polynomials in disguise.
- [[trig-values-as-roots]] — §235–§256: the $n$ roots of the multiple-angle polynomial are trig functions at equally-spaced angles; Vieta's formulas generate all partial-fraction and product identities.
- [[sine-cosine-factored-products]] — §237, §240–§245: $\sin nz = 2^{n-1}\sin z\cdot\sin(\pi/n - z)\sin(\pi/n + z)\cdots$; unified formula for odd and even $n$; matching cosine products.
- [[trig-multiple-angle-partial-fractions]] — §237, §246–§256: $n/\sin nz$, $n\cot nz$, $n\sec nz$, $n\csc nz$ each as a sum of $n$ same-function evaluations at shifted angles; tangent/cotangent products from De Moivre.
- [[sum-of-trig-in-ap]] — §258–§260: closed-form for the infinite sum $\sin a + \sin(a+b) + \cdots = (\sin a - \sin(a-b))/(2-2\cos b)$ via the recurrent-series generating function at $z = 1$, plus the standard finite-AP formula by subtracting the tail.
- [[powers-of-sine-and-cosine]] — §261–§263: inversion of the multiple-angle expansion: $(\sin z)^n$ and $(\cos z)^n$ as binomial-weighted finite sums of $\sin kz$, $\cos kz$.

### From Chapter 15

- [[euler-product-formula]] — §270–§277, §283–§284: $\sum 1/k^n = \prod_p (1-1/p^n)^{-1}$, derived both by expanding the reciprocal product (unique factorisation) and by an Eratosthenes-style sieve on the series; reciprocal Möbius relation.
- [[squarefree-and-mobius-series]] — §267–§269: $\prod(1+1/p^n) = \sum_{k\text{ squarefree}}1/k^n$; the negative-factor version is the Möbius-signed series $\sum \mu(k)/k^n = 1/\zeta(n)$.
- [[divergence-of-prime-reciprocals]] — §278–§280: $\sum 1/p = \infty$ via logarithm of the Euler product at $n = 1$; quantitative refinement of Euclid's theorem.
- [[prime-zeta-values]] — §281–§282: numerical table of $\sum 1/p^n$ for even $n = 2$ to $36$ to 12-digit precision, obtained by inverting the §278 identity.
- [[prime-sign-series-for-pi]] — §285–§296: catalogue of series and products for $\pi/4$, $\pi/2$, $\pi^3/32$, $\pi/(3\sqrt 3)$, $\pi/(2\sqrt 2)$ with signs based on prime residues mod 4, mod 6, mod 8 — the Dirichlet $L$-functions of small conductor in Euler-product form, a century before Dirichlet.

### From Chapter 16

- [[partition-of-numbers]] — §297–§331: the central concept of integer partitions; distinct vs. unrestricted; notation $p(n), p_m(n), q(n), q_m(n)$; index of the chapter's theorems.
- [[partition-generating-functions]] — §297–§315: bivariate products $\prod(1+x^{\alpha_i}z)$ and $1/\prod(1-x^{\alpha_i}z)$ enumerating partitions by part-count $z^m$ and size $x^n$; functional-equation derivation of the closed-form $P_m$ with triangular-number numerators.
- [[partitions-into-distinct-parts]] — §299–§315: $q_m(n)$ generating function, recurrent series $x^{m(m+1)/2}/\prod_{k=1}^m(1-x^k)$, the **staircase bijection** $q_m(n) = p_m(n - m(m-1)/2)$.
- [[partition-recurrence]] — §316–§318: the Pascal-like rule $p_m(n) = p_{m-1}(n) + p_m(n-m)$ by which Euler's partition table is filled column by column.
- [[eulers-pentagonal-number-theorem]] — §323–§324: $\prod(1-x^k) = \sum(-1)^n x^{n(3n-1)/2}$; the induced $O(\sqrt n)$-term recurrence for $p(n)$; Euler's empirical discovery (no proof in the *Introductio*).
- [[distinct-parts-equals-odd-parts]] — §325–§327: $\prod(1+x^k) = \prod 1/(1-x^{2k-1})$ via the one-line identity $PQ = \prod(1-x^{2k})$; partitions of $9$ as worked example; computation of $q(n)$ from $p(n)$.
- [[binary-representation-theorem]] — §328–§329: $\prod(1+x^{2^k}) = 1/(1-x)$ by fixed-point/functional equation; uniqueness of binary; weighing with $1, 2, 4, 8, \ldots$-pound weights.
- [[balanced-ternary-representation]] — §330–§331: $\prod(x^{-3^k}+1+x^{3^k}) = \sum_{n\in\mathbb Z}x^n$; every integer is uniquely a signed sum of distinct powers of $3$ with digits $\{-1, 0, +1\}$; two-pan balance weighing.

### From Chapter 17

- [[bernoullis-method-for-roots]] — §332–§347, §354–§355: from the equation's coefficients form a recurrent series with [[scale-of-the-relation|scale]] $\alpha, \beta, \gamma, \ldots$; ratio $Q/P$ of consecutive coefficients converges to the largest root in absolute value; substitution shift $x = y + k$ makes any root findable as the smallest of a transformed equation; failure modes (close roots, $\pm p$ pairs, repeated roots); §354 geometric-progression interpretation; §355 partial application to $\sin z = 1/2$.
- [[trinomial-factor-from-recurrent-series]] — §348–§353: when the dominant pole is a complex conjugate pair, $Q/P$ oscillates; Euler eliminates the unknowns and the index to recover $p = \sqrt{(R^2 - QS)/(Q^2 - PR)}$ and $\cos\phi = (QR - PS)/(2\sqrt{(Q^2-PR)(R^2-QS)})$ from four consecutive coefficients, giving both modulus and argument of the dominant complex pair.

### From Chapter 18

- [[continued-fraction]] — §357: the two forms (numerators all $1$, or arbitrary $\alpha, \beta, \gamma, \ldots$); the third kind of infinite expression after series and products.
- [[convergents-of-a-continued-fraction]] — §358–§362: three-term recurrence $N_k = b_k N_{k-1} + \beta_k N_{k-2}$ shared by numerators and denominators; the $1/0$ prefix; alternation of truncations around the true value.
- [[continued-fraction-series-equivalence]] — §363–§373: telescoping difference of convergents gives the alternating series $a + \alpha/P - \alpha\beta/(PQ) + \alpha\beta\gamma/(QR) - \cdots$; inverse templates converting alternating series back into CFs via free choice of partial denominators.
- [[brouncker-formula]] — §369 Example II: $4/\pi = 1 + 1^2/(2 + 3^2/(2 + 5^2/(2 + \cdots)))$, the first CF for $\pi$ in history, recovered as a special case of the §369 reciprocal-series template applied to the Leibniz series.
- [[continued-fraction-for-log-2]] — §369 Example I: $\log 2 = 1/(1 + 1/(1 + 4/(1 + 9/(1 + \cdots))))$, partial numerators $1, 1, 4, 9, 16, 25, \ldots$ from the alternating-harmonic series.
- [[continued-fraction-for-e]] — §381 Example III: $(e - 1)/2 = [0; 1, 6, 10, 14, 18, 22, \ldots]$, partial quotients in arithmetic progression with common difference $4$ — Euler's empirical discovery from the Euclidean algorithm on a 13-digit decimal.
- [[periodic-continued-fractions]] — §376–§379: periodic simple CFs satisfy quadratic equations, so represent quadratic irrationals; single-letter periods give $\sqrt{a^2 + 4}$; two-letter periods extend the method to all square roots; $\sqrt 7 \approx 2024/765$ with error $< 3/10^7$.
- [[euclidean-algorithm-continued-fraction]] — §381: rational $A/B$'s CF expansion = Euclidean-algorithm quotients of $A$ and $B$; applied to decimals it produces the CF of an irrational; recovers the $\sqrt 2$ pattern of §376 and discovers the AP pattern for $e$.
- [[best-rational-approximations]] — §382: Wallis's principle that the convergents are the best rational approximations with bounded denominator; $\pi \to 22/7, 333/106, 355/113$ (the famous *Metian* ratio); the solar-year computation yielding the Julian $1/4$ and Gregorian $97/400$ leap-day rules.
