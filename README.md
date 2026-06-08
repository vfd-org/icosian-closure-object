# The Icosian Closure Object and Its Arithmetic Shadow

A geometry-first study of one object — the **maximal icosian order on the 600-cell**
over $K=\mathbb{Q}(\sqrt5)$ — its exact arithmetic shadow, the certified boundary of
that shadow, and an honest localization of where the Riemann-zeta question actually
sits relative to it.

> **Status: review draft. Not a proof of the Riemann Hypothesis.** Every claim is
> stamped *verified / recalled / interpretation*, and the boundary between what is
> established and what is open is the load-bearing content. Nothing here is pushed
> anywhere; this folder is a clean, self-contained snapshot for review.

---

## The one-sentence claim

> The icosian closure object realizes the Dedekind-type $L$-function
> $\zeta_K(s)\,\zeta_K(s-1)$ **exactly** (every Euler factor verified from the lattice;
> $C_2=1$); the Riemann $\zeta$ appears as **one factor among four** but is **not
> isolated** (a mechanically certified negative); and the Weil positivity witness for
> the object's *cuspidal* face is built parameter-free from its geometry, with the
> remaining gap localized to a single named inequality — **GRH for one cuspidal
> $L$-function, not classical RH.**

## What is *not* claimed

No statement about the location of the zeros of $\zeta$ (RH); no proof of any GRH; no
operator/positivity proof; no connection between any physical or cosmological model and
RH. The physics (§ companions) is interpretation, walled off from the mathematics.

---

## Reading order

| # | file | what it is |
|---|---|---|
| 1 | `papers/the-closure-object.pdf` | **the headline result** — the object, its exact $L$-function, the certified $\zeta$-boundary |
| 2 | `papers/witness-from-triad.pdf` | **the localization** — the Weil witness built from the object's cuspidal face; the gap pinned to GRH for one cuspidal $L$ |
| 3 | `papers/note-shared-object.pdf` | the cosmology↔RH firewall note (one object, two roles, no cross-claim) |
| — | `companions/the-positivity-wall.pdf` | expository background: where this object sits in the RH landscape (one positivity, many faces; the $\mathbb{F}_1$ ledger; the joint void) |
| — | `companions/from-a-point-to-a-universe.md` | intuition: the scale–phase / Riemann-sphere picture *(interpretation only)* |
| — | `companions/vfd-rh-reformulation.md` | the falsifiable $\mathcal{V}_1$ / witness-operator reformulation *(conjectural + a test)* |

The two core results are **1** and **2**; everything else is clearly-secondary
background, context, and interpretation.

---

## Reproduce (Python 3, `numpy`, `mpmath`, `sympy`)

```bash
cd repro/src

# Exact arithmetic identity L(Theta_I, s) = zeta_K(s) zeta_K(s-1), C_2 = 1.
# Complete Fincke–Pohst enumeration in the MAXIMAL icosian order (120 units).
python3 sim_theta_maximal_order.py
#   -> r(pi)/120 = 1+N at every prime; inert-2: r(2)=600=120*5 (no anomaly); PASS

# The Weil positivity witness, prime side built parameter-free from the
# icosian Brandt eigenvalues (cuspidal face, level p_31).
python3 weil_wall.py
#   -> gate on zeta passes; W(h) >= 0 on every test; Eisenstein control fails
#      Ramanujan (32 violations); VERDICT: parameter-free, NO_RH_PROOF_CLAIMED
```

The verification gate (the engine that certifies which geometry→arithmetic
correspondences hold and rejects fitted maps) is in `engine/`:

```bash
cd engine && python3 run_programme.py     # emits a hashed, reproducible atlas
```

Outputs are written to `repro/output/` and `repro/data/`; the committed copies are the
expected results.

---

## What lives where

```
papers/        the three core/firewall papers (.tex + compiled .pdf)
companions/    expository background + interpretation (the-positivity-wall.tex/.pdf
               and two .md essays; walled off, not load-bearing)
engine/        the verification gate, certificate atlas, F_1 ledger, joint-void
repro/src/     self-contained reproducibility scripts (icosian order + Weil witness)
repro/data/    geometric Brandt eigenvalue cache + Weil-wall output
repro/output/  maximal-order verification output
figures/       curated figures + image briefs (illustrative; not load-bearing)
```

## Relationship to the published `icosian-triad-v600` bundle

The exact identity $L(\Theta_\mathcal{I},s)=\zeta_K(s)\zeta_K(s-1)$ and the icosian
triad $(\mathcal{I}, C_\varphi, N_H, \sigma)$ are established in the companion
`icosian-triad-v600` release (v1.1, the maximal-order correction). This bundle is the
**reach-and-limit + witness** layer above it: it recalls that identity, certifies the
$\zeta$-boundary, and localizes the positivity gap. The two reproducibility scripts
here are self-contained copies so this bundle stands alone.

## Governing rule

Geometry-first; the physics is the frame, not the proof. The Riemann $\zeta$ enters
only as *one factor* of the object's $L$-function. Cosmology and RH never touch as a
claim. Lead with the verified small results and the certified negative.

## Licence

Code (`repro/`, `engine/`) under Apache-2.0; prose (`papers/`, `companions/`, this
README) under CC BY 4.0. See `LICENSE`.
