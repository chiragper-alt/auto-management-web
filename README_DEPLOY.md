Auto Management Web V23 - Step 2 Categories
Deploy: the ROOT index.html is the application entry point.
The original web/Auto_Management_Web.html is preserved.
Step 2 contains Owner Information, Address, Insurance Details, Hypothecation, and Vehicle / Tax Details.


## V23 Core Import / VAHAN Record Fix
- Fixed the VAHAN workflow script parse error that prevented the record-selection renderer from initializing.
- `.xls` legacy Excel parser is retained and validated against the supplied 110-column sales workbook.
- Import mapping now carries all configured Master/VAHAN fields instead of only the original six fields.
- Added editable saved mapping management under Settings → Data & Import.
- Chassis No., Engine No. and Vehicle Model mappings are protected read-only.
