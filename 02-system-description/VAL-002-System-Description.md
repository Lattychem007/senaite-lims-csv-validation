# VAL-002 — System Description

## SENAITE LIMS

|Field|Value|
|-|-|
|Document ID|VAL-002|
|Version|1.0|
|Author|Kareem A. Ojo|
|Date|20 Sept. 2026|

## 1\. System identification

|Attribute|Value|Source|
|-|-|-|
|System name|SENAITE LIMS|Dashboard|
|Version|2.6.0|`docker exec latest-instance1-1 pip show senaite.lims`|
|Platform|Plone / Zope (Python)|Repository / application footer|
|Deployment|Docker, ZEO-clustered (zeo + instance containers)|`docker compose ps`|
|Database|ZODB via ZEO|Deployment|
|Access|Browser-based (HTTP)|Browser|

## 2\. Intended use

SENAITE LIMS manages the laboratory testing lifecycle: registration of samples, recording and
verification of analytical results, and publication of results. Within this validation it is
treated as a system holding GxP-relevant records whose integrity, attributability and
traceability must be assured.

## 3\. GAMP 5 categorisation

**Category 4 — configured product.**

SENAITE is an existing open-source software product that is adapted using its built-in
configuration tools — clients, sample types, analysis services, user roles and workflows — to
match the laboratory's processes, without changing the underlying source code. Validation
therefore focuses on the configuration and the intended use, while the core software is
leveraged from the vendor/community build. Any custom code or bespoke add-on introduced would
be assessed separately as GAMP Category 5. Basis: GAMP 5 Second Edition software categorisation.

## 4\. Workflow states (observed)

**Sample (Analysis Request) lifecycle:**
Reception pending → Results pending → To be verified → Verified → Published

**Analysis lifecycle:**
Unassigned → Assigned → To be verified → Verified → Published

The "To be verified → Verified" step separates result entry from verification — the electronic
form of a second-person review.

## 5\. Electronic records inventory

|ID|Record|GxP-critical|
|-|-|-|
|REC-01|Client|No (reference data)|
|REC-02|Sample / Analysis Request|Yes|
|REC-03|Analysis result|Yes|
|REC-04|Result verification|Yes|
|REC-05|User account and role|Yes|
|REC-06|Audit trail / activity log|Yes|
|REC-07|Published report|Yes|

## 6\. User roles (observed in Users \& Groups)

SENAITE provides role-based access via groups, with distinct roles including **Analyst** (result
entry) and **Verifier** (result verification), supporting separation of duties. Additional roles:
Lab Manager, Lab Clerk, Preserver, Publisher, Sampler, Sampling Coordinator, and Manager (admin).

## 7\. Approval

|Role|Name|Signature|Date|
|-|-|-|-|
|Author|Kareem A. Ojo|||
|Reviewer||||



