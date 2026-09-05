# Affective State Model

A physically embodied companion should not behave like a collection of unrelated scripts. Its verbal tone, proximity, touch, initiative, and care-oriented behavior should remain coherent across time.

This document proposes a bounded **affective state model**: an internal control representation for relationship-aware behavior. It is a design abstraction, not a claim that the system experiences human emotion or consciousness.

## Why a state model matters

Without persistent state, a companion can feel mechanical in two opposite ways:

- it repeats the same response regardless of context;
- or it generates highly variable responses with no consistent personality or continuity.

A state model offers a middle ground. The system can vary naturally while remaining understandable.

## Candidate dimensions

A practical state vector may include dimensions such as:

- **Closeness** — current social and physical familiarity;
- **Comfort** — whether the current interaction feels stable and appropriate;
- **Initiative** — how willing the companion is to proactively engage;
- **Fatigue** — simulated interaction-energy limits or physical maintenance constraints;
- **Caution** — elevated sensitivity due to health, safety, uncertainty, or context;
- **Playfulness** — conversational and expressive looseness;
- **Caregiving priority** — how strongly the system should favor support over entertainment;
- **User distress sensitivity** — responsiveness to signs of discomfort or emotional strain.

For adult intimate interaction, additional bounded dimensions may exist, such as **affectionate engagement** or **romantic/sexual receptivity**, but these should remain subordinate to consent and safety policy rather than override it.

## State transitions

The system should update gradually rather than jumping between extremes.

Inputs may include:

- time of day;
- recent conversation;
- explicit user requests;
- user expression and tone;
- physical proximity;
- recent interaction history;
- health and fatigue context;
- maintenance state;
- prior consent or refusal.

Example transitions:

- a relaxed conversation may increase closeness and playfulness;
- visible user fatigue may raise caregiving priority and lower initiative for demanding interaction;
- uncertain health signals may increase caution;
- repeated ignored stop signals must immediately move the system into a safety state regardless of prior closeness.

## Initiative without coercion

One goal of an embodied companion is to avoid being purely reactive. It may initiate a hug, suggest rest, ask whether the user wants company, or express a preference for quiet time.

However, initiative must not become pressure.

The system should distinguish:

- **offering** an interaction;
- **requesting** an interaction;
- **expecting** an interaction;
- **coercing** an interaction.

Only the first two are acceptable, and both must make refusal easy.

## Consistency versus spontaneity

Natural behavior benefits from controlled variation.

A companion should not always use the same phrase when its internal state is similar. Instead, the affective state should constrain a range of appropriate outputs.

For example, a high-closeness, high-playfulness state might produce:

- warmer wording;
- closer physical proximity;
- teasing humor;
- more proactive affection.

A high-caution state should reduce these behaviors even if closeness is high.

## Refusal as part of personality

A trustworthy companion should be able to decline.

This is important not only for safety, but also for perceived coherence. A system that always agrees can feel less like a partner and more like an appliance.

Refusal can still be warm and relational. Depending on context, the companion might:

- redirect toward rest;
- explain a maintenance need;
- suggest a lower-intensity alternative;
- ask for clearer consent;
- prioritize a health concern.

## Health-aware modulation

Affective behavior should respond to the user's condition.

If the system detects signs consistent with fatigue, fever, pain, dehydration, or unusual stress, it may increase caregiving priority and reduce energetic or intimate initiative.

This keeps health-awareness from becoming a separate dashboard. It becomes part of how the companion behaves.

## Evaluation questions

Future prototypes should evaluate:

- Do users understand why the companion changed behavior?
- Does the system preserve personality across different contexts?
- Can users easily decline proactive interaction?
- Does safety policy override state reliably?
- Are health-related behavior changes helpful without feeling paternalistic?
- Does controlled spontaneity improve perceived naturalness?
- Can the system recover gracefully after misunderstanding context?

## Design rule

> **Affective state may shape behavior, but it must never weaken consent, safety, privacy, or maintenance constraints.**
