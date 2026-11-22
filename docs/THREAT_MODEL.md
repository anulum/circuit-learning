<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-LEARNING — repository foundation
-->

# Data and authority boundaries

## Present tooling

**Execution inputs.** The repository controls run on the maintained checkout and the selected development environment.

**Received inputs.** Descriptors, dependency receipts and generated inventories cannot nominate an acceptance policy or an executable.

**What the checks do.** They inspect bounded local scopes and report fixed diagnostics.

Foundation qualification is in progress.

## Future model and study inputs

**Supplied data, with no authority.** Models, weights, bundles, study terms, training sources and operator context are supplied data. They grant no authority to:
- train;
- promote;
- bind a slot;
- roll one back;
- send data to a hosted model;
- publish.

**Rollback.** A rollback is a new operation, approved by a person in a named role. The inventory never rolls a slot back by itself.

## Threats and the rules that answer them

| Threat | Rule |
| --- | --- |
| Leakage of held-out items into training | Held-out bundles stay sealed in custody. One digest is never accepted as both a training and a held-out bundle. Near-duplicate checks run before any freeze. Self-play problems from a model under training never enter its own sealed families |
| A model that games its grader | The candidate writes only its declared files, and the grader is read-only in a pinned container. Static scans read the elaborated design, never its text alone. No model grades itself |
| Poisoned training data | The screen's claim covers only the planted families. A withdrawn source is followed through its lineage |
| Contamination of public comparisons | Public benchmarks are versioned and their licences read before use. Hosted models carry a contamination caveat |
| A hosted model changing silently | Models are pinned by provider, name and version. On retirement or a change, every role and slot that used the model loses its qualification and falls back to its no-model path |
| Data leaving its class | Each role that uses a hosted model records its egress ceiling. Material that is not public never goes to a hosted model or enters this public repository, its CI or its issues |
| An AI step with unknown context | Each AI step records the context its agent read, as one custody bundle. With no record, there is no AI step |

## Residuals named, not removed

**Disjoint training and evaluation sets.** Until the reward ladder is in place, keeping them disjoint is a named trust.

**What a release names:** a paraphrase that escapes the duplicate scan rests on the reviewer. A person's approval is a key and a role, with no proof of presence.

**What a promotion record names:** the residual risk that the poisoning screen reduces but cannot exclude.

**Not claimed:** no isolation, statistical, safety or durability guarantee is claimed here.
