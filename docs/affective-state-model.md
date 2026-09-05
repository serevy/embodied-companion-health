# Behavioral Continuity and Affective State

A long-lived embodied companion should not behave like a collection of unrelated scripts, but this project does **not** assume that a fixed multi-axis psychology is the correct solution.

The public research question is narrower:

> **What minimal persistent state is necessary to make behavior feel coherent across time without overengineering a simulated personality?**

## Why persistence matters

Without persistent state, a companion can fail in two opposite ways:

- it repeats the same response regardless of context;
- it produces locally plausible but globally inconsistent behavior.

A useful architecture needs continuity across conversation, routine, physical interaction, refusals, and model updates.

## State representation is an open question

Candidate concepts might include:

- familiarity or closeness;
- comfort;
- initiative;
- caution;
- interaction energy or fatigue-like limits.

These are **examples, not a prescribed state vector**. Future prototypes should test whether fewer dimensions, different dimensions, latent representations, or explicit finite-state logic work better.

The system should avoid claiming that these variables prove subjective emotion or consciousness.

## What the state may influence

A persistent interaction state may constrain:

- language and voice tone;
- timing and initiative;
- proximity;
- willingness to continue or pause;
- intensity of affectionate behavior;
- caregiving emphasis;
- how quickly the system returns to normal behavior after uncertainty or refusal.

Consent, privacy, physical safety, and maintenance constraints remain outside this state and must override it.

## Initiative without coercion

A companion that only responds to commands may feel mechanical. A companion that initiates too aggressively may feel intrusive.

Research should distinguish between:

- offering interaction;
- requesting interaction;
- assuming interaction;
- pressuring interaction.

The first two may be useful; the latter two should be avoided.

## Continuity across model updates

Long-term companionship creates a problem that ordinary chat sessions can often ignore: an underlying model may be upgraded, replaced, or retired.

A model change should not casually destroy years of user-controlled preferences or make the companion appear to become an unrelated personality overnight.

Research questions include:

- Which parts of continuity should live outside the foundation model?
- What state can be migrated safely?
- How should the system communicate unavoidable behavioral changes?
- How can users compare or roll back major personality changes?

## Evaluation

Future prototypes should test:

- perceived consistency across days and contexts;
- contradiction rate;
- user understanding of behavior changes;
- ease of declining proactive interaction;
- recovery after context mistakes;
- continuity before and after model changes;
- whether extra state actually improves experience enough to justify its complexity.

## Design rule

> **Use the smallest state representation that measurably improves continuity. Do not build a simulated psychology merely because it is possible.**
