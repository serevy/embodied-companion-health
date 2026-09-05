# Embodied Companion Health

> **Can intimate human–AI interaction become a platform for continuous preventive health?**

**Embodied Companion Health** is a public concept and research repository exploring how a physically embodied AI companion could combine everyday companionship, consensual adult intimacy, wellbeing support, and long-term health awareness.

The core idea is simple: many useful health signals appear during ordinary life — sleep, hydration, oral condition, skin condition, stress, fatigue, body temperature, movement, and close physical interaction. A future embodied AI companion could observe changes against an individual's normal baseline, support healthy routines, and encourage appropriate professional care without turning daily life into a clinical workflow.

This repository focuses on the **public research layer**: vision, system boundaries, safety, privacy, consent, affective interaction, hygiene, and a staged research roadmap. Implementation-sensitive details that may require dedicated safety review, clinical validation, or intellectual-property assessment are intentionally out of scope.

**日本語での概要:** [`docs/overview-ja.md`](docs/overview-ja.md)

## Goals

- Explore **embodied AI companionship** as more than conversation alone.
- Study how **affection, touch, routine, and wellbeing support** can coexist in one system.
- Design for **continuous baseline-aware health monitoring** rather than one-off measurements.
- Keep the companion experience human-centered: helpful, warm, autonomous, and non-clinical in everyday use.
- Treat **privacy, consent, hygiene, safety, and user agency** as first-class system requirements.
- Separate wellness-oriented screening and trend detection from medical diagnosis or treatment.

## Concept pillars

### 1. Embodied interaction

A useful physical companion needs more than a humanoid shell. The research space includes compliant materials, tactile sensing, temperature, pressure, motion, proximity, safe fluid handling, and context-aware physical behavior.

### 2. Affective state architecture

The companion should not behave like a deterministic appliance. Its behavior can be shaped by multiple internal state dimensions such as closeness, comfort, fatigue, initiative, caution, and the user's current condition. The goal is not to claim human consciousness, but to create coherent, context-sensitive interaction.

### 3. Preventive health support

The system may track changes from a user's own baseline and surface non-diagnostic signals: persistent oral changes, unusual skin changes, sleep or fatigue trends, hydration issues, mobility changes, or other deviations that may justify closer attention or professional care.

### 4. Intimacy-aware design

Consensual adult intimacy is treated as one possible interaction domain, not the sole purpose of the system. The same architecture must remain useful in non-sexual contexts such as hugs, sleep support, daily routines, caregiving, recovery, and emotional companionship.

### 5. Hygiene and maintainability

Any system involving close contact must be designed for cleaning, replaceable contact surfaces, separation of clean and waste fluid paths, contamination monitoring, maintenance reminders, and graceful degradation.

### 6. Privacy and consent

Sensitive data should default to local processing, minimal retention, explicit permissions, and narrow-purpose use. Health or intimate data must never become a hidden byproduct of companionship.

## Concept architecture

The public architecture separates perception, personal baselines, affective state, health-support logic, safety/consent/privacy controls, and embodied output rather than treating the system as one opaque end-to-end model.

See [`docs/concept-architecture.md`](docs/concept-architecture.md) for the Mermaid architecture diagram and module boundaries.

## Research questions

The project is organized around explicit open questions rather than assumed solutions, including:

- behavioral continuity and affective-state design;
- baseline-aware health support without premature diagnostic claims;
- consent in adaptive physical AI;
- meaningful companion autonomy;
- hygiene and maintainability of close-contact systems;
- privacy for intimate and longitudinal health data;
- multimodal synchronization;
- responsible evaluation of intimacy-aware HCI;
- the boundary between wellness support and regulated clinical functionality.

See [`docs/research-questions.md`](docs/research-questions.md).

## Repository map

- [`docs/overview-ja.md`](docs/overview-ja.md) — Japanese public overview / 日本語概要
- [`docs/vision.md`](docs/vision.md) — product and research vision
- [`docs/concept-architecture.md`](docs/concept-architecture.md) — high-level architecture diagram and public system boundaries
- [`docs/system-architecture.md`](docs/system-architecture.md) — conceptual system architecture
- [`docs/affective-state-model.md`](docs/affective-state-model.md) — state-driven behavior and autonomy
- [`docs/preventive-health.md`](docs/preventive-health.md) — baseline-aware health support
- [`docs/hygiene-and-fluid-management.md`](docs/hygiene-and-fluid-management.md) — hygiene and fluid-system principles
- [`docs/privacy-consent-ethics.md`](docs/privacy-consent-ethics.md) — privacy, consent, and ethical boundaries
- [`docs/research-questions.md`](docs/research-questions.md) — open research questions and evaluation themes
- [`docs/research-roadmap.md`](docs/research-roadmap.md) — staged path from concept to validated prototypes

## What this project is not

This repository does **not** claim to provide a medical device, diagnosis, treatment, STI testing, dental diagnosis, fertility assessment, or any other clinical function. Any future clinical capability would require appropriate domain expertise, validation, regulation, and safety controls.

It is also not a blueprint for unconstrained automation of intimate behavior. Adult consent, user agency, system refusal, safety limits, and contextual appropriateness are core requirements.

## Research stance

A compelling embodied companion should not merely imitate a human body. It should selectively reproduce the qualities that make close interaction comfortable and meaningful, while improving on areas where machines can offer unique value: consistent hygiene, longitudinal sensing, routine support, personalization, accessibility, and early detection of meaningful changes.

The long-term research question is therefore not:

> "How accurately can a robot copy a person?"

but rather:

> **"What should a trustworthy embodied companion become that a human partner cannot or should not be expected to be?"**

## Status

Early concept stage. Public discussion and architecture only.

No license is granted at this stage; all rights are reserved unless explicitly stated otherwise.
