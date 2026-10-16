# VAL-001 — Validation Plan

## SENAITE LIMS

|Field|Value|
|-|-|
|Document ID|VAL-001|
|Version|1.0|
|System|SENAITE LIMS 2.6.0 (open-source)|
|Deployment|Docker, ZEO-clustered|
|Author|Kareem A. Ojo|
|Date|20 Sept. 2026|
|Status|Draft — effective on approval (Section 11)|

## 1\. Purpose

This plan defines the approach for validating SENAITE LIMS for use as a laboratory information
management system handling GxP-relevant records. It establishes the scope, strategy,
deliverables, responsibilities and acceptance criteria for the validation.

## 2\. Scope

**In scope** — the following SENAITE functions as configured:

* Sample (Analysis Request) registration and lifecycle
* Analysis result entry, submission and verification
* User accounts, roles and access control
* Audit trail / activity logging on GxP-relevant records
* Electronic record integrity (ALCOA+)

**Out of scope, with justification:**

* Invoicing / financial functions — no GxP impact
* Instrument interfacing — not configured in this installation
* Report / certificate layout — cosmetic, no data-integrity impact
* Underlying Plone/Zope platform and Docker infrastructure — treated as supplier-supplied
infrastructure (GAMP Category 1); assessed at configuration level only

## 3\. System overview

SENAITE LIMS 2.6.0, deployed via Docker in a ZEO-clustered configuration. Full description in
VAL-002. **GAMP 5 category: 4 (configured product)** — justification in VAL-002.

## 4\. Validation strategy

Risk-based, following the GAMP 5 V-model. Testing effort is proportionate to risk (VAL-003):
High risks receive full OQ test cases with objective evidence; Medium risks receive documented
verification; Low risks receive a documented rationale.

## 5\. Roles and responsibilities

|Role|Responsibility|
|-|-|
|Author (Validation)|Prepares plan, risk assessment, protocols, report|
|Executor|Executes approved protocols, captures evidence, raises deviations|
|Reviewer|Reviews documents and executed protocols for accuracy|
|Approver|Approves documents; accepts residual risk|

The approver is independent of the author; that independence is the control.

## 6\. Acceptance criteria

Validation is complete when:

* All planned IQ and OQ test cases are executed
* Every requirement (VAL-004) is traced to an executed test with a recorded result (VAL-005)
* All deviations are documented, assessed for impact, and resolved or accepted with justification
* The Validation Summary Report (VAL-010) concludes the system is fit for intended use, with any
limitations stated

## 7\. Deviation handling

Any test step whose actual result differs from the expected result is recorded as a deviation
(VAL-009). The protocol is not modified and the step is not retried informally. Each deviation
receives: description, impact assessment, root cause, resolution and approval.

## 8\. Deliverables

VAL-001 Plan · VAL-002 System Description · VAL-003 Risk Assessment · VAL-004 Requirements ·
VAL-005 Traceability Matrix · VAL-006 IQ · VAL-007 OQ · VAL-008 Execution Record ·
VAL-009 Deviation Record · VAL-010 Summary Report.

## 9\. Regulatory basis

GAMP 5 Second Edition, EU GMP Annex 11, 21 CFR Part 11, ALCOA+ data integrity, ICH Q9(R1).

## 10\. Test environment

SENAITE LIMS version 2.6.0, Docker ZEO-clustered, browser-based access.

## 11\. Approval (not effective until signed)

|Role|Name|Signature|Date|
|-|-|-|-|
|Author|Kareem A. Ojo|||
|Reviewer||||
|Approver||||

## 12\. Revision history

|Version|Date|Author|Change|
|-|-|-|-|
|1.0|Sep 2026|Kareem A. Ojo|Initial issue|



