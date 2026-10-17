# Fake Job Recruitment Threat Hunting and OSINT Investigation

A threat-hunting and open-source intelligence (OSINT) portfolio project documenting the investigation of suspicious and fraudulent cybersecurity job postings encountered during a real job search between September 30 and October 17, 2026.

**Investigator:** Ronald Wolf, SOC analyst candidate

## Purpose

Job seekers, especially entry-level and career-changing candidates, may be attractive targets for suspected information-harvesting schemes. A fraudulent posting could solicit resumes and contact details before anyone questions it; whether any particular posting received or misused applicant information was not independently verified in these investigations. This project applies a structured investigation method to suspicious LinkedIn cybersecurity postings, documents the evidence for each case, correlates indicators across cases, and records what defensive lessons each investigation produced.

Across seven investigations, the outcomes were:

- 1 confirmed scam
- 4 likely fake / impersonation verdicts
- 2 postings that could not be verified and were skipped without being labelled fraudulent
- 0 applications submitted to any suspicious posting, and 0 items of personal information sent

## Investigation Methodology

The investigations follow the investigator's working principle:

> Don't assume. Gather evidence. Question it. Analyze it. Verify the source before trusting it.

Each case is structured with the same loop:

**Observation → Hypothesis → Evidence → Verification → Conclusion → Action Taken**

Within each case, confirmed facts, suspicious indicators, hypotheses, and unverified claims are kept separate. A company or individual is never described as fraudulent beyond what the documented evidence supports, and each case carries an explicit verdict label with a confidence level.

## Tools and Sources Used

- LinkedIn job postings and company pages (public view)
- Public web search, including exact-phrase searches of job description text
- DNS and domain resolution checks on contact and company domains
- Business directories (for confirming a real business exists and what it actually does)
- Employers' official websites and careers pages (cross-referencing whether a role is real)

## Key Findings

- Multiple postings reused the same generic description templates and ran template "sister postings" under the same company name.
- In the strongest cases, the postings impersonated real foreign small businesses, coalitions, or service firms that have no cybersecurity operation and no US presence.
- Listed job posters, where shown, were publicly affiliated with unrelated employers, not with the company named in the posting.
- In Cases 002 and 005, the checked contact domains did not resolve. In Case-006, no website was listed on the company page and no contact email was shown in the posting. In Cases 002, 003, 005, and 006, no corroboration for the advertised role was found outside LinkedIn. Case-001 was different: the genuine role existed at EaglePicher Technologies, while the copy appeared on LinkedIn under the Netrolynx AI name.
- Closure timing and displayed applicant counts varied by case. Case-002 closed approximately 2 hours after going live and displayed 16 applicants at first sighting. Case-006 closed within approximately 7 hours and displayed 26 applicants. Case-003 closed and displayed 26 applicants; its closure interval is Not Verified. Case-007 was still open at its investigation check, under an hour after posting, and displayed 3 applicants; its later closure status is Not Verified. Cases 001, 004, and 005 have applicant counts recorded as Not Verified.
- Two cases (Case-004, Divine Talent, and Case-007, Nexorant LLC) form a distinct second category: unverifiable blind staffing posts. A traceable firm exists in each, but the posting names no end employer and the role has no corroboration anywhere; neither case shows the impersonation indicators behind the stronger verdicts, and neither firm is labelled fraudulent.
- One case showed a LinkedIn company page displaying a placeholder name ("No aplica", Spanish for "not applicable") while its URL slug named a real Mexican law firm. A second, unrelated company's page also displayed the same placeholder. Who controlled either page, and whether any renaming was unauthorized, is Not Verified.

The evidence supports a shared pattern and playbook across several cases. It does **not** establish that a single actor operates all of them, and this project makes no attribution claim.

## Limitations

- All evidence is point-in-time public data gathered at investigation time. Postings and company pages change or disappear; several postings closed during or shortly after investigation.
- Screenshots were not retained as files. Evidence is preserved as dated investigation notes with source URLs (see `evidence/evidence-register.md` and `evidence/redacted-screenshots/README.md`). For Case-001, the original LinkedIn URL and job ID were recovered from the contemporaneous dated investigation log, and the verdict rests on that log plus the employer-site verification performed on 2026-10-02; no screenshot or side-by-side text-comparison file was preserved.
- Verdicts are analytical assessments based on public evidence, not legal determinations. Two cases (Case-004 and Case-007) are explicitly recorded as unverifiable rather than fake, because the evidence did not support a stronger label.
- Poster names recorded in the case files were publicly displayed on LinkedIn at investigation time and are documented with their publicly listed affiliation only.

## Defensive Recommendations

For job seekers:

- Verify the role on the employer's own website or careers page before applying anywhere else.
- Check that the person who posted the job is actually affiliated with that company.
- Resolve the contact email domain. A dead domain is a strong warning sign.
- Search a distinctive sentence from the description in quotation marks. A real role usually appears in more than one place.
- Treat fast-closing, template-style postings that name no employer in the text as suspect.
- Do not submit personal information to a posting you have not verified.

For platforms and impersonated businesses:

- Monitor for company pages displaying placeholder values and for jobs posted under pages whose industry and location do not match the role.
- Give impersonated businesses a fast reporting and page-recovery path, and alert applicants who already applied when a posting is confirmed fraudulent.

## Repository Structure

```
Fake-Job-Threat-Hunting/
├── README.md
├── PROJECT-DESCRIPTION.md
├── investigations/
│   ├── case-001.md
│   ├── case-002.md
│   ├── case-003.md
│   ├── case-004.md
│   ├── case-005.md
│   ├── case-006.md
│   └── case-007.md
├── evidence/
│   ├── evidence-register.md
│   └── redacted-screenshots/
├── indicators/
│   └── suspicious-listings.csv
├── analysis/
│   ├── correlation-analysis.md
│   ├── social-engineering-techniques.md
│   └── lessons-learned.md
└── reports/
    └── final-investigation-report.md
```

## Responsible Disclosure and Privacy

No suspicious party was contacted during these investigations, and no test applications were submitted. No applicant personal information appears in this repository. Identifiable individuals are referenced only where their name and affiliation were publicly displayed on the posting itself, and only as documented evidence. Suspicious behaviour is distinguished from proven fraud throughout.
