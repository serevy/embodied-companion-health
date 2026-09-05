# Contributing

Thanks for taking an interest in **Embodied Companion Health**.

This repository is currently a **public research-concept project**, not a production medical device, robotics platform, or open-source implementation project. Contributions are therefore most useful when they improve clarity, falsifiability, safety, evidence quality, or research scope.

## Good contribution areas

Contributions are especially welcome for:

- related work and references;
- HCI / HRI evaluation methods;
- experimental-design critique;
- counterexamples or failure modes;
- privacy, consent, lifecycle, and cyber-physical safety concerns;
- accessibility considerations;
- terminology corrections;
- overclaiming or unsupported assumptions;
- simpler alternatives to overengineered proposals;
- reproducible synthetic scenarios for low-risk simulation;
- negative evidence that would narrow or falsify a hypothesis.

## Please avoid

Do not submit public pull requests containing:

- personal, intimate, health, or participant-identifying data;
- vulnerability details that could increase real-world exploitability;
- proprietary or confidential third-party information;
- detailed implementation mechanisms that may require IP review;
- unvalidated medical diagnosis or treatment claims;
- instructions that bypass consent, safety, or age-related boundaries.

See [`docs/public-private-boundary.md`](docs/public-private-boundary.md) for the intended disclosure boundary.

## Before opening a pull request

Please keep changes focused and explain:

1. what problem the change addresses;
2. what claim or assumption it affects;
3. whether it adds evidence, simplifies the design, or identifies a risk;
4. whether any new medical, safety, privacy, or IP implications are introduced.

For experimental proposals, prefer one clearly testable hypothesis over broad feature expansion.

## Research claims

Please distinguish between:

- established evidence from cited external work;
- hypotheses proposed by this project;
- implementation ideas;
- speculative future possibilities.

A compelling idea should not be presented as validated merely because it is plausible.

## Security issues

Please do **not** report exploitable security details in a public issue. See [`SECURITY.md`](SECURITY.md).

## Licensing

By contributing non-code documentation or research material, you agree that accepted contributions may be distributed under the repository's stated documentation license unless a different agreement is made in advance.

Source-code contributions, if accepted in the future, require an explicitly stated software license and may be reviewed separately.
