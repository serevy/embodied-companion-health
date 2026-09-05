# Public / Private Research Boundary

Embodied Companion Health is intentionally split into a **public research-framing layer** and a **private implementation/IP layer**.

The purpose of this boundary is not to hide the research question. It is to make the public project useful for discussion, critique, and reproducible low-risk experiments while avoiding premature disclosure of implementation details that may require dedicated safety, privacy, regulatory, or intellectual-property review.

## Public repository

The public repository should answer three questions:

1. **What problem is being studied?**
2. **Why might it matter?**
3. **How can the hypothesis be tested responsibly?**

Appropriate public content includes:

- vision and scope;
- research questions and falsifiable hypotheses;
- high-level system architecture and module responsibilities;
- behavioral-continuity concepts;
- consent, privacy, ethics, cyber-physical safety, and lifecycle principles;
- high-level hygiene and maintainability requirements;
- personal-baseline wellbeing as a research hypothesis;
- simulation and experimental methodology;
- versioned synthetic scenarios suitable for public research;
- evaluation protocols and aggregate research results;
- negative findings and design changes when they are informative;
- related work and references;
- public roadmaps and non-sensitive issues.

## Private implementation / IP repository

Private material should answer a different question:

> **How exactly might the system be built, protected, validated, or commercialized?**

Content that should normally remain private until reviewed includes:

- detailed sensor placement and sensing geometry;
- material stacks and proprietary contact-surface designs;
- detailed fluid-routing, cartridge, or internal hygiene mechanisms;
- chemical formulations;
- proprietary state-update logic or detection algorithms;
- clinically actionable thresholds or medical decision logic;
- unpublished hardware mechanisms;
- implementation details that may form part of a patent application;
- security exploit details, attack paths, credentials, or unreleased mitigations;
- raw human-subject or intimate/health data;
- private participant records;
- internal threat models that would materially increase exploitability if disclosed;
- manufacturing cost models, supplier information, and commercialization strategy;
- partner, licensing, acquisition, or negotiation notes;
- unpublished competitive and patent analysis.

## Simulation code

Prototype code does not automatically belong on either side.

A simulator may be public when:

- it implements only the already-public research layer;
- it does not reveal patent-sensitive mechanisms;
- it uses synthetic or safely publishable data;
- security review finds no sensitive deployment details; and
- a deliberate software license has been chosen.

Early prototype code may remain private while architecture and research results are public. Publishing code should be a separate decision from publishing a paper-like research description.

## Study data

Default rule:

> **Publish the method and aggregate result; do not publish sensitive raw data by default.**

For human-participant work, collection, retention, anonymization, release, and deletion rules should be defined before data collection. Intimate or health-related raw data requires substantially stronger justification than ordinary usability logs.

## Pre-publication review checklist

Before moving a private item into the public repository, ask:

- Does publication reveal an implementation mechanism rather than a research principle?
- Could this disclosure affect a future patent strategy?
- Does it expose a physical or cybersecurity weakness?
- Does it contain personal, intimate, health, partner, supplier, or negotiation information?
- Does it make a medical or safety claim beyond the available evidence?
- Can the useful research point be expressed at a higher level instead?

If the answer is uncertain, keep the material private until reviewed.

## Principle

> **Public: what, why, and how to evaluate. Private: exactly how to build, protect, and commercialize.**

This boundary may evolve as evidence, collaboration, and intellectual-property strategy evolve, but disclosure should be intentional rather than accidental.
