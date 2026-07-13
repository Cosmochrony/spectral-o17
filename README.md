This repository contains the source of the **O17** Cosmochrony paper  
*Fibre-Level Admissibility from Conjugate Weil Blocks:
Structural Derivation of the Pair Observable*.

This work extends the **spectral admissibility sub-programme** by resolving the
open structural gap left by **O16**:

> Why do conjugate pairs define the correct observable, and what is their structural origin?


# Context

**O16** established that:

- the correct observable in the exact Weil regime is defined on conjugate pairs
- the pair observable
  $\sigma_{\mathrm{pair}}(n) = \sigma_c(n)\,\sigma_{q-c}(n)$
  restores the correct exponent scale
- the exponent doubling
  $\delta_{\mathrm{pair}} = 2\,\delta_c$
  matches the phenomenological lower bound

However, O16 left two open structural questions:

- why conjugate blocks $(c, q-c)$ have identical dynamics
- whether the factor $r(c,q)$ is an intrinsic invariant or a pipeline artefact

This defined the precise scope of O17.


# Core Result

The paper proves that conjugate Weil blocks carry **identical dynamical information**
at the level of raw Gram–Schmidt redundancy.

This implies:

- exact equality of asymptotic exponents:
  $  \delta_{q-c} = \delta_c
  $

- structural justification of the pair observable:
  $  \sigma_{\mathrm{pair}}(n) = \sigma_c(n)\,\sigma_{q-c}(n)
  $

- exponent doubling:
  $  \delta_{\mathrm{pair}} = 2\,\delta_c
  $

Crucially, this is no longer a hypothesis but a **derived structural result**.


# Main Structural Results

## 1. Identity of conjugate dynamics

The paper proves that:

- the Weil representations satisfy
  $\rho_{q-c} = \overline{\rho_c}$
- Gram–Schmidt orthogonalisation preserves linear independence structure
- therefore the redundancy dynamics is identical for conjugate blocks

More precisely:

- exact equality holds when initial supports coincide
- structural isomorphism holds in general
- asymptotic exponents are always equal:
  $  \delta_{q-c} = \delta_c
  $

This establishes that conjugate blocks are dynamically indistinguishable.


## 2. Elimination of the factor r(c,q)

The multiplicative ratio:
$r(c,q) = \frac{\sigma_{q-c}}{\sigma_c}$

is shown to:

- arise entirely from the normalisation used in the pipeline observable
- depend on block parameters $(b_1, b_2)$
- be independent of representation-theoretic structure

Thus:

> r(c,q) is a normalisation artefact, not an invariant.

Moreover:

- $r$ is constant in $n$
- it does not affect exponents:
  $  \delta_{\mathrm{pair}} = \delta_c + \delta_{q-c} = 2\,\delta_c
  $

This removes a previously suspected arithmetic structure.


## 3. Observable-class refinement

O17 clarifies the hierarchy of observables:

- block-level observables (O12–O15)
- pair-level observables (O16)
- fibre-level observables (O17)

The key structural statement is:

> admissibility is defined on fibres of the projection Π, not on individual blocks.

Conjugate pairs $(c, q-c)$ are identified as the minimal fibres of Π
in the Weil realisation.

Therefore:

- block observables measure partial information
- pair observables measure complete fibre-level information


## 4. Structural interpretation of exponent doubling

The relation:
$  \delta_{\mathrm{pair}} = 2\,\delta_c
$

is interpreted as:

> a consequence of measuring both branches of a single fibre.

Thus, the δ-deficit observed in O12–O15 is reinterpreted as:

- not a failure of the growth law
- not a spectral mismatch
- but a **half-fibre measurement**


## 5. Requalification of O14–O15

O17 establishes that:

- O14–O15 are correct within the block-level observable class
- their results cannot recover the fibre-level exponent
- this is not a limitation of method, but of observable definition

In particular:

> no aggregation of block-level data can reconstruct a fibre-level observable.

This confirms and explains the no-go result of O15.


# Observable Hierarchy (Updated)

O17 completes the observable hierarchy:

- \(\hat\delta_{\mathrm{exact}}\):  
  block-level exponent (single branch)

- \(\delta_{\mathrm{pair}}\):  
  fibre-level exponent (physical observable)

- \(\alpha_{\mathrm{dyn}}\):  
  exponent entering the growth law

With the identification:

$  \alpha_{\mathrm{dyn}} = \delta_{\mathrm{pair}}
$

under fibre-level admissibility.


# Interpretation of the Result

The central conceptual outcome is:

> the correct observable is dictated by the non-injective structure of Π.

More precisely:

- observables correspond to equivalence classes under Π
- conjugate blocks $(c, q-c)$ form such classes
- admissibility must therefore be assessed jointly

This establishes a direct link between:

- projection non-injectivity
- observable definition
- spectral admissibility


# Structural Role of O17

O17 completes and stabilises the chain:

- **O12–O13**: exact block extraction
- **O14**: observable mismatch identified
- **O15**: block-level failure localised
- **O16**: pair observable proposed
- **O17**: pair observable derived structurally

Thus O17 establishes:

- the observable is now correctly identified
- the exponent discrepancy is fully resolved
- the remaining questions are structural, not numerical


# What O17 Adds

- proof of identity of conjugate Gram–Schmidt dynamics
- demonstration that $r(c,q)$ is a normalisation artefact
- structural justification of fibre-level observables
- clarification of the observable hierarchy
- requalification of O14–O15 as block-level analyses
- elimination of spurious arithmetic interpretations


# Outcome

O17 closes the structural gap left by O16.

The exact Weil-block framework:

- has a well-defined physical observable (fibre-level)
- produces consistent exponents
- is free of normalisation ambiguities

The theory is now:

- structurally coherent
- observationally well-defined
- aligned with the projection Π


# Residual Open Problem

The main remaining question is:

> why is the minimal fibre given by the conjugation $c \mapsto q-c$?

Currently:

- this identification is structurally consistent
- supported by representation theory
- but not yet derived from first principles of Π

A full derivation would elevate the result to a theorem of the framework.


# Open Directions

1. **Derivation of conjugate pairing from Π**  
   Prove that $c \leftrightarrow q-c$ is the minimal non-injectivity

2. **Canonical normalisation of σ**  
   Define a normalisation independent of block parameters

3. **Extension to higher-order fibres**  
   Investigate multi-branch equivalence classes

4. **Dynamical selection within the spectrum**  
   Explain the restriction to the phenomenological window

5. **Integration into the χ-framework**  
   Connect fibre structure with Born–Infeld constraints


# Status

The programme is now:

- observationally well-defined (**O17**)
- free of normalisation artefacts
- structurally aligned with Π

Remaining work is:

- derivation of fibre structure
- dynamical selection mechanisms
- extension beyond pair observables


# Repository Structure

```text
paper/
├── out/      # Compiled O17 PDF
├── tex/      # LaTeX sources
└── README.md
```
# Citation

If you reference this work, please cite:

J. Beau, Fibre-Level Admissibility from Conjugate Weil Blocks:
Structural Derivation of the Pair Observable,
Zenodo, 2026.

# Acknowledgements

Portions of the derivations, conceptual synthesis, numerical strategy,
and editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All theoretical results, computations, and interpretations remain the
sole responsibility of the author.

# Contributions

This repository is intended as a research reference.

Critical feedback, independent verification, and further analysis of:

- fibre-level observables
- projection-induced equivalence classes
- exact-block dynamics

are welcome.

Please open an issue to discuss conceptual points,
technical details, or possible extensions.
