# Auto Management Web – VAHAN Automation Extension

## Install
1. Open Chrome or Edge and go to Extensions.
2. Enable Developer mode.
3. Choose **Load unpacked**.
4. Select this `extension` folder.
5. Open Auto Management Web and keep the VAHAN portal available in a browser tab.

## Workflow
Auto Management Web → select record → Data Preparation → Start VAHAN Processing.
The web app sends the selected record to this extension. The extension then controls the VAHAN page content script.

## Safety
- Does not automate CAPTCHA/OTP or other human-verification controls.
- Does not click final registration Save/Submit automatically.
- Stops when required fields cannot be identified instead of silently skipping them.
- Uses the attached v2.5.67 field-detection logic as the automation reference.
