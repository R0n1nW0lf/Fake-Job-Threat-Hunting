# Final Investigation Report

**Project:** Fake Job Recruitment Threat Hunting and OSINT Investigation
**Investigator:** Ronald Wolf, SOC analyst candidate
**Investigation period:** September 30 – October 16, 2026
**Report date:** 2026-10-16

## Executive Summary

During a cybersecurity job search, six suspicious LinkedIn job postings were investigated using a structured OSINT method: observe, hypothesise, gather evidence, verify against independent sources, then conclude and act. One posting was a confirmed scam that copied a real employer's job. Four postings received likely fake / impersonation verdicts, each built on multiple independent indicators: real foreign businesses with no connection to the role, posters publicly affiliated with unrelated employers, dead or absent domains, roles that existed nowhere outside LinkedIn, and rapid closure after collecting applicants. One posting could not be verified and was skipped without being labelled fraudulent, because the evidence did not support a stronger verdict. No application was submitted to any of the six postings, and no personal information was sent.

## Scope and Methodology

Scope: LinkedIn cybersecurity job postings encountered during the investigator's own job search between September 30 and October 16, 2026, that presented indicators of impersonation, copying, or information harvesting.

Methodology: each case followed the loop Observation → Hypothesis → Evidence → Verification → Conclusion → Action Taken, guided by the principle: don't assume, gather evidence, question it, analyse it, and verify the source before trusting it. Verification used public web search (including exact-phrase searches), DNS and domain resolution checks, business directories, employer websites and careers pages, and LinkedIn company pages and Jobs tabs. No suspicious party was contacted and no test application was submitted.

## Case Summaries

| Case | Advertised company | Verdict | Confidence |
|---|---|---|---|
| CASE-001 | Netrolynx AI | Confirmed scam (copied a real employer's job) | Confirmed |
| CASE-002 | NL AAA – Climate Resilient | Likely fake / impersonation | High |
| CASE-003 | Consultancy by MB | Likely fake / same pattern | High |
| CASE-004 | Divine Talent | Not verified — skip (not proven fake) | Low (insufficient evidence either way) |
| CASE-005 | VITAL • Soluciones | Likely fake / impersonation | High |
| CASE-006 | "No aplica" (Gestiuno Servicios Legales, S.C.) | Likely fake / impersonation | High |

Full evidence for each case is in `investigations/`, and the indicator dataset is in `indicators/suspicious-listings.csv`.

## Correlation Findings

Across Cases 002, 003, 005, and 006 the same playbook recurs: a real foreign business's name or page, a generic US-remote cybersecurity template aimed at entry-level candidates, a poster with no affiliation to the named company (or no poster at all), a dead or absent domain, no trace of the role anywhere outside LinkedIn, and closure within hours after collecting applicants. Sister postings reusing identical templates were documented in Cases 002, 003, and 005. Case-006 additionally showed company pages renamed to the placeholder "No aplica", including a second, unrelated company's page. Case-001 reached the same goal by a different technique, copying a real employer's job text outright.

The evidence supports a shared pattern and playbook. It does not establish that a single actor operates all of these postings, and no attribution is claimed. Full detail is in `analysis/correlation-analysis.md`.

## Impact

Each posting in this pattern collected roughly 26 applicants before closing (documented in Cases 003 and 006; 16 already at first sighting in Case-002). Every applicant on a fake posting hands a resume and contact details to an unknown party. The exposed population across the investigated postings is therefore plausibly in the dozens to low hundreds of candidates, concentrated in exactly the group least able to absorb the harm: entry-level candidates and career changers. The investigator's own exposure was zero, because verification preceded every application decision.

## Unresolved Questions

- Who operates these postings and pages. No evidence gathered supports attribution to any individual or group.
- Whether the real firms' LinkedIn pages were compromised, renamed by an insider, or imitated by lookalike pages. The evidence differs by case. In Case-006 the page URL slug matches the real firm's name, which suggests the genuine page was renamed or hijacked; that remains a hypothesis, not a proven fact.
- What applicants who did apply were later contacted for, and whether the harvested data fed further phishing or fraud. No applicant outcome data is available.
- Whether the Case-004 firm is a legitimate business with poor presentation or something else. It remains unverifiable on current evidence.

## Recommendations

**For job seekers**

- Verify the role on the employer's own website before applying.
- Check the poster's affiliation, the company page's Jobs tab, and the industry and location shown on the page itself.
- Resolve the contact domain; treat a dead domain as a stop sign.
- Phrase-search the description; treat employer-free template text as a red flag.
- Treat postings that close within hours as suspect, and never submit personal information before verification.

**For platforms**

- Detect and review company pages renamed to placeholder values, and jobs whose industry, location, and company size contradict the page that carries them.
- When a posting is confirmed fraudulent, notify every applicant who submitted information through it.

**For impersonated businesses**

- Monitor your company page name, Jobs tab, and job-board presence, especially if your business is small and outside the advertised industry. Report impersonation promptly and keep a public note on your own website stating where genuine vacancies are posted.

## Responsible Disclosure and Privacy Note

These investigations used public information only. No suspicious party was contacted, no test applications were submitted, and no applicant personal information is published in this repository. Poster names appear only where they were publicly displayed on the posting itself, with their publicly listed affiliation, as documented evidence. Verdicts are analytical assessments, not legal determinations, and Case-004 is deliberately recorded as unverifiable rather than fraudulent. Screenshots were not retained as files; evidence is preserved as dated investigation notes with source URLs, and unrecorded fields are marked "Not Verified" rather than reconstructed.
