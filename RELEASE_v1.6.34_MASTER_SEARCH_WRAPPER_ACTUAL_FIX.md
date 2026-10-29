Auto Management Web v1.6.34 — Master Search Wrapper Actual Fix
Based on v1.6.33. The Master Records markup uses .master-search-wrap with #masterRecordSearch and a direct span; previous styles missed this exact wrapper. This release directly changes that markup: removes wrapper border/background/shadow, gives the input a clean field style, and makes the search icon a blue circle with a white SVG magnifying-glass icon.
Validation: ZIP integrity checked and exact markup replacement confirmed. Browser visual testing not performed.
