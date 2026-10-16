# SENAITE LIMS — Computer System Validation Package

A hands-on **computer system validation (CSV)** project validating **SENAITE LIMS**
(an open-source laboratory information management system) against **GAMP 5**, EU GMP
**Annex 11**, **21 CFR Part 11** and **ALCOA+** data-integrity principles.

**Author:** Kareem A. Ojo  ·  **Date:** 20 Sept. 2026

\---

## Purpose

This repository is a complete, risk-based validation package for a laboratory information
management system, built to demonstrate the full CSV lifecycle end to end  from validation
plan through risk assessment, requirements, qualification protocols, execution and deviation
handling, to the summary report. It is a learning / portfolio project carried out on
open-source software, not a production validation for a regulated client.

## System under validation

|Attribute|Value|
|-|-|
|System|SENAITE LIMS|
|Version|2.6.0 (confirmed from the running container)|
|Platform|Plone / Zope / Python|
|Deployment|Docker, ZEO-clustered (zeo + instance)|
|GAMP 5 category|4 — configured product|

## Scenario

The system is validated for **Kareem Life Sciences Ltd**, a contract pharmaceutical QC testing
laboratory, performing finished-product release testing (Assay) on tablet products submitted
by a manufacturer client (**Oak Pharm Ltd**).

## Approach

Risk-based, following the GAMP 5 V-model: testing effort is proportionate to risk. Each risk
earns a requirement; each requirement earns a test; a traceability matrix proves coverage in
both directions.

```
Plan → System Description → Risk Assessment → Requirements → Traceability
     → IQ / OQ → Execution + Deviations → Summary Report
```

## The package

|ID|Document|Folder|
|-|-|-|
|VAL-001|Validation Plan|[01-planning](01-planning/VAL-001-Validation-Plan.md)|
|VAL-002|System Description|[02-system-description](02-system-description/VAL-002-System-Description.md)|
|VAL-003|**Risk Assessment**|[03-risk-assessment](03-risk-assessment/VAL-003-Risk-Assessment.md)|
|VAL-004|Requirements Specification|[04-requirements](04-requirements/VAL-004-Requirements-Specification.md)|
|VAL-005|Traceability Matrix|[04-requirements](04-requirements/VAL-005-Traceability-Matrix.csv)|
|VAL-006|Installation Qualification (IQ)|[05-qualification](05-qualification/VAL-006-Installation-Qualification.md)|
|VAL-007|Operational Qualification (OQ)|[05-qualification](05-qualification/VAL-007-Operational-Qualification.md)|
|VAL-008|Execution Record|[06-execution](06-execution/VAL-008-Execution-Record.md)|
|VAL-009|Deviation Record|[06-execution](06-execution/VAL-009-Deviation-Record.md)|
|VAL-010|Validation Summary Report|[07-summary](07-summary/VAL-010-Summary-Report.md)|

## Execution status

This package reflects a genuine, partially executed validation:

* **Installation Qualification (IQ-01 to IQ-06): executed and passed** — version pinned (2.6.0),
containers running, application reachable, site created, admin access, platform confirmed.
* **Operational Qualification: partially executed** — role separation (Analyst ≠ Verifier),
audit-trail presence and individual-login authentication confirmed; the result-lifecycle
test cases remain to be executed.
* **One open deviation (DEV-01)** is documented honestly, with an impact assessment, where an
environment issue blocked part of the OQ. Outstanding tests and the deviation are recorded
rather than omitted — in keeping with the principle that a validation package documents what
actually happened.

## Regulatory basis

GAMP 5 (Second Edition) · EU GMP Annex 11 · 21 CFR Part 11 · ALCOA+ · ICH Q9(R1).

## Disclaimer

Prepared as an independent learning and portfolio exercise on open-source software. It is not
an official validation of, or affiliated with, the SENAITE project, and the scenario entities
are illustrative.

