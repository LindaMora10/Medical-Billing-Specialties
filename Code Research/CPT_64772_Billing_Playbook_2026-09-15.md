# CPT 64772 — Billing Department Playbook

**Code:** 64772 — *Transection or avulsion of other spinal nerve, extradural*
**Provider:** Timothy A. Luke, M.D. · NPI **1437125846** · Orthopaedic Surgery (`207X00000X`) · AZ lic. 41183
**Sites:** Phoenix (8805 N 23rd Ave Ste 120) · Mesa (4860 E Baseline Rd Ste 103)
**Prepared:** 15 September 2026 · **Jurisdiction:** Arizona — Medicare Part B = **Noridian JF**

**Operating assumption: Dr. Luke is performing and billing 64772.** This document tells you how to get it
paid. Supporting research, policy citations and effective dates are in the companion
**[CPT 64772 Payer Research memo](CPT_64772_Payer_Research_2026-09-15.md)**.

---

## 1. The one thing that determines everything

**No payer reviewed publishes medical-necessity criteria for 64772.** Not Noridian, not AZ Blue, not
Humana, not UnitedHealthcare. The only governing policy is **NCD 160.1 "Induced Lesions of Nerve Tracts,"**
which covers "surgical cutting of the nerve (rhizolysis)" and then defers to the MAC's medical staff in
"selected cases."

**Consequence: there is no criteria checklist to satisfy and no covered-diagnosis list to match. Every
claim is decided on the operative report.** So the operative report *is* the billing strategy. Sections 2
and 3 exist to make that report unambiguous, and §4 onward keeps the claim mechanically clean so the
report is the only thing left to argue about.

**Practical rule: attach the operative report to the first claim for every payer, unprompted.** Do not
wait for a records request. A records request adds 30–60 days and starts the clock on an appeal you can
avoid entirely.

---

## 2. Operative-note requirements — the six elements

Have Dr. Luke's dictation template carry all six. If any one is missing, the claim reads as a
percutaneous facet procedure miscoded as an open one, which is the single most likely trigger for
recoupment.

| # | Element | Why it matters | Failure mode if missing |
|---|---|---|---|
| 1 | **Open approach** — incision, sequential dissection, exposure, layered closure | 64772 is in CPT's *Transection or Avulsion* subsection. It has no imaging-guidance or needle language. | A note describing needle/electrode placement under fluoroscopy reads as 64633–64636. Recoupment plus a coding-pattern review. |
| 2 | **The nerve named specifically, with level and side** | 64772 is the residual code — "*other* spinal nerve," i.e. one no specific code names. | "Medial branch" or "facet nerve" in the note defeats the code outright: those nerves are named by 64633–64636. |
| 3 | **Affirmative statement that the nerve is not a paravertebral facet / medial branch nerve** | Pre-empts the reviewer's first question. | Reviewer assumes facet; denial as incorrect coding. |
| 4 | **Extradural location** of the division | It is in the descriptor. | Reviewer cannot confirm the code's core anatomic condition. |
| 5 | **Mechanism — sharp or mechanical transection/avulsion, explicitly not thermal, chemical, electrical or radiofrequency** | Neurolytic destruction is a different code family. | Thermal/RF language moves the claim to 64633–64636 or 64999. |
| 6 | **Indication** — the named nerve as pain generator, conservative care tried and failed, and the diagnostic workup that localised pain to that nerve | Substitutes for the absent published criteria. This is what the medical reviewer reads. | Denial for medical necessity with nothing to appeal on. |

Plus, from Noridian LCA A58403's documentation section (the closest published standard in JF): the
performing provider's assessment tied to the complaint, relevant history, results of pertinent
tests/procedures, and a **signed and dated operative report**.

> **If the note describes a percutaneous, image-guided thermal lesion of the medial branches, 64772 will
> not survive review** — not because of a payer rule, but because the descriptor does not cover it. That
> is a documentation-alignment issue to settle with Dr. Luke before the first case, not a billing fix.

---

## 3. Diagnosis coding — the facet codes do not carry over

**The dx must identify the nerve and the underlying condition.** A facet-arthropathy diagnosis on a 64772
line is self-contradicting: it describes the exact pathology 64633–64636 exist to treat.

### 3.1 Do not use on a 64772 claim

| Code | Problem |
|---|---|
| 🔴 **`M54.5`** | **Not a billable code at all.** FY2026 category header ("Low back pain"), invalid for HIPAA transactions. Will reject on any claim, any code. Billable children: `M54.50`, `M54.51`, `M54.59`. |
| 🔴 `M54.6` | Valid, but describes axial thoracic spine pain. **Not on Noridian's covered-dx list for facet interventions either.** |
| 🔴 `M47.81x`, `M47.89x`, `M48.1x` | Spondylosis / ankylosing hyperostosis — facet pathology. Contradicts an "other spinal nerve" transection. |
| ⚠️ `M47.81`, `G58`, `M47.9` etc. | Four- and three-character **headers are not billable**. Always code to full specificity. |

### 3.2 Use instead — nerve-specific families

| Code | Description | Notes |
|---|---|---|
| `G58.0` | Intercostal neuropathy | Billable. Fits intercostal neurectomy. |
| `G58.7` | Mononeuritis multiplex | Billable. |
| `G58.8` | **Other specified mononeuropathies** | Billable. The workhorse for a named nerve with no dedicated code, and for post-surgical neuroma. |
| `G58.9` | Mononeuropathy, unspecified | Billable but non-specific — weak on review. Prefer `G58.8`. |
| `G57.x` | Lower-limb mononeuropathies (sciatic, meralgia paraesthetica, tarsal tunnel, etc.) | **Requires laterality in the code.** Code to the 5th/6th character. |
| `M79.2` | Neuralgia and neuritis, unspecified | Non-specific; acceptable as secondary, weak as primary. |
| `S*4*` series | Injury of nerve, plus the appropriate 7th character | Where there is a traumatic or surgical cause. |

**Sequencing:** the nerve-specific code first, the underlying cause/history second. Add a post-surgical or
injury code where one applies — it supplies the "why this nerve" the reviewer is looking for.

### 3.3 Diagnosis-to-CPT edits

**There are none published for 64772**, because no LCD, LCA or NCD carries a diagnosis table for it.
That cuts both ways: no edit to fail, and no published list to cite on appeal. Reinforces §1 — the
operative report is the whole defence.

---

## 4. Clean claim construction

### 4.1 Professional claim (CMS-1500)

| Field | Entry | Note |
|---|---|---|
| **CPT** | `64772` | |
| **Place of service** | **`24`** (ASC) or **`19` / `22`** (HOPD) | 🔴 **Never `11`.** See §5. |
| **Units** | 1 per nerve transected | MUE **6**, MAI **3** — see §4.3 |
| **Laterality** | `LT` / `RT` per line | See §4.2 before using `50` |
| **Dx pointer** | Nerve-specific code per §3.2 | |
| **Rendering provider** | NPI 1437125846 | |
| **Attachment** | **Operative report** | Every payer, first claim, unprompted |

### 4.2 Modifier 50 vs LT/RT — read this before billing a bilateral case

**64772's MPFS bilateral surgery indicator is `0`.** Per CMS, indicator `0` means the 150% bilateral
payment adjustment **does not apply**, and if the procedure is reported **with modifier 50, or with RT and
LT**, payment is based on the lower of (a) the total actual charge for both sides or (b) **100% of the fee
schedule amount for a single code**.

**Operational meaning: bilateral 64772 pays the same as unilateral on Medicare — about $503 professional.
Both routes cap at 100%.**

- **This is a fee-schedule indicator, not an edit.** Appealing it is not productive. Do not let anyone
  spend AR time fighting it.
- 🔴 **If the pro-forma or volume model assumes 150% for bilateral cases, it is overstated.** Flag to
  whoever built it.
- **Contrast:** 64633, 64635, 64625, 64490 and 64493 all carry indicator `1` — 150% applies and modifier
  50 is worth real money. **64772 is the outlier.** Do not carry the facet habit over.
- **Commercial payers are not bound to the MPFS indicator.** None publishes a bilateral rule for 64772.
  Get each payer's position in writing before booking bilateral cases — this is a place where a commercial
  payer may pay 150% where Medicare will not.

**Recommendation:** report `LT` and `RT` on separate lines rather than modifier `50`. It documents the
anatomy accurately, it survives commercial payers that price laterality separately, and on Medicare it
lands in the same place as modifier 50 anyway.

### 4.3 Units and multiple nerves

- **MUE 6, MAI 3** (*Practitioner Services MUE Table, NCCI v32.3, eff. 1 Oct 2026*). **MAI 3** means a
  per-date-of-service **clinical** edit: up to 6 units adjudicate normally, and **above 6 is appealable
  with documentation** — unlike an MAI 2 edit, which is absolute.
- The MUE was **raised from 2 to 6 in January 2026** — recent enough that stale payer edit tables may
  still deny at 2. If you see a unit denial at 2, cite the current MUE table.
- 🔴 **Contrast with the facet codes: 64633 and 64635 are MUE 1 with MAI `2` — absolute.** Bilateral
  single-level facet RFA is **one unit with modifier 50, never two lines.** A second unit denies
  permanently, with no modifier and no appeal. Do not let the 64772 unit logic bleed into facet billing.
- ⚠️ **Unresolved:** where multiple *distinct* nerves are transected, it is not published whether Noridian
  treats additional lines as separate units (MUE 6 implies up to six) or applies the bilateral `0` cap
  across them. **Confirm with Noridian before billing a multi-nerve case**, and document each nerve
  separately in the op note regardless. Listed as an open call in §9.

### 4.4 Global period modifiers — 64772 carries a 90-day global

`GLOB DAYS 090` (pre-op 0.11, intra-op 0.76, post-op 0.13). The 90-day global bundles the pre-op visit
on the day of or day before surgery, all normal intra-operative services, **all typical post-operative
care for 90 days** (follow-ups, dressing changes, suture removal, surgeon's post-op pain management,
related E/M), and complications not requiring a return to the OR.

| Situation inside the 90 days | Modifier | Watch out |
|---|---|---|
| **Facet RFA (64633–64636) — unrelated to the 64772** | **`79`** | 🔴 **The big one. See §4.5.** |
| Staged or related subsequent procedure | `58` | |
| Return to the OR for a complication | `78` | |
| Unrelated E/M visit | `24` | Pair with a dx that shows it is unrelated |
| E/M that led to the decision to operate | **`57`** | **Not `25`.** 64772 is major surgery (90-day global); `25` is for 0/10-day globals. |
| Post-op care transferred to another provider | `54` / `55` / `56` | Split-care billing |

### 4.5 🔴 The 90-day global vs the RFA schedule — build this into scheduling now

Dr. Luke's facet population is exactly the group most likely to need an RFA inside 90 days of a 64772.
**Every 64772 patient becomes a modifier-79 case for any subsequent RFA in that window.** Miss the `79`
and the RFA denies as included in the global (expect a bundling/global denial, not a medical-necessity
one — recoverable on appeal with the modifier, but it costs a cycle).

This problem **does not exist today**: 64633 and 64635 carry only a **010** global, and the add-ons are
`ZZZ`. Adopting 64772 introduces a 90-day encumbrance the current code set does not have.

**Action for Deanna and Bri:** add a 90-day flag to the scheduling record on every 64772, visible to
whoever books the RFA, and a pre-billing check that `79` is appended.

### 4.6 🔴 Never bill same day as 64772 — hard NCCI bundles

64772 appears as **Column 1 in 346 practitioner PTP edits and Column 2 in zero** — it is never the
bundled code. All of the below carry **modifier indicator `0`: no modifier breaks them.** Submitting these
together does not produce a fixable denial; the Column 2 code is simply lost.

| Bundled into 64772 (will deny) | Codes | Effective |
|---|---|---|
| **Paravertebral facet joint blocks** | `64490` `64491` `64492` `64493` `64494` `64495` | 2010-01-01 / 2017-04-01 |
| **Epidural steroid injections** | `62320` `62321` `62322` `62323` `62324` `62325` `62326` `62327` | 2017-01-01 |
| **Transforaminal ESI** | `64479` `64480` `64483` `64484` | 2005-10-01 / 2017-04-01 |

**Operational consequence: you cannot bill a same-day diagnostic medial branch block or any epidural
steroid injection with 64772 on any NCCI payer.** That forecloses the common "diagnostic block plus
definitive procedure in one visit" pattern. If a block is clinically needed, it must be a **separate
encounter on a separate date**, billed on its own claim.

**What is *not* bundled:** there is **no PTP edit in either direction** between 64772 and `64633`,
`64634`, `64635`, `64636` or `64625`. Same-session billing is therefore mechanically permitted — but see
§4.7.

### 4.7 Same session as facet RFA — permitted, but think first

No NCCI bundle exists, and no modifier is needed to break an edit that is not there. Three real
constraints remain:

1. **Multiple-procedure reduction applies.** 64772 and 64633/64635 all carry `MULT PROC 2` → standard
   100% / 50% surgical reduction. Medicare applies it automatically from the indicator; append `51` only
   where a commercial payer requires it.
2. **Audit exposure.** An open nerve transection and a percutaneous facet RFA in one session invites a
   records request, because the natural reading is that one of the two is miscoded. **The audit risk
   exceeds the payment at stake on the second code.**
3. **The 90-day global then captures everything downstream** (§4.5).

### 4.8 Assistant surgeon and co-surgeon — 64772 is *more* permissive than the facet codes

| | **64772** | 64633 / 64634 / 64635 / 64636 / 64625 |
|---|---|---|
| **Assistant at surgery** | **Indicator `2` — payable, no supporting documentation required.** Modifiers `80`, `81`, `82`; **`AS`** for PA/NP/CNS (Medicare requires `AS`, and pays 85% of the 16% assistant allowance) | **Indicator `1` — statutory restriction, an assistant may NOT be paid** |
| **Co-surgeon** | **Indicator `1` — payable with supporting documentation** establishing medical necessity of two surgeons. Modifier **`62`**; each surgeon bills the same code with `62` and each is paid 62.5% | **Indicator `0` — co-surgeons NOT permitted** |
| **Team surgery** | `0` — not permitted | `0` — not permitted |

⚠️ No commercial payer reviewed publishes an assistant- or co-surgeon rule specific to 64772. Most follow
the MPFS indicators; confirm before scheduling a two-surgeon case.

---

## 5. Place of service — facility only

🔴 **64772 has no Medicare office payment.** The non-facility PE RVU carries the **`NA` indicator** in the
PFS Relative Value File — CMS publishes no non-facility rate. A POS `11` claim cannot be paid.

| Setting | POS | Payable? | Facility side |
|---|---|---|---|
| **Office** | `11` | 🔴 **No — not payable on Medicare** | — |
| **ASC** | `24` | ✅ Yes | **ASC Addendum AA**, indicator **`A2`**, weight 16.8435, **$948.66**, subject to multiple-procedure discounting |
| **HOPD** | `19` / `22` | ✅ Yes | **APC 5431**, OPPS **$1,765.76** |

**Scheduling notes:**

- ✅ **64772 can be booked at the ASC.** It is on the ASC covered-procedures list and separately payable —
  scheduling does **not** have to send these out.
- **The HOPD pays ~86% more on the facility side** ($1,765.76 vs $948.66). A site-of-service economics
  decision, not a coverage one.
- **ASC facility billing:** LCA A58403 instructs that for ASC-performed facet procedures the *physician*
  uses modifier `50` while the *ASC facility* reports the code on **two lines, one unit each, with `RT`
  and `LT`**. ⚠️ That instruction is written for 64490–64495 and there is **no published equivalent for
  64772** — confirm with Noridian before the ASC bills its first bilateral case (§9).
- ⚠️ **Commercial site-of-service review is a separate gate.** UHC **MP.12.22** (eff. 1 Jul 2026) does not
  list 64772 — but it *does* list 64633 and 64635, and it expressly excludes **"surgeon-preferred or
  proprietary instruments, instrument sets, and hardware sets"** as grounds for ASC over office. **If new
  equipment is the argument for the ASC, UHC has pre-emptively rejected it.**
- **AHCCCS is the exception:** it publishes a **non-facility** rate for 64772 ($578.79), so the office is
  theoretically payable there — but coverage still has to be established per the AMPM, and contractor
  plans apply their own PA.

---

## 6. Expected reimbursement — Arizona

**Professional (Medicare Part B, Arizona locality 03102/00, GPCIs: work 1.000 · PE 0.969 · MP 0.856):**

| Code | Setting | Adj. RVU | 2026 non-QPP (CF 33.4009) | 2026 QPP (CF 33.5675) |
|---|---|---|---|---|
| **64772** | **Facility** | **15.056** | **$502.88** | **$505.39** |
| **64772** | Non-facility | — | 🔴 **not payable** | — |
| 64633 | Non-facility | 13.381 | $446.92 | $449.15 |
| 64633 | Facility | 5.076 | $169.55 | $170.40 |
| 64635 | Non-facility | 13.556 | $452.79 | $455.05 |
| 64635 | Facility | 5.087 | $169.91 | $170.76 |
| 64625 | Non-facility | 14.445 | $482.49 | $484.89 |
| 64490 | Non-facility | 5.985 | $199.92 | $200.91 |
| 64493 | Non-facility | 5.553 | $185.49 | $186.41 |

*Computed from `PPRRVU2026_Oct_nonQPP` / `_QPP` and `GPCI2026` (RVU26D, eff. 1 Oct 2026). Rounded to the
cent; actual allowables may differ by a cent from CMS rounding order. 2026 has two conversion factors —
which applies depends on qualifying-APM status.*

**Facility side (Medicare):** ASC $948.66 · HOPD $1,765.76 (APC 5431).
**AHCCCS:** 64772 = **$578.79** facility and non-facility; lower tier $405.15 (FY26 Final PFS, rates eff.
1 Oct 2025).

**Total Medicare episode, ASC:** ≈ $502.88 professional + $948.66 facility ≈ **$1,451.54**.
**Total Medicare episode, HOPD:** ≈ $502.88 + $1,765.76 ≈ **$2,268.64**.

**Commercial:** no published rates; contract-dependent. Note the professional fee is **facility-only**, so
any commercial model built on office-based RVUs for this code is wrong.

---

## 7. Pre-service actions by payer

| Payer / plan | PA required for 64772? | What to do before the case |
|---|---|---|
| **Traditional Medicare — Noridian JF** | ✅ **No.** No LCD/LCA addresses it; NCD 160.1 governs; **WISeR does not reach it** (Appendix A Table A2 = 64605/64610 only) | Run 64772 through the [Noridian PA Lookup Tool](https://med.noridianmedicare.com/web/jfb/cert-reviews/pre-claim) and **save a dated screenshot** as your no-PA evidence. Attach op report to the claim. |
| **AZ Blue — Commercial** | ⚠️ **Unverified.** eviCore precert is `N` for the facet codes and **64772 is not on the eviCore list at all**; eviCore's MSK/pain program is **Medicare Advantage only** | 🔴 **Call.** "No eviCore precert" ≠ "no AZ Blue precert." Run the [PA lookup](https://www.azblue.com/prior-authorization-lookup/providers) and request the medical policy in writing. `UtilMgmt@azblue.com` · 602-864-4320 · 1-800-322-8670 |
| **AZ Blue — Medicare Advantage** | ⚠️ **Unverified.** Facet codes = eviCore precert `Y`; 64772 not on the list → routes to **AZ Blue internal UM**, not eviCore | Same call. Also ask which entity adjudicates a code absent from the eviCore list. Some MA members route through **OHNAZ** or **Arizona Priority Care** — confirm per member. |
| **Humana — MA & DSNP** | ✅ **No** — 64772 is absent from the PA and Notification List eff. 1 Jan 2026 (facet codes 64490–64495 / 64633–64636 / 64999 and 64625 *do* require PA) | No PA submission. Verify per member, and ask whether Dr. Luke qualifies for the 2026 **Gold Card**. Cohere Health **833-283-0033** for anything that does need PA. |
| **UnitedHealthcare — Commercial / Individual Exchange** | ⚠️ 64772 unlisted in every applicable policy | Verify at UHCprovider.com/priorauth. Note 2026T0107II calls **endoscopic rhizotomy** and **SI joint ablation** *unproven* — if the technique is endoscopic, expect a written denial. |
| **UHC — Medicare Advantage (AZ)** | ⚠️ Unlisted in MMP070.12; policy **defers to LCD/LCA**, so NCD 160.1 governs | 🔴 **Check the member ID card for payer ID `LIFE1`** = delegated to **Optum Health Networks**. **HMO / HMO-POS members need a PCP referral submitted to Optum before the specialist visit** or the claim denies. 22 group numbers affected — list in the research memo §2.4. |
| **Optum (delegated)** | ⚠️ **No verified answer** — domains blocked, see §9 | 🔴 **Call.** Optum Pro portal `optumproportal.com` · **877-370-2845** · `lcd_um@optum.com`. Per UHC's own guidance, **"you must follow the delegate's protocols"** — ask each delegated IPA separately. |
| **AHCCCS / Health Choice** | ⚠️ On the fee schedule at $578.79; coverage per AMPM, not the fee schedule | Confirm AMPM coverage and the contractor plan's PA. `FFSRates@azahcccs.gov` |

---

## 8. Denial playbook

The denial reasons below are **anticipated from the edit mechanics verified in the research memo**, not
quoted from payer-published denial matrices. Use them to pre-empt, and confirm actual CARC/RARC
combinations against your first live remits.

| Denial pattern | Likely cause | Response |
|---|---|---|
| **Not medically necessary** | No published criteria exist; reviewer had only the claim | Appeal with the **operative report** + §2's six elements + **NCD 160.1** text covering "surgical cutting of the nerve (rhizolysis)." Cite that NCD 160.1 defers to MAC medical staff, so there is no criteria set the claim could have failed. |
| **Bundled / included in another procedure** | A same-day facet block or ESI was billed — **modifier indicator `0`, unbreakable** (§4.6) | **Not appealable.** Fix the process: block/ESI must be a separate date. |
| **Included in global period** | Subsequent RFA billed inside 90 days without **`79`** (§4.5) | Rebill or appeal with `79` and documentation that the RFA is unrelated to the transected nerve. |
| **Units exceed MUE** | Stale payer edit table still at the pre-2026 MUE of 2, or genuinely >6 | Cite the current **Practitioner MUE table, NCCI v32.3 eff. 1 Oct 2026: MUE 6, MAI 3**. MAI 3 is appealable with documentation. |
| **Bilateral paid at 100%, not 150%** | **Bilateral indicator `0`** — working as designed (§4.2) | 🔴 **Not a denial. Do not appeal.** Close it and correct the revenue model. |
| **Invalid / incomplete diagnosis** | `M54.5` or another header code submitted (§3.1) | Correct to a billable code at full specificity. **Audit the whole claim file for `M54.5` — this affects existing facet claims too.** |
| **Diagnosis inconsistent with procedure** | Facet dx (`M47.81x`, `M54.x`) on a 64772 line (§3) | Recode to a nerve-specific dx per §3.2. Expect a records request; send the op report. |
| **Invalid place of service** | POS `11` on Medicare — **`NA` non-facility indicator** (§5) | Cannot be fixed by appeal for Medicare. Correct POS and site going forward. |
| **Assistant surgeon denied** | Payer following the wrong indicator, or `AS` omitted for a PA/NP | 64772 **ASST = `2`, payable with no documentation requirement**. Cite the PFS Relative Value File. Ensure `AS` is present for non-physician assistants. |
| **Co-surgeon denied** | Documentation not submitted | 64772 **CO-SURG = `1`** — payable **with** documentation. Submit the medical-necessity rationale for two surgeons. |
| **Specialty / taxonomy edit** | NPI reads Orthopaedic Surgery only (§9, item 5) | Refresh NPPES and re-attest with the payer. |

---

## 9. Open calls — must be answered by a human

Five items could not be closed from published sources. Four are blocked by this environment's network
policy; one is a practice-side action.

| # | Item | Contact | Priority |
|---|---|---|---|
| 1 | **Optum's Arizona PA code lists.** `www.optum.com` and `business.optum.com` are blocked by egress policy; `events.optumcare.com` does not resolve. Five access paths attempted. **No verified answer on whether Optum requires PA for 64772.** | `optumproportal.com` · **877-370-2845** (TTY 711) · `lcd_um@optum.com` | 🔴 **Highest** — affects 22 UHC MA group numbers |
| 2 | **AZ Blue's PA position and medical policy for 64772.** Policy search is a JavaScript app with no server-rendered results; PA code list (`edge.sitecorecloud.io`) and `provider.azblue.com` both blocked. | [PA lookup](https://www.azblue.com/prior-authorization-lookup/providers) · `UtilMgmt@azblue.com` · **602-864-4320** · **1-800-322-8670** | 🔴 High |
| 3 | **Each delegated IPA's own protocol** — UHC: "you must follow the delegate's protocols." | Each delegated group directly | 🔴 High |
| 4 | **Multi-nerve unit reporting** — does Noridian treat additional nerves as separate units (MUE 6) or apply the bilateral `0` cap across them? And is there an ASC facility bilateral-reporting instruction for 64772 (A58403's `RT`/`LT` split is written for 64490–64495)? | Noridian JF Provider Contact Center | ⚠️ Medium — before the first multi-nerve or bilateral ASC case |
| 5 | **NPPES refresh.** NPI 1437125846 lists **Orthopaedic Surgery (`207X00000X`) as its only taxonomy** and was **last updated 20 January 2020**. No payer policy found restricts 64772 by taxonomy, but a pain program on an NPI reading orthopaedics alone invites specialty edits. Also confirm ASC privileging covers this procedure. | Practice credentialing | ⚠️ Before go-live |
| 6 | **Humana** coverage policy for 64772, and whether the **commercial** book differs from MA/DSNP. | Humana provider rep · Cohere **833-283-0033** | ⚠️ Medium |

---

## 10. Go-live checklist

**Before the first case**
- [ ] Dictation template updated with §2's six elements; Dr. Luke briefed that the op note is the coverage determination
- [ ] Dx list built from §3.2; **`M54.5` removed from all templates and superbills**
- [ ] POS logic set to `24` / `19` / `22` — **`11` blocked for this code**
- [ ] Noridian PA Lookup screenshot for 64772 saved and dated
- [ ] Calls 1–3 in §9 completed and answers documented in writing
- [ ] ASC privileging confirmed for the booking site
- [ ] Charge master carries the facility-only fee; no non-facility rate loaded for Medicare

**Claim scrub rules to add**
- [ ] Reject 64772 with POS `11` on any Medicare plan
- [ ] Reject 64772 on the same date as `64490`–`64495`, `62320`–`62327`, `64479`, `64480`, `64483`, `64484`
- [ ] Reject a facet dx (`M47.81x`, `M47.89x`, `M48.1x`, `M54.x`) as primary on a 64772 line
- [ ] Reject any header dx code (`M54.5`, `M47.81`, `G58`) on any claim
- [ ] Warn if 64772 units > 6
- [ ] Warn if `64633`–`64636` billed within 90 days of a 64772 for the same patient **without `79`**
- [ ] Warn if `50` used on 64772 (prefer `LT`/`RT`; no payment premium either way)
- [ ] Require the operative report attachment on every 64772 claim

**Ongoing**
- [ ] Track the first 10 claims by payer: paid / denied / records requested, and actual CARC-RARC pairs — then replace §8's anticipated denials with your real remit data
- [ ] Re-check payer policies quarterly; several cited here have 2026 effective dates and will revise

---

*Policy positions and effective dates are as published on 15 September 2026. Items marked ⚠️ or listed in
§9 are **not** verified from a published source and must be confirmed with the payer before they are
relied on for scheduling or billing. Payment indicators, MUE/MAI values, NCCI edits, ASC indicators and
GPCIs are taken from primary CMS data files — see the research memo's Sources section.*
