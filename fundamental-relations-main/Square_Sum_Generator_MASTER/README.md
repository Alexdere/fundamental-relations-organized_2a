# Square-Sum Generator — Master Research Folder

**Project:** Fundamental Relations / pre-mathematical relational structures  
**Opened:** 2026-10-17  
**Repository policy:** append-only research; no replacement, deletion, or retroactive alteration of historical versions.  
**Permitted research-document formats:** Markdown, PDF, PNG. No DOCX.

## Mission
Investigate the structures around the exact identity
$$
T_{n-1}^2+T_n^2=T_{n^2},
\qquad T_j=j(j+1)/2,
$$
the independent prime-prefix collision at 666, the negative-Pell integer-diagonal subfamily, and further generating mechanisms. The objective is to **generate freely, prove separately, and retain failures as information**.

## Read this first
- [v0.1 original research note](versions/v0.1_square_sum_generator_2026-10-17.md) — **unchanged copy** of the historical source artifact; includes its original status claims and limitations.
- [v0.2 formalization attempt](versions/v0.2_formalization_attempt.md) — explicit frames, definitions, propositions, proofs, conjectures, and new derivations.
- [Proof-status ledger](PROOF_STATUS.md) — what is established, what is finite evidence, what remains open.
- [Ideas and research directions](RESEARCH_BRANCHES.md) — live speculative work; no premature pruning.
- [Reproducibility protocol](EXPERIMENTS.md) — exact-integer algorithms, finite search bounds, and checkpoints.
- [Source crosslinks](SOURCES.md) — repository provenance and historical context.
- [Version history](VERSION_HISTORY.md) — change log preserving chronology.

## Frame discipline
Every significant statement declares or inherits a frame:
- **F-T**: triangular numbers and elementary integer algebra.
- **F-G**: Euclidean right-triangle geometry; lengths need not be integers unless stated.
- **F-D**: Diophantine / integral-length restrictions.
- **F-P**: primes and their ordered prefix sums.
- **F-C**: bounded computation, *not* universal proof.
- **F-H**: hypotheses and exploratory analogies.
- **F-R**: application to Fundamental Relations; not automatically implied by integer algebra.

Global statements about a generator and local statements about one constructed triangle are not interchangeable.

## Working conventions
1. Historical versions are frozen; corrections appear in a later version or an errata ledger.
2. Proofs, counterexamples, finite tests, and conjectures must be labeled separately.
3. Preserve independent coincidences without asserting a causal or generative link.
4. A mismatch with an external model is a question to test, not a reason to discard an idea.
5. Avoid converting a necessary condition into a universal impossibility theorem.
6. All source files outside this master folder remain untouched.

## Quick index of the generator
$$
(a_n,b_n)=(n(n-1)/2,;n(n+1)/2),
quad a_n^2+b_n^2=n^2(n^2+1)/2.
$$
- **For all integer (n\ge1):** exact identity.
- **Integer diagonal:** iff (n^2-2m^2=-1), and then (d=nm).
- **Twin-prime-centered case:** (n-1,n+1) both prime implies (n) even and the diagonal is nonintegral in this construction.
- **Prime-prefix experiment:** (S_k=\sum_{i=1}^k p_i^2) sometimes hits triangular numbers; (S_7=666=T_{36}).

## Scope clarification — 17 October 2026

The v0.1 and v0.2 above belong to the **square-sum thread only**. The broader framework's intended v0.1 is [A Constraint-First Theory of Objects, Locality, and Persistence](../Constraint_Theory_MASTER/versions/v0.1_constraint_first_theory_2026-10-16.md), dated 16 October 2026. See its [folder guide](../Constraint_Theory_MASTER/README.md). These square-sum notes remain preserved as a separate exploration.
