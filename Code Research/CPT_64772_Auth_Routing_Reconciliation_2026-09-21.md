# CPT 64772 — reconciliation of the auth routing workbook against the filed payer articles

**Workbook reviewed:** `Code Research/CPT_64772_Auth_Routing_2026.xlsx` (Last updated 21 Sep 2026)
**Sources reviewed:** all 23 files in `Payer's Prior Authorizations Articles/` (22 PDFs + `az-blue-prior-auth-code-lists.xlsx`)
**Date of review:** 21 September 2026

## Headline

**64772 does not appear in a single one of the 23 filed articles.** Every PA list, code list and
notification list in the folder was searched for `64772` — zero hits. The workbook's core answer,
that no reviewed payer subjects 64772 to a pre-service gate, **holds up**.

What does not hold up is the workbook's account of *why it could not answer*. The workbook's headline
open blocker — that Optum's Arizona PA code list is unretrieved — is contradicted by two documents
sitting in this folder. That blocker is load-bearing: it is the stated reason **19 of the workbook's
61 rows are `TO CONFIRM`**.

Findings are ranked by whether they change an answer a biller would act on.

---

## A. Answer-changing

### A1. 🔴 The Optum AZ PA code list is not unretrieved — it is in this folder

The workbook says, on the `How to use` tab and on 19 rows:

> Optum's Arizona PA code list is still unretrieved - optum.com and business.optum.com are blocked by
> the network egress policy (retried 21 Sep 2026). Every Optum row, and the UHC rows, are TO CONFIRM
> on 64772 specifically.

Two filed articles are exactly that list:

| File | Document number | Scope | Effective |
|---|---|---|---|
| `OptumPrior Authorization Requirements_ArizonaUHC_2026.pdf` | OHNC-1-25-00928_08262026 | OptumCare Network of AZ — **UHC Medicare Advantage** book | 1 Jan 2026, updated 1 Sep 2026 |
| `OptumPrior Authorization Requirements_ArizonaBCBS_2026.pdf` | OHNC-1-25-00929_09032026 | OptumCare Network of AZ — **BCBS** book | 1 Jan 2026, updated 1 Sep 2026 |

Both carry a **Pain Management** PA line, identical in each:

> `0627T, 0628T, 0629T, 0630T, 62350, 62351, 62360, 62361, 62362, 62264, 64490, 64491, 64492, 64493,`
> `64494, 64495, 64628, 64629, 64633, 64634, 64635, 64636, C9807, G0283, G0563`

**64772 is absent.** The facet codes are present, which confirms the section is the right place to
look and that its omission is meaningful rather than an artefact of scope.

**Effect:** 17 `TO CONFIRM` rows on the `Optum` tab and 2 on the `BCBS` tab (Blue Best Life
Classic/Plus) can move to **NO — published**, sourced to OHNC-1-25-00928 / OHNC-1-25-00929.

### A2. 🔴 Referral answer contradicted for H5253-035

OHNC-1-25-00928, p.2, lists the plans the new PCP-referral requirement **does not** apply to:

> • Institutional SNP plans
> • Erickson Advantage plans
> • Michigan Integrated DSNP plan (H2247-005)
> • **AARP Medicare Advantage from UHC AZ-0013 (H5253-035)**

The workbook carries two H5253 rows on the `Optum` tab, both answering referral = **YES**:

| Workbook row | CMS contract | PBP | Referral answer in workbook |
|---|---|---|---|
| AARP Medicare Advantage from UnitedHealthcare | H5253 | 036 | YES — no referral = claim denial |
| AARP Medicare Advantage Plus | H5253 | **035** | YES — no referral = claim denial |

The published exemption is for **H5253-035**. The workbook's plan *name* for the exemption
("AARP Medicare Advantage from UHC") sits on its PBP 036 row, while the exempt *PBP* (035) sits on
its "Plus" row. One of these two rows is wrong, and both currently tell the biller to chase a
referral that the payer has published as not required. Reconcile the name-to-PBP mapping against
the Optum guide's plan table before relying on either.

Two further referral nuances in OHNC-1-25-00928 that the workbook's blanket "YES" flattens:

- Referrals are **not** required for services provided by a podiatrist, radiologist, oncologist,
  ophthalmologist and 14 other listed specialties, nor for "provision of anesthesiology" —
  **except** that "pain management services rendered by an anesthesiologist do require a referral",
  and only for pain management *office visits*.
- Referrals are not required for services performed in an observation setting, or for orthopedic
  urgent care.

### A3. 🟠 The BCBS Optum book publishes no referral requirement at all

OHNC-1-25-00929 (the BCBS book) contains the word "referral" **once**, in the out-of-network
paragraph. It has no referral section, no exempt-plan list, no submission instructions. The referral
programme is documented only in the UHC MA book (OHNC-1-25-00928), which scopes it to
"UnitedHealthcare Medicare Advantage HMO and HMO-POS plans".

The workbook nonetheless answers referral = "YES — HMO" / "YES — the PCP submits the referral to
Optum BEFORE the specialist visit" on **BCBS Blue Best Life Classic and Plus**, on both the `BCBS`
and `Optum` tabs (4 rows). Those rows cite the administrative guide, not the BCBS PA article.
Either the guide carries the rule for the BCBS book — in which case cite it — or the answer is
unsupported.

---

## B. Citation and currency mismatches

### B1. 🟠 Humana list — wrong version, wrong effective date

| | Workbook | Filed article |
|---|---|---|
| Document number | `790807ALL0725-C GHHMQHEEN` | **`790807ALL0725-C GHHMXVMEN`** |
| Effective | **1 Jan 2026** | **Effective date: July 1, 2026 / Revision date: September 1, 2026** |

Same base document (790807ALL0725-C), different version stamp and a six-month-later effective date.
The **substance is unaffected** — the filed article's Facet injections entry is character-for-character
what the workbook quotes (`64490, 64491, 64492, 64493, 64494, 64495, 64633, 64634, 64635, 64636,`
`64999, 0213T, 0214T, 0215T, 0216T, 0217T, 0218T`), 64625 is separately listed as
"Radiofrequency Ablation for the SI Joint", and both route to Cohere at Next.Coherehealth.com. But
three Humana rows cite a superseded version, and the "1 Jan 2026" date in the workbook appears to
have been taken from an unrelated sentence in the article (the CMS 7-day decision deadline).

### B2. 🟠 Every Optum row names the wrong governing document

All 17 `Optum`-tab rows and the 2 Blue Best Life rows name:

> Governing document for 64772: OptumCare Network of Arizona Provider Administrative Guide
> (OHNC-1-25-00910_06182026) — "It contains NO procedure-code PA list."

That statement is accurate *about the administrative guide*, but the guide is not the governing
document for the PA question. OHNC-1-25-00928 / OHNC-1-25-00929 are, and they do contain the code
list. The administrative guide should stay as the source for **delegation tier, plan roster and
referral rules** (column J/K), with the PA articles cited in columns P–U.

### B3. 🟠 "Humana Commercial — not identified" — the list is in this folder

The workbook's `Humana` tab row 4 says:

> Governing document: Not identified. The list reviewed covers MA and D-SNP ONLY. Whether Humana's
> Arizona commercial book carries a different PA list has not been established.

`FINAL_July 2024 Commercial Prior Authorization and Notification Listpdf.pdf` is Humana's
**Commercial Preauthorization and Notification List**, document `399806ALL0224-A GCHM8R6EN`. Its
Facet injections entry is identical to the MA list, and **64772 is absent**.

Two caveats keep this from closing the row outright, and both should be written into it rather than
left as "not identified": the list is **effective 1 July 2024, revised 10 Dec 2024** — two years
stale — and its `ALL` document-number segment indicates national rather than Arizona-specific scope.
The correct status is "published but stale; refresh before relying on it", not "not identified".

---

## C. `TO CONFIRM` rows the filed articles can answer

Each of these is `TO CONFIRM` in the workbook while a filed article answers it.

| Workbook row(s) | Filed article | What it says | Resolves to |
|---|---|---|---|
| `UnitedHealthcare` rows 2–9 (MA, not delegated) | `UnitedHealthcare Medicare Advantage Prior Authorization Requirements - Effective Sept. 1, 2026` (PCA-4-26-00416-Clinical-QRG_03022026) | Pain management PA required for **62350, 62351, 62360, 62361, 62362 only** (plan exclusion: Erickson Advantage). 64772 absent — and so are the facet codes | **NO** |
| `UnitedHealthcare` row 14 (Surest) | `Prior authorization requirements for Surest health plans - Effective Sept. 1, 2026` | Pain management PA for `62320, 62322, 62324, 62325, 62326, 62327, 62350, 62351, 62360, 62361, 64451, 64484, 64520, `**`64620`**`, `**`64640`**`, E0782, E0783, E0785, E0786`. 64772 absent | **NO** (Surest only; the row also covers UMR, Level Funded, Golden Rule etc., which remain open) |
| `UnitedHealthcare` row 13 (Community Plan ACC/DD/ALTCS) | ACC Medicaid, Developmentally Disabled, and Long Term Care articles, all eff. 1 Sep 2026 | No pain-management section. Nervous system PA = `64561, 64640`; Spinal surgery PA = the 22xxx/63xxx series. 64772 absent from all three | **NO** |
| `Optum` rows 17–21 (SCAN) | `SCAN Medicare Advantage Prior Authorization Requirements` | Nervous System Surgery: Spine & Spinal Cord = `62350…63102, 63170, 63172, 63173, 63185, 63190, 63191, 63197, 63200, 63650, 63655, 63685, 63688*, 64466, 64467, 64468, 64469, 64473, 64474, 64568, 64590, `**`64722`**`, `**`64744`**. 64772 absent | **NO**, second independent source |

Worth noting for the denial playbook: **Surest is the only payer in the folder that requires PA for
64620 and 64640**, and **SCAN is the only one that lists 64722 and 64744** — the transection/avulsion
and neurolytic-destruction codes immediately adjacent to 64772. Both stop short of 64772. That is the
strongest available evidence that its omission is deliberate rather than an oversight, and it is
exactly the argument to make on a post-payment review.

⚠️ `SCAN Village Health Prior Authorization Requirements.pdf` is scoped to
"members enrolled with VillageHealth (HMO-POS) Plan **in California**". The workbook's note that SCAN
appears in the practice AR as "SCAN Health Plan (Village Health Plan)" should not be read as making
this the Arizona source.

---

## D. Substantive contradictions in the workbook's analysis

### D1. 🔴 64772 *is* in the AZ Blue source file — on its history and UM tabs

The workbook states, for AZ Blue Commercial and MA: "Is 64772 in it? **NO — absent (1,909 rows)**".
That is correct for the 2026 requirement lists, and the row count matches exactly. 64772 is absent
from all seven current lists:

| Tab | Rows | 64772 |
|---|---|---|
| 2026 STANDARD Code List | 1,909 | absent |
| 2026 State of AZ Grp List | 1,973 | absent |
| 2026 Teamsters Group List | 730 | absent |
| Snell & Wilmer Group List | 685 | absent |
| 2026 FEP List | 2,219 | absent |
| 2026 Medicare Advantage List | 2,117 | absent |
| FEPBluefocusList | 1,849 | absent |

**But the same file carries 64772 on five other tabs, and the workbook cites none of them:**

- **`M300`** — `64772 | TRANSECTION/AVULSION OF OTHER SPINAL NERVE, EXTRADURAL | Ambulatory Surgery`
  with `2019 Precert List = OFF`, **`2020 Precert List = ON`**, **`Medicare = ON`**,
  **`ACA, IU65 Suite A, C and E = ON`**, **`Med3000 PCP Coordinated Care HMO = ON`**
  (ADOA, City of Phoenix PPO/HMO, Snell & Wilmer, Teamsters all OFF).
- **`CommercialMR`** — `64772 | ON` (commercial medical-review flag).
- **`Denied2019`** — `64772 | 20` denied claims.
- **`UMList`**, **`ClaimsDetail2`** — further entries.

These are historical and working tabs, not the 2026 requirement lists, so they **do not** change the
answer: 64772 does not require prior auth at AZ Blue today. They matter for a different reason. The
workbook's central warning is that a green "NO" only means there is no pre-service gate and that "the
risk moves to post-payment review, where there is no published standard to appeal against." Here is
the payer's own file showing 64772 carrying a precert flag as recently as the 2020 list, an `ON`
commercial medical-review flag, and a denial history. That is the best evidence in the repo for the
workbook's own thesis, and it is uncited.

### D2. 🟠 "No EviCore pathway exists on commercial" is too broad

Workbook, AZ Blue Commercial (Standard) row:

> eviCore's MSK / interventional pain programme is Medicare Advantage only, so no eviCore pathway
> exists on commercial either.

The AZ Blue `Introduction` tab says the opposite about the programme's scope:

> Three of the lists on the following tabs (**Standard, State of Arizona Group**, and AZ Blue-Administered
> Medicare Advantage) include the codes in our EviCore prior authorization program. However, some
> employer groups using the standard prior authorization requirements are not delegated for the
> EviCore program.

The Standard list's PA Administrator column carries `EviCore for delegated members only` across a
large share of its 1,909 rows, and the State of Arizona Group list is flagged "Group is delegated for
EviCore" in its header.

What is true is narrower and per-code: on the **commercial Standard and State of AZ lists the facet
codes 64633–64636 route to `AZ Blue`**, not EviCore; on the **MA list 64625 and 64633–64636 route to
`EviCore`**. So the workbook's MA row ("Facet codes carry an eviCore precert requirement") is right,
and the conclusion for 64772 is unchanged either way — but the commercial row's reasoning should be
restated as "the interventional pain codes on the commercial lists are administered by AZ Blue, not
EviCore", not as "no EviCore pathway exists on commercial".

### D3. 🔴 AZ Blue's 1 July 2026 non-reimbursement rule is nowhere in the workbook

AZ Blue `Introduction` tab:

> Note: For dates of service on and after **July 1, 2026**, when a required prior auth is not
> obtained, the claim (or claim line) for that service **will not be reimbursed**. AZ Blue network
> providers **may not bill the member** for the service. Lack of inpatient notification will still
> result in a financial penalty.

This is the consequence clause for every AZ Blue row in the book, and it is the single most important
sentence in the source for a routing sheet whose whole purpose is not misrouting a member. It belongs
on the `How to use` tab alongside the existing routing traps, and it sharpens the M2K trap in
particular: route an M2K member to AZ Blue when the card says AZPC, and the AZPC auth is never filed,
and the claim is both unpayable and unbillable.

---

## E. Gaps in coverage

### E1. 🟠 Three published AZ Blue commercial lists have no rows, and the catch-all absorbs them

`az-blue-prior-auth-code-lists.xlsx` publishes four distinct commercial requirement lists. The
workbook has a row for one:

| Published list | Prefixes / group | In workbook? |
|---|---|---|
| Standard | 61 prefixes (B4H, B4R, CDC … Z9P) | yes, as "(none of the below)" |
| State of Arizona Group | **SYD, S3Z** (group 030855), delegated for EviCore | **no row** |
| Teamsters Group | **TYW** (groups 031843, 031844) | **no row** |
| Snell & Wilmer Group | **SWB, SNK** (group 030313) | **no row** |

64772 is absent from all four, so no answer changes. But the workbook's own note warns that
"(none of the below)" is "a catch-all that defaults to 'no auth'. Any prefix not yet catalogued lands
there silently" — and three catalogued, published, separately-administered groups are currently
landing there. Each also has its own PA administrator column and its own Gold Card rules.

Also note **the Snell & Wilmer list is dated 3/01/2024**, while the other three are 09/01/2026. It is
two years stale in the payer's own current file.

### E2. 🟠 The AZ Blue source contradicts itself on prefix IVR

- `Introduction`, exceptions: "Prefixes **AOZ, AZI, AZK, and IVR** (Strategic Hub plans): A Blue Plan
  partner (BCBS South Carolina) handles utilization management for these plans (800-868-1032)."
- `2026 STANDARD Code List`, row 2: "APPLICABLE MEMBER ID PREFIXES: B4H, B4R, CDC, CGF, COV, CTZ,
  EBB, EJX, EJY, FPZ, FZI, GLK, HMO, ISD, **IVR**, KIP, …"

IVR is listed both as a Strategic Hub exception routed to BCBS South Carolina **and** as a prefix the
Standard list applies to. The same overlap exists for SYD and S3Z (Standard *and* State of Arizona
Group) and SWB and SNK (Standard *and* Snell & Wilmer). This is a defect in the payer's document, not
the workbook — but it is precisely the kind of thing the workbook's "Routing traps" section exists to
capture, and an IVR member can currently be routed two ways with no flag.

### E3. 🟡 Published identifiers the workbook's own column convention calls for

The workbook's stated convention is that alpha prefix, payer ID, CMS contract, PBP and group number
"each gets its own column and is never mixed into a single field." Several are published in the filed
articles and left blank:

**`2026-az-blue-tpa-jointly-administered-plans.pdf` (as of 07/2026)** — the workbook's two Jointly
Administered rows have **empty Payer ID (F) and Group number (I)** columns. The article publishes:

- **Claim submission: AZ Blue, EDI #53589** → column F for both rows.
- Group numbers per prefix: JAR #102441, JAZ #102623, JCG #102466, JGF #102556, JKS #102621,
  JPZ #102465, K8Y/K8Z #039176, MKQ #045928, NBT #037461, PTP #044410 → column I.
- **Seven different AmeriBen prior-auth phone numbers**, which the workbook collapses into
  "AmeriBen, per the group's SPD":

  | Prefix | Group | Prior auth | Medical policies |
  |---|---|---|---|
  | JCG | Cochise Combined Trust #102466 | 855-240-3698 | 855-258-6455 |
  | JKS | Kyrene Elementary #102621 | 855-961-5401 | 855-961-5408 |
  | JPZ | Arizona Metropolitan Trust #102465 | 855-778-9053 | 855-350-8699 |
  | K8Y, K8Z | Amkor Technology #039176 | 800-388-3193 | 866-879-6128 |
  | MKQ | Microchip Technologies #045928 | 866-947-9522 | 833-206-0582 |
  | PTP | Pioneer Holding #044410 | 833-359-2505 | 833-359-2284 |
  | JAR, JAZ, JGF, JSW, NBT | (AHG groups) | 800-847-7605 | 800-847-7605 |

  For a workbook whose stated purpose is "where do I go to check and where do I submit", six of the
  seven AmeriBen numbers are missing and are published.

**Health Choice rows** (IAZ, HCI, MZH — 3 rows): the AZ Blue `Introduction` publishes
**800-322-8670** for the Health Choice UM team. The workbook's "Where to SUBMIT" says only
"Health Choice portal".

### E4. 🟡 AZ Blue runs a Gold Card programme; the workbook only tracks Humana's

The workbook has a dedicated Humana row for "Gold Card and 90-day continuity of care", noting it is
"worth resolving once — it applies across the whole Humana book". AZ Blue runs its own: every one of
the Standard, State of AZ, Teamsters, Snell & Wilmer, FEP and MA lists carries an
**`Eligible for Gold Card Program`** column. For the facet codes it is populated —
64635/64636 = `Yes`, 64633/64634 = `Code included in Gold Card Program? Yes, if being perfor…`.
The same "resolve it once for the whole book" logic applies, and there is no AZ Blue equivalent row.

### E5. 🟡 The workbook's prefix mapping is stronger than its own Status column admits

Four BCBS rows are marked `To confirm` / `Practice-supplied` when the AZ Blue `Introduction` tab
publishes the answer verbatim:

- **Strategic Hub** — workbook note: "Four prefixes grouped on the assumption they behave alike -
  confirm each." Published: "Prefixes AOZ, AZI, AZK, and IVR (Strategic Hub plans): A Blue Plan
  partner (BCBS South Carolina) handles utilization management for these plans (800-868-1032)."
  AZ Blue itself groups all four under one administrator and one number — the assumption is the
  payer's, not the practice's.
- **M2K three-way trap** — published verbatim: "Utilization management may be handled by AZ Blue,
  Optum Health Network Arizona (OHNAZ), or Arizona Priority Care (AZPC). Check ID card." The workbook
  labels this "Practice-supplied"; it is published, which makes it stronger, not weaker.
- **Jointly Administered / CHS** — both published, prefix-for-prefix and word-for-word.

Every one of these should move from `Practice-supplied` to `Published`, cited to
`az-blue-prior-auth-code-lists.xlsx` → `Introduction`.

---

## F. Internal consistency and housekeeping

### F1. 🟠 Five rows are colour-coded green on a source the workbook calls unretrieved

The `How to use` colour key states: "GREEN = no auth required. YELLOW = to confirm, meaning no
published source has been located." `Optum` rows 17–21 (SCAN Balance, Classic, MyChoice, Strive,
LACERA) are filled **green** with `PA required for 64772? = NO`, while carrying
`Status = To confirm` and `Where to CHECK = Optum's AZ PA code list - STILL UNRETRIEVED`.

A green cell on an admittedly unretrieved source is the exact failure the workbook's own
"Read this before trusting a green cell" warning is about. The answer turns out to be defensible
(§A1 and §C both support NO), but it was green before it was sourced. Either the fill or the status
needs to move, and after §A1 the right move is to make the status `Published`.

### F2. 🟡 `Code Research/README.md` names a file that does not exist

The README's table lists **`CPT_64772_Auth_Routing_2026-09-21.xlsx`**; the file on disk is
**`CPT_64772_Auth_Routing_2026.xlsx`**. The README's own convention line dates the workbook to
21 Sep 2026, so the filename is probably what should change, not the README.

### F3. 🟡 `Payer's Prior Authorizations Articles/README.md` says the folder is empty

> Empty for now; this README holds the folder in git until the first article is added.

and its index table reads `_(none yet)_`. The folder holds 23 files. The README also sets a naming
convention — `<Payer>_<Topic>_<YYYY-MM-DD>.<ext>`, dated to publication or effective date — that
none of the 23 files follow. Several carry an effective date only in prose (`FINAL_July 2024…`,
`…- Effective Sept. 1, 2026`), and two carry a bare year (`OptumPrior Authorization
Requirements_ArizonaBCBS_2026.pdf`) despite the documents themselves being stamped
OHNC-1-25-00929_09032026.

### F4. 🟡 The folder mixes markets; the workbook is Arizona-scoped

Six filed articles are for non-Arizona books: Oxford Health Plans (NY/NJ/CT), Neighborhood Health
Partnership (FL), UnitedHealthcare Mid-Atlantic (MD/DC/VA), UnitedHealthcare Community Plan Florida,
UnitedHealthcare West, and SCAN VillageHealth (CA). None is wrong to keep — the workbook's BlueCard
row turns on out-of-area home-plan rules — but the README index should mark market, so an Arizona
question is not answered from a Florida list. 64772 is absent from all six, so nothing is currently
mis-answered.

---

## Summary of what to change

| # | Row(s) affected | Change | Severity |
|---|---|---|---|
| A1 | 19 `TO CONFIRM` rows (Optum ×17, BCBS ×2) | → **NO — Published**, cite OHNC-1-25-00928 / -00929 | 🔴 |
| A2 | Optum H5253-035 / H5253-036 | Reconcile name-to-PBP; one row's referral = YES is contradicted | 🔴 |
| A3 | Blue Best Life Classic/Plus (4 rows, 2 tabs) | Referral = YES is unsupported by the BCBS PA article | 🟠 |
| B1 | Humana ×3 | Update to `GHHMXVMEN`, eff. 1 Jul 2026 / rev. 1 Sep 2026 | 🟠 |
| B2 | Optum ×19 | Move PA citation from the admin guide to the PA articles | 🟠 |
| B3 | Humana Commercial | "Not identified" → 399806ALL0224-A, flagged stale (Jul 2024) | 🟠 |
| C | UHC ×8, Surest, Community Plan, SCAN ×5 | → **NO**, cite the filed articles | 🟠 |
| D1 | AZ Blue Commercial + MA | Cite `M300` / `CommercialMR` / `Denied2019` as post-payment evidence | 🔴 |
| D2 | AZ Blue Commercial | Narrow the EviCore claim to the facet codes | 🟠 |
| D3 | `How to use` + all AZ Blue rows | Add the 1 Jul 2026 no-pay / no-balance-bill rule | 🔴 |
| E1 | new rows ×3 | State of AZ Group (SYD, S3Z), Teamsters (TYW), Snell & Wilmer (SWB, SNK) | 🟠 |
| E2 | `How to use` routing traps | Flag the IVR / SYD / S3Z / SWB / SNK prefix overlap | 🟠 |
| E3 | Jointly Administered ×2, Health Choice ×3 | Fill payer ID 53589, group numbers, 6 AmeriBen numbers, 800-322-8670 | 🟡 |
| E4 | new row | AZ Blue Gold Card programme | 🟡 |
| E5 | BCBS ×4 | `Practice-supplied` → `Published` | 🟡 |
| F1 | Optum rows 17–21 | Green fill vs `To confirm` status — resolve to Published | 🟠 |
| F2–F4 | READMEs | Filename, empty-folder text, market column | 🟡 |

**What does not change:** the answer for 64772 itself. No filed article requires prior authorization
for it, and the two payers that come closest — Surest (64620, 64640) and SCAN (64722, 64744) — list
its immediate neighbours and stop short of it. The workbook's conclusion stands; its sourcing,
currency and referral answers are what need the work.
