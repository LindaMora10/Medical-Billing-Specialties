# Timely Filing Database

`Timely_Filing_10_Day_Watchlist_2026-08-10.xlsx` — pending claims whose timely filing deadline
falls **within the next 10 days**, based on the **primary payer** on each claim.

Built from:

- `Specialty Claims Pending 2026-S1.xlsx` — the `Merged` sheet (1,086 claim lines)
- `Carrier_Timely_Filing_Reference.xlsx` — the `Timely Filing` sheet (carrier limits)

Snapshot date: **10 August 2026**.

## Tabs

| Tab | What it holds |
|---|---|
| `Read Me` | Method, counts, how to use the file, assumptions and caveats |
| `Payers Needing Limits` | Primary payers with no limit on file — these claims could not be given a deadline |
| `BH` | Behavioral Health — 14 claim lines |
| `DME` | Durable Medical Equipment — 5 claim lines |
| `GAE` | Genicular Artery Embolization — 0 claim lines in the window |
| `ORTHO` | Orthopedic — 11 claim lines |
| `US` | Ultrasound — 17 claim lines |
| `All Claims` | All 47 claim lines, no specialty split |

## Column order

Every claims tab uses the same layout, starting with:

`Claim Status` · `Notes` · `Primary Claim ID` · `Chart Number` · `Responsible Payer` ·
`Primary Payer Name` · `Secondary Payer Name` · `Date of Service` · `Procedure Code`

then `Specialty`, the deadline calculation (`Filing Deadline`, `Days Until Deadline`,
`Timely Filing Limit (Days)`, `Reference Carrier`, `Limit Basis / Caveat`), then the billing
detail (modifiers, units, charges, payments, balance, AR age) and the reference detail
(provider, location, secondary claim ID, created date, check date, diagnosis codes).

## Linked Claim Status and Notes

`Claim Status` and `Notes` are the **amber** columns — they are the only cells meant to be typed in,
and only on the **specialty** tabs.

On `All Claims`, those two columns are formulas pointing at the matching row on the specialty tab
(`=IF('US'!A12="","",'US'!A12)`). Edit a status or a note on a specialty tab and it appears on
`All Claims` on the next recalculation. Do not type over columns A and B of `All Claims` — that
overwrites the link. The last column of `All Claims` names the exact cell each row is linked to.

## How the deadline is calculated

`Filing Deadline` = `Date of Service` + the carrier's timely filing limit, as a live formula.
`Days Until Deadline` = `Filing Deadline` − `TODAY()`, so the countdown stays current every time
the file is opened; red at 3 days or less, amber at 4–7, green above 7.

Each claim's `Primary Payer Name` was matched to a carrier through column F
(*Likely Payer Name(s) in AR Data*) of the reference file. `Responsible Payer` was not used for the
filter.

## Where the other claims went

| Bucket | Claim lines |
|---|---|
| On the watchlist (0–10 days) | 47 |
| Deadline more than 10 days away | 521 |
| Deadline already passed | 281 |
| No timely filing limit on file | 124 |
| **Total in source file** | **1,086** |

The 281 already past their deadline are outside what this watchlist was asked for, but they are
worth a separate appeal / write-off review.

## Assumptions

Full detail is on the `Read Me` tab. The ones that affect claim selection:

- **Humana / Humana Gold Plus HMO** carry two limits (180 days physicians, 90 days ancillary).
  The shorter 90 days is applied so nothing is missed — using 180 instead would change one claim
  on this watchlist. Confirm the provider category.
- **TRIWEST VA CCN CLAIMS** covers TriWest (120 days) and VA CCN (180 days) under one payer name.
  The shorter 120 days is applied; no claim under this payer reaches the window either way.
- **BCBS AZ** moved from 365 to 90 days on 01/01/2026. Every date of service in the source file is
  in 2026, so 90 days applies throughout.
- Limits are counted from the date of service. Secondary claims are commonly counted from the
  primary carrier's remittance date instead — not captured in the reference file, so check it per
  carrier on any row with a `Secondary Payer Name`.
