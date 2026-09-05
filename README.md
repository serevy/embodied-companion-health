# Embodied Companion Health

> **Can a long-term embodied AI companion support wellbeing by noticing meaningful changes from a person's own baseline?**

**Embodied Companion Health** is a public concept and research repository about physically embodied AI companions that participate in everyday life over long periods of time.

The core hypothesis is deliberately narrow:

> A companion that is continuously present may be able to support wellbeing with less friction by learning a user's ordinary patterns and surfacing meaningful deviations — without pretending to be a doctor.

Embodiment matters because daily life contains context that occasional measurements miss: sleep, activity, recovery, hydration-related patterns, routine, posture, conversation, touch, proximity, and other user-permitted signals.

Companionship matters because a useful system must do more than collect data. It must behave coherently, respect boundaries, remain safe when models or hardware fail, and preserve user trust over years rather than sessions.

## What this project focuses on

### 1. Long-term embodied companionship

How can an AI companion remain useful, understandable, and behaviorally coherent across days, model updates, hardware changes, and changing user preferences?

### 2. Personal-baseline wellbeing support

Can low-friction longitudinal observation identify useful changes from a person's own recent normal while communicating uncertainty and avoiding unsupported medical claims?

### 3. Trust, consent, safety, and privacy

A physical companion may perceive highly sensitive parts of daily life and can also affect the physical world. Consent, data minimization, cyber-physical security, safe refusal, and user control therefore belong in the architecture rather than in a policy appendix.

### 4. Embodied HCI and maintainability

Comfortable physical interaction requires compliant behavior, predictable safety limits, inspectable maintenance state, hygienic contact interfaces, and graceful failure.

## Intimacy is a research context, not the whole product

Close physical interaction can be affectionate, comforting, romantic, caregiving, practical, or — for consenting adults — sexual.

This project treats adult intimacy as one possible HCI domain, not as a requirement for health support and not as the sole purpose of the system. Essential wellbeing and safety functions must remain available without intimate interaction.

## What is intentionally future-facing

Potential future domains include oral health, skin health, sexual health, richer close-contact sensing, and clinically validated screening. These are **not current capabilities** and would require domain experts, evidence, safety review, and potentially medical-device regulation before any diagnostic or therapeutic claims could be made.

## Repository map

- [`docs/overview-ja.md`](docs/overview-ja.md) — 日本語概要
- [`docs/vision.md`](docs/vision.md) — research vision and scope
- [`docs/system-architecture.md`](docs/system-architecture.md) — consolidated conceptual architecture
- [`docs/affective-state-model.md`](docs/affective-state-model.md) — behavioral continuity as an open research problem
- [`docs/preventive-health.md`](docs/preventive-health.md) — personal-baseline wellbeing support
- [`docs/hygiene-and-fluid-management.md`](docs/hygiene-and-fluid-management.md) — high-level hygiene and contact-interface requirements
- [`docs/privacy-consent-ethics.md`](docs/privacy-consent-ethics.md) — privacy, consent, cyber-physical security, and lifecycle trust
- [`docs/research-questions.md`](docs/research-questions.md) — five focused public research questions
- [`docs/research-roadmap.md`](docs/research-roadmap.md) — staged path from software validation to advanced research

## Public / private boundary

This repository publishes the **research framing layer**: vision, responsibilities, research questions, system boundaries, safety principles, and evaluation ideas.

It intentionally avoids implementation-sensitive details such as exact sensor placement, material stacks, fluid-channel geometry, chemical formulations, proprietary detection logic, or clinically actionable thresholds. Those may require dedicated safety, IP, or regulatory review before publication.

## What this project is not

This repository does **not** provide a medical device, diagnosis, treatment, STI test, dental diagnosis, fertility assessment, or autonomous healthcare system.

It also does not assume that a useful companion must imitate a human perfectly or claim human-like consciousness. The research target is trustworthy behavior and useful long-term interaction.

## Current status

**Concept / research-framing stage.**

The near-term goal is not a full humanoid platform. It is to determine whether the core hypotheses are testable with smaller software and low-risk embodied prototypes.

## Long-term question

> **What should a trustworthy embodied companion do uniquely well — rather than merely copying a human partner?**

No license is granted at this stage; all rights are reserved unless explicitly stated otherwise.
