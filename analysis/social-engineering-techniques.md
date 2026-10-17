# Social Engineering Techniques Observed

Each technique below was observed in at least one investigated case. A defensive countermeasure follows each one.

## 1. Impersonation of real foreign small businesses and coalitions

Postings ran under the names of real organisations: a Dutch climate-finance coalition (Case-002), a Dutch youth-care sole proprietorship (Case-003), a Costa Rican outsourcing firm (Case-005), and a Mexican law firm (Case-006). Real names borrow credibility, and small foreign organisations are less likely to notice or police a US job board quickly.

**Countermeasure:** Verify the business independently. Check what the real organisation actually does, where it is based, and whether it operates in the advertised country and industry at all.

## 2. Placeholder company-page display name (mechanism Not Verified)

In Case-006, a real firm's LinkedIn page displayed the name "No aplica" ("not applicable") while its URL slug still named the firm. A second company's page displayed the same placeholder name. How the placeholder display came about — unauthorized renaming, account compromise, platform error, or another cause — is **Not Verified**; no evidence in the investigation establishes the mechanism. The observable effect, whatever the cause, is a page whose displayed name conceals the business identified by its URL, industry, and location fields.

**Countermeasure:** Read the company page URL slug, industry, headquarters, and size, not just the displayed name. A mismatch between the page's actual business and the advertised role is a strong warning sign.

## 3. Borrowed credibility

Real organisation names, plausible job titles, and familiar tool keywords (SIEM, Splunk, Security+) make a template posting look like a genuine opening at a genuine employer.

**Countermeasure:** Treat recognisable names as a claim to verify, not as proof. Search for the role on the organisation's own site before trusting the listing.

## 4. Template job text and junior-role framing

Most of the patterned postings were junior-titled (Cases 003, 005, and 006), and Case-002 was open to 0–3 years of experience. Their descriptions were generic, listing standard tools and duties and naming no employer in the text itself (explicit in Case-006; template reuse documented in Cases 002, 003, and 005). Case-001 does not fit this point: its copied body text described a senior role. Junior roles draw high application volume, and candidates new to the field may have less experience spotting recruitment fraud.

**Countermeasure:** Phrase-search a distinctive sentence from the description. Check whether the text names the employer, a team, a location, or anything specific. Pure template text is a red flag.

## 5. Low-friction application routes

The postings used LinkedIn Easy Apply (Cases 002–005). One-click applying lowers the applicant's guard and moves personal information (resume, contact details) to the poster quickly.

**Countermeasure:** Slow down at the apply step. Easy Apply is exactly where verification matters most, because it is designed to make you submit before you think.

## 6. Urgency through rapid open and close windows

Two postings are documented as closing within hours of going live: roughly 2 hours in Case-002, which displayed 16 applicants at first sighting, and roughly 7 hours in Case-006, which displayed 26 applicants. Case-003 also closed with 26 applicants displayed, but its closure interval is Not Verified, so it is not counted here. A short window can pressure candidates to apply immediately and limits the time available for scrutiny or reporting; that pressure effect is an interpretation of the pattern, not a measured outcome.

**Countermeasure:** A posting that appears and vanishes within hours is itself an indicator. Legitimate employers rarely run a full hiring window in a single morning.

## 7. Geographic bait

Listings used attractive US locations and remote labels: Los Angeles County (Case-002), New York (Case-005), Pennsylvania remote (Case-006), Ohio remote (Case-003). In Case-002 the listed location even contradicted the description text. Remote US roles draw the largest applicant pool.

**Countermeasure:** Cross-check the listed location against the description and against where the real business actually operates.

## 8. Exposure of career changers and new graduates

The precise seniority record across the seven cases is mixed: Cases 003, 005, and 006 were junior-titled, Case-002 was open to 0–3 years of experience, Case-004's level is unknown, Case-007 stated no seniority level, and Case-001's copied body text described a senior role. What the cases share is where they surfaced — in searches for junior cybersecurity roles, the segment with the most applicants and the strongest motivation to apply quickly and share information freely.

**Countermeasure:** New candidates should assume they are a preferred target for this pattern and apply the verification steps in `analysis/lessons-learned.md` before every submission, especially for junior remote roles.
