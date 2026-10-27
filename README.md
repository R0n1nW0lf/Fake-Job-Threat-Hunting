# Fake Job Recruitment Threat Hunting and OSINT Investigation

A threat-hunting and open-source intelligence (OSINT) portfolio project documenting the investigation of suspicious and fraudulent cybersecurity job postings encountered during a real job search between September 30 and October 25, 2026.

**Investigator:** Ronald Wolf, SOC analyst candidate

## Purpose

Job seekers, especially entry-level and career-changing candidates, may be attractive targets for suspected information-harvesting schemes. A fraudulent posting could solicit resumes and contact details before anyone questions it; whether any particular posting received or misused applicant information was not independently verified in these investigations. This project applies a structured investigation method to suspicious LinkedIn cybersecurity postings, documents the evidence for each case, correlates indicators across cases, and records what defensive lessons each investigation produced.

Across fifteen investigations, the outcomes were:

- 1 confirmed scam
- 5 likely fake verdicts (4 impersonation of real businesses, 1 fabricated employer identity)
- 9 postings that could not be verified and were skipped without being labelled fraudulent
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
- Closure timing and displayed applicant counts varied by case. Case-002 closed approximately 2 hours after going live and displayed 16 applicants at first sighting. Case-006 closed within approximately 7 hours and displayed 26 applicants. Case-003 closed and displayed 26 applicants; its closure interval is Not Verified. Case-007 was still open at its investigation check, under an hour after posting, and displayed 3 applicants; its later closure status is Not Verified. Case-008 was likewise still open at its investigation check, approximately one hour after posting, and displayed 7 applicants; its later closure status is Not Verified. Cases 001, 004, and 005 have applicant counts recorded as Not Verified.
- Two cases (Case-004, Divine Talent, and Case-007, Nexorant LLC) form a distinct second category: unverifiable blind staffing posts. A traceable firm exists in each, but the posting names no end employer and the role has no corroboration anywhere; neither case shows the impersonation indicators behind the stronger verdicts, and neither firm is labelled fraudulent.
- One case showed a LinkedIn company page displaying a placeholder name ("No aplica", Spanish for "not applicable") while its URL slug named a real Mexican law firm. A second, unrelated company's page also displayed the same placeholder. Who controlled either page, and whether any renaming was unauthorized, is Not Verified.
- Case-008 went one step further than impersonation: no LinkedIn company page exists for the advertised employer at all, and no website, business registration, or any other trace of a business under that name could be found anywhere. The employer identity appears fabricated wholesale rather than borrowed.
- Case-009 is the register's first stale-requisition case: the employer (Wrench Group) is real and the posting ran under its own name, but at verification time its own applicant tracking system carried no such opening at all — only an unrelated HVAC technician job — and the listing text matches an approximately 8-month-old mirror under a different title. It is recorded as not verified, not fake: a closed role recirculating through aggregators is a documented possibility, and no impersonation indicator was established.
- Case-010 is the register's sharpest grading call: the advertised employer (Spiralation) is a real Sri Lankan government startup-accelerator program with no US presence and no security-sector activity, the company website listed on its LinkedIn page does not resolve, the poster is publicly an ETL/Informatica developer with no affiliation to the program, and the posting exists only on LinkedIn — the same indicator cluster behind the likely-fake impersonation verdicts in Cases 002, 003, 005, and 006. It is nevertheless recorded as not verified, not likely fake, on the investigator's verdict: the evidence establishes a total employer/job mismatch, but not who created the posting or why.
- Case-011 is a second instance of the Case-009 variant, and the register's first sighting from an aggregator rather than LinkedIn: a RemoteRocketship card advertised a "Security Engineer" role under DISCO's name as fully remote with pay undisclosed, the full description behind a sign-up wall — but DISCO's own careers board, read in full, carries no security-titled role at all, and its standalone Greenhouse board is deactivated. The card could not be corroborated on the employer's own site: stale, mislabeled, or never a live DISCO requisition. It is recorded as not verified, not fake, and DISCO is not labelled fraudulent.
- Cases 012 (V2Soft) and 014 (Blue Mantis) are further instances of the employer-board-absence variant: in both, the advertised role had no presence on the poster's or employer's own careers board at verification time — V2Soft's board listed 150 jobs with no Network Security Engineer, and Blue Mantis's board listed 37 jobs with no Security Analyst L1 — and in both the LinkedIn posting itself had already been removed, so no posting text survives to verify against. Case-012's poster is a staffing firm whose posting named no client employer; Case-014's listing additionally contradicted itself on location. Neither firm is labelled fraudulent.
- Cases 013 (Torentify / Innodata) and 015 (TaskVerse / FetchJobs) are the register's first mislabeled-repost cases: a third-party front republishes a real employer's job under its own name, and the repost misrepresents the work. Case-013's card advertised a full-time remote cybersecurity role, while the named employer's own posting for the matching work describes part-time, project-based AI-training contributor work at $15/hr. Case-015's body paraphrases a real CrowdStrike Systems Engineer II role with its experience requirement and pay stripped out, and the duties are production-systems / SRE work, not cybersecurity analysis. Whether either repost was authorized is Not Verified, and neither poster is labelled fraudulent.

The evidence supports a shared pattern and playbook across several cases. It does **not** establish that a single actor operates all of them, and this project makes no attribution claim.

## Limitations

- All evidence is point-in-time public data gathered at investigation time. Postings and company pages change or disappear; several postings closed during or shortly after investigation.
- Screenshots were not retained as files. Evidence is preserved as dated investigation notes with source URLs (see `evidence/evidence-register.md` and `evidence/redacted-screenshots/README.md`). For Case-001, the original LinkedIn URL and job ID were recovered from the contemporaneous dated investigation log, and the verdict rests on that log plus the employer-site verification performed on 2026-10-02; no screenshot or side-by-side text-comparison file was preserved.
- Verdicts are analytical assessments based on public evidence, not legal determinations. Nine cases (Case-004, Case-007, Case-009, Case-010, Case-011, Case-012, Case-013, Case-014, and Case-015) are explicitly recorded as unverifiable rather than fake, because the evidence did not support a stronger label.
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
│   ├── case-007.md
│   ├── case-008.md
│   ├── case-009.md
│   ├── case-010.md
│   ├── case-011.md
│   ├── case-012.md
│   ├── case-013.md
│   ├── case-014.md
│   └── case-015.md
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
