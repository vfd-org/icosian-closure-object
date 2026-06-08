Publication-ready: **No, narrowly.** The RH/GRH scope is correct, and the boxed disclaimer/future-work remark are right. The blocker is that the computed truncated functional is still called \(W(h)\) in result statements.

**1. Claim Audit**

- “not … classical Riemann zeta… GRH for that cuspidal \(L\)-function, not classical RH” ([lines 27-34](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:27>)): correct and consistent with `CLAIMS.md`.

- “\(L(\Theta_\Icos,s)=\zetaK(s)\zetaK(s-1)\) exactly” ([line 64](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:64>)): locally supported by `the-closure-object` and `repro/output/theta_maximal_order_results.json`; the full triad source is external, not in this repo.

- “eigenvalues … no point-counting, no fitting … independently checked out-of-sample to equal point counts” ([lines 72-75](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:72>)): Brandt/no-fitting is supported by code and cache. The point-count comparison is not verifiable locally; I found only prose comments.

- “global Ramanujan … follows from Hilbert-modular / Jacquet--Langlands identification” ([lines 75-77](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:75>)): plausible standard input, but uncited and not proved here. Add a real reference or weaken.

- “conductor \(775\)” ([line 82](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:82>)): supported by code comment `31*25=775`; add this formula in text.

- “\(W(h)=...=\sum_\gamma h(\gamma)\), zeros \(\rho=1/2+i\gamma\)” ([lines 84-90](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:84>)): too schematic. As written it visually assumes critical-line zeros. Say “schematically” is not enough for final release.

- Proposition “prime side is parameter-free…” ([lines 97-103](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:97>)): established only for the cached/truncated prime side \(N(\mathfrak q)\le150\). Do not let this read as the full Weil functional.

- “reproduces \(\sum_\gamma h(\gamma)\)” ([lines 114-120](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:114>)): supported by committed results; but implementation uses first 30 zeta zeros and a prime cutoff. Acceptable as implementation validation, not theorem.

- “For the cuspidal level-31 \(L\)-function, \(W(h)\ge0\)” ([lines 122-125](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:122>)): overclaim as written. The data establish \(W_{\le150}(h)\ge0\), not full \(W(h)\), since no tail bound is supplied.

- “32 Ramanujan violations” ([lines 127-133](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:127>)): verified. But “witness is not satisfied by arbitrary input” is too strong; the control shows inadmissibility, not failure of positivity.

**2. Internal Consistency**

The paper’s main scope is consistent: prime side only; archimedean side standard automorphic completion; quantifier is GRH for the cuspidal level-31 \(L\)-function; relevance to RH is structural, not a reduction.

Main inconsistency: \(W(h)\) denotes the full Weil functional in [lines 84-95](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:84>), but the computed object is truncated at \(N(\mathfrak q)\le150\) by [lines 99-100](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:99>) and [lines 147-149](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:147>). Use \(W_{\le150}\) for numerical claims.

No unresolved `\ref`/`\eqref`: there are no actual refs in the file. Citations all have bibitems.

**3. External Consistency**

- `IcosianTriad` ([lines 182-184](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:182>)): not present as a local paper. Local `the-closure-object` recalls the identity and local reproducibility data support it, but the full triad \((\Icos,C_\varphi,N_H,\sigma)\) is not locally verifiable.

- `BrandtCuspidal` ([lines 185-190](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:185>)): local `repro/src/geometric_aP.py`, `brandt_matrices.py`, and `weil_wall.py` verify the Brandt/cache/witness claims. I cannot verify the “out-of-sample checked against point counts” part locally.

- `Weil` ([lines 90-95](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:90>)): standard external theorem; not checked locally.

**4. Tightness**

- [Line 123](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:123>): replace “\(W(h)\ge0\)” with “the truncated computed functional \(W_{\le150}(h)\ge0\)”.

- [Lines 130-131](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:130>): replace “the witness is not satisfied by arbitrary input” with “the Eisenstein input is not admissible for this cuspidal Satake residual.”

- [Lines 90-95](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:90>): replace the zero-side display with a precise Weil-criterion statement that does not parametrize all zeros as \(1/2+i\gamma\).

**5. Surface Issues**

- Inconsistent \(q\) vs \(\mathfrak q\): [line 66](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:66>) should use prime ideals consistently.

- Bibliography path `icosian_brandt_cuspidal_geometry/route_b` ([line 186](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:186>)) does not match the local bundle path `repro/src`.

- “\(L_\infty\) its gamma factor, conductor 775” ([line 82](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:82>)) is ambiguous: say whether conductor is included in \(L_\infty\) or write the completed form explicitly.

**6. Top Three Fixes**

1. Rename numerical \(W(h)\) to \(W_{\le150}(h)\) everywhere numerical: [lines 122-125](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:122>), [lines 167-170](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:167>).

2. Remove or substantiate the point-count verification claim: [lines 73-75](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:73>), [lines 188-189](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:188>).

3. Make the Weil formula statement exact enough not to presuppose GRH: [lines 84-95](</mnt/c/Users/nexus/OneDrive/Documents/My Projects/vfd-crystalisation-paper/release-bundles/vfd-closure-object/papers/witness-from-triad.tex:84>).

The page-1 disclaimer and future-work remark are correct. The paper has no classical-RH overclaim. It is not publication-ready until the truncated-\(W\) wording is fixed.
