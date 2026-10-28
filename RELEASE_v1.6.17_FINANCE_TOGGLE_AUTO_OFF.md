# v1.6.17 — Finance Toggle Auto-Off

- Customer Details record view now initializes the Hypothecation / Financer ON/OFF switch as OFF when no financer or HP details are present.
- Existing populated financer details keep the switch ON unless the saved state explicitly indicates OFF.
- This removes the need to manually switch OFF for records imported without financer/HP details.
