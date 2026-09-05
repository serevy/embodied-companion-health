# Research Roadmap

Embodied Companion Health crosses AI, HCI, robotics, privacy, safety, maintenance, and potentially regulated health domains. The project should therefore add complexity only when an earlier stage produces evidence that justifies it.

The roadmap is intentionally reduced to **four stages**.

## Stage A — Software and simulated-embodiment validation

**Goal:** test the core hypotheses without building a robot.

The preferred first demonstrator is a low-cost avatar-based simulation rather than a text-only chatbot. Unity, Unreal Engine, or an AITuber / virtual-avatar stack may be used, but the engine itself is not the research contribution. The implementation should be chosen for speed, inspectability, and experimental control.

Prototype areas:

- conversational companion behavior;
- simple 2D/3D avatar expression, gaze, posture, and voice;
- minimal persistent state for continuity;
- a small set of routine contexts such as waking, work, meals, rest, and bedtime;
- explicit consent and permission state;
- user-controlled personal baselines using synthetic or manually entered data;
- uncertainty-aware wellbeing summaries;
- simulation of model upgrades and relationship-state migration;
- event logging for continuity, refusal, permission, proactivity, and contradiction analysis.

Key questions:

- Does persistent state measurably improve continuity over a stateless baseline?
- Does visible multimodal embodiment add useful cues before physical hardware is introduced?
- Can proactive support remain useful without becoming annoying or paternalistic?
- Can users understand and revoke permissions easily?
- Can a model change occur without making the companion feel unrelated?
- Can behavior, permissions, and baseline-aware prompts be evaluated without collecting unnecessary raw media?

Explicit non-goals at this stage include photorealism, VR/AR, robotics, real medical sensors, autonomous diagnosis, detailed artificial physiology, adult intimate simulation, complex simulated psychology, and large-scale memory systems.

See [`simulation-prototype.md`](simulation-prototype.md) for the minimal experiment design.

**Exit criterion:** demonstrate that continuity, consent, baseline support, and avatar-based multimodal behavior create measurable value before physical embodiment is added.

## Stage B — Low-risk embodied HCI

**Goal:** determine where physical presence adds value that software or simulated embodiment cannot provide.

Prototype areas may include:

- gaze and proximity;
- hand contact or hugs;
- compliant low-force motion;
- temperature-controlled contact surfaces;
- basic touch and pressure sensing;
- emergency stop;
- maintenance-state communication.

Key questions:

- Which interactions genuinely benefit from a physical body?
- What latency and compliance feel natural enough to justify hardware complexity?
- How should the system signal approach, refusal, pause, and disengagement?
- Can physical safety remain independent of the generative model?
- Which apparent benefits from Stage A disappear or change when real physical contact is introduced?

**Exit criterion:** show a clear HCI benefit from embodiment under low-risk conditions that could not be established adequately in simulation.

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

The most credible first demonstrator is deliberately modest:

> **An avatar-based software companion with transparent continuity state, inspectable permissions, a few routine contexts, synthetic personal-baseline summaries, uncertainty-aware proactive behavior, and a simulated model-migration event.**

A 2D avatar, simple 3D character, Unity scene, Unreal prototype, or AITuber-style front end can all be valid if they answer the experiment with minimal extra complexity.

If that does not create measurable value, adding expensive humanoid hardware would be premature.
