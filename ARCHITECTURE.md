<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-LEARNING — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

**Not implemented:**
- the inventory generator;
- grader bundles;
- study templates;
- graph exchange.

The metadata keeps domain capabilities, claims and qualified formats empty.

## Intended data flow

1. **The inventory** is generated from the operation profiles of every circuit repository and the slots bound in each release. CI checks it against those profiles. It is never maintained by hand.
2. **Grader bundles** are built per reward family. Each family has two bundles:
   - **a training bundle,** which a training role may read;
   - **a held-out bundle,** which is sealed in custody and frozen before a study. Its items are checked against every training bundle of the same family for near-duplicates, and zero overlap is required.
3. **A study** is fixed before its first look. Its terms set:
   - the deterministic reference;
   - the arms;
   - the partitions and their near-duplicate check;
   - the declared secondary public comparisons;
   - the statistical rule.
4. **The outcome** is a promotion, a rejection or a rollback. Each is a record that DIRECTOR-AI acts on and that a person in a named role approves where the approval kernel requires it.

## Ownership

**This project owns** the inventory, the grader bundle specifications, the study templates and the graph artefact contract.

**Owned elsewhere:**

| What | Owner |
|---|---|
| models, training and promotion mechanics | DIRECTOR-AI |
| operation profiles, the approval kernel and model slot admission | Circuit Core |
| technology and facility readiness | Circuit Technology |
| learning records for design steps | Circuit Flow |
| the slot-rights check at release | Circuit Acceptance |
| sealed custody | REMANENTIA |

## Interpretation

**What a model's output is:** a proposal or a surrogate.

**What decides a verdict:** a verifier or a person.

**Hosted models:**
- **A retired or changed model** loses its qualification at once, and its operations fall back to their no-model path.
- **What it is sent:** never more than the data class that role's egress ceiling allows.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records and their rules.
