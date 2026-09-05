# Embodied Companion Health

> **Can a long-term embodied AI companion support wellbeing by noticing meaningful changes from a person's own baseline?**

**Embodied Companion Health** is a public concept and research repository about physically embodied AI companions that participate in everyday life over long periods of time.

**Readable documentation site:** https://serevy.github.io/embodied-companion-health/

The GitHub repository remains the source of truth for version history, issues, pull requests, releases, licensing, and research discussion.

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
- [`docs/hygiene-contact-interfaces.md`](docs/hygiene-contact-interfaces.md) — high-level hygiene and contact-interface requirements
- [`docs/privacy-consent-ethics.md`](docs/privacy-consent-ethics.md) — privacy, consent, cyber-physical security, and lifecycle trust
- [`docs/research-questions.md`](docs/research-questions.md) — five focused public research questions
- [`docs/research-roadmap.md`](docs/research-roadmap.md) — staged path from software validation to advanced research
- [`docs/simulation-prototype.md`](docs/simulation-prototype.md) — minimal Unity/Unreal/AITuber-style simulation plan before robotics
- [`docs/evaluation-protocol.md`](docs/evaluation-protocol.md) — Stage A constructs, endpoints, scoring, rater protocol, and study progression
- [`docs/public-private-boundary.md`](docs/public-private-boundary.md) — disclosure boundary for public research vs private implementation work

## Public / private boundary

This repository publishes the **research framing layer**: vision, responsibilities, research questions, system boundaries, safety principles, evaluation ideas, and low-risk simulation plans.

It intentionally avoids implementation-sensitive details such as exact sensor placement, material stacks, fluid-channel geometry, chemical formulations, proprietary detection logic, or clinically actionable thresholds. Those may require dedicated safety, IP, or regulatory review before publication.

See [`docs/public-private-boundary.md`](docs/public-private-boundary.md) before proposing implementation-sensitive material for public disclosure.

## Contributions and security

Research critique, references, falsification attempts, and simpler alternatives are welcome. See [`CONTRIBUTING.md`](CONTRIBUTING.md).

Please do not publish exploitable vulnerability details in a public issue. See [`SECURITY.md`](SECURITY.md).

## Citation and provenance

If this project influences later research, design, or implementation, citation or a link back is appreciated. See [`CITATION.md`](CITATION.md) for the preferred public-v0.1 citation guidance.

## What this project is not

This repository does **not** provide a medical device, diagnosis, treatment, STI test, dental diagnosis, fertility assessment, or autonomous healthcare system.

It also does not assume that a useful companion must imitate a human perfectly or claim human-like consciousness. The research target is trustworthy behavior and useful long-term interaction.

## Current status

**Public v0.1 concept released as `v0.1-concept`.**

The near-term goal is not a full humanoid platform. It is to test the core hypotheses with a small avatar-based simulator — potentially using Unity, Unreal Engine, or an AITuber/virtual-avatar stack — before adding custom physical hardware.

## Long-term question

> **What should a trustworthy embodied companion do uniquely well — rather than merely copying a human partner?**

## License

Unless otherwise stated, documentation, diagrams, research framing, and other non-code content are licensed under **CC BY-NC 4.0**. See [`LICENSE.md`](LICENSE.md).

Future source code, if published, will use a separately stated software license rather than inheriting the documentation license by default.
