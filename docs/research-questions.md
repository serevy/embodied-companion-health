# Research Questions

This document collects the public research questions that define the current scope of **Embodied Companion Health**.

The project is intentionally interdisciplinary. Many questions sit between HCI, embodied AI, robotics, affective computing, preventive health, privacy engineering, and safety.

## RQ1 — What makes an embodied companion feel coherent over time?

A useful companion should not simply generate locally plausible responses. It should behave in a way that remains recognizable across days, contexts, and interaction modes.

Questions include:

- Which internal state variables are sufficient to create continuity without overengineering a simulated psychology?
- How should closeness, fatigue, initiative, caution, and playfulness influence behavior?
- How much variability feels natural before it starts to feel inconsistent?
- How should an AI preserve personality while adapting to a user's preferences?
- How should the system represent uncertainty about the user's mood or intent?

Potential evaluation targets:

- perceived consistency
- perceived responsiveness
- relationship continuity
- user trust
- frequency of surprising or contradictory behavior

## RQ2 — Can personal baselines provide useful health awareness without becoming diagnosis?

A central hypothesis is that longitudinal observation of one individual may surface changes that population-level thresholds alone miss.

Questions include:

- Which everyday signals are stable enough to establish a meaningful personal baseline?
- How much history is needed before a deviation becomes actionable?
- How should the system distinguish transient noise from persistent change?
- How should uncertainty and false-positive risk be communicated?
- When should the system recommend self-care, monitoring, or professional consultation?

The public research target is **trend awareness and referral support**, not medical diagnosis.

## RQ3 — How can health support remain embedded in normal life instead of feeling clinical?

The system should not turn companionship into a permanent medical examination.

Questions include:

- When is the right moment to surface a health-related observation?
- How can routine support be integrated into mornings, meals, sleep, recovery, and ordinary conversation?
- How should urgency affect tone and interruption behavior?
- What interaction patterns encourage healthy behavior without becoming controlling or patronizing?

A key design goal is **low-friction care without loss of autonomy**.

## RQ4 — How should consent work in an adaptive physical AI system?

A single yes/no consent flag is insufficient for a system that can speak, sense, remember, touch, and potentially process health information.

Questions include:

- Which permissions must be independent?
- How should context-dependent consent expire or be renewed?
- How can the user inspect what is currently allowed?
- How quickly can sensing, storage, or physical interaction be stopped?
- How should the companion respond to ambiguity rather than assuming permission?
- How should safety-driven refusal interact with user preference?

Consent must be **specific, revocable, observable, and easy to change**.

## RQ5 — What does meaningful autonomy look like for a companion?

A companion that only obeys commands may feel like an appliance. A companion that behaves unpredictably or ignores the user may feel unsafe.

Questions include:

- How much initiative improves perceived companionship?
- When should the system initiate conversation, proximity, routine support, or physical affection?
- How should fatigue-like or caution-like internal states influence willingness to engage?
- How can the system say "not now" without creating confusion about system capability or human-like consciousness?

The goal is coherent **behavioral agency**, not unsupported claims of subjective experience.

## RQ6 — How should close-contact systems be designed around hygiene and maintenance?

For physical companions, hygiene is a core interaction constraint rather than an afterthought.

Questions include:

- How can clean and waste paths remain clearly separated at the system level?
- Which contact surfaces should be replaceable or inspectable?
- How should the system detect that maintenance is overdue?
- How should a maintenance requirement change available behaviors?
- How should degradation, leakage, contamination risk, or sensor faults trigger safe lockout?

Public discussion should focus on architecture and requirements rather than implementation-sensitive mechanisms.

## RQ7 — How should intimacy-aware interaction be evaluated responsibly?

Consensual adult intimacy may be a valid HCI domain, but evaluation requires particularly strong safeguards.

Questions include:

- Which research questions can first be studied through non-sexual close-contact scenarios such as hugs, rest, caregiving, and sleep support?
- Which properties are unique to adult intimate interaction and require separate evaluation?
- How should participant privacy and sensitive-data minimization be handled?
- What forms of interaction should be excluded from early-stage prototypes?
- How can the system avoid coupling access to health support with intimate behavior?

A core requirement is that **health functionality must remain available independently of intimate interaction**.

## RQ8 — How should privacy work when the most valuable data is also the most sensitive?

The companion may potentially observe unusually private aspects of daily life.

Questions include:

- Which inference should happen locally by default?
- Which raw data should never be retained?
- Can long-term baseline models be useful without keeping reconstructable source data?
- How should users delete or export their personal history?
- What information, if any, should be shareable with a clinician?
- How should intimate and health data be prevented from becoming advertising or profiling data?

Privacy is treated as a product capability, not merely a policy document.

## RQ9 — How can multimodal behavior remain synchronized?

Physical companionship involves simultaneous language, voice, gaze, posture, touch, timing, and movement.

Questions include:

- What latency becomes perceptibly unnatural in close interaction?
- How should conflicting model outputs be resolved?
- Which behavioral channel should have authority during safety-critical situations?
- How can a pause or refusal appear intentional rather than like system failure?

The research target is a **coordinated embodied response**, not a collection of independently impressive modalities.

## RQ10 — Where should the clinical boundary be drawn?

A wellness companion may eventually encounter signals relevant to medical care, but capability claims must not outrun evidence.

Questions include:

- Which observations can safely be presented as non-diagnostic trends?
- What evidence threshold should be required before recommending professional review?
- When does a feature cross from wellness into regulated medical functionality?
- How should the system communicate "I noticed a change" without implying "I diagnosed a disease"?

Any clinical extension would require dedicated experts, validation, ethics review, regulatory analysis, and a separate development process.

## Cross-cutting evaluation themes

Across all research questions, the following dimensions matter:

- safety
- consent clarity
- privacy
- perceived warmth
- behavioral coherence
- false-positive burden
- user agency
- maintainability
- accessibility
- transparency
- graceful failure

## Near-term public research priorities

The current concept stage prioritizes:

1. defining a testable affective-state model;
2. formalizing consent and permission boundaries;
3. defining personal-baseline health-support requirements;
4. establishing hygiene and maintenance requirements for close-contact hardware;
5. identifying evaluation methods that can begin with low-risk, non-sexual embodied interaction;
6. separating public architectural discussion from implementation details that require safety, clinical, or IP review.

## Open invitation

Feedback is especially valuable from researchers and practitioners in:

- HCI / Human–Robot Interaction
- embodied AI
- affective computing
- soft robotics
- privacy engineering
- preventive health
- dentistry and oral health
- medical-device safety
- accessibility
- ethics and consent design

The purpose of this repository is not to pretend these questions are solved, but to make them concrete enough to discuss, challenge, and eventually test.
