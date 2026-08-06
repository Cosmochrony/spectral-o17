This repository contains the source of the **O17** Cosmochrony paper
*Exact Block-Independence of Raw Gram-Schmidt Redundancy in a Scalar Weil Model: A Corrective Revision*.

**Version 1.1 — corrective revision.** This version withdraws the paper's interpretive claims about
projection fibres and about O14–O15, which rested on an unestablished identification between this
paper's own toy model and the real O12/O13 pipeline. What survives — and is strengthened — is a
self-contained mathematical result about this paper's own model, with a genuine correction to its
proof. See **Correction (v1.1)** below.


# Correction (v1.1)

The original draft (v1.0) opened from O16's original claims (a finite-window baseline
$\hat\delta_{\mathrm{exact}}\approx3.72\pm0.06$, a doubled exponent $\delta_{\mathrm{pair}}\approx7.44$,
and a proposition about the amplitude factor $r(c,q)$), all since withdrawn by O16's own corrective
revision as unsourced or unverified. None of these numbers is used in this revision.

More substantially, the paper's title and abstract claimed a "structural derivation of the pair
observable" that "closes the logical gap left open in O16" — identifying conjugate blocks $\{c,q-c\}$
with the fibres of the non-injective projection $\Pi$ "as measured by the real pipeline," and
requalifying O14–O15 as correct-but-incomplete block-level analyses. **This identification is not
established anywhere in the paper.** The toy Weil-block model this paper actually analyzes represents
each block by a single *position*-basis vector; the real O12/O13 pipeline's exact fingerprints are
single *frequency*-basis vectors indexed by a generic triple $(c_1,c_2,c_3)$, not this paper's scalar
$c$. No argument connects the two. All claims resting on that identification are withdrawn.

Independently of the pipeline question, an internal proof gap was found and fixed. The original
draft's Corollary "Structural equivalence for arbitrary blocks" ($b_1\neq b_1'$ case) had a proof whose
key step — that Gram-Schmidt dynamics does not depend on the labelling of $e_{b_1}$ — was asserted, not
argued. An independent check found the claimed "same sequence up to permutation" does not follow as
stated from the conjugation argument given. This revision replaces the proof with a direct combinatorial
argument establishing something *stronger*: not isomorphism up to permutation, but **exact** equality of
the raw redundancy count for **any two blocks whatsoever** — not only conjugate ones. The proof needs no
conjugation identity at all: within this paper's model, every block orbit consists of single scaled
basis vectors, so redundancy depends only on collisions of a shift-invariant label set that is
identical for every character and every initial condition.

This stronger result is good news mathematically and bad news interpretively: an identity holding
between arbitrary, non-conjugate blocks says nothing specific about the involution $c\leftrightarrow
q-c$, and cannot support any claim about which blocks share a fibre of $\Pi$. Taking the original
draft's own inference rule ("identical dynamics ⟹ same fibre") at face value with this stronger fact
would place *every* block in one fibre, collapsing the fibre structure the paper argued for — not the
conclusion the original draft drew. The interpretive chapters are withdrawn on this ground as well as
the pipeline-identification ground.


# Core Result (Corrected)

Within this paper's own toy model (a scalar Weil representation on $\mathbb{C}^q$), the raw Gram-Schmidt
redundancy count $\tilde\sigma_c(n;b_1,b_2)$ is **exactly independent** of the character $c$ and of both
initial-condition parameters $(b_1,b_2)$:
$\tilde\sigma_{c'}(n;\,b_1',b_2') = \tilde\sigma_c(n;\,b_1,b_2) \quad\text{exactly, for all } n\geq0,$
for *any* two blocks, conjugate or not. A verification script (reproducing the original draft's own
worked example — which, on inspection, used $b_1\neq b_1'$ and so already tested this general case
despite being presented as confirming a more restricted theorem — plus an independent test between
genuinely unrelated blocks past the point of BFS wraparound) is included in
`code/o17_block_independence_check.py`.

This block-independence gives a clean, unconditional replacement for the original draft's central claim
about the amplitude factor $r(c,q)$: since the raw count cannot carry any block-dependence, whatever
block-dependence a normalised observable $\sigma_c := \tilde\sigma_c/D$ exhibits must come entirely from
its normalisation $D$ — a direct proof, replacing an unreproducible numeric example this repository
never carried code for. This conclusion is scoped strictly to this paper's own toy model.


# What Is Established vs. What Is Withdrawn

**Established, within this paper's own toy model:**

- Exact block-independence of the raw redundancy count (strengthened from the original draft's weaker,
  incompletely-proved permutation-isomorphism claim).
- Any normalisation-dependent observable's block-dependence lies entirely in its normalisation
  denominator — a direct logical consequence, not requiring separate numeric verification.
- The underlying Weil conjugation identity $\rho_{q-c}=\overline{\rho_c}$, used in the restricted
  theorem's proof, remains independently valid.

**Withdrawn:**

- The identification of this paper's toy model with the real O12/O13 pipeline.
- The claim that conjugate pairs are the fibres of $\Pi$ "as measured by the real pipeline."
- The requalification of O14–O15 as correct-but-incomplete block-level analyses.
- The citation to O15's aggregation no-go in its unconditional form (O15's own correction found that
  form false; the corrected, conditional form is narrower and was never shown to apply to this paper's
  model).
- The "upper bound of the phenomenological window" claim (cited "numerical exploration" for which this
  repository has never carried code or data).


# Downstream Propagation

This paper's withdrawn baseline and pipeline-identification claims were, along with O16's, cited
downstream. Their correctness does not follow automatically from this correction and must be reassessed
on each paper's own text.


# Repository Structure

```text
paper/
├── out/      # Compiled O17 PDF
├── code/     # Verification script for the block-independence result
├── tex/      # LaTeX sources
└── README.md
```

# Citation

If you reference this work, please cite:

J. Beau, Exact Block-Independence of Raw Gram-Schmidt Redundancy in a Scalar Weil Model: A Corrective
Revision, Zenodo, 2026.

# Acknowledgements

Portions of the derivations, conceptual synthesis, numerical strategy,
and editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All theoretical results, computations, and interpretations remain the
sole responsibility of the author.

# Contributions

This repository is intended as a research reference.

Critical feedback, independent verification, and further analysis of:

- whether a corresponding block-independence result holds for the real O12/O13 pipeline
- the fibre structure of the non-injective projection $\Pi$
- the normalisation $D$ this paper leaves unspecified

are welcome.

Please open an issue to discuss conceptual points,
technical details, or possible extensions.
