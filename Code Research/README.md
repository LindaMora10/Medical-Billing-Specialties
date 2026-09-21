# Code Research

Per-code payer research memos. One file per code, named
`CPT_<code>_Payer_Research_<YYYY-MM-DD>.md`, dated to the day the policies were pulled.
The folder also holds the per-code **routing workbook**, which answers "who decides, and is auth
required" for a given member rather than documenting the code itself.

| File | Code | Question | Date |
|---|---|---|---|
| `CPT_64772_Billing_Playbook_2026-09-15.md` | 64772 | **Operational — how the billing department bills it.** Op-note requirements, dx, claim construction, modifiers, POS, AZ allowables, denial playbook, go-live checklist | 15 Sep 2026 |
| `CPT_64772_Payer_Research_2026-09-15.md` | 64772 | **Reference — the underlying research.** Code validation (vs 64633–64636 / 64625) + AZ payer coverage, PA, POS, NCCI, dx, modifiers, with full citations | 15 Sep 2026 |
| `CPT_64772_Auth_Routing_2026-09-21.xlsx` | 64772 | **Routing — who decides prior auth, and where to go.** One tab per network (`BCBS`, `Optum`, `UnitedHealthcare`, `Medicare`, `Humana`), one row per plan. Each row carries the plan's identifiers (alpha prefix, payer ID, CMS contract, PBP, group number — each in its own column), the authorization answer and referral rule, where to check and where to submit, and the governing document with what it requires | 21 Sep 2026 |

Where a code has both, the **playbook is the working document** and the research memo is what it cites.

The workbook is sourced from the payer documents in `Plan Guides/` and from the research memo. Its
`Status` column separates **Published** from **Practice-verified**; `TO CONFIRM` means no published
source has been located yet, not that the answer is no. Member-identifying data (alpha prefix, payer
ID, CMS contract, PBP, group number) each gets its own column and is never mixed into a single field.
Every tab shares the same 24-column layout: **A–H** identify the plan, **I–N** answer the
authorization question, **O–U** give the governing policy and its criteria, **V–X** record provenance.

## What each memo covers

1. **Code validation** — exact AMA descriptor, what the code actually describes, and whether the
   procedure as described should be reported with a different code.
2. **Payer-by-payer** — coverage status, prior authorization and vendor, approved place of service,
   NCCI/bundling, frequency limits, conservative-care prerequisites, documentation, and how the rule
   changes by plan type (commercial / Medicare Advantage / AHCCCS) or plan group number.
3. **Diagnosis / medical necessity** — which ICD-10 families support the code, whether a covered-dx
   table exists at all, and dx-to-CPT edits.
4. **Modifiers and particularities** — laterality and modifier 50, MUE and MAI, same-session billing,
   assistant/co-surgeon indicators, ASC vs HOPD, global period, credentialing.
5. **What could delay scheduling or trigger a denial** — ranked, plus open items that could not be
   closed from published sources.

## Conventions

- Every policy is cited by **name, number, effective date, link, and the path within that link**.
- ⚠️ marks a finding that is **not** verified from a published source.
- 🔴 marks a blocker or an active denial risk.
- Where no published policy exists, the memo says so explicitly rather than inferring one. Items in the
  memo's *Open Items* table need a human answer from the payer before they are relied on.
- Payment indicators, MUE/MAI values and NCCI edits are taken from the **primary CMS data files**
  (PFS Relative Value File, Practitioner MUE table, Practitioner PTP edit files, ASC Addenda), not from
  secondary code-lookup sites.
