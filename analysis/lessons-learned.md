# Lessons Learned

## What the investigations taught

1. **Verify on the employer's own site first.** None of the eight postings could be validated as a genuine opening at the advertised employer through an official careers source. In Cases 002, 003, 005, and 006 no corroboration for the role was found outside LinkedIn at all; Case-007's role likewise had no corroboration anywhere and could not be confirmed on the firm's own site; Case-008 had no employer site to check at all, because no business behind the name could be found; Case-001's genuine role did exist, but at EaglePicher Technologies, not under the advertised Netrolynx AI name. That single check would have flagged all eight postings before any information was shared.
2. **Check the poster's affiliation.** Where a poster was shown (Cases 002, 003, 005), the person was publicly affiliated with an unrelated employer, in an unrelated profession, often on another continent. Where no poster was shown at all (Case-006), that absence was itself an indicator.
3. **Resolve the contact domain.** Two contact or company domains did not resolve at all (nlaaa.nl in Case-002, vital-soluciones.com in Case-005). A dead domain behind a live job posting is close to decisive on its own.
4. **Check the company page's own Jobs tab.** In Case-002 the real organisation's Jobs tab was empty while a posting ran under its name. In Case-005 the tab held exactly one job: the suspicious one. And in Case-008 there was no company page to check at all — the employer name on the posting was plain text, not a link — which is itself close to decisive: a real employer hiring on LinkedIn has a page.
5. **Search the description text.** Comparing description text across postings exposed template reuse and sister postings (Cases 002, 003, 005). In Case-006, exact-phrase searches for two distinctive lines returned zero results anywhere, showing the text could be found nowhere else.
6. **Read the page, not the name.** Displayed names can be placeholders ("No aplica", Case-006) or borrowed identities. The URL slug, industry, headquarters, size, and specialties told the true story.
7. **Treat fast-closing template posts as suspect.** Two postings opened and closed within hours (Case-002 in roughly 2 hours, displaying 16 applicants at first sighting; Case-006 within roughly 7 hours, displaying 26 applicants). Short-lived template postings behave less like hiring processes and more like collection windows; that characterisation is an inference from the pattern, and actual receipt or use of applicant data was not verified in any case.
8. **Grade the verdict to the evidence.** Case-004 could not be verified, but the evidence did not prove fraud, so it was recorded as unverifiable and skipped. Skipping does not require proving a posting fake; labelling one fake requires evidence.
9. **Never submit personal data before verification.** Across fifteen suspicious postings, zero applications were submitted and zero personal information was sent. Verification happened first, every time.

## How this maps to SOC and threat-intelligence skills

| Investigation practice | SOC / threat-intel equivalent |
|---|---|
| Collecting domains, URLs, job IDs, and poster affiliations per case | IOC collection and consistent indicator logging |
| Checking domain resolution and website behaviour | IOC enrichment and validation |
| Comparing templates, domains, and patterns across cases | Correlation and campaign analysis |
| Using verdict labels (confirmed, likely, not verified) | Confidence levels in intelligence reporting |
| Separating facts, indicators, hypotheses, and unverified claims | Structured analytic technique; avoiding assumption-driven reporting |
| Recording "Not Verified" instead of guessing | Evidence discipline and honest reporting under uncertainty |
| Writing a dated case file for every investigation | Incident documentation and knowledge retention |
| Refusing attribution without evidence | Attribution discipline |
