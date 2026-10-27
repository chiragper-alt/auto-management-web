# Auto Management Web v1.5.87 — Extension Download Feedback

- Added a visible download status beneath Settings → Extension/API → Download Extension ZIP.
- Download button displays a preparing state and prevents duplicate clicks while the ZIP is fetched.
- Successful non-empty response triggers the browser download and displays a clear “Download started” status/toast.
- Failed HTTP/network/empty-file responses display an error message and allow retry.
- Kept the bundled extension package at v1.3.21 because its manifest reports 1.3.21.

Validation: HTML/inline JavaScript syntax and ZIP integrity checked in the build environment. Browser and live-host end-to-end download still require testing after deployment.
