# Fake Job Recruitment Threat Hunting and OSINT Investigation

A threat-hunting and open-source intelligence (OSINT) portfolio project documenting the investigation of suspicious and fraudulent cybersecurity job postings encountered during a real job search between September 30 and October 16, 2026.

**Investigator:** Ronald Wolf, SOC analyst candidate

## Purpose

Job seekers, especially entry-level and career-changing candidates, are attractive targets for information harvesting. A fake job posting can collect resumes, contact details, and other personal information from dozens of applicants before anyone questions it. This project applies a structured investigation method to suspicious LinkedIn cybersecurity postings, documents the evidence for each case, correlates indicators across cases, and records what defensive lessons each investigation produced.

Across six investigations, the outcomes were:

- 1 confirmed scam
- 4 likely fake / impersonation verdicts
- 1 posting that could not be verified and was skipped without being labelled fraudulent
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
- Contact domains were dead or absent, company websites were missing, and the advertised roles existed only on LinkedIn, nowhere else on the web.
- Several postings closed within hours of going live, after collecting roughly 26 applicants each.
- One case showed a real firm's LinkedIn company page displaying a placeholder name ("No aplica", Spanish for "not applicable"), and a second, unrelated company's page renamed to the same placeholder.

The evidence supports a shared pattern and playbook across several cases. It does **not** establish that a single actor operates all of them, and this project makes no attribution claim.

## Limitations

- All evidence is point-in-time public data gathered at investigation time. Postings and company pages change or disappear; several postings closed during or shortly after investigation.
- Screenshots were not retained as files. Evidence is preserved as dated investigation notes with source URLs (see `evidence/redacted-screenshots/README.md`).
- Verdicts are analytical assessments based on public evidence, not legal determinations. One case (Case-004) is explicitly recorded as unverifiable rather than fake, because the evidence did not support a stronger label.
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

- Monitor for company pages renamed to placeholder values and for jobs posted under pages whose industry and location do not match the role.
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
│   └── case-006.md
├── evidence/
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
