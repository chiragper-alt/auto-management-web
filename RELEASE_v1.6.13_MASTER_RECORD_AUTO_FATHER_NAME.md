# v1.6.13 — Master Record automatic Father Name fallback

- When a customer record is imported/created with a full name of at least three words and Father Name is blank, the second name token is filled into Father Name.
- The fallback also applies when an existing record is updated while Father Name remains blank.
- An explicitly provided Father Name is never overwritten.
- This is a heuristic for common First Middle Surname names; verify imported records where the name format differs.
