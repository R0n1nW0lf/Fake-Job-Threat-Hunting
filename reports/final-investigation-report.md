# Final Investigation Report

**Project:** Fake Job Recruitment Threat Hunting and OSINT Investigation
**Investigator:** Ronald Wolf, SOC analyst candidate
**Investigation period:** September 30 – October 24, 2026
**Report date:** 2026-10-16 (updated 2026-10-17 to add Case-007; updated 2026-10-20 to add Case-008; updated 2026-10-23 to add Case-009; updated 2026-10-23 to add Case-010; updated 2026-10-24 to add Case-011)

## Executive Summary

During a cybersecurity job search, eleven suspicious job postings were investigated using a structured OSINT method: observe, hypothesise, gather evidence, verify against independent sources, then conclude and act. One posting was a confirmed scam that copied a real employer's job. Five postings received likely fake verdicts: four built on multiple independent indicators of impersonation (real foreign businesses with no connection to the role, posters publicly affiliated with unrelated employers, dead or absent domains, and — in Cases 002, 003, 005, and 006 — no corroboration for the role found outside LinkedIn), and one (Case-008) where the advertised employer appears fabricated wholesale — no LinkedIn company page, website, business registration, or any other trace of the business could be found. Rapid closure is documented in two of the patterned cases (Case-002 in approximately 2 hours, Case-006 within approximately 7 hours). Whether any posting's purpose was information harvesting is a hypothesis, not an established finding. Five postings could not be verified and were skipped without being labelled fraudulent, because the evidence did not support a stronger verdict. No application was submitted to any of the eleven postings, and no personal information was sent.

## Scope and Methodology

Scope: Cybersecurity job postings encountered during the investigator's own job search between September 30 and October 24, 2026, that presented indicators of impersonation, copying, or information harvesting. Ten were sighted on LinkedIn; one (Case-011) was sighted as an aggregator card on RemoteRocketship.

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
| CASE-007 | Nexorant LLC | Not verified — skip (not proven fake) | Low (insufficient evidence either way) |
| CASE-008 | REVO — Revolutionary Volatility Operations | Likely fake / fabricated employer | High (no trace of the business found in any source checked) |
| CASE-009 | Wrench Group | Not verified — skip (not proven fake) | Low (insufficient evidence either way; no live requisition on the employer's own ATS) |
| CASE-010 | Spiralation | Not verified — skip (not proven fake) | Low (insufficient evidence either way; no corroboration for the role outside LinkedIn) |
| CASE-011 | DISCO | Not verified — skip (not proven fake) | Low (insufficient evidence either way; no security-titled role on the employer's own careers board) |

Full evidence for each case is in `investigations/`, and the indicator dataset is in `indicators/suspicious-listings.csv`. Every source checked is logged in `evidence/evidence-register.md`.

**Evidence basis for Case-001:** the confirmed-scam verdict rests on the contemporaneous dated investigation log of 2026-10-02 — which records the recovered original LinkedIn URL and job ID (4474739609), the header/body mismatch, and the genuine employer's identity — together with the verification performed that day against EaglePicher Technologies' own careers (iCIMS) page. No screenshot or side-by-side text-comparison file was preserved; that limitation is stated in the case file and the evidence register.

## Correlation Findings

Across Cases 002, 003, 005, and 006 the same pattern recurs: a real foreign business's name or page, a generic US-remote cybersecurity template, a poster with no affiliation to the named company (or no poster at all), a dead or absent domain, and no corroboration for the role found outside LinkedIn. On seniority the record is precise rather than uniform: Cases 003, 005, and 006 were junior-titled, while Case-002 was open to 0–3 years of experience. On closure: Case-002 closed approximately 2 hours after going live and Case-006 within approximately 7 hours; Case-003 also closed (interval Not Verified) and Case-005's closure status is Not Verified. Sister postings reusing identical templates were documented in Cases 002, 003, and 005. Case-006 additionally showed two company pages displaying the placeholder name "No aplica"; how that display came about is Not Verified (see Unresolved Questions). Case-001 used a different technique, copying a real employer's job text outright, and its copied body text described a senior role.

The evidence supports a shared pattern and playbook. It does not establish that a single actor operates all of these postings, and no attribution is claimed. Full detail is in `analysis/correlation-analysis.md`.

Case-007 (Nexorant LLC, investigated 2026-10-17) does not extend that pattern. It shares the blind-posting indicators — a generic template naming no end employer, and no corroboration for the role found anywhere — but none of the impersonation indicators: the account appears to be the firm's own, no poster mismatch or copied text was found, and no dead domain was involved. Together with Case-004, it forms a second, distinct category in this register: unverifiable blind staffing posts, recorded as not verified rather than fake.

Case-008 (REVO — Revolutionary Volatility Operations, investigated 2026-10-20) is a third variant. It shares the generic-template and zero-corroboration indicators, but no real business was impersonated and no traceable firm posted it: no LinkedIn company page exists for the advertised employer, no website or business registration under the name was located, and an exact-name web search found no trace of any such business. The employer identity appears fabricated wholesale. Who created the posting, and why, is Not Verified.

Case-009 (Wrench Group, investigated 2026-10-23) is a fourth variant, and the register's first stale-requisition case. The employer is real and the posting ran under its own name, but at verification time its own iCIMS applicant tracking system carried no such opening at all — an unfiltered search showed only an unrelated HVAC Maintenance Technician job, and keyword searches and the IT category filter all returned "no jobs found". The listing text matches an approximately 8-month-old mirror under a different title, and one mirror already records the role as no longer listed. The evidence supports "not verified — skip", not "fake": a closed role recirculating through aggregators, or a sync failure, cannot be excluded, and no impersonation indicator was established.

Case-010 (Spiralation, investigated 2026-10-23) carries the impersonation pattern's indicator cluster — a real foreign business unconnected to the role (a Sri Lankan government startup-accelerator program with no US presence), a poster publicly affiliated elsewhere, a listed company website that does not resolve, and no corroboration for the role outside LinkedIn — but it is recorded as not verified, not likely fake, on the investigator's verdict. The evidence establishes a total employer/job mismatch and the absence of any legitimate US hiring employer behind the posting; it does not establish who created the posting or why, and the verdict is not upgraded on the strength of the cluster alone.

Case-011 (DISCO, investigated 2026-10-24) is a second instance of the Case-009 variant, and the register's first sighting from an aggregator rather than LinkedIn. A RemoteRocketship card advertised a "Security Engineer" role under DISCO's name as fully remote with pay undisclosed, the full description behind a sign-up wall. DISCO's own careers board, read in full across every department, carries no "Security Engineer" and no security-titled role of any kind, and its standalone Greenhouse board is deactivated, so the checked embedded board is the only official board where the role could appear. The employer is real and the card ran under its own name; no impersonation indicator was established. Whether the card was stale, mislabeled, or pointed to a posting that never was a live DISCO requisition is Not Verified, and the evidence supports "not verified — skip", not "fake".

## Impact

The applicant counts documented in these investigations are the counts LinkedIn displayed: 16 applicants displayed at first sighting in Case-002, 26 applicants displayed in Case-003, 26 applicants displayed in Case-006, 3 applicants displayed in Case-007 (whose posting was still open at the investigation check), and 7 applicants displayed in Case-008 (also still open at its investigation check). The displayed counts for Cases 001, 004, 005, 009, 010, and 011 are Not Verified. Case-010's posting displayed "Be among the first 25 applicants" — that is a display prompt, not an applicant count, and it is not recorded as one.

A displayed applicant count does not prove that any applicant's information was received, stored, or misused. It is not known how many complete applications were submitted through any of these postings, what information each applicant sent, or what happened to it afterwards. If a posting was fraudulent, applicants who applied through it could have exposed their resumes and contact details to an unknown party — that exposure is a **potential risk (hypothesis)**, not a measured outcome, and no total of affected people can be supported by the available evidence. The investigator's own exposure was zero, because verification preceded every application decision.

## Unresolved Questions

- Who operates these postings and pages. No evidence gathered supports attribution to any individual or group.
- Whether the real firms' LinkedIn pages were compromised, renamed by an insider, or imitated by lookalike pages. The evidence differs by case. For Case-006, the hypothesis that the genuine page was renamed or hijacked without authorization is **Not Verified**: the confirmed observations are the placeholder display name and its mismatch with the URL slug, and there is no direct evidence of compromise, unauthorized renaming, or of who controls the page. Alternatives such as a platform data error or repurposing of an abandoned page cannot be excluded.
- What applicants who did apply were later contacted for, and whether any information they submitted was received or used for further phishing or fraud. No applicant outcome data is available, so this remains unknown rather than assumed.
- Whether the Case-004 firm is a legitimate business with poor presentation or something else. It remains unverifiable on current evidence.
- Whether the Case-007 posting was a genuine client role posted blind by the staffing firm, or something else. The end employer is unnamed and the role is uncorroborated, so it remains unverifiable on current evidence; the firm's inconsistent HQ claims (Moline, IL vs Chicago, IL) are documented but unexplained.
- Whether any business at all stands behind the Case-008 advertised name. No trace of one was found in any source checked; whether the name was invented for this posting or belongs to an unregistered, unlisted operation cannot be determined from public evidence.
- Whether the Case-009 role was ever a live Wrench Group opening that closed before verification, or a requisition that recirculated without the employer's involvement. The employer's ATS carried no trace of it at verification time, and public evidence cannot distinguish between a filled-and-removed opening, a sync error, and an unauthorised repost.
- Who created the Case-010 posting under the Spiralation name, and whether the real program's name and page were used with or without authorization. Public evidence establishes the employer/job mismatch, the dead listed domain, and the poster's lack of affiliation, but not the mechanism, the actor, or the purpose behind the posting.
- Whether the Case-011 aggregator card was stale, mislabeled, or pointed to a posting that never was a live DISCO requisition. The employer's own careers board carried no trace of the role at verification time, and the card's description could not be read behind the sign-up wall, so public evidence cannot distinguish those possibilities.

## Recommendations

**For job seekers**

- Verify the role on the employer's own website before applying.
- Check the poster's affiliation, the company page's Jobs tab, and the industry and location shown on the page itself.
- Resolve the contact domain; treat a dead domain as a stop sign.
- Phrase-search the description; treat employer-free template text as a red flag.
- Treat postings that close within hours as suspect, and never submit personal information before verification.

**For platforms**

- Detect and review company pages displaying placeholder values, and jobs whose industry, location, and company size contradict the page that carries them.
- When a posting is confirmed fraudulent, notify every applicant who submitted information through it.

**For impersonated businesses**

- Monitor your company page name, Jobs tab, and job-board presence, especially if your business is small and outside the advertised industry. Report impersonation promptly and keep a public note on your own website stating where genuine vacancies are posted.

## Corrections Applied 2026-10-16

This report and the repository were reviewed after initial drafting, and the following corrections were applied. Original findings were not deleted; wording was corrected and provenance added.

- **Case-001 evidence recovered.** The original LinkedIn URL and job ID (4474739609), the YAZAKI header/body mismatch, the EaglePicher identification, and the repost history were recovered from the contemporaneous dated investigation log of 2026-10-02 and added to the case file, the CSV, and the evidence register. The confirmed-scam verdict is retained on that documented basis, with the limitation now stated everywhere it matters: no screenshot or side-by-side comparison file was preserved.
- **Applicant-count terminology corrected.** Earlier drafts said postings "collected" or "harvested" applicants, including a claim that each patterned posting collected roughly 26 applicants. A displayed LinkedIn count does not prove receipt or misuse of anyone's information. All such statements were replaced with per-case displayed counts (Case-002: 16 at first sighting; Case-003: 26; Case-006: 26; Cases 001, 004, 005: Not Verified), and information harvesting is now framed throughout as a hypothesis / potential risk.
- **Case-006 observations separated from hypothesis.** The confirmed observations (placeholder display name, URL-slug mismatch, law-practice page fields, second page displaying the same placeholder, rapid closure) are now listed separately from the hypothesis that the genuine page was renamed or hijacked without authorization, which is marked **Not Verified** in the case file, the correlation analysis, and this report.
- **Unsupported generalizations corrected.** Claims that every posting targeted entry-level candidates, that every role existed only on LinkedIn, and that all postings showed roughly 26 applicants were replaced with the per-case record: Case-001's copied body was senior-level and its genuine role existed at the real employer; Case-002 allowed 0–3 years; Case-004's level is unknown; "no corroboration found outside LinkedIn" is now scoped to the cases where searches were actually performed.
- **Evidence register added.** `evidence/evidence-register.md` now logs every source checked, per case, with collection dates, verification methods, and limitations. It records plainly that no screenshots or evidence files were preserved and therefore no SHA-256 hashes exist.
- **Sources sections added.** Each case file now ends with a Sources list naming the concrete references documented in the investigation logs; anything beyond those is marked "Not Verified".

## Responsible Disclosure and Privacy Note

These investigations used public information only. No suspicious party was contacted, no test applications were submitted, and no applicant personal information is published in this repository. Poster names appear only where they were publicly displayed on the posting itself, with their publicly listed affiliation, as documented evidence. Verdicts are analytical assessments, not legal determinations, and Cases 004, 007, 009, 010, and 011 are deliberately recorded as unverifiable rather than fraudulent. Screenshots were not retained as files; evidence is preserved as dated investigation notes with source URLs (itemised in `evidence/evidence-register.md`), and unrecorded fields are marked "Not Verified" rather than reconstructed.
