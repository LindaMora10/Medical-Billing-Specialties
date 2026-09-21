# Code Research

Per-code payer research memos. One file per code, named
`CPT_<code>_Payer_Research_<YYYY-MM-DD>.md`, dated to the day the policies were pulled.
The folder also holds the payer **routing workbook**, which answers "who decides, and is auth
required" per plan rather than documenting the code itself.

| File | Code | Question | Date |
|---|---|---|---|
| `CPT_64772_Billing_Playbook_2026-09-15.md` | 64772 | **Operational — how the billing department bills it.** Op-note requirements, dx, claim construction, modifiers, POS, AZ allowables, denial playbook, go-live checklist | 15 Sep 2026 |
| `CPT_64772_Payer_Research_2026-09-15.md` | 64772 | **Reference — the underlying research.** Code validation (vs 64633–64636 / 64625) + AZ payer coverage, PA, POS, NCCI, dx, modifiers, with full citations | 15 Sep 2026 |
| `AZ_Blue_Prefix_Routing_2026-09-15.xlsx` | 64772 + general | **Routing — which entity decides prior auth.** Tab `64772`: PA answer by payer, prefix / payer ID and delegated vendor across BCBS, Optum, Medicare, UnitedHealthcare and Humana. Tab `Optum & UHC Plans`: the Optum-delegated and UHC plan inventory — plan name, CMS contract, group numbers, plan type, delegation level, referral rule | 21 Sep 2026 |

Where a code has both, the **playbook is the working document** and the research memo is what it cites.

The workbook is sourced from the payer documents in `Plan Guides/` and from the research memo. Its
`Status` column separates **Published** from **Practice-verified**; `TO CONFIRM` means no published
source has been located yet, not that the answer is no.

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
