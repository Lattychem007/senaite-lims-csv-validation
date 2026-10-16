# VAL-007 : Operational Qualification (OQ)

## SENAITE LIMS 2.6.0 

|Field|Value|
|-|-|
|Document ID|VAL-007|
|Version|1.0|
|Executor|Kareem A. Ojo|
|Date|20 Sept 2026|
|Status|Partially executed — see Execution status and VAL-009|

### TC-01 — Audit trail on result change (REQ-01, R-01)

|Step|Action|Expected result|Actual|Result|
|-|-|-|-|-|
|1|Register a sample (Paracetamol 500 mg Tablets, client Oak Pharm) with an Assay analysis|Sample created, status Reception pending|Sample was created|Passed|
|2|Receive sample; enter Assay result = 98.5%|Result saved, status To be verified|Result was saved and Verified |Passed|
|3|Change the result 98.5% → 99.2%|Change accepted| Change Was Accepted|Passed|
|4|Open the Audit Log for the sample/analysis|Both values shown, with user and system timestamp|Both old and New value Saved |Passed|
|5|Check whether a reason-for-change was requested|Record whether captured|Reason for change was captured|Passed|

### TC-02 — Self-verification control (REQ-02, R-02)

|Step|Action|Expected result|Actual|Result|
|-|-|-|-|-|
|1|Locate the self-verification setting in SENAITE Setup → Security|Setting exists|Security configuration tab located|Passed|
|2|As a user, submit an Assay result|Assay Submitted|Assay  Submitted|Passed|
|3|As the same user, attempt to verify it|Blocked when self-verification disabled|Blocked when self-verification disabled|Passed|

### TC-03 — No hard delete (REQ-03, R-03)

|Step|Action|Expected|Actual|Result|
|-|-|-|-|-|
|1|Attempt to permanently delete a sample/result|Not available; only cancel/invalidate|Not available; only cancel/invalidate|Passed|
|2|Cancel a sample; check it is retained with cancelled status|Record retained|Record retained|Passed|

### TC-04 — Audit trail scope (REQ-04, R-04)

|Step|Action|Expected|Actual|Result|
|-|-|-|-|-|
|1|Open the Audit Log|Log present|Audit Log present at sample/client level|Pass|
|2|Perform create / change / verify and confirm each is logged|All three recorded||Pending|

### TC-06 — Role-based access (REQ-06, R-06)

|Step|Action|Expected|Actual|Result|
|-|-|-|-|-|
|1|Confirm distinct Analyst and Verifier groups exist|Both present|Both present (Users \& Groups)|Pass|
|2|Create an Analyst user; log in; attempt a Verifier-only action|Blocked||Pending|

### TC-07 — No silent change after verification (REQ-07, R-07)

|Step|Action|Expected|Actual|Result|
|-|-|-|-|-|
|1|Verify a result|Status → Verified||Pending|
|2|Attempt to change the verified result|Blocked, or recorded and forces re-verification||Pending|

### TC-05, 08, 09, 11 — Medium checks

|TC|Requirement|Check|Actual|Result|
|-|-|-|-|-|
|TC-05|REQ-05|Each log entry shows named user + timestamp||Pending|
|TC-08|REQ-08|Result ties to the correct sample ID||Pending|
|TC-09|REQ-09|Timestamp is system-set, not editable||Pending|
|TC-11|REQ-11|Login requires individual credentials|Individual-login authentication required|Pass|

## Execution status

* **Passed:** TC-O1 TC-02,TC-03, TC-04 (audit trail present), TC-06 (role separation), TC-11 (authentication).
* **Pending:** TC-03, TC-05, TC-07, TC-08, TC-09 — blocked by DEV-01 (VAL-009).

