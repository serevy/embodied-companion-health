# Personal-Baseline Wellbeing Support

Embodied Companion Health treats preventive support primarily as a **longitudinal change-detection problem**, not as automated diagnosis.

The near-term question is whether a companion that participates in daily routines can notice persistent changes from a user's own baseline and surface them with low friction and appropriate uncertainty.

## Near-term scope

Public research should begin with lower-risk, broadly understandable signals such as:

- sleep and recovery patterns;
- activity and mobility trends;
- hydration-related routines or persistent dryness reported by the user;
- temperature trends from appropriate sensors;
- fatigue patterns;
- user-reported symptoms and discomfort;
- routine adherence chosen by the user.

These categories are examples, not validated product claims.

## Why personal baseline?

Population reference ranges remain important, but a long-term companion can ask an additional question:

> **Is this meaningfully different from this person's ordinary recent state?**

A useful system therefore needs to reason about:

- normal variation;
- persistence;
- sensor uncertainty;
- temporary context such as travel, exercise, illness, or sleep loss;
- the cost of false alarms;
- whether the user already knows about the change.

## Everyday integration

Wellbeing support should not turn companionship into a permanent examination.

Examples of low-friction integration include:

- waking: summarize sleep or recovery trends;
- after exercise: suggest hydration or recovery based on user-selected goals;
- during conversation: connect repeated user-reported symptoms with a reminder;
- before sleep: surface a persistent routine or fatigue change;
- on request: show a clear history of the signals and assumptions behind a suggestion.

The user should be able to disable a wellbeing feature without disabling unrelated companion functions.

## Escalation without diagnosis

An early system should prefer language such as:

> "This has been different from your recent baseline for several days. I can't tell you why, but it may be worth paying attention to or discussing with a professional."

It should avoid unsupported statements such as:

> "You have condition X."

The threshold for interrupting the user should depend not only on deviation magnitude, but also on persistence, uncertainty, and potential consequence.

## Future health domains

Some forms of close physical interaction may eventually make additional health-relevant observations possible. Potential domains include:

- oral health;
- skin health;
- sexual and reproductive health;
- richer physiological sensing;
- clinically validated screening.

These are **future research domains**, not current project capabilities. Each would require dedicated domain expertise, evidence, safety evaluation, privacy controls, and potentially medical-device regulation.

Sexual activity itself must never be represented as a diagnostic procedure, STI test, or treatment.

## Data minimization

Where possible, wellbeing functionality should:

- compute locally;
- retain derived trends instead of raw media;
- use explicit retention windows;
- expose deletion and export controls;
- separate preference data from health-related observations;
- require explicit authorization before clinician or third-party sharing.

## Research questions

The useful questions are not "How many conditions can the companion detect?" but:

- Which signals remain stable enough to support a personal baseline?
- How much history adds value?
- Can false-positive burden remain acceptable?
- Does contextual timing make health support more useful or merely more intrusive?
- Can the system communicate uncertainty clearly enough that users do not mistake it for diagnosis?

## Product boundary

The first credible milestone is intentionally modest:

> **A companion that can reliably say, "This has been different from your normal for a while," and explain why it is mentioning it.**
