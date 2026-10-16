# VAL-003 — Risk Assessment

## SENAITE LIMS

|Field|Value|
|-|-|
|Document ID|VAL-003|
|Version|1.0|
|Author|Kareem A. Ojo|
|Date|20 Sept. 2026|

## 1\. Method

Each risk is scored **Severity × Probability × Detectability**, 1–4 each.
**RPN = S × P × D.** Bands: ≥ 27 High · 9–26 Medium · < 9 Low.

* High → full OQ test case with objective evidence
* Medium → documented verification
* Low → documented rationale

## 2\. Risk register

|ID|Risk scenario|Record|S|P|D|RPN|Band|
|-|-|-|-|-|-|-|-|
|R-01|A result is changed after entry with no record of the old value or who changed it|REC-03/06|4|3|4|48|High|
|R-02|One person both enters and verifies the same result (no enforced second-person review)|REC-04|4|3|3|36|High|
|R-03|A result or sample record is deleted, destroying the history|REC-02/03|4|2|4|32|High|
|R-04|The audit trail can be edited or disabled|REC-06|4|2|4|32|High|
|R-05|An action is recorded against the wrong user, or attribution is missing|REC-05|4|2|3|24|Medium|
|R-06|A user can reach functions beyond their role|REC-05|3|3|3|27|High|
|R-07|A verified result can be silently altered after verification|REC-03/04|4|2|4|32|High|
|R-08|Result entered against the wrong sample|REC-02/03|4|2|2|16|Medium|
|R-09|Timestamp is wrong or user-editable|REC-06|2|2|3|12|Medium|
|R-10|Data lost — no recoverable copy|all|3|2|3|18|Medium|
|R-11|Weak authentication allows unauthorised access|REC-05|3|2|3|18|Medium|

## 3\. Scoping decision

Testing effort is allocated by risk band. The six High risks receive full OQ test cases with
objective evidence; the Medium risks receive documented verification.

|Full OQ test (High)|Documented check (Medium)|
|-|-|
|R-01 audit trail on result change|R-05 attribution|
|R-02 self-verification|R-08 sample–result binding|
|R-03 delete vs void|R-09 timestamp|
|R-04 audit trail integrity|R-10 backup|
|R-06 privilege enforcement|R-11 authentication|
|R-07 post-verification alteration||

## 4\. Residual risk

After testing, each risk is restated with its outcome and any accepted residual risk. Completed
in VAL-010 once results exist.

## 5\. Approval

|Role|Name|Signature|Date|
|-|-|-|-|
|Author|Kareem A. Ojo|||
|Reviewer||||



