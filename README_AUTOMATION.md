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
