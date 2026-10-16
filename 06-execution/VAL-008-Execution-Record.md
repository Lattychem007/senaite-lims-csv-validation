# VAL-008 — Execution Record
## SENAITE LIMS 2.6.0 — Oak Life Sciences Ltd

| Field | Value |
|---|---|
| Document ID | VAL-008 |
| Version | 1.0 |
| Executor | Kareem A. Ojo |
| Date | October 2026 |

## Environment at execution
- System: SENAITE LIMS 2.6.0
- Deployment: Docker, ZEO-clustered (`latest-zeo-1`, `latest-instance1-1`)
- Executed by: admin
- Scenario: Oak Life Sciences Ltd (contract QC lab); client Fidson Pharm Limited (FPL-001)

## Activities executed
| Ref | Activity | Outcome |
|---|---|---|
| IQ-01…06 | Installation Qualification | All passed — version 2.6.0 confirmed, containers up, application reachable, site created, admin access, platform confirmed |
| Setup | Created Client "Fidson Pharm Limited" (FPL-001) | Saved successfully |
| TC-06 | Role model | Analyst and Verifier are separate groups — separation of duties supported |
| TC-04 | Audit trail | Audit Log present at sample/client level |
| TC-11 | Authentication | Individual login required |
| Observation | Security configuration | "Automatic log-off" set to 0 (disabled) — noted against R-11 |

## Remaining to execute
Register a sample with an Assay analysis, enter and change a result, then inspect the Audit Log
(TC-01); test the self-verification setting (TC-02); test cancel-versus-delete (TC-03); and
post-verification change (TC-07). Execution is blocked by DEV-01 (VAL-009).
