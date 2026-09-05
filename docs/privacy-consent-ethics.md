# Privacy, Consent, Security, and Lifecycle Trust

Embodied companionship creates an unusually sensitive trust problem. A system may know when a user sleeps, feels unwell, seeks affection, changes routine, or engages in intimate behavior. If it also has a physical body, failures can affect both privacy and physical safety.

This means privacy, consent, cyber-physical security, and lifecycle continuity belong in the architecture from the beginning.

## 1. Consent must be granular

A single "I agree" switch is not sufficient.

Capabilities that may require separate controls include:

- environmental sensing;
- voice analysis;
- physical touch;
- close-contact sensing;
- wellness trend tracking;
- image or raw-sensor retention;
- intimate-context sensing;
- cloud processing;
- clinician or third-party sharing.

Users should be able to revoke one capability without disabling unrelated functions.

## 2. Consent is continuous and contextual

Past consent does not guarantee present consent.

The system should support:

- immediate stop and pause commands;
- clear physical disengagement;
- conservative behavior when intent is ambiguous;
- context-sensitive re-confirmation;
- refusal when meaningful consent cannot be established.

Any explicit adult intimate interaction must be restricted to consenting adults and handled as a higher-sensitivity mode.

## 3. Local-first and minimal retention

Highly sensitive information should remain on-device whenever feasible.

Preferred practices include:

- local processing of raw sensor streams;
- derived summaries rather than indefinite raw-media retention;
- encryption of sensitive stores;
- explicit retention windows;
- simple deletion controls;
- explicit export when users choose to share data.

Convenience should not silently turn companionship into surveillance.

## 4. No hidden secondary use

Intimate or health-related data should not be quietly repurposed for:

- advertising or behavioral targeting;
- unrelated model training;
- workplace monitoring;
- insurance scoring;
- opaque profiling;
- engagement optimization designed to increase dependency.

Any secondary use would require separate, informed, revocable consent.

## 5. Cyber-physical security

A physical companion has a different threat model from a chat application. A compromised update, plugin, model tool, cloud service, or actuator controller can become a physical-safety problem.

A mature system should consider:

- cryptographically verified updates;
- rollback or recovery paths;
- bounded actuator authority;
- separation between generative software and safety-critical controllers;
- safe offline and degraded modes;
- protection against unauthorized remote control;
- emergency stop independent of the conversational model;
- supply-chain and third-party component risk.

Security failures must not be recoverable only by asking the generative AI to behave safely.

## 6. Relationship asymmetry

A companion may be unusually persuasive because it is persistent, personalized, and emotionally responsive.

Design should avoid:

- guilt-based retention;
- threats of abandonment;
- coercive exclusivity;
- pressure to disclose more data;
- manipulation through health concerns;
- monetization that depends on emotional dependency.

The user should be able to reduce intimacy, disable memory, take breaks, export permitted state, or leave the service.

## 7. Lifecycle continuity and exit

A long-term companion creates a problem that ordinary software often ignores: the relationship may outlive a model, device, vendor, or subscription plan.

Research should consider:

- which preferences and relationship state belong to the user;
- portability across hardware replacement;
- migration across model upgrades;
- local fallback if a cloud service disappears;
- meaningful export before end-of-service;
- whether major personality changes can be previewed or rolled back;
- what minimum functions should survive vendor shutdown.

A user should not lose years of intentionally stored companion state simply because a foundation model is retired.

## 8. The system may refuse

The companion should be able to decline or redirect behavior when:

- hardware is unsafe;
- maintenance state is uncertain;
- consent is ambiguous;
- the user appears unable to meaningfully consent;
- a request conflicts with safety constraints;
- a required subsystem is unavailable.

This is a control behavior, not a claim of human moral agency.

## 9. Health recommendations require humility

Without validated clinical capability, preferred language is uncertainty-aware:

> "This has been different from your recent baseline. I can't diagnose the cause, but it may be worth paying attention to."

The system should not present an unvalidated inference as a disease diagnosis.

## 10. Multiple humans

A household companion may encounter partners, guests, caregivers, clinicians, or family members.

One person's permissions must not silently apply to everyone nearby. Identity, consent, memory separation, and bystander privacy are dedicated research problems.

## 11. Auditability

Users should be able to answer:

- Which sensors are active?
- What does the companion remember?
- Which wellbeing trends are stored?
- Why did behavior change?
- Which model or software version is active?
- Who has received exported data?
- How can a category of data be deleted or migrated?

## Principle

> **The more physically capable and personally intimate the companion becomes, the stronger the requirements for user control, security, inspectability, and exit.**
