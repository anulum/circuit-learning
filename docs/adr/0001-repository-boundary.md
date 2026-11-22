<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-LEARNING — repository foundation
-->

# Decision: govern design-process learning apart from training, sign-off and on-chip learning

## Context

A model that helps design circuits is useful only when its help is measured against a deterministic path on sealed items. Three things defeat that measurement:
- held-out items reaching training;
- a model shaping its own grade;
- an unpinned hosted model changing silently.

On-chip learning in spiking hardware is a different subject with a different owner.

## Decision

**What Circuit Learning owns:**
- the process model inventory;
- the grader bundle specifications;
- the learning study templates;
- the circuit graph artefact contract.

**What it imports:** only Circuit Core and Circuit Technology.

**Owned elsewhere:**

| What | Owner |
|---|---|
| training and promotion mechanics | DIRECTOR-AI |
| sealed custody | REMANENTIA |
| sign-off | Circuit Acceptance |
| on-chip spiking-network training | SC-NC Learn |

## Consequences

**What can be qualified now:** repository tooling, before any model exists.

**What it cannot qualify:** models, studies or promotions that are absent.

**What domain support requires:**
- a generated inventory checked in CI;
- sealed held-out bundles in which the near-duplicate check detects no overlap with the training bundles, at a stated recall;
- studies fixed before their first look;
- a no-model path for every operation.

**Who decides:** a verifier decides a verdict, and a person in a named role approves a rollback.
