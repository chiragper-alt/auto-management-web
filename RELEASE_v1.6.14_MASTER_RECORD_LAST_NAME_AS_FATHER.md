# v1.6.14 — Master Record: Last Name as Father Name Fallback

- Changed automatic Father Name fallback to use the last word of Customer Name instead of the middle word.
- Only fills Father Name when it is blank; existing Father Name values remain unchanged.
- Example: `CHIRAG RAMESHBHAI PATEL` -> Father Name: `PATEL`.
