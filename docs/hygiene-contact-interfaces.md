# Hygiene and Replaceable Contact Interfaces

Any embodied companion designed for close physical contact must treat hygiene and maintainability as architectural requirements, not cosmetic details.

This public document intentionally stays at the requirements level. Exact materials, cleaning chemistry, fluid routing, sensor placement, and device mechanisms remain outside the public concept pending dedicated engineering, safety, and IP review.

## Core requirements

A close-contact system should be designed so that users and maintainers can answer simple questions:

- Which surfaces are safe to touch now?
- Which components need cleaning or replacement?
- Has a required cleaning cycle completed successfully?
- Is any contamination, leakage, wear, or installation fault suspected?
- Which interaction modes must be disabled until maintenance is complete?

## Replaceable and inspectable interfaces

High-contact areas should favor:

- removable or replaceable contact components where practical;
- inspectable wear surfaces;
- materials compatible with intended cleaning processes;
- clear installation state;
- simple service workflows;
- avoidance of inaccessible retention spaces that are difficult to verify.

The design target is not "maintenance free." It is **maintenance that is predictable, visible, and difficult to perform incorrectly**.

## Separation by function

Any future system that handles clean consumables, maintenance fluids, or biological waste should enforce structural separation between those functions.

The public architecture does not prescribe a specific cartridge or flow design. The requirement is simpler:

> **A failure in a waste or maintenance subsystem must not silently contaminate a user-facing path.**

## Hygiene state as system state

The companion should maintain an explicit maintenance state, for example:

- ready;
- cleaning required;
- cleaning in progress;
- verification incomplete;
- replaceable component required;
- fault detected;
- hygiene state unknown.

When safe status cannot be established, affected close-contact modes should fail closed.

## Failure handling

A mature design should conservatively handle conditions such as:

- incomplete cleaning;
- suspected leakage;
- abnormal temperature;
- expired or incorrectly installed consumables;
- missing replaceable components;
- sensor disagreement;
- unknown contamination state.

The behavior layer should be able to explain the maintenance limitation without disguising it as personality.

## User experience

Good hygiene engineering can still fail as a product if routine maintenance is awkward, embarrassing, expensive, or easy to postpone.

Useful design goals include:

- low-friction cleaning workflows;
- minimal exposure to waste;
- discreet status reporting;
- clear replacement intervals;
- predictable consumable cost;
- accessible maintenance for users with different physical abilities.

## Research boundary

Detailed close-contact fluid systems, consumable formulations, waste-processing mechanisms, and intimate-interface designs may eventually be valuable research areas. They are deliberately **not specified here**.

## Design rule

> **Any interface close enough to require trust is close enough to require verifiable hygiene, serviceability, and safe lockout.**
