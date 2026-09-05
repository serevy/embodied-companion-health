# Research Questions

This document defines the **five public research questions** that currently frame Embodied Companion Health.

The project intentionally avoids treating every interesting subsystem as a separate research program. These questions are broad enough to organize the work but narrow enough to test in stages.

## RQ1 — What minimal state is necessary for long-term behavioral continuity?

A companion should remain recognizable across days and contexts without requiring an elaborate simulated psychology.

Questions include:

- Which persistent state actually improves perceived continuity?
- How much variation feels natural before it becomes contradictory?
- Which parts of continuity should live outside the foundation model?
- How should behavior change across model upgrades or hardware migration?
- Can users understand why the companion changed tone, initiative, or proximity?

Evaluation should compare simpler and richer state representations rather than assuming more state is better.

## RQ2 — Can personal baselines provide useful low-friction wellbeing support?

The central health-related hypothesis is that long-term within-person trends may add value beyond occasional measurements.

Questions include:

- Which low-risk signals are stable enough to support a useful personal baseline?
- How much history is needed?
- How should transient noise be separated from persistent change?
- Can false-positive burden remain acceptable?
- When should the system surface a change, remain quiet, or suggest professional consultation?
- Does contextual timing make the observation more useful or more intrusive?

The public target is **wellbeing support and trend awareness**, not diagnosis.

## RQ3 — How should consent, privacy, and cyber-physical safety constrain adaptive behavior?

An embodied companion may speak, sense, remember, touch, and potentially process health-related information. One permission flag and one generative safety prompt are not sufficient.

Questions include:

- Which permissions must be independent and revocable?
- How should ambiguity be handled?
- Which safety rules must remain outside the generative model?
- How quickly can sensing and physical action be stopped?
- What happens when network, model, sensor, or actuator components fail?
- How can the system resist unauthorized physical control or malicious updates?

A core design goal is that users can understand and change what the system is allowed to do.

## RQ4 — What makes embodied interaction safe, maintainable, and worth the hardware complexity?

Physical embodiment should only be added where it creates measurable value.

Questions include:

- Which interaction benefits cannot be reproduced adequately by voice, screens, or wearables?
- What response latency and compliance are required for comfortable low-risk touch?
- How should intent, refusal, pause, and disengagement be signaled physically?
- What hygiene and maintenance state must be visible to the user?
- Which contact interfaces should be replaceable or serviceable?
- Can the system fail closed without making routine use frustrating?

Adult intimate interaction is one possible future HCI domain, but early studies should use lower-risk close-contact scenarios whenever they answer the same research question.

## RQ5 — How should long-term trust survive model, hardware, and vendor changes?

A companion designed for years of use cannot treat model replacement or service shutdown as a normal app update.

Questions include:

- Which relationship state and preferences belong to the user?
- What should be portable across model and hardware changes?
- Can major behavioral changes be previewed, compared, or rolled back?
- What minimum capability should remain available offline?
- What happens when a vendor ends service?
- How can migration preserve continuity without copying unsafe or unnecessary sensitive data?

This is both a technical and product-governance problem.

## Cross-cutting evaluation themes

Across all five questions, evaluation should consider:

- user agency;
- safety and graceful failure;
- consent clarity;
- privacy;
- behavioral coherence;
- false-positive burden;
- perceived usefulness;
- maintainability;
- accessibility;
- inspectability;
- complexity versus measurable benefit.

## Near-term priorities

The first public research cycle should focus on:

1. a software-only continuity prototype;
2. a transparent consent and permission model;
3. synthetic or user-entered personal-baseline experiments;
4. threat modeling for a future physical system;
5. low-risk embodied interaction experiments before advanced close-contact work.

## Open invitation

Feedback is especially valuable from researchers and practitioners in:

- HCI / Human–Robot Interaction;
- embodied AI and robotics;
- affective computing;
- privacy and security engineering;
- longitudinal wellbeing research;
- accessibility;
- safety and consent design.

Specialist medical or intimate-interface domains become relevant only if later stages produce enough evidence to justify that expansion.
