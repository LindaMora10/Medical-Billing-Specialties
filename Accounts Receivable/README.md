# Accounts Receivable

`AR_Analysis_Grid_Merged_2026-09-21.xlsx` — the AR Service Line Analysis Grid collapsed to
**one row per claim**, with Lien, Workers' Compensation and Self Pay claims removed.

Built from the practice management export `Account_Receivable.ARAnalysisGrid_2026-09-21.xlsx`
(AR Service Line - Analysis Grid, ADVANCED SPINE AND PAIN LLC, date span 01/01/2026 - 09/21/2026,
date type Date of Service).

Snapshot date: **21 September 2026**.

## What changed from the source export

| | Claims | Service lines |
|---|---|---|
| Source export | 3,532 | 5,944 |
| Removed — Lien payers | 315 | 498 |
| Removed — Workers' Compensation payers | 32 | 45 |
| Removed — Self Pay | 61 | 77 |
| **In this workbook** | **3,124** | — |

Control totals for the retained claims, unchanged from the source:

| Column | Total |
|---|---|
| Insurance Payment | 1,533,901.37 |
| Insurance Balance | 7,718,220.84 |
| Total Balance | 7,802,171.34 |

## Merge rules

Claims are grouped on `Primary Claim ID`. Every other column except the ones below is identical
across the service lines of a claim, so nothing is lost in the collapse.

- `Procedure Code` — all codes for the claim, comma separated, in original service line order.
  Repeated codes are kept as repeats, since each is a separate service line with its own payment.
- `Insurance Payment`, `Insurance Balance`, `Total Balance` — summed across the claim's lines.
- `Insurance Check Date` — the **most recent** check date where a claim's lines disagree
  (54 claims in the source). Not specified by the merge request; chosen as the AR-relevant value.

## Exclusions

- **Lien** — `Primary Payer Name` beginning `LIEN` (LIEN 01, 03, 05, 06, 12, 14).
- **Workers' Compensation** — any `WC *` payer name, plus any row whose `Primary Payer Type`
  or `Primary Payer Class` is Workers Compensation. This captures `WC OWCP DFEC` (classed
  Commercial but federal workers' comp) and `MSA Care Guard - RelayHealth 20572`
  (classed Workers Compensation).
- **Self Pay** — `Primary Payer Name` of `SELF PAY`.

Two claims carry a `Primary Payer Class` of Self-pay but a real insurance payer name
(`HealthSpring Medicare Advantage`, `Humana Gold Plus HMO`). These look like misclassified
claims rather than self pay and were **kept**.

Other liability payers (Auto Accident, non-LIEN Liability Medical) were kept — only Lien and
Workers' Compensation were in scope.

## Prefix column

`Prefix` sits immediately after `Primary Insurance ID` and holds the member ID prefix where the
payer uses one. Populated on 1,365 of 3,124 rows; blank where the member ID is purely numeric
(Medicare MBIs, most UnitedHealthcare, Tricare), which genuinely have no prefix.

Rules, applied in order:

1. **BCBS payers** — first 3 characters, since the BCBS alpha prefix is always exactly 3
   characters (`M2K`, `P9H`, `S3Z`, `Y4M`, `DOM`, `NDZ` — 84 distinct on BCBS AZ).
   `HCIA…` IDs landing on BCBS-labelled claims return `HCIA`, as those are Health Choice IDs.
2. **BCBS alpha prefix under another payer name** — IDs matching letter-digit-letter followed by
   digits take the first 3 characters, so `M2K860127490` on Optum Care and Arizona Priority Care
   Plus returns `M2K`, not `M`.
3. **Devoted Health Plan** — always `D`. Their IDs are `D` plus 5 alphanumerics
   (`D3WECW`, `DWZ39K`), so the generic rule would produce false prefixes.
4. **Everything else** — the leading run of letters: `A` for AHCCCS plans, `R` for FEP style IDs,
   plus `H` Humana, `W` Aetna, `U` Cigna/HealthSpring, `C` Centene, `B` Banner Medicare Advantage,
   `OSC` Oscar, `HCIA` Health Choice, `HIM` Imperial, `MZHHC` Health Choice Pathway,
   `UZ` Ambetter, `MA`, `ZZ`, `G`, `SN`.
5. **Member ID starting with a digit** — blank.

## Row order

Sorted by payer key ascending, then newest to oldest within each key.

The payer key is `Primary Payer Name` + `Primary Payer Type` + `Primary Payer Class` +
`Primary Payer Group Name` + `Primary Payer Group Number` + `Prefix`, with `Prefix` joining the
key only where the row has one. That gives **603 keys**, each in one contiguous block.

Comparison is case-insensitive, so group numbers differing only in casing (`AZHCCCS` / `azhcccs`,
`AZMCARE` / `azmcare`, and 6 others) stay in one block rather than splitting into two.

Within a key, rows run newest to oldest by `Date of Service` — the report's own date type — with
`Created Date` and then `Primary Claim ID` as tiebreakers. Range: 09/15/2026 back to 01/05/2026.

## Concentration

Across the 603 keys:

| | Claims | Share | Total Balance | Share |
|---|---|---|---|---|
| Top 5 keys | 940 | 30.1% | 1,519,159.55 | 19.5% |
| Top 10 keys | 1,196 | 38.3% | 2,382,286.58 | 30.5% |
| Top 20 keys | 1,496 | 47.9% | 3,338,640.57 | 42.8% |
| Top 50 keys | 1,945 | 62.3% | 4,754,494.32 | 60.9% |

The largest single key is `Medicare Part B Arizona *` / Medicare FFS at 539 claims (17.3%) and
626,942.76 in total balance, followed by `DME Region D` / Medicare FFS at 181 claims (5.8%) and
526,671.33. The tail is long: 296 keys hold a single claim, together 9.5% of volume.

Claim count and balance do not track each other. `UHC Group Medicare Advantage` (group 12754)
carries 318,209.83 over just 32 claims, and `Humana Gold Plus HMO` / Commercial FFS / `H` carries
155,972.49 over 11 claims — roughly 14,000 per claim, the highest of any sizable key.
