This repository contains the source of the **O17** Cosmochrony paper
*Exact Block-Independence of Raw Gram-Schmidt Redundancy in a Scalar Weil Model*.


# Core Result

Within a scalar Weil-representation toy model (a representation on $\mathbb{C}^q$), the raw Gram-Schmidt
redundancy count $\tilde\sigma_c(n;b_1,b_2)$ is **exactly independent** of the character $c$ and of both
initial-condition parameters $(b_1,b_2)$:
$\tilde\sigma_{c'}(n;\,b_1',b_2') = \tilde\sigma_c(n;\,b_1,b_2) \quad\text{exactly, for all } n\geq0,$
for *any* two blocks, conjugate or not. A verification script (reproducing a worked example between
blocks with $b_1\neq b_1'$, plus an independent test between genuinely unrelated blocks past the point of
BFS wraparound) is included in `code/o17_block_independence_check.py`.

This block-independence gives a clean, unconditional statement about the amplitude factor $r(c,q)$:
since the raw count cannot carry any block-dependence, whatever block-dependence a normalised observable
$\sigma_c := \tilde\sigma_c/D$ exhibits must come entirely from its normalisation $D$ — a direct proof.
This conclusion is scoped strictly to this paper's own toy model.


# What Is Established vs. What Is Open

**Established, within this paper's own toy model:**

- Exact block-independence of the raw redundancy count, for any two blocks whatsoever.
- Any normalisation-dependent observable's block-dependence lies entirely in its normalisation
  denominator — a direct logical consequence, not requiring separate numeric verification.
- The underlying Weil conjugation identity $\rho_{q-c}=\overline{\rho_c}$, used in the restricted
  theorem's proof, remains independently valid.

**Open:**

- Whether a corresponding block-independence result holds for the real O12/O13 pipeline. The toy model
  represents each block by a single *position*-basis vector; the real pipeline's exact fingerprints are
  single *frequency*-basis vectors indexed by a generic triple $(c_1,c_2,c_3)$, not this paper's scalar
  $c$. No argument connects the two.
- The fibre structure of the non-injective projection $\Pi$: the block-independence result holds too
  broadly (for any two blocks, not only conjugate ones) to serve, by itself, as a criterion for grouping
  specifically conjugate blocks into fibres.
- The normalisation $D$ this paper leaves unspecified.


# Downstream Propagation

O16's fibre-level proposal and this paper's own results were, along with each other, cited downstream in
O18–O21. Their correctness does not follow automatically from either paper and must be reassessed on
each paper's own text.


# Version History

- **v1.0** — initial release. Opened from O16's original (since withdrawn) finite-window baseline and
  amplitude-factor claims, and asserted that this paper's toy model identifies conjugate blocks with the
  fibres of $\Pi$ "as measured by the real pipeline," and that O14–O15 were correct-but-incomplete
  block-level analyses. The proof of the arbitrary-blocks corollary asserted, without arguing, that
  Gram-Schmidt dynamics is independent of $e_{b_1}$'s labelling.
- **v1.1** — corrective revision. Withdrew the pipeline identification (no argument connects the toy
  model's position-basis fingerprints to the real pipeline's frequency-basis ones) and the O14–O15
  requalification. Replaced the asserted labelling-independence step with a direct combinatorial proof
  establishing something stronger: exact block-independence for *any* two blocks, not only conjugate
  ones — proved without appeal to the conjugation identity at all. This stronger fact undercuts, rather
  than supports, the withdrawn fibre claim: applied uniformly, "identical dynamics ⟹ same fibre" would
  place every block in one fibre.
- **v1.2** — the PDF body was rewritten to state only the current, established content natively, with no
  narrative of what was withdrawn or corrected; that history is preserved here and in this paper's
  Zenodo record notes instead. The title's "A Corrective Revision" suffix was dropped. No mathematical
  content changed between v1.1 and v1.2.


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

J. Beau, Exact Block-Independence of Raw Gram-Schmidt Redundancy in a Scalar Weil Model, Zenodo, 2026.

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
