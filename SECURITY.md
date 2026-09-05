# Security Policy

Embodied Companion Health is currently a research-concept repository, but its scope includes cyber-physical systems, sensitive data, and future embodied interaction. Security disclosures should therefore be handled conservatively even before production software exists.

## Reporting a vulnerability

Please **do not open a public issue** containing exploit details, sensitive attack paths, credentials, or information that could materially increase the exploitability of a future prototype.

Use a private GitHub security advisory for this repository when available:

https://github.com/serevy/embodied-companion-health/security/advisories/new

If that route is unavailable, contact the repository owner privately through an appropriate GitHub channel before publishing technical details.

## What should be reported privately

Examples include:

- bypasses of consent or permission enforcement;
- remote or local paths to unauthorized physical control;
- ways to bypass emergency stop or safety-state logic;
- sensitive-data exposure;
- insecure model, plugin, firmware, or update supply chains;
- privilege escalation between generative and safety-critical subsystems;
- attacks that silently alter continuity state or relationship memory;
- unsafe rollback or migration behavior;
- vulnerabilities in authentication, encryption, local storage, or export mechanisms.

## Public discussion is still welcome

High-level threat modeling, architectural safety principles, and non-exploitable design critique may be discussed publicly. The distinction is whether publication would provide a practical attack recipe against an implementation.

## Current support scope

There is no production deployment or supported release at the current concept stage. This policy exists so that future prototypes inherit a responsible disclosure path from the beginning.
