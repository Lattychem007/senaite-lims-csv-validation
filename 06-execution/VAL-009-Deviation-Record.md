# VAL-009 — Deviation Record
## SENAITE LIMS 2.6.0 — Oak Life Sciences Ltd

| Field | Value |
|---|---|
| Document ID | VAL-009 |
| Version | 1.0 |
| Author | Kareem A. Ojo |
| Date | October 2026 |

A deviation is any departure from the expected or planned execution. Each is recorded with an
impact assessment, root cause, resolution and status.

| Dev ID | Raised | Description | Impact assessment | Root cause | Resolution | Status |
|---|---|---|---|---|---|---|
| DEV-01 | October 2026 | Unable to reach the Sample Types / Analysis Services configuration pages in this SENAITE 2.6.0 Docker install (setup pages return an error). This prevented registration of a test sample, blocking execution of TC-01, TC-02, TC-03 and TC-07. | Medium — blocks execution of the result-lifecycle OQ test cases. Does not affect the confirmed results (IQ, role separation, audit-trail presence, authentication). No product or data-integrity impact; this is a test-environment configuration-access issue, not a system failure. | Configuration/navigation access issue in the clustered ZEO Docker image (suspected stale-session routing or a build-specific setup path change in 2.6.0). | (a) Retry from a clean browser session; (b) if unresolved, re-pull the image or deploy a single-instance configuration; (c) execute the remaining OQ tests once setup access is restored. The confirmed IQ and OQ controls stand as executed. | Open |

## Items to investigate on re-execution
When the remaining OQ tests are executed, the following are to be verified (not pre-judged):
- Whether self-verification is permitted by default (TC-02) and, if so, a recommendation to
  disable it to enforce second-person review.
- Whether the audit trail captures a *reason* for a result change (TC-01), assessed against the
  ALCOA+ "Complete" principle.
