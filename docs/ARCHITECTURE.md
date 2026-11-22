<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-LEARNING — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared scope.

**What received metadata cannot do:** select another policy, or grant a model, a study or a promotion.

Foundation qualification is in progress.

## Intended learning boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Process model inventory | Every operation's learning role, model family, graders and no-model baseline. Every operator-agent role, with its model version, harness digest, tool allowlist and grant. Two autonomy levels per operation: what a model has shown it can do, and what the platform permits it to do | Generated from the operation profiles and the bound slots; checked in CI. Each bound slot records its grader-bundle digest and its effective data class |
| Grader bundle specification | Per reward family: tool containers, process design kits and models pinned by digest, on open PDKs only; one training bundle and one sealed held-out bundle | No near-duplicate detected between the held-out and the training bundles, for the declared kinds of edit, each at a stated lower confidence bound on recall; kinds the check does not cover are listed as limits. Independent verification of any model-written test. Re-evaluation when a bundle version changes |
| Learning study template | The terms of a study: one deterministic reference, its arms, partitions, secondary comparisons and statistical rule | Fixed before the first look; measured concurrently on the same sealed items; caps on verifier calls and wall time per item |
| Circuit graph artefact contract | Graph tensors, feature schemas and weight files exchanged with DIRECTOR-AI | A pinned extractor that gives byte-identical tensors for the same netlist. Evaluated only against ground-truth tools on sealed design families |

## Grading rules

- **No model grades itself.**
- **The candidate is boxed in.** It writes only the files its task declares. The grader's files are read-only inside its pinned container.
- **A golden reference means formal equivalence decides.** A testbench is then only a pre-filter. The verdict states its proof mode:
  - **"equivalent"** only after an unbounded proof;
  - **"equivalent up to depth k"** after a bounded one;
  - **"not equivalent"** with a counterexample.
- **Mutation adequacy.** A simulation or property bundle states its mutation score, with a one-sided lower confidence bound, for a declared mix of mutation operators, measured on a separate seeded set after the bundle is frozen. Its claim covers that mix only.
- **Analogue yield claims.** A claim for analogue circuits states, for each process corner:
  - the sample size;
  - the estimator;
  - a one-sided confidence lower bound.

  With zero failures, a claim that at least 99.865 % of circuits pass (the one-sided three-sigma level) needs at least 2,218 independent passing samples at 95 % one-sided confidence. With weighted or importance sampling, the bound uses the effective sample size. A claim across several corners holds only if it holds at every corner.

## Study and release rules

- **Exactly one reference per study.** A comparison with a second no-model path is a second study.
- **Human references.**
  - A recorded human reference declares its participants, its pairing and its aggregation before the freeze.
  - Participants take part by consent.
  - Participants are kept away from any later model-visible use of the sealed items.
- **The poisoning screen.**
  - Its detection claim covers only the poison families planted, on a planted set fixed before its threshold is tuned.
  - Its false-positive rate is reported with an upper confidence bound measured on a declared clean reference set, and the share of excluded items is reported for each source.
- **Public comparisons.** A comparison with a model whose pretraining corpus is not disclosed carries a contamination caveat. This includes every hosted model.
- **Withdrawn training sources.**
  - A source withdrawn after use follows its data lineage to every derived dataset and model.
  - The closed set of causes includes a newly added text-and-data-mining reservation.
- **On-chip adaptation.** A deployment that adapts its own weights in the field declares an adaptation envelope beside its promoted envelope.

## Planned record schemas

- `circuit_learning.process_model_inventory.v1`
- `circuit_learning.circuit_grader_bundle_spec.v1`
- `circuit_learning.learning_study_template.v1`

The circuit graph artefact contract keeps the name DIRECTOR-AI's circuit graph family binds it by, the companion-contract prefix `sc-ncs.circuit-graph-artefact-contract.`; its schema names are set with DIRECTOR-AI when its first version is written.

These are planned names. None of them is registered or qualified here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
