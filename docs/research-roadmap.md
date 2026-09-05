# Research Roadmap

Embodied Companion Health is intentionally staged. The concept crosses AI, robotics, HCI, hygiene engineering, privacy, and potentially regulated health domains. Trying to solve everything at once would make both research and safety evaluation weaker.

The roadmap below starts with software-only work and progressively introduces physical embodiment and health-awareness.

## Phase 0 — Concept and requirements

**Goal:** define the problem before building hardware.

Deliverables:

- public vision and system boundaries;
- use-case catalog;
- consent and privacy model;
- affective-state vocabulary;
- preliminary risk register;
- separation between wellness functions and clinical claims;
- identification of areas that should remain private pending IP or safety review.

Success means the project can explain what it is, what it is not, and why the architecture is trustworthy enough to prototype.

## Phase 1 — Software companion simulation

**Goal:** test interaction logic without a robot body.

Prototype:

- conversational companion;
- persistent but bounded affective state;
- routines for waking, meals, work, rest, and bedtime;
- user-controlled wellness observations;
- explicit consent state machine;
- health trend summaries using synthetic or manually entered data.

Research questions:

- Does state-driven behavior feel more coherent than stateless generation?
- Can the system proactively care without becoming annoying or paternalistic?
- Are refusal and consent transitions understandable?
- How much personal history is needed before the system feels consistent?

## Phase 2 — Low-risk embodied interaction

**Goal:** introduce physical presence without intimate or clinical functions.

Prototype domains:

- gaze and proximity;
- safe touch and pressure sensing;
- hand-holding or hugs;
- compliant movement;
- temperature-controlled contact surfaces;
- emergency stop and fault handling.

Research questions:

- What latency makes touch responses feel natural?
- How should a robot signal intent before approaching?
- Which physical cues make refusal or disengagement legible?
- How can contact remain comfortable across different users and body types?

## Phase 3 — Everyday wellness sensing

**Goal:** connect embodiment with low-risk preventive-health awareness.

Possible domains:

- sleep and recovery summaries;
- posture and movement trends;
- temperature and activity changes;
- hydration reminders;
- user-reported symptoms;
- visible external changes when the user explicitly opts in.

Research questions:

- Can personal baselines reduce unnecessary alerts?
- How should uncertainty be communicated?
- Which observations are useful enough to justify data collection?
- How much raw data can be discarded while preserving useful trends?

## Phase 4 — Hygiene and replaceable contact systems

**Goal:** validate maintenance architecture before higher-contact applications.

Prototype areas:

- removable contact modules;
- sealed clean and waste paths;
- leak and installation detection;
- maintenance-state machine;
- cartridge replacement workflows;
- cleaning verification;
- safe lockout when hygiene cannot be confirmed.

Research questions:

- Can routine maintenance be made discreet and low-friction?
- Which components should be disposable, replaceable, or washable?
- How should the system communicate hygiene state without disrupting companionship?

## Phase 5 — Advanced close-contact HCI

**Goal:** study richer adult and non-adult close-contact interaction under strict safety and consent controls.

This phase may include research into:

- highly compliant artificial skin;
- richer tactile sensing;
- context-aware pressure response;
- safe thermal and moisture control;
- adult intimate interaction as one explicitly permissioned domain;
- emotional-state transitions during high-closeness interaction.

Any adult intimate research must be restricted to consenting adults and should be evaluated with dedicated ethics and safety review.

Research questions:

- Can the same physical architecture support comforting, caregiving, romantic, and adult intimate contexts without conflating them?
- Does bounded autonomous initiative improve partner-like interaction?
- Can health-awareness remain optional and non-coercive during close contact?

## Phase 6 — Clinically adjacent research

**Goal:** explore whether selected wellness signals justify formal clinical collaboration.

Before any diagnostic or therapeutic claim, the project would require:

- clinicians and domain specialists;
- validated measurement protocols;
- dataset governance;
- safety and bias evaluation;
- human-subject research oversight where applicable;
- appropriate regulatory strategy.

Potential research areas might include screening or trend detection in oral health, skin health, mobility, hydration, or other domains — but only where evidence supports the transition.

## Phase 7 — Integrated companion platform

**Goal:** unify companionship, embodiment, hygiene, user-controlled health trends, and bounded autonomy into a coherent long-lived system.

The target is not a robot that performs the maximum number of functions.

The target is a companion that:

- behaves consistently;
- respects boundaries;
- maintains itself safely;
- notices useful changes;
- communicates uncertainty;
- improves daily life without demanding unnecessary data or dependence.

## Parallel workstreams

Across all phases, the following should progress continuously:

- threat modeling and privacy engineering;
- accessibility;
- mechanical safety;
- adversarial testing of consent logic;
- maintenance economics;
- personalization without dependency manipulation;
- interoperability with professional healthcare only when explicitly authorized;
- intellectual-property review before publishing implementation-sensitive discoveries.

## First practical milestone

The most realistic near-term demonstrator is deliberately modest:

> **A software companion with a transparent affective-state model, user-controlled wellness baselines, consent-aware proactive behavior, and a simulated embodied interface.**

That prototype can validate a large part of the concept before expensive robotics work begins.
