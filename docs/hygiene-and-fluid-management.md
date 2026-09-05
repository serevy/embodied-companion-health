# Hygiene and Fluid Management

Any embodied companion designed for close physical contact must treat hygiene as a core architectural problem, not an afterthought.

This document describes public, high-level principles for contact-surface hygiene, clean-fluid delivery, waste-fluid handling, maintenance, and failure safety. It intentionally avoids exact materials, formulations, flow geometry, or disinfection recipes.

## 1. Separate clean and waste paths

One of the most important design rules is strict separation between:

- clean water or maintenance fluids;
- any user-facing consumable or moisturizing fluids;
- lubricating fluids intended for external contact;
- biological waste and used fluids;
- internal maintenance or cooling systems.

Cross-contamination between these paths should be prevented structurally, not merely by software.

## 2. Replaceable contact interfaces

High-contact areas should be designed with serviceability in mind.

Useful properties include:

- removable liners or contact modules;
- inspectable wear surfaces;
- easy replacement without disassembling the whole robot;
- materials compatible with repeated cleaning;
- unambiguous orientation and installation;
- tamper or misuse detection where safety requires it.

A long-lived machine should not rely on inaccessible internal cavities remaining perfectly clean forever.

## 3. Short, drainable paths

Fluid systems should minimize hidden retention zones.

The design should favor:

- short flow paths;
- complete drainage;
- minimal dead volume;
- easy inspection;
- replaceable tubing or modules where practical;
- leak detection;
- one-way barriers where appropriate.

The objective is to reduce odor, residue, microbial growth, and maintenance uncertainty.

## 4. Waste capture

Biological fluids should be treated as potentially contaminated regardless of whether the user appears healthy.

A practical future system may use sealed waste capture with properties such as:

- isolated collection;
- backflow prevention;
- fill-state sensing;
- leak detection;
- simple removal;
- clear disposal guidance;
- lockout if the waste path is not safely installed.

Where useful, the system could perform user-authorized, non-diagnostic trend analysis before disposal, but waste should not be casually recirculated into user-facing fluid systems.

## 5. Consumable fluid design

If a companion supplies a user-facing fluid, the design problem is broader than simply making it pleasant.

It must consider:

- ingestion safety where swallowing is reasonably foreseeable;
- allergy risk;
- oral and skin compatibility;
- shelf life;
- microbial stability;
- temperature control;
- flavor and odor neutrality;
- residue and cleanability;
- cartridge traceability.

Any therapeutic claim would move the system into a substantially different regulatory category and should be treated separately.

## 6. Cleaning modes

A robust companion should make hygiene status visible and operationally simple.

Possible maintenance states include:

- ready;
- recently used, cleaning required;
- cleaning in progress;
- drying or post-cleaning verification;
- consumable replacement required;
- waste cartridge replacement required;
- contact module replacement required;
- hygiene state unknown — intimate contact disabled.

The system should fail closed when cleanliness cannot be verified.

## 7. User experience matters

A technically hygienic system can still fail as a product if maintenance is unpleasant or embarrassing.

Good design should aim for:

- minimal manual handling of waste;
- sealed cartridges;
- discreet status reporting;
- automatic reminders;
- simple cleaning workflows;
- no need for users to expose internal machinery during routine maintenance.

The companion experience should remain emotionally coherent while the machine quietly handles unglamorous maintenance in the background.

## 8. Failure handling

The system should detect and respond conservatively to:

- leaks;
- blocked paths;
- abnormal temperature;
- contaminated or expired consumables;
- missing replaceable modules;
- incomplete cleaning;
- sensor disagreement;
- unexpected fluid in a clean path.

Where safe status cannot be established, the relevant contact mode should be unavailable until maintenance is complete.

## Design rule

> **Any interface intimate enough to be pleasant is intimate enough to require professional-grade thinking about hygiene, maintenance, and failure containment.**
