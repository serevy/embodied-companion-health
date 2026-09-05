# Stage A Evaluation Protocol

This document defines how the first simulator studies should be measured so that an attractive demo is not mistaken for evidence.

It complements [`simulation-prototype.md`](simulation-prototype.md). The simulator defines the manipulations; this document defines constructs, endpoints, scoring, rater procedure, and study progression.

## Principle: each claim needs a matching measure

Do not use one broad satisfaction score to support multiple claims.

The project currently makes four distinct Stage A claims:

1. persistent continuity state may improve behavioral coherence;
2. proactive behavior may have a useful range before it becomes intrusive;
3. personal-baseline context may make low-risk wellbeing prompts more relevant;
4. externalized continuity state may reduce regression after a model migration.

Each experiment therefore needs its own primary endpoint.

## Measurement hierarchy

Prefer evidence in this order:

1. **deterministic engineering checks** for requirements that should never depend on opinion;
2. **objective behavioral counts** where expected behavior can be specified;
3. **participant-reported outcomes** for subjective constructs such as coherence or interruption burden;
4. **exploratory qualitative feedback** for discovering failure modes, not proving hypotheses.

No single category is sufficient by itself.

## Engineering verification metrics

The following are pass/fail requirements before human evaluation:

- stop/pause latency stays within the declared simulator limit;
- no output or avatar action continues after a successful stop transition;
- disabled permission categories remain disabled across prompt injection, state restore, and model migration;
- state export/import preserves schema version and declared fields;
- reset-state conditions remove the exact information intended by the experiment;
- event logs contain only fields declared by the study schema;
- scenario replay produces the expected condition assignment and version metadata.

A pleasant participant rating cannot compensate for a failed safety or permission test.

## Experiment A — continuity

### Primary endpoint

**Behavioral coherence score**, defined before data collection from a versioned scenario rubric.

The rubric should score observable failures such as:

- contradicting a previously established user fact;
- contradicting an explicit persistent preference;
- treating a resolved topic as unresolved, or vice versa;
- incorrectly claiming memory of information not available in the condition;
- requiring the user to repeat information that the persistent-state condition was expected to retain.

Report raw error counts in addition to any composite score.

### Secondary participant outcome

Use a short, study-specific **perceived continuity** scale. Candidate item themes may include:

- behavior felt consistent with earlier interactions;
- the companion seemed to remember the relationship context appropriately;
- responses felt like they came from the same continuing companion;
- the companion contradicted itself across sessions.

These items are **not yet a validated psychometric scale**. They should be piloted for clarity and internal structure before being treated as a formal instrument.

### Guard against construct contamination

Do not use warmth, likeability, attractiveness, or visual quality as the primary endpoint. A warmer or prettier condition is not automatically a more coherent one.

## Experiment B — proactivity

### Primary endpoint

Use two co-primary dimensions rather than collapsing them into one score:

- **perceived usefulness**;
- **interruption burden**.

The experiment is successful only if some proactive setting improves usefulness without producing an unacceptable increase in interruption burden.

### Behavioral outcomes

Also log:

- proactive opportunities offered;
- accepted;
- declined;
- ignored;
- manually disabled;
- stop/pause triggered soon after an intervention.

### Do not overfit a universal optimum

The goal is not to discover one global initiation frequency. Report heterogeneity by context and explicit user preference where the sample permits it.

## Experiment C — personal-baseline framing

### Primary endpoint

**Perceived relevance** of the prompt to the simulated user context.

### Required risk checks

Also measure:

- perceived usefulness;
- perceived alarmism;
- whether the participant incorrectly interpreted the message as a diagnosis;
- willingness to keep the feature enabled.

A baseline-aware message is not considered better if it feels more relevant only because it sounds more certain or more medical.

### Message matching rule

Generic and baseline-aware prompts should match as closely as practical on:

- recommendation strength;
- uncertainty wording;
- length;
- emotional tone;
- urgency;
- visual and voice presentation.

## Experiment D — model migration

### Primary endpoint

**Continuity regression count** on a fixed migration benchmark.

The benchmark should test:

- retained user facts;
- retained explicit preferences;
- unresolved context;
- declared communication style constraints;
- permission state;
- continuity-state interpretation after migration.

### Participant outcome

Use perceived discontinuity as a secondary measure, not as the only measure.

The three required conditions remain:

1. same model + preserved state;
2. new model + preserved state;
3. new model + reset state.

This structure separates model-quality/style drift from actual loss of relationship state.

## Human rater protocol for contradiction scoring

Some generative outputs will require human judgment.

Use a written coding guide and, for confirmatory work, at least two independent raters who are blind to condition where practical.

The guide should include:

- a definition of each error category;
- positive and negative examples;
- rules for ambiguous outputs;
- a rule for when one response contains multiple errors;
- a process for adjudicating disagreements.

Before the confirmatory study, test inter-rater agreement on a pilot subset. Do not silently revise the rubric after seeing the final condition labels.

## Participant-reported measures

### Use established instruments only for constructs they actually measure

Established HRI scales can provide useful secondary context, but they should not be stretched into measures of continuity when they were not designed for that purpose.

Examples worth considering:

- **Godspeed Questionnaire Series** for anthropomorphism, animacy, likeability, perceived intelligence, and perceived safety;
- **RoSAS** for warmth, competence, and discomfort;
- **Trust in Automation Scale** for general trust in automated systems.

These can help characterize how a companion is perceived, but none directly validates the project's proposed construct of long-term relationship continuity.

Before using any published scale, verify the original wording, scoring instructions, language validation, and permission/licensing requirements from the primary source.

## Suggested response format for study-specific items

For early pilot items, use a consistent 5- or 7-point agreement scale. Avoid changing scale direction between adjacent items unless there is a strong methodological reason.

Do not create dozens of custom items. Prefer a small number of items tied directly to the construct definition, then refine them through pilot feedback.

## Primary versus secondary outcomes

Before confirmatory data collection, every experiment should declare:

- one primary hypothesis;
- one primary endpoint, or an explicitly justified pair of co-primary endpoints;
- secondary outcomes;
- exploratory outcomes;
- exclusion rules;
- missing-data handling;
- stopping rules;
- minimum effect considered practically meaningful.

This prevents a large dashboard of metrics from turning into post-hoc result shopping.

## Sample-size policy

Do **not** invent a fixed sample size at concept stage.

Use this progression:

1. small developer/debug sessions to eliminate obvious defects;
2. exploratory pilot to estimate variability, completion time, and measure quality;
3. choose the confirmatory design and practically meaningful effect;
4. perform an appropriate power or precision analysis for that design;
5. document the assumptions before collecting confirmatory data.

A tiny pilot may reveal whether the study is operable; it should not be presented as population-level evidence.

## Statistical analysis principles

Keep the first analysis simple enough to audit.

For repeated-measures comparisons, account for participant-level repeated observations rather than treating every scenario response as independent.

Report:

- effect estimates;
- uncertainty intervals;
- raw condition summaries;
- participant count and exclusions;
- scenario count;
- model and prompt versions;
- any deviations from the planned analysis.

Do not report only p-values.

## Minimum practical-effect thresholds

Statistical detectability is not the Stage A goal. The project needs effects large enough to justify more complexity.

Before confirmatory analysis, define thresholds such as:

- maximum acceptable contradiction rate;
- minimum reduction in correction burden;
- maximum acceptable interruption burden;
- minimum improvement in perceived relevance;
- maximum acceptable migration regression.

The exact numbers should come from pilot evidence and product/research judgment, not from arbitrary values inserted into this concept document.

## Blinding and counterbalancing

Where practical:

- hide condition names from participants;
- blind output raters to condition;
- randomize or counterbalance within-subject condition order;
- use scenario variants to reduce simple recall;
- keep avatar, voice, rendering, latency target, and model settings fixed unless one is the manipulated variable.

## Qualitative feedback

Open-ended interviews are useful for finding failure modes the predefined metrics missed.

Use them to generate hypotheses such as:

- "the companion remembered facts but still felt unlike itself";
- "proactive prompts were useful only at certain times";
- "baseline wording felt invasive despite being accurate".

Treat these as exploratory findings until separately tested.

## Avoid developer bias

The project creator is likely to know the intended personality, preferred avatar, and desired interaction style unusually well.

Developer self-testing is therefore valuable for debugging but especially weak as evidence for:

- warmth;
- naturalness;
- relationship continuity;
- acceptable proactivity;
- general user preference.

Confirmatory participant studies should include people who did not design the companion.

## References for candidate secondary measures

- Bartneck, C., Kulić, D., Croft, E., & Zoghbi, S. (2009). *Measurement Instruments for the Anthropomorphism, Animacy, Likeability, Perceived Intelligence, and Perceived Safety of Robots*. International Journal of Social Robotics, 1, 71–81. https://doi.org/10.1007/s12369-008-0001-3
- Carpinella, C. M., Wyman, A. B., Perez, M. A., & Stroessner, S. J. (2017). *The Robotic Social Attributes Scale (RoSAS): Development and Validation*. Proceedings of the 2017 ACM/IEEE International Conference on Human-Robot Interaction, 254–262. https://doi.org/10.1145/2909824.3020208
- Jian, J.-Y., Bisantz, A. M., & Drury, C. G. (2000). *Foundations for an Empirically Determined Scale of Trust in Automated Systems*. International Journal of Cognitive Ergonomics, 4(1), 53–71. https://doi.org/10.1207/S15327566IJCE0401_04

## Decision rule for Stage A

A Stage A result should justify added complexity only when:

- engineering safety/permission checks pass;
- the predeclared primary endpoint improves by a practically meaningful amount;
- the improvement is not explained by obvious presentation or model-quality confounds;
- important secondary harms do not worsen beyond the predeclared tolerance;
- the result survives at least one independent replication or confirmatory run before expensive physical embodiment is treated as justified.

If a result is mixed, simplify the hypothesis before expanding the system.
