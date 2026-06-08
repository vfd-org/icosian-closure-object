# Claim ledger

**Bottom line (read this first):**

> **This bundle does not prove RH, GRH, or any zero-location theorem.**
>
> **It constructs and documents a concrete icosian object, identifies its arithmetic
> shadow, rejects the strong $\zeta$-identity, and derives the *prime side* of a Weil
> witness for a related cuspidal $L$-function.**
>
> **The remaining wall is universal positivity.**

One page, read first. Exactly what is proved, computed, interpreted, and **not**
claimed across this bundle. Every paper is consistent with this ledger; if any sentence
in a paper reads stronger than a line here, the line here governs.

> **Thesis.** The icosian closure object is **not** an RH-proof object. It is a concrete
> geometry-first object that *reaches* the RH/GRH positivity wall without crossing it:
> its theta face contains classical $\zeta$ as one factor but does not isolate it; its
> cuspidal Brandt face supplies a parameter-free *prime side* for a Weil witness; the
> remaining wall is universal positivity. **We did not cross it. We built a concrete,
> testable object that reaches it cleanly and says exactly what remains unproved.**

---

## Proved / standard theory imported

- The maximal icosian order on the 600-cell over $K=\mathbb{Q}(\sqrt5)$ is a known,
  rigorous object (maximal order in the definite quaternion algebra; underlying lattice
  $E_8$; class number one — Kirschmer–Voight).
- Its theta face gives $L(\Theta_\mathcal{I},s)=\zeta_K(s)\zeta_K(s-1)$ via the classical
  Siegel–Weil / maximal-order Eisenstein framework. **The theorem carries the identity;
  computation verifies the implementation.**
- $\zeta(s)$ is one factor through $\zeta_K(s)=\zeta(s)\,L(s,\chi_5)$.
- Weil's explicit-formula criterion: RH/GRH $\iff$ a positivity $W(h)\ge0$ for all $h$ of
  positive type (a theorem, used as the wall, not proved here).

## Computed / certified (finite, reproducible)

- Finite spectral and 9-class association-scheme data of the 600-cell.
- Maximal-order representation counts $r(\pi)=120(1+N_Q(\pi))$ at every prime type,
  including the inert prime 2 ($r(2)=600$, no anomaly) — complete short-vector
  enumeration.
- **Gate rejection of the strong "object $\leftrightarrow\zeta$" correspondence** — the
  decisive grounds are *structural*: degree ($4\ne1$), on-line density (too dense), and
  pointwise mismatch. (A provenance/no-hardcoding check is an auxiliary guardrail only.)
- Brandt/Hecke eigenvalues of the cuspidal face (level $\mathfrak p_{31}$),
  parameter-free, out-of-sample checked against point counts.
- Finite Gaussian tests of the Weil witness ($\sigma_h=3,4,5,6$, all $W(h)\ge0$). These
  **validate the implementation; they are not evidence for the universal quantifier**
  (archimedean-dominated, prime side truncated to $N(\mathfrak q)\le150$, no tail bound).

## Interpretive (clearly walled, not load-bearing)

- The compactified scale–phase–witness reading $\mathcal{V}_1$.
- VFD physical language; "one geometric object, multiple roles."
- "A single door seen from two rooms" (the joint-void picture).

## NOT claimed

- **No proof of RH. No proof of GRH.**
- **No isolation of classical $\zeta$** by the icosian object (the strong bridge is
  certified *negative*).
- **No cosmology-to-$\zeta$ implication.** One object, multiple roles, **no proven
  cross-role implication**; the bridge is open.
- No construction of the missing arithmetic surface / Frobenius degree-form.
- No proof of the universal positivity quantifier on any witness.
- The witness is a witness for a **specific cuspidal level-31 $L$-function**, **not** for
  classical $\zeta$; its relevance to RH is **structural, not a reduction**.

---

## What would actually move the wall (future work)

1. A certified **tail bound** for the truncated prime residual in the witness.
2. **Adversarial positive-type test functions** with $\mathrm{PRIME}(h)$ comparable to
   $\mathrm{ARCH}(h)$ — a sharp test of the quantifier, which the current tests are not.
3. Published Brandt matrices / eigenvalue cache with hash certificates.
4. A dependency graph (which claims rest on classical theorems, which on computation,
   which are interpretation) — this ledger is the first cut.

*Do not retreat; sharpen. The negative result — the object does not isolate $\zeta$ — is
front and centre by design: it is the credibility, not a weakness.*
