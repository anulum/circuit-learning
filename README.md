<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-LEARNING — repository foundation
-->

# Circuit Learning

**Two different repositories.** Circuit Learning is the learning application of the circuit design process. It is built on DIRECTOR-AI and decides how models that help design circuits are studied, graded, promoted and rolled back. It is not SC-NC Learn, which trains spiking networks on chip.

Circuit Learning is part of the **SC Neuromorphic Computing Systems** group (SC-NEUROMORPHIC-COMPUTING-SYSTEMS). The [group and project map](https://github.com/anulum/sc-neurocore/blob/main/docs/ecosystem.md) shows the whole programme and where this repository sits in it.

**What this project is not:**
- It trains nothing itself.
- It is never a sign-off verifier.

**What this checkout holds:** repository validation tooling and documentation only. Full foundation qualification is in progress.

**What does not exist yet:**
- a model inventory;
- a grader bundle;
- a study;
- a promotion record;
- a registered record format.

No training, study or promotion has been run.

## Boundary

**What it owns.** This project owns four planned records:

| Record | What it covers |
|---|---|
| The process model inventory | Every operation of every circuit repository: its learning role, its model family, the graders that judge it, its no-model baseline, and the promoted envelope bound in each release |
| The grader bundle specification | For each reward family: the pinned tools, process design kits and models, plus a training bundle and a sealed held-out bundle |
| The learning study template | The terms a study is fixed by before its first look |
| The circuit graph artefact contract | How circuit graphs and model weights are exchanged with DIRECTOR-AI |

**What it imports:** only Circuit Core and Circuit Technology.

**What it reads as records:** prototype runs, partitions and host bindings from Circuit Prototyping, and the other repositories' operation profiles.

**Who else is involved:**
- DIRECTOR-AI trains and promotes models.
- Held-out bundles and operator context stay in REMANENTIA custody.
- Experiment Ledger and Neuro Evidence Bench receive study records through their registered interfaces.

**The no-model rule.**
- Every operation has a no-model path.
- An operation with no promoted model is listed as deterministic only, so the platform is complete without any model.
- An AI step with no context record does not run.

## Current tooling

**What the repository controls inspect:**
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and the inventory;
- preflight orchestration.

**What the metadata declares:** architecture-only maturity, with empty domain capability and claim inventories.

**How to run them:**
- Use the exact environment in [Contributing](CONTRIBUTING.md).
- See [Validation](VALIDATION.md) for the scope.

## Intended evidence

A study compares one candidate with one deterministic reference, on the same sealed items in the same look. The reference is one of:
- a deterministic tool;
- a generator or high-level synthesis flow;
- a recorded human procedure.

A model baseline, when one is present, is a separate arm.

**Promotion.** It rests on evidence the study declared before it began.

**Rollback.** It is a new operation, approved by a person in a named role.

**Formats.** None of these records is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a trained model, a performed study or a benchmark result.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
