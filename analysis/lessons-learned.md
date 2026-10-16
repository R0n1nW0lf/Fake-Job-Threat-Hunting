# Lessons Learned

## What the investigations taught

1. **Verify on the employer's own site first.** In every case, the advertised role did not exist on the real employer's website or careers page. That single check would have flagged all six postings before any information was shared.
2. **Check the poster's affiliation.** Where a poster was shown (Cases 002, 003, 005), the person was publicly affiliated with an unrelated employer, in an unrelated profession, often on another continent. Where no poster was shown at all (Case-006), that absence was itself an indicator.
3. **Resolve the contact domain.** Two contact or company domains did not resolve at all (nlaaa.nl in Case-002, vital-soluciones.com in Case-005). A dead domain behind a live job posting is close to decisive on its own.
4. **Check the company page's own Jobs tab.** In Case-002 the real organisation's Jobs tab was empty while a posting ran under its name. In Case-005 the tab held exactly one job: the suspicious one.
5. **Phrase-search the description.** Exact-phrase searches exposed template reuse across sister postings (Cases 002, 003, 005), and in Case-006 returned zero results anywhere, showing the text existed nowhere legitimate.
6. **Read the page, not the name.** Displayed names can be placeholders ("No aplica", Case-006) or borrowed identities. The URL slug, industry, headquarters, size, and specialties told the true story.
7. **Treat fast-closing template posts as suspect.** Postings that open and close within hours, after collecting roughly 26 applicants, behave like harvesting windows, not hiring processes.
8. **Grade the verdict to the evidence.** Case-004 could not be verified, but the evidence did not prove fraud, so it was recorded as unverifiable and skipped. Skipping does not require proving a posting fake; labelling one fake requires evidence.
9. **Never submit personal data before verification.** Across six suspicious postings, zero applications were submitted and zero personal information was sent. Verification happened first, every time.

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
