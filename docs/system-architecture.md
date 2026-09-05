# Conceptual System Architecture

This document describes a high-level architecture for an embodied AI companion that combines physical interaction, context-aware behavior, and preventive-health support.

It intentionally avoids implementation-sensitive details such as exact sensor placement, diagnostic thresholds, proprietary control algorithms, or chemical formulations.

## 1. Perception layer

The perception layer gathers contextual signals from the environment, the user's behavior, and permitted close-contact sensing.

Potential input classes include:

- vision and proximity;
- voice and conversational context;
- pressure and tactile sensing;
- temperature and motion;
- posture and movement patterns;
- user-entered health context;
- optional wellness sensors;
- maintenance and contamination state.

Sensitive modalities should be individually permissioned rather than bundled behind a single consent switch.

## 2. Personal baseline layer

A core system capability is learning the user's ordinary range over time.

Rather than interpreting every signal against a generic population threshold, the system maintains trend summaries such as:

- typical sleep duration and recovery pattern;
- usual temperature range;
- normal activity and posture patterns;
- recurring dryness or hydration patterns;
- stable oral and skin observations;
- normal interaction energy and fatigue patterns.

The baseline layer should favor derived summaries over raw data retention wherever possible.

## 3. Context and intent layer

The system should infer the current interaction context before choosing behavior.

Example contexts:

- waking routine;
- meal preparation;
- work or concentration;
- rest and recovery;
- affectionate interaction;
- health check requested by the user;
- maintenance required;
- potentially unsafe condition.

Context detection should remain probabilistic and reversible. A mistaken inference must not lock the system into an inappropriate mode.

## 4. Affective state layer

The companion maintains a bounded internal interaction state that influences expression and initiative.

Candidate dimensions include:

- closeness;
- comfort;
- initiative;
- fatigue;
- caution;
- playfulness;
- caregiving priority;
- user-distress sensitivity.

These dimensions are system state variables, not claims of subjective feeling.

## 5. Policy and safety layer

Before physical or verbal behavior is executed, it passes through safety and consent policy.

This layer can enforce:

- adult-only boundaries for sexual interaction;
- explicit and ongoing consent;
- user stop or pause commands;
- health-state constraints;
- hardware force and temperature limits;
- maintenance locks when hygiene state is uncertain;
- contextual refusal when the user is asleep, impaired, or otherwise unable to meaningfully consent;
- clinical-boundary rules that prevent unsupported diagnosis or treatment claims.

Safety policy should be independently testable from the generative behavior model.

## 6. Behavior generation layer

The behavior layer maps context, affective state, safety constraints, and user preferences into multimodal output:

- language;
- voice tone;
- facial expression;
- gaze;
- posture;
- proximity;
- touch;
- reminders and health suggestions;
- maintenance requests.

The goal is coherent behavior rather than maximum compliance.

## 7. Physical interaction layer

The physical body may include compliant structures, soft contact surfaces, distributed sensing, thermal control, and replaceable contact components.

The architecture should emphasize:

- low-force compliance;
- fast stop behavior;
- fault detection;
- hygienic separation of clean and waste pathways;
- serviceability;
- inspectable wear state;
- graceful fallback when a subsystem becomes unavailable.

## 8. Health-awareness layer

The health layer receives derived trends and permitted sensor outputs.

Its initial role is limited to:

- trend detection;
- deviation detection;
- user-facing summaries;
- reminders;
- recommendations to seek professional evaluation when appropriate.

Any future diagnostic or therapeutic capability would be treated as a separate regulated subsystem requiring domain-specific validation.

## 9. Data boundary

A trustworthy architecture should distinguish at least four data classes:

1. **Ephemeral interaction data** — used momentarily and discarded.
2. **Preference data** — user-controlled personalization.
3. **Derived wellness trends** — retained only when useful.
4. **Highly sensitive raw health/intimate data** — minimized, protected, and preferably not retained by default.

Cloud processing should not be assumed. The safest default for highly intimate information is local-first computation with explicit export when the user chooses it.

## 10. Design principle

The architecture should preserve one invariant:

> **A companion may become more helpful as it learns more, but it must never require unnecessary intimacy in order to provide essential health or safety functions.**
