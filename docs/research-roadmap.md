# Research Roadmap

Embodied Companion Health crosses AI, HCI, robotics, privacy, safety, maintenance, and potentially regulated health domains. The project should therefore add complexity only when an earlier stage produces evidence that justifies it.

The roadmap is intentionally reduced to **four stages**.

## Stage A — Software validation

**Goal:** test the core hypotheses without building a robot.

Prototype areas:

- conversational companion behavior;
- minimal persistent state for continuity;
- explicit consent and permission state;
- user-controlled personal baselines using synthetic or manually entered data;
- uncertainty-aware wellbeing summaries;
- simulation of model upgrades and relationship-state migration.

Key questions:

- Does persistent state measurably improve continuity?
- Can proactive support remain useful without becoming annoying or paternalistic?
- Can users understand and revoke permissions easily?
- Can a model change occur without making the companion feel unrelated?

**Exit criterion:** demonstrate that continuity, consent, and baseline support create measurable value before physical embodiment is added.

## Stage B — Low-risk embodied HCI

**Goal:** determine where physical presence adds value that software alone cannot provide.

Prototype areas may include:

- gaze and proximity;
- hand contact or hugs;
- compliant low-force motion;
- temperature-controlled contact surfaces;
- basic touch and pressure sensing;
- emergency stop;
- maintenance-state communication.

Key questions:

- Which interactions genuinely benefit from a body?
- What latency and compliance feel natural enough to justify hardware complexity?
- How should the system signal approach, refusal, pause, and disengagement?
- Can physical safety remain independent of the generative model?

**Exit criterion:** show a clear HCI benefit from embodiment under low-risk conditions.

## Stage C — Personal-baseline wellbeing study

**Goal:** test whether embodiment and long-term context improve low-friction wellbeing support.

Initial domains should remain conservative, for example:

- sleep and recovery;
- activity and mobility;
- hydration-related routines;
- fatigue;
- temperature trends;
- user-reported symptoms.

Key questions:

- Which signals are stable enough to support a personal baseline?
- Can useful deviations be detected without excessive false alarms?
- Does contextual timing improve adherence or trust?
- How much raw data can be discarded while preserving value?
- How should the system escalate uncertainty without implying diagnosis?

**Exit criterion:** evidence that longitudinal, within-person support adds value beyond ordinary reminders or standalone measurements.

## Stage D — Advanced physical interaction and specialist collaboration

**Goal:** expand only where earlier stages justify the cost and risk.

Possible research domains include:

- richer soft-robotic contact;
- advanced hygiene and replaceable interfaces;
- adult intimate interaction under explicit consent and dedicated safety review;
- non-sexual close-contact interaction such as caregiving, recovery, or sleep support;
- oral, skin, or sexual-health research with appropriate specialists;
- clinically validated screening where evidence supports it.

This stage is not a promise that every domain will be built. Each extension should have its own go/no-go decision based on usefulness, safety, ethics, regulation, and maintainability.

**Exit criterion:** defined per specialist domain rather than by a single "complete humanoid" milestone.

## Parallel requirements

Across every stage:

- privacy and threat modeling;
- cyber-physical security;
- accessibility;
- adversarial testing of consent and stop behavior;
- complexity-versus-benefit review;
- lifecycle and end-of-service planning;
- model and hardware migration strategy;
- IP review before publishing implementation-sensitive discoveries.

## Near-term practical milestone

The most credible first demonstrator remains deliberately modest:

> **A software companion with transparent continuity state, inspectable permissions, personal-baseline summaries, uncertainty-aware proactive behavior, and a simulated model-migration event.**

If that does not create measurable value, adding expensive humanoid hardware would be premature.
