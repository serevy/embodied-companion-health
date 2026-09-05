# Minimal Simulation Prototype

Before building custom robotics, the project should test as much of the research hypothesis as possible in a low-cost simulated embodiment.

The simulation is **not** intended to prove that a screen avatar is equivalent to a physical companion. Its purpose is narrower: validate continuity, context, consent, proactive behavior, multimodal coordination, and model-migration behavior before hardware complexity is introduced.

## Research objective

The first simulation should answer one question:

> **Does a companion with a visible body, persistent continuity state, explicit permissions, and routine context feel measurably more coherent and useful than a stateless conversational baseline?**

If the answer is unclear, adding robotics is premature.

## Implementation shell

The research logic should remain engine-agnostic. A practical prototype could use:

- **Unity** — suitable for rapid 3D avatar, animation, Timeline/Playable, IK, UI, and sensor-simulation work;
- **Unreal Engine** — useful if higher-fidelity facial or human-presence studies justify the additional production cost;
- **AITuber / virtual-avatar stacks** — useful for quickly testing voice, expression, gaze, conversational initiative, and long-running personality behavior.

The engine is a delivery mechanism, not a research contribution. The project should choose the least expensive stack that can answer the current research question.

## Minimum viable simulator

The first useful prototype needs only six parts.

### 1. Avatar presentation

A simple 2D or 3D avatar with:

- gaze direction;
- a small set of facial expressions;
- basic posture or gesture states;
- voice output;
- visible acknowledgement of pause/refusal states.

Photorealism is not required.

### 2. Minimal continuity state

Maintain the smallest persistent state that could plausibly affect behavior, for example:

- current interaction stance;
- recent unresolved context;
- a bounded relationship/continuity summary;
- user preferences explicitly chosen for persistence.

The exact state representation is an experimental variable, not a fixed design commitment.

### 3. Routine context

Simulate a small number of everyday contexts such as:

- waking;
- work/focus;
- meal time;
- rest;
- bedtime.

Context may initially be selected manually or replayed from scripted scenarios. Automatic sensing is not required for the first experiment.

### 4. Consent and permission panel

Users should be able to inspect and change permissions such as:

- proactive conversation;
- persistent memory;
- wellbeing trend analysis;
- virtual proximity/affection cues;
- data retention for the current study.

A stop or pause action must override generative behavior immediately.

### 5. Synthetic wellbeing baseline

Use synthetic or manually entered data for early studies.

Examples:

- sleep duration;
- subjective fatigue;
- hydration routine;
- activity level;
- self-reported discomfort.

The simulator should test timing, uncertainty communication, and usefulness of baseline-aware prompts — not medical accuracy.

### 6. Event log for evaluation

Record research-relevant derived events rather than indiscriminate raw media, for example:

- context transition;
- state transition;
- proactive suggestion;
- user acceptance/decline;
- permission change;
- refusal/stop event;
- contradiction marker;
- model/version change.

This makes behavior review possible without requiring a surveillance-heavy dataset.

## Suggested experiment set

### Experiment A — Stateless vs continuity-aware companion

Compare the same scripted scenarios with and without persistent continuity state.

Measure:

- perceived consistency;
- contradiction frequency;
- perceived warmth/responsiveness;
- user preference;
- number of corrections required from the user.

### Experiment B — Proactivity threshold

Vary how often the companion initiates conversation or routine support.

Measure:

- usefulness;
- interruption burden;
- perceived pressure;
- decline rate.

### Experiment C — Personal-baseline phrasing

Compare generic reminders with baseline-aware, uncertainty-explicit prompts.

Measure:

- perceived relevance;
- trust;
- false-alarm annoyance;
- willingness to continue the feature.

### Experiment D — Model migration / continuity regression

Replace the underlying language model or behavior model while preserving the same external continuity state.

Measure:

- perceived personality discontinuity;
- contradiction rate;
- preference drift;
- whether rollback is needed.

This directly tests a long-lived companion problem that ordinary single-session chatbot evaluation misses.

## Explicit non-goals for the first simulator

Do **not** add these unless an earlier experiment shows they are required:

- photorealistic graphics;
- VR/AR;
- custom robotics;
- real medical sensors;
- autonomous health diagnosis;
- detailed artificial physiology;
- complex multi-axis simulated psychology;
- adult intimate simulation;
- large-scale long-term memory;
- cloud-heavy analytics.

Each item adds cost, privacy risk, or confounding variables without being necessary to test the initial hypothesis.

## Exit criteria

A simulation is successful only if it produces evidence strong enough to justify the next layer of complexity.

Before physical hardware work, the project should be able to show at least that:

1. continuity state improves perceived coherence over a stateless baseline;
2. permission and stop behavior are understandable and reliable;
3. proactive support can be tuned below an unacceptable annoyance/pressure threshold;
4. personal-baseline framing adds value over generic reminders in at least one low-risk domain;
5. model migration can be evaluated without silently destroying relationship continuity.

If these cannot be demonstrated in software, physical embodiment should remain out of scope.
