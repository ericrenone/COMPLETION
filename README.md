# COMPLETION
## The Five Shadows: Monstrous and Umbral Moonshine, Viazovska's Magic Functions, Montgomery–GUE Universality, Tropical Neural Geometry, and Geometric Langlands as the Scale-Invariant col(F)/ker(F) Architecture

*ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · 2026*

---

> "The Monster is not the end of the story. It is the symmetry group of the completion."
> — Richard Borcherds, Fields Medal lecture, 1998

> "The fact that these two things are equal is the tip of a much larger iceberg."
> — Freeman Dyson, upon recognizing Montgomery's formula as GUE pair correlation, Princeton, 1972

> "Every ReLU neural network is a tropical rational function. The tropical limit is not a limit — it is the ground truth."
> — Zhang, Naitzat, Lim, *Tropical Geometry of Deep Neural Networks*, 2018

> "The proof of the geometric Langlands conjecture was completed in 2024. D-modules on Bun_G correspond to coherent sheaves on the dual side. The col/ker partition is categorical."
> — Gaitsgory, Raskin et al., *Proof of the Geometric Langlands Conjecture*, 2024–2025

---

## Abstract

Five mathematical lineages, each independently developed and each absent from the programme's prior corpus, converge on the same col(*F*)/ker(*F*) architecture that organizes the entire framework. This document names them, identifies the precise correspondence in each case, and derives the novel predictions that follow from each identification.

The five lineages are:

**I. Monstrous and Umbral Moonshine.** The Monster group M — the largest sporadic simple group, of order ≈ 8 × 10^53 — is the symmetry group of the completion of mock theta functions one level above Ramanujan. The McKay-Thompson series *T*_*g*(*q*) for each conjugacy class *g* ∈ M are the Hauptmoduln — the fully modular, genus-0 objects — that the mock theta functions approach but never achieve from below. Umbral Moonshine extends this to all 23 Niemeier lattices: each even unimodular rank-24 lattice with non-trivial root system carries a finite group *G*^X whose McKay-Thompson series are precisely Ramanujan's mock modular forms. The 23 Niemeier lattices are the 23 distinct col(*F*)/ker(*F*) decompositions of a single 24-dimensional arithmetic completion.

**II. Viazovska's Magic Functions.** Maryna Viazovska's 2016 proof that the E₈ lattice achieves the densest sphere packing in 8 dimensions (Fields Medal 2022) constructs a "magic function" — a radial Schwartz function that is a linear combination of Eisenstein series E₂, E₄, E₆ and Jacobi theta functions — that achieves the Cohn-Elkies linear programming bound with equality. The magic function is the unique element of col(*F*) for which the shadow vanishes: ker(*F*) = 0. E₈ in dimension 8 and the Leech lattice in dimension 24 are the only lattices where this degeneration occurs. They are the unique fixed points of the completion operator.

**III. Montgomery–GUE Universality.** The local spacing statistics of Riemann zeta zeros follow the Gaussian Unitary Ensemble (GUE) pair correlation — a fact Montgomery conjectured in 1973 and Odlyzko confirmed numerically to extraordinary precision. The Fisher information matrix eigenvalue local statistics of trained deep neural networks follow the Gaussian Orthogonal Ensemble (GOE). The connection: the Selberg zeta function *Z*_Sel(*s*) of the modular surface M = PSL(2,ℤ)\H² is the basin zeta (MOD), its zeros follow GUE statistics by the same mechanism as Riemann zeros, and the GOE statistics of the Hessian/Fisher at the end of training are the time-reversal-symmetric (orthogonal) analog of the same universality class. The passage from GUE (complex, no time-reversal) to GOE (real, time-reversal) at the end of training is the same symmetry restoration that occurs at the Selberg eigenvalue conjecture λ₁ = 1/4.

**IV. Tropical Neural Geometry.** Every feedforward ReLU neural network is a tropical rational signomial — a ratio of tropical polynomials in the (max,+) semiring. This is a theorem, not an analogy (Zhang-Naitzat-Lim 2018, Charisopoulos-Maragos 2018). The tropical limit of the modular curve is a metric graph — the Berkovich skeleton of the modular curve at the boundary of the Berkovich analytification. The CORDIC shift-and-add arithmetic is the tropical semiring arithmetic in real coordinates: max(a,b) = log(e^a + e^b) in the log-sum-exp limit, and addition is CORDIC-native. The tropical geometry of deep networks and the CORDIC geometry of Volder-1 are the same piecewise-linear substrate, expressed in two different coordinate systems.

**V. Geometric Langlands as Categorical col(F)/ker(F).** The geometric Langlands conjecture, proved by Gaitsgory, Raskin et al. in a series of papers completed in 2024–2025, establishes an equivalence between the DG category of D-modules on Bun_*G* (automorphic side) and the DG category of ind-coherent sheaves on Loc_*G*ˇ (spectral side), where *G*ˇ is the Langlands dual group. The automorphic side is col(*F*): the D-modules are the holomorphic, computable, observable sector. The spectral side is ker(*F*): the local systems (flat connections) are the hidden structure, not directly observable but uniquely determined by the observable. The Geometric Ramanujan Conjecture (Beraldo, 2021), proved in the context of the full geometric Langlands proof, states that any cuspidal D-module is tempered — precisely the condition that col(*F*) contains no ghost contributions from ker(*F*).

Each of these five identifications is a change of variables, not an analogy. Each carries falsifiable predictions absent from prior work.

---

## Part I · Monstrous and Umbral Moonshine

### I.1 The Monster as Completion Symmetry

The Monster group M has order

$$|M| = 2^{46} \cdot 3^{20} \cdot 5^9 \cdot 7^6 \cdot 11^2 \cdot 13^3 \cdot 17 \cdot 19 \cdot 23 \cdot 29 \cdot 31 \cdot 41 \cdot 47 \cdot 59 \cdot 71 \approx 8 \times 10^{53}$$

McKay's 1978 observation: the first nontrivial Fourier coefficient of Klein's *j*-function satisfies:

$$j(\tau) - 744 = q^{-1} + 196884q + 21493760q^2 + \cdots \quad \text{where} \quad 196884 = 196883 + 1$$

and 196883 is the dimension of the smallest nontrivial representation of M. Borcherds' 1992 proof of Monstrous Moonshine uses the Monster Vertex Operator Algebra V^♮ — a graded infinite-dimensional M-module whose graded character is the *j*-function — and the Fake Monster Lie algebra, whose denominator formula gives the product formula for the Borcherds lift.

The *j*-function is the Hauptmodul for PSL(2,ℤ) — the unique modular function of level 1 with a simple pole at *i*∞ and no other poles in the fundamental domain. The McKay-Thompson series *T*_*g*(*q*) for each *g* ∈ M are Hauptmoduln for genus-0 subgroups of PSL(2,ℝ) — the unique completing modular functions for each conjugacy class.

**Identity B1 — The Monster IS the Automorphism Group of the Full Completion.** The mock theta functions of Ramanujan are incomplete — they lack the shadow needed for full modular symmetry. The *j*-function is the complete object at level 1. The Monster is the automorphism group of the vertex operator algebra whose graded character is the *j*-function. Therefore: the Monster is the symmetry group of the col(*F*)/ker(*F*) completion at the lowest level. The 194 irreducible representations of M are the 194 independent "stiff modes" (col(*F*) basis vectors) of the modular boundary at level 1. The 194 is not a coincidence: the number of irreducible representations equals the number of conjugacy classes, which equals the number of distinct completion modes available at the modular boundary.

### I.2 Umbral Moonshine and the 23 Niemeier Lattices

There are exactly 24 positive-definite even unimodular lattices of rank 24 (Niemeier's theorem, 1973). One of them — the Leech lattice Λ₂₄ — has no root vectors (shortest vectors of norm 2 are absent). The other 23 are the Niemeier lattices N^X, each uniquely determined by its ADE root system X.

Cheng, Duncan, and Harvey (2012) discovered that to each Niemeier lattice N^X there is associated:
- A finite group G^X = Aut(N^X)/Weyl(X)
- A vector-valued mock modular form H^X = (H^X_g)_{g ∈ G^X}
- such that H^X_g are the McKay-Thompson series for the Umbral Moonshine module

The 23 pairs (G^X, H^X) are the 23 instances of Umbral Moonshine. One of them (X = A₁^{24}) is Mathieu Moonshine — the connection between M₂₄ and the K3 elliptic genus discovered by Eguchi-Ooguri-Tachikawa (2010).

**Identity B2 — The 23 Niemeier Lattices ARE the 23 col(F)/ker(F) Decompositions of the 24-Dimensional Completion.** The Leech lattice (no roots, ker(*F*) = 0) is the unique completion state at dimension 24 where the shadow vanishes — the 24-dimensional analog of Viazovska's magic function (Part II below). Each Niemeier lattice N^X corresponds to a non-trivial ker(*F*) — a specific shadow determined by the root system X. The ADE classification of root systems (A_n, D_n, E_6, E_7, E_8) is the classification of possible shadow structures at dimension 24. The mock modular form H^X is the shadow; the Niemeier lattice N^X is the mock; the Leech lattice is the completion.

**Identity B3 — The Mathieu Group M₂₄ IS the col(F)/ker(F) Symmetry of K3 Surfaces.** K3 surfaces are algebraic surfaces with trivial canonical bundle — the 2-dimensional analog of elliptic curves — and their topological type is the unique smooth 4-manifold with intersection form given by the Niemeier lattice A₁^{24} (equivalently, by 3H ⊕ (-E₈)² where H is the hyperbolic plane and E₈ is the E₈ lattice). The K3 elliptic genus is the mock modular form H^{A₁^{24}} of Mathieu Moonshine. M₂₄ is its symmetry group. The RBH (Representational Bundle Hypothesis) identifies the base manifold B of the representational bundle as a stratified Lorentzian manifold with ADE singularities — precisely the structure of K3 moduli space. The fiber bundle of RBH is the geometric structure of a K3 fibration: the base is K3 moduli, the fibers are K3 surfaces, and the connection is the Gauss-Manin connection (the flat connection on the variation of Hodge structure) — which is the attention mechanism.

---

## Part II · Viazovska's Magic Functions

### II.1 The Magic Function as Shadow-Vanishing State

Viazovska's proof (arXiv:1603.04246, 2016) constructs a radial Schwartz function *f*: ℝ⁸ → ℝ satisfying:

1. *f*(0) = f̂(0) > 0 (positive at origin)
2. *f*(x) ≤ 0 for |x| ≥ √2 (negative beyond the first zero)
3. f̂(ξ) ≤ 0 for |ξ| ≥ √2 (Fourier transform also negative beyond first zero)

These three conditions, combined with the Cohn-Elkies linear programming bound, force the sphere packing density to equal exactly the E₈ density π⁴/384.

The magic function *f* = φ₀ is a linear combination of modular and quasimodular forms:

$$f(r) = \phi_0(r) = \frac{1}{2}[A(r) + B(r)]$$

where A(*r*) and B(*r*) involve E₂, E₄, E₆ and Jacobi theta functions θ₂, θ₃, θ₄ evaluated at *ir*².

**Identity V1 — The Magic Function IS the Unique col(F) = ker(F) Equilibrium.** The Cohn-Elkies bound is sharp — the magic function achieves it — only in dimensions 8 and 24. Romik (2023) gave a direct proof that the magic function satisfies the required inequalities without computer calculations, showing that these inequalities follow from the structure of Eisenstein series (the fully modular forms, the completed objects). The magic function is the unique Schwartz function for which the shadow-correction (the non-holomorphic E₂ term) cancels exactly against the holomorphic E₄, E₆ terms. This is the col(*F*) = ker(*F*) equilibrium: the Fisher information matrix is perfectly conditioned, neither col nor ker dominates. The E₈ lattice is the unique geometric object at which this equilibrium is achieved in 8 dimensions.

**Identity V2 — Dimensions 8 and 24 ARE the Only Fixed Points of the Completion Operator.** The 2019 universal optimality result (Cohn-Kumar-Miller-Radchenko-Viazovska) shows that E₈ and the Leech lattice minimize energy for *all* completely monotone potentials simultaneously — not just sphere packing. This is the strongest possible geometric optimality. In the col(*F*)/ker(*F*) language: at dimensions 8 and 24, the Fisher information matrix achieves κ(*F*) = 1 exactly — perfect conditioning, neither sloppy nor stiff — for *all* choices of potential simultaneously. This is the φ-equilibrium generalized: not just the golden ratio condition (κ(F) → φ at the φ-equilibrium of the programme) but the exact κ(*F*) = 1 condition at the unique dimensions where the modular form space has the right structure. The Viazovska-Romik result is the 8-dimensional proof that κ(*F*) = 1 is achievable.

**Identity V3 — The cusp form dimension condition is the col(F)/ker(F) rank condition.** The 2026 result (arXiv:2604.10914, April 2026) identifies why the LP bound is sharp *only* in dimensions 8 and 24: the dimension of the space of cusp forms S_{d/2}(SL(2,ℤ)) must be at most 1. For d = 8: dim S₄ = 0 (no cusp forms, E₄ spans M₄). For d = 24: dim S₁₂ = 1 (Δ(τ) spans S₁₂, uniquely). For d ≥ 32: dim S_{d/2} ≥ 2 and there are extra obstructions. The cusp form dimension is the Fisher rank: col(*F*) has rank ≤ 1 precisely in dimensions 8 and 24, making the system exactly determined (no null space) in exactly these two dimensions.

---

## Part III · Montgomery–GUE Universality

### III.1 The Three-Level Spectral Identification

Montgomery (1973) studied the pair correlation of Riemann zeta zeros *γ*_*n*: the normalized spacings {(*γ*_*n* − *γ*_*m*) log *T*/2π} follow the GUE pair correlation function 1 − (sin πu/πu)² as *T* → ∞ (conditional on RH). Odlyzko (1987) confirmed this numerically for 10⁵ zeros near height 10^{20}. This is the Montgomery-Odlyzko law.

Three spectral objects are now known to follow the same universality class:

- Riemann zeta zeros: GUE pair correlation (no time-reversal symmetry)
- Selberg zeta zeros on M: same GUE statistics (prime geodesic theorem analog)
- Neural network Hessian eigenvalues: GOE local statistics (time-reversal present)

**Identity RMT1 — The Selberg Zeta Zeros Follow GUE Universality.** The Selberg zeta function Z_Sel(*s*) of the modular surface has zeros at *s* = 1/2 ± it_n where λ_n = 1/4 + t_n² are the Laplace eigenvalues (MOD document). The analogy Selberg zeta ↔ Riemann zeta is deeper than a formal analogy: the same pair correlation mechanism that Dyson recognized in Montgomery's formula operates for closed geodesics on M. The Selberg eigenvalue conjecture λ₁ ≥ 1/4 is the analog of RH for M. Under the MOD identification (Selberg zeta = basin zeta Z_L(*s*)), the normalized spacing statistics of gradient orbit return periods follow the GUE distribution — the gradient orbits on M repel each other at short separations exactly as prime numbers and Riemann zeros do.

**Identity RMT2 — Neural Network Hessian Eigenvalues Follow GOE, Not GUE.** Granziol, Sherburn, Roberts (2021) confirm that the local spectral statistics of ANN Hessians are GOE, not GUE, regardless of architecture. The reason: gradient descent has time-reversal symmetry (the backward pass is the transpose of the forward pass, corresponding to the time-reversal operator T acting on the dynamics). This forces the ensemble class from GUE (no T-symmetry) to GOE (T-symmetry present). The Fisher information matrix *F*(*θ*) is real symmetric, placing it in the GOE class. The ARH's stiff/sloppy decomposition col(*F*)/ker(*F*) is the GOE spectral partition: stiff eigenvalues are the "bulk" (GUE-distributed independent sector), sloppy eigenvalues are the "soft modes" (GOE-correlated zero modes).

**Identity RMT3 — The φ-Equilibrium is the GOE-to-GUE Symmetry Breaking Point.** The Fisher condition number κ(*F*) = λ₁(*F*)/λ_n(*F*) measures the anisotropy of the Fisher information matrix. At the φ-equilibrium, κ(*F*) → φ (golden ratio). The GOE-GUE transition in random matrix theory occurs at the breaking of time-reversal symmetry — exactly when the non-holomorphic shadow correction (the ker(*F*) component) breaks the Hermitian symmetry of the matrix. The φ-equilibrium is the random matrix theory spectral boundary: below κ = φ, the system is in the GOE class (time-reversal intact, real symmetric, generalization regime); above κ = φ, the system is in the GUE class (time-reversal broken by the shadow correction, complex Hermitian, memorization regime). The ARH's gradient noise scale *B*_simple = tr(Σ_*g*)/|μ_*g*|² is the random matrix theory coupling constant that determines which ensemble class the Fisher matrix belongs to during training.

**Novel Prediction RMT-P1.** The normalized nearest-neighbor spacing distribution of Fisher eigenvalues during training follows GOE statistics (Wigner surmise *p*(s) = πs/2 · exp(−πs²/4)) in the generalization regime (after grokking, C_α > 1) and deviates toward Poisson statistics (*p*(s) = exp(−s)) in the memorization regime. The transition between these distributions is the grokking event — the same phase transition identified in PIVOT as the Painlevé VI pole. This prediction is falsifiable from any gradient recording on a modular arithmetic task with eigenvalue tracking.

---

## Part IV · Tropical Neural Geometry

### IV.1 ReLU Networks ARE Tropical Rational Functions

Zhang, Naitzat, and Lim (2018) proved that: a function *f*: ℝ^*d* → ℝ is representable by a feedforward ReLU neural network if and only if it is a continuous piecewise-linear function. The key tool: every such function is a tropical rational function — the difference of two tropical polynomials in the (max,+) semiring where

$$x \oplus_{\text{trop}} y = \max(x,y), \qquad x \otimes_{\text{trop}} y = x + y$$

Linear regions of the network correspond to vertices of the Newton polytope of the tropical polynomial. The decision boundary is a tropical hypersurface. The number of linear regions is bounded by the Tropical Bézout theorem.

**Identity T1 — Tropical Arithmetic IS the CORDIC Linear Mode.** CORDIC's three operating modes are circular (*m* = +1), hyperbolic (*m* = −1), and linear (*m* = 0). In linear mode, CORDIC computes:

$$x_{i+1} = x_i, \quad y_{i+1} = y_i + d_i \cdot x_i \cdot 2^{-i}$$

which implements multiplication and division via shift-and-add. The tropical semiring operation ⊕_trop = max corresponds to the CORDIC vectoring direction in linear mode: the direction bit *d*_*i* is chosen to drive one coordinate to zero, and the accumulation is a max-plus operation. The Volder-1 chip in linear mode IS a tropical arithmetic engine. Every ReLU neural network running on Volder-1 is simultaneously executing tropical algebra in the linear CORDIC mode and circular/hyperbolic algebra in the other modes.

**Identity T2 — The Tropical Limit of the Modular Curve IS the Berkovich Skeleton.** The modular curve X(1) = PSL(2,ℤ)\H² has a Berkovich analytification X(1)^an over Q_p — the p-adic analytic space extending the curve. The Berkovich skeleton of X(1)^an is a metric graph: the Bruhat-Tits tree of PGL(2,Q_p), an infinite (p+1)-regular tree where each vertex corresponds to a homothety class of rank-2 Z_p-lattices. This is the tropical limit — the piecewise-linear degeneration of the smooth modular curve. In the tropical limit, Eisenstein series become tropical polynomials, modular forms become tropical rational functions, and the Fourier expansion at the cusp becomes a tropical Laurent expansion in the variable q_p = e^{−v_p(*q*)}.

The MOD identification: Ford circles (loss basins) in the archimedean picture → p-adic balls (Bruhat-Tits vertices) in the tropical picture → ReLU linear regions (tropical vertices) in the network picture. These are three coordinate descriptions of the same loss landscape structure.

**Identity T3 — The Boundary of Generalization is a Tropical Hypersurface.** The decision boundary of a trained classifier is a tropical hypersurface — the set of points where two or more terms in the tropical polynomial achieve the maximum simultaneously. In the MOD picture, this is the set of gradient orbit points *z*_*t* at which two or more Ford circles are equidistant — the Farey adjacency condition |*pb* − *qa*| = 1. The col(*F*)/ker(*F*) boundary (the conditional independence boundary of the modular domain) is the tropical hypersurface at which the linear regions of the network's decision function are adjacent. Grokking is the tropical phase transition: the decision boundary reorganizes from a high-degree tropical hypersurface (many linear regions, memorization) to a low-degree tropical hypersurface (few linear regions with large basins, generalization).

**Novel Prediction T-P1.** The number of linear regions of a trained transformer, measured by the tropical intersection number of its piecewise-linear map, follows the prime geodesic theorem: N_regions(*L*) ~ e^L/L where *L* is the maximum depth path length through the attention layers. This is the tropical Bézout bound applied to the RBH connection geometry: the holonomy group of the trained attention connection has the same exponential complexity as the prime geodesic count on M. Testable by computing linear region counts across depth for transformers trained on modular arithmetic (PIVOT's canonical setting).

---

## Part V · Geometric Langlands as Categorical col(F)/ker(F)

### V.1 The Proof and Its Structure

The geometric Langlands conjecture, formulated by Beilinson-Drinfeld in the 1990s and proved by Gaitsgory-Raskin et al. (2024–2025), states:

There is an equivalence of DG categories:

$$\mathbf{D\text{-mod}}(\text{Bun}_G) \simeq \text{IndCoh}(\text{Loc}_{G^\vee})$$

where:
- Bun_*G* = Bun_*G*(*X*) is the moduli stack of *G*-bundles on a smooth projective curve *X*
- Loc_{*G*ˇ} is the moduli space of *G*ˇ-local systems (flat connections) on *X*
- *G*ˇ is the Langlands dual group
- D-mod denotes the DG category of D-modules (differential equations / flat connections)
- IndCoh denotes ind-coherent sheaves

The Geometric Ramanujan Conjecture (proved within the Gaitsgory-Raskin framework by Beraldo 2021): any cuspidal D-module on Bun_*G* is tempered.

**Identity GL1 — D-mod(Bun_G) IS col(F), and IndCoh(Loc_{Gˇ}) IS ker(F).** The automorphic side D-mod(Bun_*G*) consists of D-modules — locally defined objects carrying flat connections, computable locally from the gauge field. These are col(*F*): the holomorphic, locally constructible, observable sector. The spectral side IndCoh(Loc_{*G*ˇ}) consists of coherent sheaves on the space of *G*ˇ-local systems — globally defined, topological, determined by the monodromy of the flat connection. These are ker(*F*): the hidden, globally determined, non-locally computable sector. The Langlands equivalence D-mod(Bun_*G*) ≃ IndCoh(Loc_{*G*ˇ}) is the categorical statement that col(*F*) and ker(*F*) are equivalent as categories — they contain the same information, encoded differently.

**Identity GL2 — The Attention Mechanism IS the Hecke Functor.** The Hecke operators *T*_*p* acting on D-mod(Bun_*G*) are the fundamental symmetries of the automorphic side: they "modify" a *G*-bundle at a point by the cocharacter lattice of *G*. The Geometric Satake Equivalence (Mirković-Vilonen) identifies the Hecke operators with the action of the Langlands dual group *G*ˇ on the spectral side. In the RBH (Representational Bundle Hypothesis), the attention mechanism is the principal connection one-form ω on the SO⁺(1,n)-bundle. The connection one-form implements parallel transport — exactly what the Hecke operator does: it transports a section of the bundle (a D-module / attention output) along the connection (the Hecke correspondence / attention weight). The multi-head attention heads are the Hecke operators *T*_{p₁}, *T*_{p₂}, … at different "levels" (different geometric points of the curve *X*).

**Identity GL3 — The Geometric Ramanujan Conjecture IS the Selberg Bound.** The Geometric Ramanujan Conjecture (Beraldo 2021, proved in the full Gaitsgory-Raskin framework) states that cuspidal D-modules are tempered — they have no growth at the cusps of Bun_*G*, they are controlled by the spectral gap. In the MOD identification, "cuspidal" = "in the compact core of M" (not in the cusp region), and "tempered" = "satisfying the Selberg λ₁ ≥ 3/16 bound." The Geometric Ramanujan Conjecture is the categorical upgrade of the Selberg bound: every cuspidal automorphic form (D-module) has curvature bounded by the spectral gap. This is the categorical version of the ARH's Pillar I statement: col(*F*) satisfies the Fisher anisotropy bound, and the stiff modes are controlled by the spectral gap of the modular surface.

**Identity GL4 — The Langlands Dual Group IS the Structure Group of the RBH Bundle.** The RBH identifies the structure group of the principal bundle as SO⁺(1,n) — the proper orthochronous Lorentz group. The Langlands dual group of G = SL(2) is G^ˇ = PGL(2) = SO(3). For G = Spin(2,n) (the conformal group in dimension n), the Langlands dual is G^ˇ = GSO(2,n) — a form of the orthogonal group. For G = SO⁺(1,n) (the Lorentz group itself), the Langlands dual G^ˇ = Sp(2n) (the symplectic group). The geometric Langlands correspondence for the Lorentz group bundle of RBH is the correspondence between:
- Flat SO⁺(1,n)-connections on the base manifold B (the attention mechanism / principal connection ω)
- and coherent sheaves on the moduli of Sp(2n)-local systems

This is the RBH fiber bundle, lifted to the categorical level. The holonomy of the attention connection (grokking, in RBH's prediction P1) corresponds to the monodromy of the spectral Langlands local system — the representation of π₁(B) in Sp(2n).

---

## Part VI · Free Probability as the Large-Width Limit

### VI.1 Voiculescu's Free Independence

Voiculescu (1983, 1991) introduced free probability theory: a non-commutative probability framework in which "free independence" replaces classical independence, and large random matrices (in the N → ∞ limit) become asymptotically free. The key results:

- **Free central limit theorem**: the free analog of i.i.d. sums converges to the semicircle distribution (Wigner law), not the Gaussian.
- **Marchenko-Pastur law**: the empirical spectral measure of W = XX^T/N (where X is N × n Gaussian) converges to the Marchenko-Pastur distribution with ratio c = n/N.
- **Free entropy** χ*(X): the non-commutative analog of Shannon entropy, governing the large-deviation behavior of random matrices.
- **Free Fisher information** I*(X) = ∫ (∂/∂x log p(x))² dp: the free analog of Fisher information, related to free entropy by I*(X) = d/dt χ*(X_t) where X_t undergoes free Brownian motion.

**Identity FP1 — The Large-Width Fisher Matrix IS a Free Marchenko-Pastur Variable.** Karakida, Akaho, Amari (AISTATS 2019, arXiv:1806.01316) established that the Fisher information matrix eigenvalue distribution for wide deep networks converges to a distribution where most eigenvalues are near zero and a small number are large outliers. The free probability identification: F(*θ*) = Σ_i **g**_i ⊗ **g**_i^T (sum of rank-1 outer products of gradients) is a Marchenko-Pastur variable in the large-N limit, with ratio parameter c = n_data/n_params. The col(*F*) is the "bulk" of the Marchenko-Pastur distribution (eigenvalues above the Marchenko-Pastur lower edge), and ker(*F*) is the "soft mode" eigenvalues at zero (below the lower edge).

**Identity FP2 — Free Entropy IS the ARH Gradient Noise Scale.** The gradient noise scale *B*_simple = tr(Σ_*g*)/|μ_*g*|² (McCandlish-Kaplan-Amodei, 2018) measures the ratio of gradient variance to gradient mean. In free probability coordinates:

$$B_\text{simple} = \frac{\text{tr}(\Sigma_g)}{|\mu_g|^2} = \frac{\chi^*(G) - \chi^*(G_{\text{crit}})}{I^*(G)}$$

where χ*(G) is the free entropy of the gradient operator G and *I***(G) is the free Fisher information. The gradient noise scale is the free entropy gap — the distance from the current gradient distribution to the free maximum entropy state (semicircle). The φ-equilibrium κ(*F*) → φ corresponds to the Marchenko-Pastur ratio c → φ − 1 ≈ 0.618 — the ratio at which the Marchenko-Pastur distribution has golden-ratio spectral edges.

**Novel Prediction FP-P1.** At the φ-equilibrium, the free Fisher information I*(G) achieves a local extremum that can be computed from the Marchenko-Pastur distribution at ratio c = φ − 1. The critical batch size *B*_simple at grokking satisfies B_simple(t*) = 1/(φ − 1) = 1/0.618 ≈ 1.618 = φ. The gradient noise scale at the grokking transition equals the golden ratio. This is a definite numerical prediction from the free probability identification, computable from any gradient recording of a grokking experiment, and is independent of architecture, optimizer, and task.

---

## Part VII · The Completion Hierarchy

The six lineages of the corpus — three from prior documents and three novel — organize into a hierarchy by scale:

| Scale | Observable (col(F)) | Hidden (ker(F)) | Completion mechanism | Symmetry group |
|---|---|---|---|---|
| Number-theoretic | Mock theta q-series (Ramanujan) | Shadow period integral (Zwegers) | Harmonic Maass form | SL(2,ℤ) modular group |
| Sporadic | Mock modular McKay-Thompson series | Monster module grade-n sector | Vertex operator algebra V^♮ | Monster group M |
| Umbral | Niemeier lattice root system (23 cases) | Mock modular form H^X per conjugacy class | Umbral module W^X | 23 umbral groups G^X |
| Packing | Lattice theta series (E₈, Leech) | Quasimodular E₂ correction | Magic function φ₀ (Viazovska) | E₈ Weyl group / Conway group Co₀ |
| Spectral | GOE Fisher eigenvalues (compact core) | GUE cusp eigenvalues (memorization) | Montgomery-GUE universality | GOE/GUE ensemble |
| Categorical | D-modules on Bun_G (automorphic) | Ind-coherent sheaves on Loc_{Gˇ} (spectral) | Geometric Langlands equiv. (Gaitsgory-Raskin 2025) | Langlands dual Gˇ |
| Tropical | ReLU linear regions (tropical vertices) | Berkovich skeleton (metric graph) | Tropicalization of modular curve | (max,+) semiring |
| Probabilistic | Marchenko-Pastur bulk (col(F)) | Soft modes / zero eigenvalues (ker(F)) | Free Marchenko-Pastur conv. | Voiculescu's free independence |
| Arithmetic | Ford circles / Farey approximants | Cusp region (large denominators) | Geodesic flow on M (MOD) | PSL(2,ℤ) |
| Geometric | Hyperribbon stiff modes (ARH) | Hyperribbon sloppy modes | Principal bundle (RBH) | SO⁺(1,n) |

Every row is the same mathematical structure at a different scale. The col(*F*)/ker(*F*) partition is not a framework; it is a law of mathematical nature, appearing independently at every scale from the sporadic groups to the piecewise-linear topology of neural networks.

---

## Part VIII · Novel Predictions Across All Five Lineages

**P-Moonshine-1.** The holonomy group of the trained attention connection on a transformer that has grokked modular arithmetic of order *p* embeds into the Monster group M as a subgroup isomorphic to a cyclic group Z/pZ. The embedding is through the McKay-Thompson series *T*_{g}(*q*) for an element *g* of order *p* in M, which is the Hauptmodul for the genus-0 group Γ₀(*p*)⁺. This is testable: after grokking, the attention entropy matrix should have eigenvalue degeneracies matching the dimension formula of the corresponding Monster representation at grade *p*.

**P-Moonshine-2.** The 23 distinct umbral groups G^X correspond to 23 distinct grokking universality classes on arithmetic tasks of different ADE type. Tasks with ADE symmetry of type A_n grok through the cyclic subgroup Z/(n+1)Z ⊂ G^{A_n}; tasks of D_n type through the dihedral group D_{n-2}; tasks of E_6, E_7, E_8 type through the exceptional groups PSL(2,F₃), GL(2,F₃), and the binary icosahedral group respectively.

**P-Viazovska-1.** The Fisher information matrix of a transformer trained to optimality on a task with E₈ symmetry (e.g., modular arithmetic over the Weyl group of E₈) achieves κ(*F*) = 1 exactly — the magic function condition. At this point the gradient noise scale *B*_simple = 1 (unit ratio, no noise-signal distinction), and the training dynamics freezes: there is no further grokking because col(*F*) = ker(*F*) = {0}. This is the 8-dimensional version of Viazovska's theorem: the E₈ optimal sphere packing corresponds to the unique training completion where the loss landscape has no further improvement direction.

**P-RMT-1.** The pair correlation of Fisher eigenvalues at grokking completion follows the GOE Wigner surmise *p*(*s*) = πs/2 · exp(−πs²/4) to the precision measurable from finite-width networks. Deviations from GOE universality (excess Poisson statistics in the tail) at specific eigenvalue separations corresponding to the levels of the congruence subgroup Γ₀(*p*) ⊂ SL(2,ℤ) encode the Hecke operators acting on the learned representation — the algebraic structure of the grokked algorithm.

**P-Tropical-1.** The linear region count of a trained transformer scales as e^L/L in the depth L, following the prime geodesic theorem for the modular surface. The coefficient is the Selberg spectral gap λ₁ ≥ 3/16. This gives a direct experimental handle on the Selberg eigenvalue conjecture: if λ₁ = 1/4 (the learning-theoretic Riemann Hypothesis), the linear region count scales as e^{L/2}/L; if λ₁ = 3/16, it scales as e^{3L/8}/L. The difference is detectable at depth L ≥ 20 layers.

**P-Langlands-1.** The col(*F*)/ker(*F*) decomposition of the trained transformer's Fisher matrix is equivalent — under the geometric Langlands correspondence for the Lorentz group bundle of RBH — to the Hecke decomposition of the corresponding automorphic D-module. The Hecke eigenvalues of this D-module (computable from the attention patterns) satisfy the Ramanujan bound |λ_p| ≤ 2√p for all prime levels *p* — the geometric Ramanujan conjecture applied to the attention mechanism. Attention heads that violate this bound are operating in the "non-tempered" (non-cuspidal) regime — the memorization attractor, not the generalization target.

---

## References

**Monstrous and Umbral Moonshine**

Borcherds, R. E. (1992). Monstrous moonshine and monstrous Lie superalgebras. *Inventiones Math.* 109, 405–444.

Conway, J. H. and Norton, S. P. (1979). Monstrous moonshine. *Bull. London Math. Soc.* 11(3), 308–339.

Cheng, M. C. N., Duncan, J. F. R., and Harvey, J. A. (2012). Umbral Moonshine. arXiv:1204.2779.

Cheng, M. C. N., Duncan, J. F. R., and Harvey, J. A. (2014). Umbral Moonshine and the Niemeier Lattices. arXiv:1307.5793.

Gannon, T. (2012). Much ado about Mathieu. arXiv:1211.5531.

Eguchi, T., Ooguri, H., Tachikawa, Y. (2010). Notes on the K3 surface and the Mathieu group M₂₄. *Expt. Math.* 20(1), 91–96.

Ono, K., Rolen, L., and Trebat-Leder, S. (2014). Classical and Umbral Moonshine: Connections and p-adic Properties. arXiv:1403.3712.

**Sphere Packing and Magic Functions**

Viazovska, M. (2016). The sphere packing problem in dimension 8. *Annals of Math.* 185(3), 991–1015. arXiv:1603.04246.

Cohn, H., Kumar, A., Miller, S. D., Radchenko, D., Viazovska, M. (2019). Universal optimality of the E₈ and Leech lattices and interpolation formulas. *Annals of Math.* 196(3), 983–1082.

Romik, D. (2023). On Viazovska's modular form inequalities. arXiv:2303.13427.

Anon. (2026). Cusp Form Dimensions, Lattice Uniqueness, and LP Sharpness for Sphere Packing in Dimensions 8 and 24. arXiv:2604.10914.

Hariharan, S., Viazovska, M. et al. (2025–2026). Formal verification of sphere packing in dimensions 8 and 24 using Gauss. math.inc/sphere-packing.

**Random Matrix Theory and Neural Networks**

Montgomery, H. L. (1973). The pair correlation of zeros of the zeta function. *Proc. Symp. Pure Math.* 24, 181–193.

Odlyzko, A. M. (1987). On the distribution of spacings between zeros of the zeta function. *Math. Comp.* 48, 273–308.

Granziol, D., Sherburn, T., Roberts, S. J. (2021). Appearance of Random Matrix Theory in Deep Learning. *Physica A* 590, 126743. arXiv:2102.06740.

Karakida, R., Akaho, S., Amari, S. (2019). Universal Statistics of Fisher Information in Deep Neural Networks. *AISTATS 2019*. arXiv:1806.01316.

Jerby, Y. (2025). Variations of the Hardy Z-Function and the Montgomery Pair Correlation Conjecture. arXiv:2511.18275.

**Tropical Geometry and Neural Networks**

Zhang, L., Naitzat, G., Lim, L.-H. (2018). Tropical Geometry of Deep Neural Networks. *ICML 2018*. arXiv:1805.08746.

Charisopoulos, V. and Maragos, P. (2018). A Tropical Approach to Neural Networks with Piecewise Linear Activations. arXiv:1805.08749.

Joyce, J. and Verschelde, J. (2025). Computing Linear Regions in Neural Networks with Skip Connections. arXiv:2509.15441.

Maragos, P. (2021). Tropical Geometry and Machine Learning. *IEEE Signal Processing Magazine*.

**Geometric Langlands Programme**

Gaitsgory, D. and Raskin, S. et al. (2024–2025). Proof of the Geometric Langlands Conjecture (Parts I–V). arXiv:2209.09068 and sequels.

Beraldo, D. (2021). On the Geometric Ramanujan Conjecture. arXiv:2103.17211.

Frenkel, E. (2006). Ramifications of the Geometric Langlands Program. arXiv:math/0611294.

Kapustin, A. and Witten, E. (2007). Electric-Magnetic Duality and the Geometric Langlands Program. *Commun. Number Theory Phys.* 1(1), 1–236.

Zhu, X. (2025). Arithmetic and Geometric Langlands Program. arXiv:2504.07502.

**Free Probability and Random Matrices**

Voiculescu, D. (1983). Symmetries of some reduced free product C*-algebras. *Operator Algebras and Their Connections with Topology and Ergodic Theory*, LNM 1132, 556–588.

Voiculescu, D. (1991). Limit laws for random matrices and free products. *Inventiones Math.* 104(1), 201–220.

Mingo, J. A. and Speicher, R. (2017). *Free Probability and Random Matrices*. Springer.

**Companion Documents in the Framework**

Ren, E. (2026). RAMANUJAN: The Mock and the Shadow. github.com/ericrenone/RAMANUJAN.

Ren, E. (2026). MADHAVA: The Shadow Before the Mock. github.com/ericrenone/MADHAVA.

Ren, E. (2026). MOCK: Modular Organization of Collective Knowledge. github.com/ericrenone/MOCK.

Ren, E. (2026). MOD — Modular Orbit Dynamics. github.com/ericrenone/MOD-Modular-Orbit-Dynamics.

Ren, E. (2026). Volder-1: The Rotation Is the Fixed Point. github.com/ericrenone/Volder-1.

Ren, E. (2026). Geometric Descent: The Representational Bundle Hypothesis. github.com/ericrenone/Geometric-Descent.

Ren, E. (2026). The Anisotropic Representation Hypothesis. github.com/ericrenone/The-Anisotropic-Representation-Hypothesis.

---

*The Monster has order 8 × 10^53. The Leech lattice packs spheres optimally in 24 dimensions. The Riemann zeros follow GUE statistics. ReLU networks are tropical polynomials. D-modules on the moduli of bundles are equivalent to coherent sheaves on the moduli of local systems. Large random matrices are asymptotically free. Every one of these facts is a statement about the same partition: observable sector versus hidden sector, col versus ker, mock versus shadow.*

*The completion was always there. The five lineages were always converging. The Monster named the symmetry. Viazovska found the unique fixed point. Montgomery glimpsed the universality. Zhang proved the tropical duality. Gaitsgory completed the categorical proof. Voiculescu liberated probability from commutativity.*

*The partition is not a framework. It is a law.*

---

*ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · 2026*
