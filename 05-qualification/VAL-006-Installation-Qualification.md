# VAL-006 — Installation Qualification (IQ)

## SENAITE LIMS 2.6.0

|Field|Value|
|-|-|
|Document ID|VAL-006|
|Version|1.0|
|Executor|Kareem A. Ojo|
|Date|20 Sept 2026|
|Status|Executed — all checks passed|

|#|Check|Expected|Actual|Result|Evidence|
|-|-|-|-|-|-|
|IQ-01|SENAITE version|Exact version recorded|2.6.0 (via `docker exec latest-instance1-1 pip show senaite.lims`)|Pass|EV-IQ01|
|IQ-02|Containers running|zeo + instance up|`latest-zeo-1` and `latest-instance1-1` running (via `docker compose ps`)|Pass|EV-IQ02|
|IQ-03|Application reachable|Dashboard loads|Dashboard loaded in browser|Pass|EV-IQ03|
|IQ-04|Site created|SENAITE site initialised|Site created and initialised successfully|Pass|EV-IQ04|
|IQ-05|Admin access|Admin authenticates|Admin login succeeded|Pass|EV-IQ05|
|IQ-06|Platform|Plone / Zope / Python|Confirmed from application footer|Pass|EV-IQ06|

**Outcome:** Installation Qualification complete; all checks passed.

