# v0.1.0-review — The Icosian Closure Object and Its Arithmetic Shadow

**Review draft. Not a proof of the Riemann Hypothesis.** Every claim is stamped
*verified / recalled / interpretation*; the boundary between what is established and what
is open is the load-bearing content. See [`CLAIMS.md`](CLAIMS.md) for the full ledger.

## What this is

A geometry-first study of one object — the **maximal icosian order on the 600-cell** over
K = ℚ(√5) — its exact arithmetic shadow, the certified boundary of that shadow, and an
honest localization of where the Riemann-ζ question actually sits relative to it.

## The one-sentence claim

The object's L-function is the Dedekind-type product **ζ_K(s)·ζ_K(s−1)** (C₂ = 1, no
local-2 correction) — identified by the classical Siegel–Weil / maximal-order theorem and
checked by complete short-vector enumeration. The Riemann ζ appears as **one factor among
four** but is **not isolated** (a mechanically certified negative, on structural grounds).
The object's *cuspidal* face supplies the **parameter-free prime side** of a Weil witness,
with the remaining gap localized to a single named inequality — **GRH for one cuspidal
L-function, not classical RH.**

## Contents

| file | what it is |
|---|---|
| `papers/the-positivity-wall.pdf` | the RH landscape: one positivity, many faces; where the wall is; the 𝔽₁ ledger; where this object lands |
| `papers/the-closure-object.pdf` | the object, its exact L-function ζ_K(s)ζ_K(s−1), and the certified negative (it does *not* isolate ζ) |
| `papers/witness-from-triad.pdf` | the parameter-free *prime side* of a Weil witness on the cuspidal face; gap pinned to GRH for one cuspidal L |
| `papers/note-shared-object.pdf` | the cosmology↔RH firewall (one object, multiple roles, no proven cross-role implication) |
| `companions/*.md` | interpretation only (scale–phase / V₁ reformulation), walled off |
| `engine/`, `repro/` | verification gate + certificate atlas + self-contained reproducibility |

## What is *not* claimed

No statement about the zeros of ζ (RH); no proof of any GRH; no operator/positivity
proof; no isolation of ζ by the object; **no connection between any physical or
cosmological model and RH.** The finite Gaussian positivity tests are archimedean-
dominated and truncated (N(𝔮) ≤ 150, no tail bound) — they validate the implementation,
not the universal quantifier.

## Review status

Two hostile-review passes plus a final codex referee pass applied across all four papers.
One real overclaim removed in review (the cuspidal witness is for a level-31 L-function —
GRH — not classical RH). All four PDFs compile clean (0 undefined refs/citations).

## Relationship to the triad

Builds on **[`vfd-org/icosian-triad-v600`](https://github.com/vfd-org/icosian-triad-v600)**
(v1.1.0), where the exact identity ζ_K(s)ζ_K(s−1) (C₂ = 1) is established. This bundle is
the reach-and-limit + witness layer above it; its reproducibility scripts are
self-contained copies so it stands alone.

## Reproduce

```bash
cd repro/src
python3 sim_theta_maximal_order.py   # exact identity, C₂ = 1
python3 weil_wall.py                  # prime side parameter-free; Eisenstein control fails Ramanujan
cd ../../engine && python3 run_programme.py   # hashed certificate atlas
```

Licence: Apache-2.0 (code), CC BY 4.0 (prose).
