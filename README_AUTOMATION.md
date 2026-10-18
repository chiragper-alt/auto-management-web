# VAHAN Automation Supervisor — v1.4.11

The web application now includes a stateful automation supervisor around the existing VAHAN extension bridge.

## What it adds
- Start/stop/pause/resume/retry commands through the existing `postMessage` bridge.
- Initial extension-response timeout with limited reconnect attempts.
- Explicit automation states: starting, running, paused, stopped, error, completed.
- Step-aware status handling when the extension supplies `step`, `currentStep`, `phase`, `stepName`, or `phaseName`.
- Persistent automation status on the selected local record.
- Operator controls on VAHAN Processing: Pause, Resume, Retry, Stop.
- Existing extension message names remain supported.

## Important integration note
The web layer cannot control DOM waits inside the VAHAN portal unless the installed extension implements those waits. The existing extension bridge remains intact. For full portal-side smoothness, the extension should emit status events using `AM_EXTENSION_VAHAN_STATUS` and ideally include `step`/`stepName`; the supervisor will consume them automatically.


## v1.4.46 — Financer Master Dropdown Fix
- Customer Details Hypothecation Financer Name is a visible native select populated from the same `am_financers_v1` list as Sidebar → Financer.
- Added shared API and local storage fallbacks, selected ID/name matching, and auto-fill of branch address, city/district, state and pincode.
- Added an inline count/help message so an empty list is diagnosable.
