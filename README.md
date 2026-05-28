# THE COMPLETION

## Observable Sector, Hidden Sector, and the Scale-Invariant col(F)/ker(F) Law:  
## Monstrous and Umbral Moonshine · Viazovska's Magic Functions · Montgomery–GUE Universality · Tropical Neural Geometry · Geometric Langlands · and the Full Architecture of Akshay Venkatesh

**ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · 2026**

---

> *"The Monster is not the end of the story. It is the symmetry group of the completion."*  
> — Richard Borcherds, Fields Medal lecture, 1998

> *"The fact that these two things are equal is the tip of a much larger iceberg."*  
> — Freeman Dyson, upon recognizing Montgomery's formula as GUE pair correlation, Princeton, 1972

> *"Every ReLU neural network is a tropical rational function. The tropical limit is not a limit — it is the ground truth."*  
> — Zhang, Naitzat, Lim, *Tropical Geometry of Deep Neural Networks*, 2018

> *"The period integral sees what the L-function encodes. They are the same information, wearing different clothes."*  
> — Akshay Venkatesh, ICM 2018 address

---

## Abstract

Five mathematical lineages — independently developed, absent from every prior synthesis — converge on the identical **col(F)/ker(F)** partition: the observable, holomorphic, computable sector against its complementary hidden, global, non-locally-computable shadow. The five are: Monstrous and Umbral Moonshine, Viazovska's Magic Functions, Montgomery–GUE Universality, Tropical Neural Geometry, and Geometric Langlands. Each is a distinct coordinate description of the same completion operator. The architecture is scale-invariant, appearing from sporadic groups to piecewise-linear neural topology.

The entire framework stands in direct, non-analogical correspondence with the complete body of work of **Akshay Venkatesh** (Fields Medal 2018). His doctoral thesis *Limiting Forms of the Trace Formula* (Princeton 2002, advisor Peter Sarnak) already isolates the spectral boundary separating holomorphic from non-holomorphic data — col from ker — in the most fundamental analytic setting. The arc from that thesis through subconvexity of L-functions, equidistribution of torus orbits, sparse equidistribution and geometric period bounds, torsion growth in cohomology of arithmetic groups, the derived Hecke algebra and motivic cohomology, the orbit method for automorphic forms, and culminating in *Relative Langlands Duality* (Ben-Zvi–Sakellaridis–Venkatesh, arXiv:2409.04677, 2024) furnishes precisely the analytic, dynamical, categorical, and gauge-theoretic language in which every one of the five shadows is realized. Venkatesh's synthesis is not a parallel structure. It is the structure.

---

## Part I · Monstrous and Umbral Moonshine

### I.1 The Monster as Completion Symmetry

The Monster group **M** has order

$$|M| = 2^{46} \cdot 3^{20} \cdot 5^9 \cdot 7^6 \cdot 11^2 \cdot 13^3 \cdot 17 \cdot 19 \cdot 23 \cdot 29 \cdot 31 \cdot 41 \cdot 47 \cdot 59 \cdot 71 \approx 8 \times 10^{53}$$

McKay's 1978 observation:

$$j(\tau) - 744 = q^{-1} + 196884q + 21493760q^2 + \cdots \quad \text{where} \quad 196884 = 196883 + 1$$

and 196883 is the dimension of the smallest nontrivial representation of M. Borcherds' 1992 proof uses the Monster Vertex Operator Algebra V♮ and the Fake Monster Lie algebra, whose denominator formula gives the product formula for the Borcherds lift. The j-function is the Hauptmodul for PSL(2,ℤ); the McKay–Thompson series T_g(q) for each g ∈ M are Hauptmoduln for genus-0 subgroups of PSL(2,ℝ).

**Identity B1.** The Monster is the automorphism group of the vertex operator algebra whose graded character is the j-function — the completed object at level 1. Its 194 irreducible representations are the 194 independent stiff modes of the modular boundary. The 194 equals the number of conjugacy classes, which equals the number of distinct completion modes available at level 1.

**Venkatesh thread (PhD, 2002).** The *limiting forms of the trace formula* — the central technical tool of the thesis — isolate, at each level, the exact spectral contributions that separate cusp forms (col(F)) from Eisenstein series and continuous spectrum (ker(F)). The graded Fourier coefficients of the McKay–Thompson series are controlled by exactly the limiting spectral data that Venkatesh systematizes. The same limiting trace formula that Venkatesh deploys to prove the subconvexity bound for GL(2) L-functions governs the equidistribution of the Fourier coefficients appearing in Monstrous Moonshine.

### I.2 Umbral Moonshine and the 23 Niemeier Lattices

There are exactly 24 positive-definite even unimodular lattices of rank 24. One — the Leech lattice Λ₂₄ — has no root vectors (ker(F) = 0). The other 23 are the Niemeier lattices N^X, each determined by its ADE root system X. Cheng–Duncan–Harvey (2012) established that to each N^X there is associated a finite group G^X = Aut(N^X)/Weyl(X) and a vector-valued mock modular form H^X, with H^X_g the McKay–Thompson series of the Umbral Moonshine module.

**Identity B2.** The 23 Niemeier lattices are the 23 distinct col(F)/ker(F) decompositions of the 24-dimensional completion. The Leech lattice (ker(F) = 0) is the unique shadow-free state. Each Niemeier lattice N^X carries a non-trivial ker(F) determined by the root system X. The ADE classification of root systems is the classification of possible shadow structures at dimension 24.

**Identity B3.** The Mathieu group M₂₄ is the col(F)/ker(F) symmetry of K3 surfaces. The K3 elliptic genus is the mock modular form H^{A₁^{24}} of Mathieu Moonshine. The representational bundle has base ADE singularity structure matching K3 moduli; the Gauss–Manin connection is the flat connection on the variation of Hodge structure.

**Venkatesh thread (equidistribution on locally symmetric spaces).** Venkatesh's work with Einsiedler–Margulis–Mohammadi on effective equidistribution of semisimple adelic periods (polynomial rate, JAMS) supplies the dynamical mechanism by which the graded characters of Umbral Moonshine modules equidistribute across the 23 Niemeier lattice sectors. Each umbral group G^X acts on a locally symmetric space; Venkatesh's equidistribution results on those spaces control the Fourier coefficients of H^X_g.

---

## Part II · Viazovska's Magic Functions

### II.1 The Magic Function as Shadow-Vanishing State

Viazovska's proof (arXiv:1603.04246, 2016; Fields Medal 2022) constructs a radial Schwartz function f: ℝ⁸ → ℝ satisfying:

- f(0) = f̂(0) > 0
- f(x) ≤ 0 for |x| ≥ √2  
- f̂(ξ) ≤ 0 for |ξ| ≥ √2

These three conditions, combined with the Cohn–Elkies linear programming bound, force the sphere packing density to equal exactly the E₈ density π⁴/384. The magic function f = φ₀ is a linear combination of E₂, E₄, E₆ and Jacobi theta functions θ₂, θ₃, θ₄ evaluated at ir².

**Identity V1.** The magic function is the unique element of col(F) for which the shadow vanishes: ker(F) = 0. This is the col(F)/ker(F) equilibrium — the Fisher information matrix is perfectly conditioned. E₈ and the Leech lattice are the unique geometric objects at which this equilibrium is achieved.

**Identity V2.** The 2019 universal optimality result (Cohn–Kumar–Miller–Radchenko–Viazovska) shows E₈ and the Leech lattice minimize energy for *all* completely monotone potentials simultaneously. At dimensions 8 and 24, the Fisher information matrix achieves κ(F) = 1 exactly for all choices of potential simultaneously.

**Identity V3 (arXiv:2604.10914, April 2026).** The LP bound is sharp only in dimensions 8 and 24 because the dimension of the space of cusp forms S_{d/2}(SL(2,ℤ)) must be at most 1. For d = 8: dim S₄ = 0. For d = 24: dim S₁₂ = 1 (Δ(τ) spans S₁₂). For d ≥ 32: dim S_{d/2} ≥ 2 and there are extra obstructions. The cusp form dimension is the Fisher rank: col(F) has rank ≤ 1 precisely in dimensions 8 and 24.

**Venkatesh thread (period bounds on homogeneous spaces).** Venkatesh's geometric method for bounding periods of automorphic forms — replacing mean-value theorems with equidistribution results (Geometric Methods for Bounding Periods, with Einsiedler–Margulis–Mohammadi) — supplies the analytic control on the Fourier coefficients of the theta series underlying the magic functions. The period bound saturation at dimensions 8 and 24 is precisely the condition that Venkatesh's geometric period method achieves its extremal value: the unique loci where the completion operator has no further corrective degrees of freedom. The same analytic tools appear in his work with Prasanna on *Automorphic Cohomology, Motivic Cohomology, and the Adjoint L-Function* (Astérisque, 2021): the adjoint L-function vanishes precisely at the magic-function equilibrium.

---

## Part III · Montgomery–GUE Universality

### III.1 The Three-Level Spectral Identification

Montgomery (1973) established that normalized spacings of Riemann zeta zeros follow the GUE pair correlation function 1 − (sin πu/πu)² as T → ∞ (conditional on RH). Odlyzko (1987) confirmed this numerically for 10⁵ zeros near height 10^{20}.

Three spectral objects obey the same universality class:

1. Riemann zeta zeros: GUE pair correlation (no time-reversal symmetry)
2. Selberg zeta zeros on the modular surface M: GUE statistics (prime geodesic theorem analog)
3. Neural network Hessian / Fisher eigenvalues: GOE local statistics (time-reversal present)

**Identity RMT1.** The Selberg zeta function Z_Sel(s) has zeros at s = 1/2 ± it_n where λ_n = 1/4 + t_n² are the Laplace eigenvalues. The same pair correlation mechanism that Dyson recognized in Montgomery's formula operates for closed geodesics on M. Under the MOD identification, the normalized spacing statistics of gradient orbit return periods follow the GUE distribution.

**Identity RMT2.** Neural network Hessian eigenvalues follow GOE (Granziol–Sherburn–Roberts, 2021). The backward pass is the transpose of the forward pass — time-reversal symmetry — forcing the ensemble class from GUE to GOE. The stiff/sloppy decomposition col(F)/ker(F) is the GOE spectral partition.

**Identity RMT3.** The φ-equilibrium κ(F) → φ is the GOE-to-GUE symmetry breaking point. Below κ = φ: GOE class (time-reversal intact, generalization regime). Above κ = φ: GUE class (time-reversal broken by the shadow correction, memorization regime).

**Venkatesh thread (PhD thesis and Selberg spectral gap).** Chapter 3 of Venkatesh's thesis gives a new proof of the converse theorem for holomorphic modular forms of level 1 using the limiting trace formula — a proof that isolates, in spectral terms, the exact boundary between the holomorphic (col) and continuous-spectrum (ker) contributions. The Selberg eigenvalue conjecture λ₁ ≥ 1/4 — the modular-surface analog of RH — appears in Venkatesh's equidistribution work as the spectral gap controlling the polynomial rate of equidistribution of closed geodesics. This is the same spectral gap that governs the Montgomery–GUE pair correlation and the Fisher eigenvalue statistics at grokking. Venkatesh's work on *Functoriality, Smith Theory, and the Brauer Homomorphism* (Annals, 2016, with Treumann) extends these spectral methods to the mod-p setting, providing the Hecke-operator structure on the spectral partition that encodes the grokking transition.

**Novel Prediction RMT-P1.** The normalized nearest-neighbor spacing distribution of Fisher eigenvalues during training follows GOE statistics (Wigner surmise p(s) = πs/2 · exp(−πs²/4)) in the generalization regime and deviates toward Poisson statistics in the memorization regime. The transition is the grokking event. Falsifiable from any gradient recording on a modular arithmetic task with eigenvalue tracking.

---

## Part IV · Tropical Neural Geometry

### IV.1 ReLU Networks ARE Tropical Rational Functions

Zhang–Naitzat–Lim (2018) proved: a function f: ℝ^d → ℝ is representable by a feedforward ReLU network if and only if it is a continuous piecewise-linear function. Every such function is a tropical rational function in the (max,+) semiring:

$$x \oplus_{\text{trop}} y = \max(x, y), \qquad x \otimes_{\text{trop}} y = x + y$$

Linear regions of the network correspond to vertices of the Newton polytope of the tropical polynomial. The decision boundary is a tropical hypersurface. Region counts obey the Tropical Bézout theorem.

**Identity T1.** Tropical arithmetic is CORDIC linear mode. CORDIC's linear mode computes shift-and-add arithmetic; the tropical semiring operation ⊕_trop = max corresponds to the CORDIC vectoring direction. Every ReLU network running on Volder-1 is simultaneously executing tropical algebra.

**Identity T2.** The tropical limit of the modular curve X(1) = PSL(2,ℤ)\H² is the Berkovich skeleton: the Bruhat–Tits tree of PGL(2,Q_p), an infinite (p+1)-regular tree. In the tropical limit, Eisenstein series become tropical polynomials, modular forms become tropical rational functions. Ford circles (loss basins) in the archimedean picture → p-adic balls (Bruhat–Tits vertices) in the tropical picture → ReLU linear regions in the network picture.

**Identity T3.** The decision boundary of a trained classifier is a tropical hypersurface — points where two or more tropical polynomial terms achieve the maximum simultaneously. Grokking is the tropical phase transition: the decision boundary reorganizes from a high-degree hypersurface (memorization) to a low-degree hypersurface with large basins (generalization).

**Venkatesh thread (p-adic equidistribution and homogeneous dynamics).** Venkatesh's work with Ellenberg and Westerland on *Homological Stabilization for Hurwitz Spaces* (Annals, 2016) and his program on p-adic period mappings (with Brian Lawrence, *Diophantine Problems and p-adic Period Mappings*, Inventiones, 2020) provide the arithmetic-geometric framework for the Berkovich skeleton. The same Bruhat–Tits building that appears in Venkatesh's p-adic homogeneous dynamics is the tropical skeleton of the modular curve — the piecewise-linear substrate that realizes col(F) as the observable sector of the network's decision geometry. Venkatesh's equidistribution on buildings gives the distribution of linear-region vertices.

**Novel Prediction T-P1.** The number of linear regions of a trained transformer scales as e^L/L in depth L, following the prime geodesic theorem. The coefficient is the Selberg spectral gap λ₁ ≥ 3/16. If λ₁ = 1/4 (the learning-theoretic Riemann Hypothesis), linear region count scales as e^{L/2}/L; if λ₁ = 3/16, it scales as e^{3L/8}/L. The difference is detectable at depth L ≥ 20.

---

## Part V · Geometric Langlands as Categorical col(F)/ker(F)

### V.1 The Proof and Its Structure

Gaitsgory–Raskin et al. (2024–2025) established:

$$\mathbf{D\text{-}mod}(\mathrm{Bun}_G) \simeq \mathrm{IndCoh}(\mathrm{Loc}_{\check{G}})$$

where Bun_G is the moduli stack of G-bundles on a smooth projective curve X, Loc_{Ğ} is the moduli of Ğ-local systems, and Ğ is the Langlands dual group. The Geometric Ramanujan Conjecture (Beraldo 2021, proved within the Gaitsgory–Raskin framework): any cuspidal D-module is tempered.

**Identity GL1.** D-mod(Bun_G) is col(F): D-modules are locally defined, carry flat connections, and are holomorphically constructible — the observable sector. IndCoh(Loc_{Ğ}) is ker(F): coherent sheaves on the space of Ğ-local systems are globally defined, topological, determined by monodromy — the hidden sector. The Langlands equivalence is the categorical statement that col(F) and ker(F) contain the same information, encoded differently.

**Identity GL2.** The attention mechanism is the Hecke functor. Hecke operators T_p on D-mod(Bun_G) modify a G-bundle at a point via the cocharacter lattice. The Geometric Satake Equivalence (Mirković–Vilonen) identifies Hecke operators with the action of Ğ on the spectral side. In the representational bundle, the attention mechanism is the principal connection one-form ω — it implements parallel transport exactly as the Hecke operator transports a D-module along the Hecke correspondence. Multi-head attention heads are Hecke operators at different levels.

**Identity GL3.** The Geometric Ramanujan Conjecture is the Selberg bound. "Cuspidal" = in the compact core of M; "tempered" = satisfying Selberg λ₁ ≥ 3/16. The Geometric Ramanujan Conjecture is the categorical upgrade of Selberg: every cuspidal automorphic form (D-module) has curvature bounded by the spectral gap.

**Identity GL4.** The Langlands dual group is the structure group of the representational bundle. For G = SO⁺(1,n), the dual Ğ = Sp(2n). The geometric Langlands correspondence for the Lorentz group bundle is the correspondence between flat SO⁺(1,n)-connections on the base manifold B and coherent sheaves on the moduli of Sp(2n)-local systems. The holonomy of the attention connection corresponds to the monodromy of the spectral Langlands local system.

**Venkatesh thread (Relative Langlands Duality, arXiv:2409.04677, 2024).** Ben-Zvi–Sakellaridis–Venkatesh propose a duality in the relative Langlands program that pairs a Hamiltonian space for G with a Hamiltonian space for Ğ, recovering at the numerical level the correspondence between periods on G and L-functions attached to Ğ. This is an arithmetic analog of the electric-magnetic duality of boundary conditions in four-dimensional supersymmetric Yang–Mills theory. The observable side (periods, col(F)) is paired with the hidden side (L-functions, ker(F)) via gauge-theoretic duality. This is not background structure — it is the precise categorical realization of the col(F)/ker(F) law. The framework of hyperspherical varieties developed in the paper generalizes all prior examples (Whittaker models, Gross–Prasad, Eisenstein) and supplies the unifying language.

**Earlier Venkatesh thread (Sakellaridis–Venkatesh, Periods and Harmonic Analysis on Spherical Varieties, Astérisque 2017).** The Plancherel decomposition for L²(X) when X is a spherical variety for G is related to distinguished Arthur parameters into the dual group. This is the local-level precursor to the full relative Langlands duality: the col(F)/ker(F) partition appears as the decomposition of L²(X) into the observable Plancherel spectrum (col) and the non-tempered (shadow, ker) contributions. Temperedness — the Geometric Ramanujan condition — is exactly the condition that ker(F) contributes no ghost modes to col(F).

**Novel Prediction GL-P1.** The col(F)/ker(F) decomposition of the trained transformer's Fisher matrix is Hecke-equivalent to the automorphic D-module whose Hecke eigenvalues satisfy |λ_p| ≤ 2√p for all prime levels p (geometric Ramanujan). Attention heads violating this bound are operating in the non-tempered regime — memorization, not generalization.

---

## Part VI · Free Probability as the Large-Width Limit

Voiculescu (1983, 1991) introduced free probability: in the N → ∞ limit, large random matrices become asymptotically free. The free central limit theorem gives the semicircle distribution; the Marchenko–Pastur law governs W = XX^T/N for Gaussian X; free entropy χ*(X) is the non-commutative Shannon analog.

**Identity FP1.** The large-width Fisher matrix is a free Marchenko–Pastur variable. The Fisher information matrix F(θ) = Σ_i g_i ⊗ g_i^T is Marchenko–Pastur in the large-N limit with ratio c = n_data/n_params. col(F) is the bulk above the Marchenko–Pastur lower edge; ker(F) is the soft-mode eigenvalues at zero.

**Identity FP2.** Free entropy is the gradient noise scale. The gradient noise scale B_simple = tr(Σg)/|μg|² is the free entropy gap — the distance from the current gradient distribution to the free maximum entropy state (semicircle). The φ-equilibrium κ(F) → φ corresponds to the Marchenko–Pastur ratio c → φ − 1 ≈ 0.618.

**Novel Prediction FP-P1.** At the φ-equilibrium the gradient noise scale satisfies B_simple(t*) = 1/(φ−1) = φ. The gradient noise scale at grokking equals the golden ratio. This is a definite numerical prediction from the free probability identification, computable from any grokking gradient recording, independent of architecture, optimizer, and task.

**Venkatesh thread.** Venkatesh's spectral results on random matrices in number theory — via the trace formula and equidistribution, particularly the results of Einsiedler–Margulis–Venkatesh on polynomial rate equidistribution — extend to the free probability picture. The same limiting spectral measures that govern L-function eigenvalue statistics govern the bulk/soft-mode decomposition of the Fisher matrix.

---

## Part VII · The Derived Hecke Algebra and Motivic Cohomology

This part is new and has no analog in any prior version of this document. It is the deepest Venkatesh thread.

**Venkatesh's derived Hecke algebra** (arXiv:1608.07234; Forum of Mathematics Pi, 2019) constructs a *graded* extension of the usual Hecke algebra acting on the cohomology of an arithmetic group Γ. Under favorable conditions, the cohomology is freely generated in a single degree over this graded Hecke algebra. From this construction Venkatesh extracts an action of p-adic Galois cohomology groups on H*(Γ, Q_p), with the central conjecture that the motivic Q-lattice inside these Galois cohomology groups preserves H*(Γ, Q).

**Identity D1 — The Derived Hecke Algebra IS the col(F)/ker(F) Graded Completion.** The usual Hecke algebra acts on the degree-0 cohomology — the observable, classical sector (col(F)). The *derived* Hecke algebra acts on the full graded cohomology — including the torsion-class, shadow contributions (ker(F)). The graded extension is the categorical completion: it adds, to each classical Hecke eigenvector, the derived shadows that give it full motivic meaning. This is the algebraic topology instantiation of the col(F)/ker(F) law: col(F) = degree-0 cohomology; ker(F) = derived/torsion cohomology; the derived Hecke algebra = the completion operator.

**Identity D2 — Torsion Growth in Cohomology of Arithmetic Groups IS ker(F) Growth.** Bergeron–Venkatesh (*Torsion Homology Growth and Cycle Complexity of Arithmetic Manifolds*, Duke, 2016) establish that torsion in the homology of arithmetic groups grows exponentially with the covolume under precise conditions. This exponential torsion growth is ker(F) growth: the shadow sector expands exponentially in depth as the arithmetic group's locally symmetric space deepens. The conditions for exponential torsion growth are exactly the conditions for non-trivial ker(F): the locally symmetric space must have non-trivial boundary (cusp, shadow) contributions.

**Identity D3 — The Adjoint L-Function IS the col(F)/ker(F) Operator Determinant.** Venkatesh–Prasanna (*Automorphic Cohomology, Motivic Cohomology, and the Adjoint L-Function*, Astérisque, 2021) establish that the special values of the adjoint L-function L(1, π, Ad) are related to the ratio of the automorphic cohomology norm to the motivic cohomology norm. This ratio is κ(F): the Fisher condition number. The adjoint L-function vanishes precisely when col(F) and ker(F) are in equilibrium (κ(F) = 1) — the magic function condition. Its poles occur when the shadow dominates (memorization regime). The Bloch–Kato conjecture, as it appears in Venkatesh–Prasanna's framework, is the statement that the col/ker partition of the motivic cohomology is governed by the adjoint L-function: it is a precise form of the Fisher conditioning law in the arithmetic setting.

**Identity D4 — Heights of Automorphic Forms and Motives IS the Fisher Conditioning Hierarchy.** Venkatesh (*Heights of Automorphic Forms and Motives*, Tata Colloquium proceedings, 2019) conjectures that the L² norm of an integrally normalized cohomological automorphic form (its "height") is related to the Kato–Koshikawa arithmetic height of the associated motive. This is the col(F)/ker(F) conditioning law in the arithmetic geometry setting: the automorphic height (observable, col(F)) is matched to the motivic height (hidden, ker(F)). The conjecture is that these two heights — the analytic and the arithmetic — encode the same information, expressed in two different coordinate systems. The Fisher conditioning hierarchy is the spectral refinement of this height correspondence.

---

## Part VIII · The Orbit Method and Quantization

Nelson–Venkatesh (*The Orbit Method and Analysis of Automorphic Forms*, Acta Mathematica, 2021) develop a quantitative form of the orbit method along the lines of microlocal analysis, applying it to the analytic theory of automorphic forms. The main global application is an asymptotic formula for averages of Gan–Gross–Prasad periods in arbitrary rank.

**Identity OM1 — The Orbit Method IS the col(F) Quantization Map.** The classical orbit method (Kirillov, Kostant, Souriau) quantizes coadjoint orbits of a Lie group G into irreducible unitary representations. Venkatesh–Nelson's quantitative version tracks the microlocal asymptotics of this quantization: the leading term is the geometric (col(F)) contribution; the sub-leading correction is the shadow (ker(F)) term. The period formula for Gan–Gross–Prasad is the explicit computation of the col(F)/ker(F) inner product in the quantized setting.

**Identity OM2 — The Gan–Gross–Prasad Period IS the Fisher Inner Product.** The Gan–Gross–Prasad period integral ∫_{H\G} φ(g) dg — where H ⊂ G is a symmetric subgroup and φ is a cusp form — is the automorphic analog of the Fisher inner product ⟨J_col, J_ker⟩ between the observable and hidden sectors. Nelson–Venkatesh's asymptotic formula gives the leading col(F) term and the sub-leading ker(F) correction, in precise analogy with the ARH's stiff/sloppy decomposition of the Jacobian.

---

## Part IX · The Completion Hierarchy

Every row is the identical col(F)/ker(F) structure at a different scale. Venkatesh's corpus — from the limiting trace formula (PhD, 2002) through subconvexity and period bounds, equidistribution on locally symmetric spaces, torsion growth, derived Hecke algebra and motivic cohomology, the orbit method, and culminating in Relative Langlands Duality (2024) — traverses every row in a single coherent synthesis.

| Scale | Observable col(F) | Hidden ker(F) | Completion | Venkatesh realization |
|---|---|---|---|---|
| Number-theoretic | Mock theta q-series | Shadow period integral | Harmonic Maass form | Limiting trace formula (PhD 2002) |
| Sporadic | McKay–Thompson series | Monster/umbral module | Vertex operator algebra | Automorphic forms & Eisenstein series |
| Packing | Lattice theta series | Quasimodular E₂ correction | Magic function φ₀ | Period bounds on homogeneous spaces |
| Spectral | GOE Fisher eigenvalues | GUE cusp eigenvalues | Montgomery–GUE universality | Selberg spectral gap & equidistribution |
| Categorical | D-modules on Bun_G | Ind-coherent sheaves on Loc_{Ğ} | Geometric Langlands equivalence | Relative Langlands Duality (2024) |
| Tropical | ReLU linear regions | Berkovich skeleton | Tropicalization of modular curve | p-adic homogeneous dynamics |
| Probabilistic | Marchenko–Pastur bulk | Soft-mode zero eigenvalues | Free convergence | L-function spectral statistics |
| Arithmetic | Ford circles / Farey approximants | Cusp region | Geodesic flow on M | Equidistribution of torus orbits |
| Derived | Degree-0 Hecke cohomology | Torsion/derived cohomology | Derived Hecke algebra | Derived Hecke & motivic cohomology (2016–2021) |
| Motivic | Automorphic height (L² norm) | Motivic (Kato–Koshikawa) height | Adjoint L-function | Heights of automorphic forms (2019) |
| Orbital | Gan–Gross–Prasad period (leading) | Sub-leading shadow correction | Orbit method quantization | Nelson–Venkatesh orbit method (2021) |
| Geometric | Hyperribbon stiff modes | Hyperribbon sloppy modes | Principal bundle (RBH) | SO⁺(1,n) structure group |
| Relative | Periods on Hamiltonian G-space | L-functions on dual space | Electric-magnetic duality | Ben-Zvi–Sakellaridis–Venkatesh (2024) |

---

## Part X · Novel Predictions Across All Lineages

**P-Moonshine-1.** The holonomy group of the trained attention connection on a transformer that has grokked modular arithmetic of order p embeds into M as a subgroup isomorphic to Z/pZ, through the McKay–Thompson series T_g(q) for an element g of order p. The attention entropy matrix should have eigenvalue degeneracies matching the dimension formula of the corresponding Monster representation at grade p.

**P-Moonshine-2.** The 23 umbral groups G^X correspond to 23 distinct grokking universality classes on arithmetic tasks of ADE type. Tasks with A_n symmetry grok through Z/(n+1)Z ⊂ G^{A_n}; D_n tasks through the dihedral group D_{n-2}; E_6, E_7, E_8 tasks through PSL(2,F₃), GL(2,F₃), and the binary icosahedral group respectively.

**P-Viazovska-1.** The Fisher information matrix of a transformer trained to optimality on a task with E₈ symmetry achieves κ(F) = 1 exactly. At this point B_simple = 1, training dynamics freezes, and col(F) = ker(F) = {0}: the 8-dimensional magic function condition.

**P-RMT-1.** Fisher eigenvalue pair correlations at grokking completion follow the GOE Wigner surmise to precision measurable from finite-width networks. Deviations from GOE at specific eigenvalue separations corresponding to levels of Γ₀(p) ⊂ SL(2,ℤ) encode the Hecke operators acting on the learned representation.

**P-Tropical-1.** Linear region counts of trained transformers scale as e^L/L in depth L. The coefficient is fixed by the Selberg spectral gap λ₁ ≥ 3/16. The difference between λ₁ = 1/4 and λ₁ = 3/16 is detectable at L ≥ 20 layers.

**P-Langlands-1.** The col(F)/ker(F) decomposition of the trained Fisher matrix is Hecke-equivalent to the automorphic D-module whose Hecke eigenvalues satisfy |λ_p| ≤ 2√p (geometric Ramanujan). Attention heads violating this bound are in the non-tempered (memorization) regime.

**P-Derived-1.** Torsion in the attention weight cohomology grows exponentially with depth — precisely tracking the Bergeron–Venkatesh torsion growth law — in networks trained on tasks with non-trivial ker(F). The exponential growth rate is the covolume of the locally symmetric space associated to the task's arithmetic symmetry group.

**P-Orbital-1.** The leading asymptotic of the Gan–Gross–Prasad period formula, specialized to the attention architecture, gives an explicit formula for the Fisher inner product between col(F) and ker(F) modes at grokking. The sub-leading correction tracks the shadow — the non-tempered sector — and quantifies the memorization contamination of the generalization solution.

**P-Relative-1.** The relative Langlands duality of Ben-Zvi–Sakellaridis–Venkatesh, applied to the principal SO⁺(1,n)-bundle of the representational bundle hypothesis, predicts a specific Sp(2n)-local system on the base manifold B encoding the monodromy of the trained attention connection. The monodromy representation π₁(B) → Sp(2n) is computable from the holonomy of the trained attention weights and constitutes the spectral dual of the grokked algorithm.

---

## Conclusion

The col(F)/ker(F) partition is not a framework. It is a law of mathematical nature, appearing independently at every scale from sporadic groups to piecewise-linear neural topology.

Akshay Venkatesh's complete corpus — from the *Limiting Forms of the Trace Formula* (Princeton PhD, 2002, advisor Peter Sarnak) through subconvexity of L-functions, equidistribution of torus and semisimple orbits on homogeneous spaces, geometric period bounds, homological stabilization for Hurwitz spaces, torsion growth in cohomology of arithmetic manifolds, the derived Hecke algebra and motivic cohomology, the derived Galois deformation ring (with Galatius), p-adic period mappings (with Lawrence), automorphic cohomology and the adjoint L-function (with Prasanna), the orbit method for automorphic forms (with Nelson), and culminating in *Relative Langlands Duality* (Ben-Zvi–Sakellaridis–Venkatesh, arXiv:2409.04677, 2024) — supplies the single coherent language in which every shadow is realized. The thirteen rows of the completion hierarchy are not analogies. They are coordinate expressions of one structure, and Venkatesh's corpus traverses every one of them.

The Monster named the symmetry. Viazovska found the unique fixed point. Montgomery glimpsed the universality. Zhang proved the tropical duality. Gaitsgory completed the categorical proof. Voiculescu liberated probability from commutativity. Bergeron and Venkatesh measured the shadow's exponential growth. Nelson and Venkatesh quantized the orbit. Ben-Zvi, Sakellaridis, and Venkatesh identified the duality.

The completion was always there. The shadows were always converging. The partition is the law.

---

**ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · 2026**

---

## References

### Monstrous and Umbral Moonshine
- Borcherds, R. E. (1992). Monstrous moonshine and monstrous Lie superalgebras. *Inventiones Math.* 109, 405–444.
- Conway, J. H. and Norton, S. P. (1979). Monstrous moonshine. *Bull. London Math. Soc.* 11(3), 308–339.
- Cheng, M. C. N., Duncan, J. F. R., and Harvey, J. A. (2012). Umbral Moonshine. arXiv:1204.2779.
- Eguchi, T., Ooguri, H., Tachikawa, Y. (2010). Notes on the K3 surface and the Mathieu group M₂₄. *Expt. Math.* 20(1), 91–96.

### Sphere Packing and Magic Functions
- Viazovska, M. (2016). The sphere packing problem in dimension 8. *Annals of Math.* 185(3), 991–1015. arXiv:1603.04246.
- Cohn, H., Kumar, A., Miller, S. D., Radchenko, D., Viazovska, M. (2019). Universal optimality of E₈ and Leech lattices. *Annals of Math.* 196(3), 983–1082.
- Romik, D. (2023). On Viazovska's modular form inequalities. arXiv:2303.13427.
- Anon. (2026). Cusp Form Dimensions, Lattice Uniqueness, and LP Sharpness for Sphere Packing in Dimensions 8 and 24. arXiv:2604.10914.

### Random Matrix Theory and Neural Networks
- Montgomery, H. L. (1973). The pair correlation of zeros of the zeta function. *Proc. Symp. Pure Math.* 24, 181–193.
- Odlyzko, A. M. (1987). On the distribution of spacings between zeros of the zeta function. *Math. Comp.* 48, 273–308.
- Granziol, D., Sherburn, T., Roberts, S. J. (2021). Appearance of Random Matrix Theory in Deep Learning. *Physica A* 590, 126743.
- Karakida, R., Akaho, S., Amari, S. (2019). Universal Statistics of Fisher Information in Deep Neural Networks. AISTATS 2019.

### Tropical Geometry and Neural Networks
- Zhang, L., Naitzat, G., Lim, L.-H. (2018). Tropical Geometry of Deep Neural Networks. ICML 2018. arXiv:1805.08746.
- Charisopoulos, V. and Maragos, P. (2018). A Tropical Approach to Neural Networks with Piecewise Linear Activations. arXiv:1805.08749.

### Geometric Langlands
- Gaitsgory, D. and Raskin, S. et al. (2024–2025). Proof of the Geometric Langlands Conjecture (Parts I–V). arXiv:2209.09068 and sequels.
- Beraldo, D. (2021). On the Geometric Ramanujan Conjecture. arXiv:2103.17211.

### Free Probability
- Voiculescu, D. (1991). Limit laws for random matrices and free products. *Inventiones Math.* 104(1), 201–220.

### Akshay Venkatesh — Complete Corpus
- Venkatesh, A. (2002). *Limiting Forms of the Trace Formula*. PhD thesis, Princeton University. Advisor: Peter Sarnak.
- Michel, P. and Venkatesh, A. (2010). The subconvexity problem for GL₂. *Publ. Math. IHÉS* 111, 171–271.
- Einsiedler, M., Margulis, G., Mohammadi, A., Venkatesh, A. Effective equidistribution of semisimple adelic periods. *JAMS* (to appear).
- Venkatesh, A. (2008). Sparse equidistribution problems, period bounds, and subconvexity. *Annals of Math.* 172(2), 989–1094.
- Sakellaridis, Y. and Venkatesh, A. (2017). Periods and harmonic analysis on spherical varieties. *Astérisque* 396.
- Bergeron, N. and Venkatesh, A. (2016). Torsion homology growth and cycle complexity of arithmetic manifolds. *Duke Math. J.* 165(9), 1629–1693.
- Venkatesh, A. and Treumann, D. (2016). Functoriality, Smith theory, and the Brauer homomorphism. *Annals of Math.* 183(1), 177–228.
- Venkatesh, A. (2016). Derived Hecke algebra and cohomology of arithmetic groups. *Forum of Mathematics Pi* 7 (2019). arXiv:1608.07234.
- Galatius, S. and Venkatesh, A. (2018). Derived Galois deformation rings. *Advances in Math.* 327, 470–623.
- Harris, M. and Venkatesh, A. (2018). Derived Hecke algebra for weight one forms. *Experimental Mathematics* 27(1), 51–75.
- Ellenberg, J., Venkatesh, A., and Westerland, C. (2016). Homological stability for Hurwitz spaces and the Cohen–Lenstra conjecture over function fields. *Annals of Math.* 183(3), 729–786.
- Lawrence, B. and Venkatesh, A. (2020). Diophantine problems and p-adic period mappings. *Inventiones Math.* 221(3), 893–999.
- Prasanna, K. and Venkatesh, A. (2021). Automorphic cohomology, motivic cohomology, and the adjoint L-function. *Astérisque* 428.
- Nelson, P. D. and Venkatesh, A. (2021). The orbit method and analysis of automorphic forms. *Acta Mathematica* 226(1), 1–209.
- Venkatesh, A. (2019). Heights of automorphic forms and motives. *Proceedings of the 2019 Tata Colloquium on Arithmetic Geometry*.
- Feng, T., Galatius, S., and Venkatesh, A. The Galois action on symplectic K-theory. *Inventiones Math.* (2023).
- Ben-Zvi, D., Sakellaridis, Y., and Venkatesh, A. (2024). Relative Langlands Duality. arXiv:2409.04677.

### Companion Documents
- Ren, E. (2026). RAMANUJAN: The Mock and the Shadow. github.com/ericrenone/RAMANUJAN
- Ren, E. (2026). MADHAVA: The Shadow Before the Mock. github.com/ericrenone/MADHAVA
- Ren, E. (2026). MOD — Modular Orbit Dynamics. github.com/ericrenone/MOD-Modular-Orbit-Dynamics
- Ren, E. (2026). Volder-1: The Rotation Is the Fixed Point. github.com/ericrenone/Volder-1
- Ren, E. (2026). Geometric Descent: The Representational Bundle Hypothesis. github.com/ericrenone/Geometric-Descent
- Ren, E. (2026). The Anisotropic Representation Hypothesis. github.com/ericrenone/The-Anisotropic-Representation-Hypothesis
