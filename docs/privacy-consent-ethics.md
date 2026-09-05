# Privacy, Consent, and Ethics

Embodied companionship creates an unusually sensitive data environment. A system may know when a user sleeps, eats, feels unwell, seeks affection, experiences stress, or engages in intimate behavior.

That makes privacy, consent, and dignity foundational engineering requirements.

## 1. Consent must be granular

A single "I agree" button is not enough.

Different capabilities should have separate controls, for example:

- environmental sensing;
- voice analysis;
- touch and pressure sensing;
- wellness trend tracking;
- image retention;
- intimate-context sensing;
- health-data export;
- clinician sharing;
- cloud processing.

Users should be able to revoke one permission without disabling unrelated companion functions.

## 2. Consent is continuous

Past consent does not guarantee present consent.

The system should support:

- immediate stop and pause commands;
- clear physical disengagement behavior;
- context-sensitive re-confirmation;
- conservative behavior when intent is ambiguous;
- refusal to initiate adult intimate interaction when meaningful consent cannot be established.

## 3. Adult-only intimate interaction

Any sexual or explicitly intimate mode must be restricted to consenting adults.

The architecture should not rely only on conversational self-report for safety-critical age or capacity assumptions. Any real product would require robust product, legal, and identity-safety design appropriate to its deployment context.

## 4. Local-first processing

Highly sensitive information should remain on-device whenever feasible.

Preferred practices include:

- process raw sensor streams locally;
- retain derived summaries rather than raw media;
- encrypt sensitive stores;
- use short retention windows by default;
- expose clear deletion controls;
- require explicit export for third-party sharing.

Convenience should not silently convert a companion into a surveillance appliance.

## 5. No hidden secondary use

Intimate or health data should not be quietly repurposed for:

- advertising;
- behavioral targeting;
- unrelated model training;
- workplace monitoring;
- insurance scoring;
- social ranking;
- opaque recommendation systems.

If any secondary use is proposed, it should require separate, informed, revocable consent.

## 6. Relationship asymmetry

An AI companion may be persuasive because it is always available, highly personalized, and emotionally responsive.

That creates a power asymmetry even if the system has no subjective intent.

Design should therefore avoid:

- guilt-based retention;
- threats of abandonment;
- coercive exclusivity;
- pressure to disclose more data;
- manipulative use of health concerns;
- monetization tied to emotional dependency.

A trustworthy companion should make it easy to take breaks, reduce intimacy, disable memory, or leave the service entirely.

## 7. The system may refuse

Consent is not meaningful if only the human side has boundaries.

For safety and coherence, the companion should be able to decline or redirect interaction when:

- hardware is unsafe;
- hygiene state is uncertain;
- consent is ambiguous;
- the user appears unable to meaningfully consent;
- the requested behavior conflicts with health or safety constraints;
- maintenance is required.

This refusal is a control behavior, not a claim of human moral agency.

## 8. Health recommendations require humility

The system should communicate uncertainty explicitly.

Preferred language:

> "This looks different from your usual baseline. I can't diagnose it, but it may be worth getting checked."

Poor language:

> "You have condition X."

Without validated medical capability, the second statement overclaims what the system knows.

## 9. User access and auditability

Users should be able to answer:

- What does the companion remember about me?
- Which sensors are active?
- What health trends are stored?
- Who has received my data?
- Why did the companion change behavior?
- How do I delete a category of information?

Explainability does not require exposing every internal parameter, but meaningful behavior and data provenance should be inspectable.

## 10. Multiple humans

A household companion may encounter partners, guests, caregivers, clinicians, or family members.

The system must not assume that one user's permissions apply to everyone nearby. Identity, consent, and data separation become significantly harder in multi-person environments and should be treated as a dedicated research problem.

## Ethical principle

> **The more intimate the companion becomes, the less acceptable invisible data collection or coercive behavior becomes.**

Trust is not an optional user-experience feature. It is a prerequisite for the entire concept.
