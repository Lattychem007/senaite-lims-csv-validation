# VAL-004 :Requirements Specification

## SENAITE LIMS 2.6.0

|Field|Value|
|-|-|
|Document ID|VAL-004|
|Version|1.0|
|Author|Kareem A. Ojo|
|Date|20 Sept. 2026|

Each requirement is a testable statement derived from a risk in VAL-003 and is verified by a
test case in VAL-007. The chain is risk → requirement → test.

|ID|Requirement|From risk|Test|Priority|
|-|-|-|-|-|
|REQ-01|When an analysis result is changed after submission, the system shall retain the previous value and record the user who made the change together with a system-generated date/time.|R-01|TC-01|High|
|REQ-02|The system shall provide the capability to prevent the same user from both submitting and verifying the same analysis result (self-verification control).|R-02|TC-02|High|
|REQ-03|The system shall not permit permanent deletion of a sample or result record; cancellation/invalidation shall retain the record and its history.|R-03|TC-03|High|
|REQ-04|The audit trail shall be system-generated and shall record create, change, verify and cancel actions on critical records.|R-04|TC-04|High|
|REQ-05|Every create/change/verify/cancel action on a critical record shall be attributable to a uniquely identified user with a timestamp.|R-05|TC-05|Medium|
|REQ-06|The system shall provide role-based access control with distinct roles for result entry (Analyst) and result verification (Verifier).|R-06|TC-06|High|
|REQ-07|A verified result shall not be silently altered; any change after verification shall be recorded and shall return the result to an unverified state (re-verification required).|R-07|TC-07|High|
|REQ-08|Each analysis result shall be bound to the correct sample via a unique sample identifier.|R-08|TC-08|Medium|
|REQ-09|Timestamps shall be system-generated from the server clock and shall not be user-editable.|R-09|TC-09|Medium|
|REQ-11|Access to the system shall require authentication with individual user credentials.|R-11|TC-11|Medium|



