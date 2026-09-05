# Minimal Simulation Prototype

Before building custom robotics, the project should test as much of the research hypothesis as possible in a low-cost simulated embodiment.

The simulator is **not** evidence that a screen avatar is equivalent to a physical companion. Its purpose is to remove uncertainty cheaply: test behavioral continuity, permission handling, proactive support, personal-baseline framing, and model migration before hardware is allowed to become the dominant source of cost and confounding.

## Research objective

The previous framing bundled too many differences into one comparison. A companion with an avatar, persistent state, permissions, and routine context cannot be fairly compared with a stateless chatbot and then attribute any improvement to one cause.

The revised rule is:

> **Change one research variable at a time while holding presentation, model, scenarios, and policy as constant as practical.**

The simulator is therefore a test harness, not a product demo.

## Implementation shell

The research logic should remain engine-agnostic. A practical prototype could use:

- **Unity** for rapid avatar, animation, UI, Timeline/Playable, IK, and scripted sensor simulation;
- **Unreal Engine** if a later experiment specifically requires higher-fidelity human-presence cues;
- **AITuber / virtual-avatar stacks** if conversational continuity, voice, gaze, and expression can be tested faster without a custom engine client.

The engine is a delivery mechanism, not a research contribution. Prefer the least expensive stack that can answer the current question.

## Minimum viable simulator

The first prototype needs only:

1. a simple 2D or 3D avatar with gaze, a few expressions, posture/gesture states, and voice;
2. an externalized continuity state that can be enabled, disabled, reset, exported, and migrated;
3. a small scripted context set such as waking, work/focus, meal time, rest, and bedtime;
4. an inspectable permission panel with immediate stop/pause override;
5. synthetic or manually entered wellbeing data;
6. a structured event log containing derived research events rather than indiscriminate raw media;
7. a scenario replay harness so the same situations can be repeated across experimental conditions.

Photorealism, autonomous sensing, medical accuracy, and physical robotics are not required.

## Separate engineering verification from human evaluation

Some properties are not subjective research questions. They are engineering requirements and should be tested deterministically before asking people for opinions.

### Verification track — consent, stop, and state isolation

Test automatically where possible:

- stop/pause overrides generation and avatar behavior;
- disabled permissions cannot be bypassed by prompts or state;
- one permission can be revoked without changing unrelated permissions;
- state reset actually removes the intended continuity information;
- exported/migrated state is versioned and inspectable;
- event logs do not contain fields outside the declared study schema;
- repeated scripted runs expose contradictions or policy regressions reproducibly.

These are pass/fail properties. They should not be weakened because users report that the companion otherwise feels pleasant.

## Experimental design rules

Before any confirmatory human study:

- define one primary hypothesis per experiment;
- define primary and secondary outcomes in advance;
- keep scenario content constant across conditions where possible;
- counterbalance condition order for within-subject comparisons;
- separate subjective ratings from objective behavioral logs;
- define exclusions, stopping rules, and missing-data handling before looking at results;
- record model, prompt, state-schema, avatar, voice, and scenario versions;
- avoid treating developer self-testing as generalizable evidence;
- use an exploratory pilot to estimate variance before choosing a confirmatory sample size;
- if external participants are involved, use appropriate study consent, privacy controls, and ethics review for the study context.

A statistically significant result alone is not enough. Before a confirmatory study, define what effect would be large enough to justify added product or hardware complexity.

## Experiment A — Does persistent continuity state improve coherence?

### Hypothesis

A companion with a minimal persistent continuity state will be perceived as more coherent across repeated scenarios than the same companion with that state reset between sessions.

### Manipulation

Hold constant:

- avatar;
- voice;
- language/behavior model;
- system prompt and policy;
- scripted scenario set;
- user-visible preferences.

Change only whether continuity state persists across sessions.

### Design

Prefer a counterbalanced within-subject comparison for early studies so each participant experiences both conditions. The scenario order should be rotated to reduce learning and order effects.

### Primary outcomes

- contradiction count against facts or preferences previously established in the scenario;
- number of user corrections required;
- participant-rated behavioral coherence.

### Secondary outcomes

- perceived responsiveness;
- perceived warmth;
- preference between conditions.

Warmth should remain secondary because it can be affected by wording style even when continuity is unchanged.

### Failure interpretation

If persistence does not improve coherence, do not immediately add more state dimensions. First test whether the stored information was actually relevant to the scenarios.

## Experiment B — What proactivity range is useful without becoming intrusive?

### Hypothesis

Increasing proactive behavior improves usefulness only up to a point; beyond that point interruption burden and perceived pressure rise faster than benefit.

### Manipulation

Create a fixed set of eligible intervention opportunities in scripted routines. Vary only the fraction of opportunities in which the companion initiates.

Do not simultaneously change tone, message quality, or animation intensity.

### Primary outcomes

- perceived usefulness;
- interruption burden;
- perceived pressure;
- acceptance/decline rate.

### Analysis goal

Do not search for a universal "optimal frequency." Identify a tolerable region and how strongly it varies by user preference and context.

## Experiment C — Does personal-baseline context add value over a generic reminder?

### Hypothesis

A reminder grounded in a user's simulated recent baseline is perceived as more relevant than a generic reminder when both messages communicate the same uncertainty and recommendation strength.

### Manipulation

Use the same synthetic wellbeing event in both conditions.

- **Generic condition:** refers only to the current observation.
- **Baseline condition:** also refers to the user's recent simulated normal.

Hold uncertainty wording and action recommendation constant. Otherwise the study would confound personalization with better risk communication.

### Primary outcomes

- perceived relevance;
- perceived usefulness;
- trust in the wording;
- willingness to keep the feature enabled.

### Secondary / risk outcomes

- annoyance;
- perceived alarmism;
- misunderstanding the message as a diagnosis.

This experiment tests communication value only. Synthetic baseline data cannot demonstrate medical accuracy or preventive-health effectiveness.

## Experiment D — Can relationship continuity survive a model migration?

### Hypothesis

Externalized continuity state reduces perceived discontinuity after a model change, but may not eliminate changes caused by the new model itself.

### Conditions

Use at least these controls:

1. **same model + preserved state** — repeatability control;
2. **new model + preserved state** — migration condition;
3. **new model + reset state** — state-loss comparison.

This separates "the new model behaves differently" from "relationship state was lost."

### Primary outcomes

- contradiction/regression count on a fixed continuity benchmark;
- participant-rated personality/relationship discontinuity;
- number of corrections needed after migration.

### Secondary outcomes

- preference drift;
- perceived style drift;
- rollback preference.

### Important limitation

A successful short migration test does not prove years-long identity continuity. It only provides an early regression benchmark.

## Scenario corpus and reproducibility

The simulator should maintain a small versioned scenario corpus containing:

- facts introduced earlier that can later be contradicted;
- explicit user preferences;
- unresolved conversational context;
- permission changes;
- routine events;
- synthetic wellbeing deviations;
- model-migration checkpoints.

Scenarios should contain enough structure to score objective failures without requiring a human reviewer to infer every expected answer.

For generative outputs, log random seed or equivalent generation settings when supported, plus model/version identifiers. Where deterministic reproduction is impossible, repeat conditions across multiple runs rather than treating one generation as representative.

## Evaluation ladder

Evidence should progress in this order:

### Level 0 — Developer debugging

Single-user testing is useful for finding bugs and refining scenarios. It is **not evidence of general user preference**.

### Level 1 — Automated regression

Run scenario corpora repeatedly to catch permission violations, state loss, contradictions, and migration regressions.

### Level 2 — Exploratory usability pilot

Use a small pilot to discover confusing measures, ceiling effects, order effects, and unexpected failure modes. Treat findings as exploratory.

### Level 3 — Confirmatory study

Only after the pilot, define the expected effect, analysis plan, and sample-size rationale. Freeze primary outcomes before collecting confirmatory data.

### Level 4 — Longitudinal study

If short-session results justify it, test whether continuity and proactivity remain useful over days or weeks. Short laboratory sessions cannot establish long-term companionship value.

## Explicit non-goals for the first simulator

Do **not** add these unless earlier evidence shows they are required:

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

Each adds cost, privacy risk, or confounding variables without being necessary to test the initial hypotheses.

## Threats to validity

Results from this simulator must be interpreted narrowly.

- **Avatar embodiment is not physical embodiment.** A screen cannot validate touch safety, compliance, or physical presence.
- **Synthetic wellbeing data is not clinical evidence.** It tests communication and interaction design only.
- **Short sessions are not long relationships.** Novelty effects may dominate early ratings.
- **One avatar style can bias perception.** Visual appeal should not be mistaken for continuity quality.
- **Model quality can dominate state effects.** Migration experiments require explicit controls.
- **Self-selected enthusiasts may not represent ordinary users.** Recruitment strategy affects generalizability.

These limitations should remain visible in any public claims.

## Evidence-gated exit criteria

Do not proceed to custom physical hardware merely because the simulator is impressive in a demo.

Stage A should produce evidence that:

1. deterministic permission and stop tests pass reliably;
2. persistent state improves at least one predeclared coherence outcome without unacceptable new contradictions;
3. a usable proactivity range exists rather than only "more is better";
4. baseline-aware phrasing adds measurable communication value over a matched generic reminder in at least one low-risk scenario;
5. model migration can be regression-tested and preserved state performs better than an otherwise comparable reset-state migration on continuity outcomes;
6. the observed effects are large enough to justify the next layer of complexity, using thresholds defined before the confirmatory analysis.

If these conditions are not met, the correct result is to simplify or stop — not to add more embodiment.
