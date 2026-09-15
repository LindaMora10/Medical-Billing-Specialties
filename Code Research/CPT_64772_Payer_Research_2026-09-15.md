# CPT 64772 — Code Validation and Payer Research (Arizona)

**Prepared:** 15 September 2026
**Requested for:** Dr. Timothy Luke (NPI 1437125846) — Executive Team presentation this week;
Deanna and Bri, auth & scheduling meeting next week.
**Jurisdiction priority:** Arizona — Medicare Part B is **Noridian Healthcare Solutions, Jurisdiction F**
(contract 03101 Part A / 03102 Part B).

> **Status: 15 Sep 2026 — updated.** Dr. Luke has confirmed he is performing **64772**. This memo is the
> **reference research**; the operational instructions for billing it are in the companion
> **[CPT 64772 Billing Playbook](CPT_64772_Billing_Playbook_2026-09-15.md)**.
>
> **What the billing department needs to carry from this document:** 64772 is an **open**
> transection/avulsion code, **payable only in a facility** (ASC or HOPD — never the office on Medicare),
> with a **90-day global**, **MUE 6 / MAI 3**, a **bilateral indicator of `0`** (modifier 50 earns no
> premium), and **hard NCCI bundles against facet blocks and all ESI codes**. **No payer reviewed
> publishes medical-necessity criteria for it**, so every claim is decided on the operative report.
>
> **Correction (see [§2.1](#21-traditional-medicare--noridian-jurisdiction-f-arizona)): 64772 is NOT in
> WISeR scope.** An earlier version of this memo flagged possible WISeR exposure because NCD 160.1 is an
> in-scope policy. The WISeR Operational Guide's Appendix A has since been located: the NCD 160.1 code set
> is **64605 and 64610 only**. That blocker is cleared.
>
> [Part 1](#part-1--code-validation) records the code-validation analysis that was requested before
> coverage research. It is retained as the documentation standard 64772 has to meet — **§1.5 is the
> operative-note checklist** — not as an argument against using the code.

---

## Part 1 — Code validation

### 1.1 Exact descriptions

| Code | Official AMA descriptor | CPT subsection | CMS short descriptor |
|---|---|---|---|
| **64772** | **Transection or avulsion of other spinal nerve, extradural** | Surgery › Nervous System › Extracranial Nerves, Peripheral Nerves and Autonomic Nervous System › **Transection or Avulsion** | `Incision of spinal nerve` |
| 64633 | Destruction by neurolytic agent (eg, chemical, thermal, electrical or radiofrequency), paravertebral facet joint nerve(s), with imaging guidance (fluoroscopy or CT); **cervical or thoracic, single facet joint** | …› **Destruction by Neurolytic Agent** | `Destroy cerv/thor facet jnt` |
| +64634 | …; cervical or thoracic, **each additional** facet joint (list separately in addition to code for primary procedure) | ″ | `Destroy c/th facet jnt addl` |
| 64635 | …; **lumbar or sacral, single facet joint** | ″ | `Destroy lumb/sac facet jnt` |
| +64636 | …; lumbar or sacral, **each additional** facet joint (list separately…) | ″ | `Destroy l/s facet jnt addl` |
| 64625 | **Radiofrequency ablation, nerves innervating the sacroiliac joint, with image guidance (ie, fluoroscopy or computed tomography)** | ″ | `Rf abltj nrv nrvtg si jt` |
| 64999 | Unlisted procedure, nervous system | Nervous System, unlisted | `Unlisted px nervous system` |

Source for CMS descriptors and all payment indicators below: **CMS PFS Relative Value File
`PPRRVU2026_Oct_nonQPP`, RVU26D, effective 1 October 2026** —
[cms.gov PFS Relative Value Files](https://www.cms.gov/medicare/payment/fee-schedules/physician/pfs-relative-value-files)
→ *RVU26D* → `PPRRVU2026_Oct_nonQPP.csv`.

### 1.2 What 64772 actually describes

- **Open, not percutaneous.** It sits in the *Transection or Avulsion* subsection. "Transection" is
  sharp division of the nerve; "avulsion" is tearing it away. Both are **mechanical** acts requiring
  surgical exposure. There is no imaging-guidance language and no needle/electrode language in the
  descriptor.
- **Extradural** — the nerve is divided outside the dura.
- **"Other spinal nerve"** — a spinal nerve that no more specific code in the series names. It is the
  residual code of its family (64771 is the same construction for "other cranial nerve"). In practice
  it is used for named peripheral neurectomies; the common real-world application is an
  **AIN/PIN (anterior/posterior interosseous nerve) neurectomy** at the wrist
  ([KZA coding coach, 5 Mar 2026](https://www.kzanow.com/coding-coaches/nerve-transection-cpt-64772-03-05-26)).
- **Mechanism is not neurolysis.** Nothing in 64772 describes destruction by a neurolytic agent —
  chemical, thermal, electrical or radiofrequency.

### 1.3 Verdict — the procedure as described is 64633–64636, not 64772

If what Dr. Luke is presenting is **medial branch rhizotomy / facet radiofrequency ablation**, then
64772 is wrong in three independent ways, any one of which is disqualifying:

| | 64772 requires | Medial branch RFA is |
|---|---|---|
| **Mechanism** | transection or avulsion (mechanical division) | destruction by a neurolytic agent (thermal RF lesion) |
| **Approach** | open surgical exposure | percutaneous, needle/electrode under fluoro or CT |
| **Target nerve** | "other spinal nerve" — one no specific code names | **paravertebral facet joint nerve(s)** — specifically named by 64633–64636 |

CPT's own structure forecloses the substitution. A code for "other X" is reportable only when no
specific code describes the anatomy **and** technique. Because 64633–64636 name the paravertebral
facet joint nerves and the neurolytic mechanism precisely, the medial branches can never be the
"other spinal nerve" of 64772. Reporting 64772 for this work would also claim an **open** service
that the operative note will not support, and it would claim a **90-day global** where the correct
code carries **10 days**.

**64625** is a third, separate thing: radiofrequency ablation of the nerves innervating the **sacroiliac
joint** (lateral branches), reported **once per side for the whole joint**. Per CPT instruction it is not
reportable with 64635 for the same session even though medial and lateral branches are anatomically
distinct. It is not a substitute for either of the above.

### 1.4 The other candidate — 64999, not 64772

If the procedure is a facet denervation performed **during an open spinal exposure or endoscopically**,
the applicable guidance is that **no CPT code describes mechanical destruction of the facet nerves
during an open spinal procedure**, and the **unlisted code 64999** is used. The fallback is *not* 64772.
That route has consequences of its own:

- **Medicare status code `C`** — contractor-priced, zero published RVUs; every claim is manually priced.
- **Excluded from ASC payment** — 64999 is on **ASC Addendum EE** (*Surgical Procedures to be Excluded
  from Payment in ASCs for CY 2026*). **The ASC cannot be paid for it by Medicare at all.**
- **AHCCCS pays it `BR` (by report)** — narrative required.
- **Humana requires prior authorization** for 64999 (see [§2.3](#23-humana)).
- MUE 1, MAI 3.

### 1.5 What documentation would have to support 64772 instead

To defend 64772 rather than 64633–64636, the operative report must establish **all** of the following.
Anything less and the claim is, on its face, a miscoded facet procedure:

1. **An open surgical approach** — incision, sequential dissection and exposure, layered closure.
   A note describing needle placement under fluoroscopic guidance defeats the code outright.
2. **The nerve transected or avulsed, named specifically**, with **level and side** — and an affirmative
   statement that it is **not** a paravertebral facet joint / medial branch nerve.
3. **The extradural location** of the division.
4. **The mechanism** — sharp or mechanical division/avulsion, explicitly not a thermal, chemical,
   electrical or radiofrequency lesion.
5. **Why no more specific code applies** — i.e. why this nerve is an "other" spinal nerve.
6. A true **operative report**, not a procedure note, with indication, conservative care history, and the
   diagnostic workup that localised the pain to that named nerve.
7. If the target really is the facet medial branch done open or endoscopically → **64999 with a narrative
   and a comparison code**, not 64772.

> **For the Executive Team slide:** the equipment and the technique decide the code, not the other way
> around. If the device is a percutaneous RF probe, the code is 64633–64636 and the economics of this
> proposal change materially — 64772 pays a facility-only $15.46 total RVU with a 90-day global;
> 64635 pays 13.92 total RVU in the office with a 10-day global and **is** payable in the office.

---

## Part 2 — Payer-by-payer

### 2.1 Traditional Medicare — Noridian Jurisdiction F (Arizona)

**Coverage status: covered in principle by a national policy, with no code-level criteria — adjudicated case-by-case.**

| Item | Finding |
|---|---|
| **LCD** | **Not addressed.** 64772 appears **nowhere** in **LCD L38801 "Facet Joint Interventions for Pain Management,"** Noridian, rev. eff. **16 Apr 2026** (v23; original eff. 25 Apr 2021). Confirmed to cover Arizona (contracts 03101/03102). [Link](https://www.cms.gov/medicare-coverage-database/view/lcd.aspx?lcdid=38801&ver=23) → *Coverage Guidance › Indications and Limitations*. |
| **LCA** | **Not addressed.** Absent from **A58403 "Billing and Coding: Facet Joint Interventions for Pain Management,"** Noridian, rev. eff. **21 May 2026** (v27, R8). [Link](https://www.cms.gov/medicare-coverage-database/view/article.aspx?articleid=58403&ver=27) → *CPT/HCPCS Codes* and *ICD-10-CM Codes that Support Medical Necessity*. |
| **Governing NCD** | **NCD 160.1 "Induced Lesions of Nerve Tracts,"** Pub. 100-3, longstanding (CMS has not posted an effective date for the current version); benefit category *Physicians' Services*. [Link](https://www.cms.gov/medicare-coverage-database/view/ncd.aspx?ncdid=19) → *Indications and Limitations of Coverage*. |
| **NCD text** | Covers lesions "produced by **surgical cutting of the nerve (rhizolysis)**, chemical destruction of the nerve, or by creation of a radio-frequency lesion," for "chronic or acute pain arising from conditions such as terminal cancer or lumbar degenerative arthritis." Payment "may be made for these denervation procedures **when used in selected cases (concurred in by the Medicare Administrative Contractor's medical staff)** to treat chronic pain." |
| **Medical necessity criteria** | **None published at code level.** NCD 160.1 has no criteria list, no frequency limit, no conservative-care prerequisite and **no covered-diagnosis table**. It delegates to MAC medical staff. Practical effect: **every 64772 claim is a medical-review claim**, and there is no published standard to appeal against. |

**Prior authorization — no requirement, and WISeR does not reach 64772 (resolved)**

There is **no standing Medicare prior-auth requirement** for 64772, and **no WISeR requirement either.**

Arizona is one of six states in the **WISeR Model** (Wasteful and Inappropriate Service Reduction),
effective **1 January 2026**, implementation from **5 January 2026**, running six years through
**31 December 2031**. **NCD 160.1 "Induced Lesions of Nerve Tracts" is an in-scope WISeR policy** — which
is why this needed checking, since NCD 160.1 is the policy that governs 64772.

**It does not capture 64772.** The **WISeR Model Provider and Supplier Operational Guide, Appendix A,
Table A2 "Induced Lesions of Nerve Tracts (NCD 160.1)"** lists exactly two codes:

| Code | Description |
|---|---|
| **64605** | Destruction by neurolytic agent, trigeminal nerve; second and third division branches at foramen ovale |
| **64610** | Destruction by neurolytic agent, trigeminal nerve; second and third division branches at foramen ovale under radiologic monitoring |

The guide states plainly at §6.2.2: **"For this NCD, WISeR will initially focus on neurolytic destruction
of the trigeminal nerve."** Appendix C Table C2 (associated/ancillary codes drawn into review) lists
61790, 64605, 64610, 70450, 76000, 77002, 00222, 01991 — **64772 appears in neither table.**

Source: [CMS WISeR Model Provider and Supplier Operational Guide](https://www.cms.gov/priorities/innovation/files/wiser-provider-supplier-guide.pdf)
→ *§6.2.2 Induced Lesions of Nerve Tracts*; *Appendix A, Table A2*; *Appendix C, Table C2*.
Noridian confirms "**Only certain CPT codes, from certain policies, are included in the WISeR model**"
([WISeR Common Questions and Answers, JF Part B](https://med.noridianmedicare.com/web/jfb/cert-reviews/pre-claim/wiser-model/wiser-common-questions-and-answers)).

Also in scope for Arizona but **not reaching 64772**: Epidural Steroid Injections (LCD L39240),
Percutaneous Vertebral Augmentation (L34228), Cervical Fusion (L39758), arthroscopic knee lavage/
debridement (NCD 150.9, code 29877), VNS, phrenic and sacral nerve stimulation, HGNS. **Facet codes
64633–64636 are not in the WISeR service list either.**

**Verification step for the billing department:** Noridian has loaded the WISeR CPT/HCPCS codes into its
**Prior Authorization Lookup Tool**. Run 64772 through it once to capture a dated screenshot for the file —
that is the cleanest evidence that no PA applies.
[Noridian JF Part B Prior Authorization](https://med.noridianmedicare.com/web/jfb/cert-reviews/pre-claim) ·
[WISeR page](https://med.noridianmedicare.com/web/jfb/cert-reviews/pre-claim/wiser-model).

*(Arizona's WISeR solution participant is **Zyter Inc.**; Washington's is Virtix Health LLC. Where WISeR
does apply, PA is voluntary, an approval is valid 120 days, and skipping it routes the claim to
pre-payment review where "associated services may be denied if the primary service is denied." None of
that attaches to 64772.)*

**Place of service — 64772 is facility-only**

| Setting | Status |
|---|---|
| **Office (POS 11)** | **Not payable.** The non-facility PE RVU carries the **`NA` indicator** in PPRRVU2026 — Medicare publishes no non-facility rate. |
| **ASC (POS 24)** | **Covered.** On **ASC Addendum AA**, payment indicator **`A2`** = "Surgical procedure on ASC list in CY 2007; payment based on OPPS relative payment weight." Weight 16.8435, **rate $948.66**, subject to multiple-procedure discounting. |
| **HOPD (POS 19/22)** | **Covered.** APC **5431**, OPPS rate **$1,765.76** (Addendum FF). |

Source: **July 2026 ASC Addenda, file `July 2026 ASC Addenda.07.08.26.xlsx`, eff. 1 July 2026** —
[ASC Payment Rates Addenda](https://www.cms.gov/medicare/payment/prospective-payment-systems/ambulatory-surgical-center-asc/asc-payment-rates-addenda)
→ *July 2026 ASC Addenda* → sheets `July 2026 ASC AA`, `DD1`, `EE`, `FF`.

No site-of-service review applies on traditional Medicare — but the `NA` indicator makes the office
economically impossible regardless.

**Payment indicators — 64772 vs the facet codes**

| Indicator | **64772** | 64633 / 64635 | +64634 / +64636 | 64625 |
|---|---|---|---|---|
| Status code | A | A | A | A |
| Work RVU | 7.64 | 3.24 / 3.24 | 1.29 / 1.13 | 3.31 |
| Non-facility total | **NA (not payable)** | 13.74 / 13.92 | 7.98 / 7.53 | 14.84 |
| Facility total | 15.46 | 5.17 / 5.18 | 1.73 / 1.52 | 5.29 |
| **Global days** | **090** | **010** | ZZZ | 010 |
| Multiple procedure | 2 | 2 | 0 | 2 |
| **Bilateral surgery** | **0** — 150% adjustment does **not** apply | **1** — 150% applies | 1 | 1 |
| **Assistant surgeon** | **2** — payable, no documentation required | **1** — **not payable** (statutory restriction) | 1 | 1 |
| **Co-surgeon** | **1** — payable **with** documentation | **0** — **not permitted** | 0 | 0 |
| Team surgeon | 0 | 0 | 0 | 0 |
| PC/TC | 0 | 0 | 0 | 0 |

2026 conversion factor on this file: **33.4009**.

**MUE (Medically Unlikely Edits)** — *Practitioner Services MUE Table, NCCI v32.3, effective 1 October 2026*
([link](https://www.cms.gov/medicare/coding-billing/national-correct-coding-initiative-ncci-edits/medicare-ncci-medically-unlikely-edits) → *Practitioner Services MUE Table*):

| Code | MUE | MAI | Rationale | What MAI means |
|---|---|---|---|---|
| **64772** | **6** | **3** | Clinical: Data | Per date of service, **clinical** — can be exceeded on appeal with documentation |
| 64633 | **1** | **2** | Code Descriptor / CPT Instruction | Per date of service, **policy** — **absolute. No modifier and no appeal gets you a second unit.** |
| 64635 | **1** | **2** | Code Descriptor / CPT Instruction | same — absolute |
| +64634 | 4 | 3 | Clinical: Data | clinical |
| +64636 | 4 | 3 | Clinical: Data | clinical |
| 64625 | 1 | 2 | CMS Policy | absolute |
| 64490 / 64493 | 1 | 2 | CMS Policy | absolute |
| 64999 | 1 | 3 | Clinical: CMS Workgroup | clinical |

64772's MUE was **raised from 2 to 6 units in January 2026** (corroborated by KZA, above).

**NCCI procedure-to-procedure edits** — *Practitioner PTP Edits, `ccipra-v323r0`, NCCI v32.3, effective
1 October 2026* ([link](https://www.cms.gov/medicare/coding-billing/national-correct-coding-initiative-ncci-edits/medicare-ncci-procedure-procedure-ptp-edits)
→ *Practitioner PTP Edits, files f1–f4*):

64772 appears as **Column 1 in 346 edits and as Column 2 in zero** — it is never the bundled code.
All edits below carry **modifier indicator `0`, meaning a hard bundle that no modifier can break:**

| Column 1 | Column 2 (denied) | Effective | MI | Rationale |
|---|---|---|---|---|
| 64772 | **64490, 64493** | 2010-01-01 | **0** | Anesthesia service included in surgical procedure |
| 64772 | **64491, 64492, 64494, 64495** | 2017-04-01 | **0** | Misuse of Column Two code with Column One code |
| 64772 | **62320, 62321, 62322, 62323, 62324, 62325, 62326, 62327** (ESI) | 2017-01-01 | **0** | Misuse of Column Two code with Column One code |
| 64772 | **64479, 64483** (transforaminal ESI) | 2005-10-01 | **0** | Misuse of Column Two code with Column One code |
| 64772 | **64480, 64484** | 2017-04-01 | **0** | Misuse of Column Two code with Column One code |

**There is no PTP edit, in either direction, between 64772 and 64633, 64634, 64635, 64636, or 64625.**

**Frequency limits / conservative care:** none published for 64772. (For contrast, L38801 imposes on facet
RFA: pain ≥3 months with documented failure of non-invasive conservative management; **two** diagnostic
medial branch blocks each giving **≥80% sustained relief**, second no sooner than 2 weeks after the first;
**max 2 RFA sessions per rolling 12 months per spinal region**; **1–2 levels per session**, unilateral or
bilateral; repeat RFA needs ≥50% improvement sustained ≥6 months; three- and four-level procedures
**non-covered**; no CT/fluoro guidance = non-covered; sedation/MAC not reasonable and necessary for
facet injections.)

**Required documentation** (A58403, verbatim): "The patient's medical record should include but is not
limited to: The assessment of the patient by the performing provider as it relates to the complaint of the
patient for that visit, Relevant medical history, Results of pertinent tests/procedures, Signed and dated
office visit record/operative report."

---

### 2.2 Blue Cross Blue Shield of Arizona (AZ Blue)

**Coverage status: unlisted in the vendor program. Not in any eviCore code list or guideline I could retrieve.**

| Item | Finding |
|---|---|
| **PA vendor** | **eviCore by Evernorth** — program *Musculoskeletal – Advanced Procedures (spine, joint, interventional pain management)*. [AZ Blue eviCore page](https://www.evicore.com/resources/healthplan/blue-cross-blue-shield/arizona) → *Musculoskeletal—Advanced Procedures*. |
| **Plan-type split** | eviCore's MSK/interventional-pain program applies to **Medicare Advantage members only, "not for commercial members."** Radiology, lab and radiation oncology are commercial **and** MA; medical drug management is commercial only. |
| **Code list** | **`BCBSAZ_MSK_CodeList_Eff01.01.26`, effective 1 January 2026** (published 12 Dec 2025). [Link](https://www.evicore.com/sites/default/files/resources/2025-12/BCBSAZ_MSK_CodeList_Eff01.01.26_Pub12.12.2025.pdf). |
| **64772 on that list?** | **No — absent entirely.** |
| **Facet codes on that list** | 64490–64495, 64625, 64633, 64634, 64635, 64636 → **Commercial Precert `N`** / **Medicare Advantage Precert `Y`**, Claims Studio `N` both, program "MSK – Interventional Pain Management." |

**eviCore clinical guideline: CMM-208 "Ablations/Denervations of Facet Joints and Peripheral Nerves,"
V1.0.2025, published 28 February 2025**
([link](https://www.evicore.com/sites/default/files/clinical-guidelines/2025-02/EviCore_CMM-208%20Ablat%20Denerv%20Nerves_Final_V1.0.2025_Pub02.28.2025.pdf)
→ *Procedure Codes* and *Not Medically Necessary*):

- Code list: **64633, +64634, 64635, +64636, 64640**. **64772 is not in it.**
- **Not medically necessary techniques:** pulsed RFA; **"endoscopic radiofrequency denervation/endoscopic
  dorsal ramus rhizotomy"**; cryoablation/cryoneurolysis/cryodenervation; chemical ablation (alcohol,
  phenol, glycerol); laser ablation; cooled radiofrequency ablation.
- **Peripheral nerve destruction** is "considered not medically necessary for the treatment of ANY of the
  following conditions: chronic pain syndromes, foot/heel pain, hip pain, knee pain, shoulder pain."
- Diagnostic blocks limited to **two** before RFA; medial branch RFA C2-3 through L5-S1 requires a
  **six-month interval**.

**What this means operationally**

- On **AZ Blue commercial**, facet RFA needs **no eviCore precert** — so there is **no pre-service
  approval available to obtain**. All risk is post-service. Same for 64772: no precert pathway, no
  published criteria, review happens after you've done the case.
- On **AZ Blue Medicare Advantage**, facet RFA **does** need eviCore precert. 64772 is not on the list,
  so it would route to **AZ Blue's own utilisation management**, not eviCore.
- If the technique is **endoscopic rhizotomy**, eviCore calls it **not medically necessary** outright for
  the MA book.

> ⚠️ **Unverified gap — needs a written answer from AZ Blue.** I could **not** retrieve (a) an AZ Blue
> medical policy for 64772 or for facet joint denervation, or (b) AZ Blue's own prior-auth code list.
> Their policy search is a JavaScript application I could not query, and the PA code list
> (`az-blue-prior-auth-code-lists.xlsx` on `edge.sitecorecloud.io`) is blocked from this environment.
> **Do not assume "no eviCore precert" means "no AZ Blue precert."** Run 64772 through the
> [AZ Blue prior authorization lookup](https://www.azblue.com/prior-authorization-lookup/providers) and
> request the medical policy in writing. UM contact: `UtilMgmt@azblue.com`, 602-864-4320.
> Note AZ Blue also routes some Medicare Advantage members through **Optum Health Network Arizona
> (OHNAZ)** and **Arizona Priority Care (AZPC)**, each with its own determination process —
> so the answer can differ by delegated group for the same code.

---

### 2.3 Humana

**Coverage status: not on the prior-auth list; no code-specific policy found.**

| Item | Finding |
|---|---|
| **Document** | **Medicare Advantage and Dual Eligible Special Needs Plans Prior Authorization and Notification List, effective 1 January 2026** (doc ref `790807ALL0725-C GHHMQHEEN`). [Link](https://assets.humana.com/is/content/humana/FINAL_Medicare%20and%20DSNP%20Prior%20Authorization%20and%20Notification%20List%20-%201-1-2026pdf) → *Facet injections*; *Radiofrequency Ablation for the SI Joint*. |
| **PA required** | "**Facet injections** — 64490, 64491, 64492, 64493, 64494, 64495, **64633, 64634, 64635, 64636, 64999**, 0213T, 0214T, 0215T, 0216T, 0217T, 0218T." Separately: "**Radiofrequency Ablation for the SI Joint** — 64625." |
| **64772** | **Not listed** → no prior authorization required per the published list. Adjudicated against Humana coverage criteria at claim time. |
| **Note on 64999** | **64999 requires prior authorization** at Humana. The unlisted-code route is therefore a PA route, not a way around one. |
| **Vendor** | **Cohere Health** for multiple PA categories — portal `next.coherehealth.com`, onboarding `next.coherehealth.com/organization_onboarding`, phone **833-283-0033** (M–F 8am–8pm ET), fax 857-557-6787; expedited/urgent via the portal. Humana contracted Cohere for musculoskeletal prior authorization. |
| **Continuity of care** | "Humana does not require prior authorization for basic Medicare benefits during the **first 90 days** of a new member's enrollment for active courses of treatment that started prior to enrollment," with the caveat that services may still be reviewed against coverage criteria at payment. Append the modifier per Humana **MA Payment Policy CP2023011** or submit records evidencing an active course of treatment. |
| **Frequency (facet RFA)** | No more than **two RFA sessions per rolling 12-month period per spinal area**; moderate-to-severe predominantly axial chronic neck or low back pain with a functional deficit on a pain or disability scale. |
| **Site of service** | Facet injections/ablations performed in an **ASC, physician office or Critical Access Hospital** may not require authorization under some plans — **plan- and state-specific, must be verified per member.** |
| **2026 change** | Effective 1 Jan 2026 Humana removed roughly a third of outpatient PA requirements and launched a **Gold Card** program waiving PA for qualifying providers on eligible services. Confirm whether Dr. Luke qualifies. |

> ⚠️ **Unverified gap.** I found **no Humana medical coverage policy addressing 64772**. Absence from the
> PA list means no pre-service review, **not** that it is covered. Request the applicable coverage policy
> in writing, and confirm whether Humana's Arizona commercial book (as distinct from MA/DSNP) carries a
> different PA list.

---

### 2.4 UnitedHealthcare

**Coverage status: unlisted in every applicable UHC policy reviewed. Related techniques are affirmatively unproven.**

| Policy | Number | Effective | 64772? | Key content |
|---|---|---|---|---|
| **Ablative Treatment for Spinal Pain** (Commercial & Individual Exchange) | **2026T0107II** | **1 Feb 2026** (rev. 28 Jan 2026) | **Absent** | Codes: 22899, 27299, **64625**, 64628, 64629, 64999. **Unproven and not medically necessary:** pulsed RFA; **"endoscopic radiofrequency ablation/endoscopic rhizotomy"**; cryoablation; **cooled RFA**; chemical ablation; laser ablation. **"Ablation for treating sacroiliac pain is unproven and not medically necessary"** → 64625 not covered commercially. Intraosseous BVN RFA (Intracept) unproven. Header note: **"Conventional (Thermal) Radiofrequency Ablation requires site of service review."** [Link](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/ablative-treatment-spinal-pain.pdf) → *Coverage Rationale*; *Applicable Codes*. |
| **Facet Joint and Medial Branch Block Injections for Spinal Pain** (Commercial & IE) | **2026T0004WW** | **10 Sep 2026** | **Absent** | Codes: 0213T–0218T, 64490–64495. Diagnostic block covered only when: facet loading pain on exam; **no clinically significant improvement (pain still ≥3/10) after ≥4 weeks conservative care**; imaging excludes other causes; segment **not fused**; **and an RFA procedure is being considered**. Second block must be same level/side after a positive first. **Unproven:** any block where RFA is not a treatment option at that level; >2 blocks same level/side; **all therapeutic** facet injections/MBB; untreated radiculopathy at the same level; MBB local anaesthetic volume >0.5 mL; **ultrasound guidance**. [Link](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/facet-joint-injections-spinal-pain.pdf) → *Coverage Rationale*. |
| **Office-Based Procedures – Site of Service** | **MP.12.22** | **1 Jul 2026** | **Absent** | **Includes 64633 and 64635.** ASC is medically necessary only for: local anaesthetic allergy; bleeding disorder with significant morbidity risk; developmental/cognitive status; **failed office-based attempt** due to body habitus, abnormal anatomy or technical difficulty; complications/comorbidity making an office procedure unsafe; **or** no geographically accessible office with the required equipment (e.g. fluoroscopy) or no geographically accessible in-network provider. **"Surgeon-preferred or proprietary instruments, instrument sets, and hardware sets" are expressly excluded** as a justification. Applies to Commercial except UnitedHealthcare West; IE in all states except IL, MA, TX, WI. [Link](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/office-based-procedures-site-service.pdf) → *Coverage Rationale*; *Applicable Codes*. |
| **Outpatient Surgical Procedures – Site of Service** | **MP.11.27** | **1 Aug 2026** | **Absent** | 64772 not found in the code list. |
| **Pain Management** (Medicare Advantage) | **MMP070.12** | **1 Sep 2026** (committee approval 12 Aug 2026) | **Absent** | Addresses 64625 (SI denervation), 64405, 64722, 64744, BVN RFA. States: "Medicare does not have a National Coverage Determination… **Local Coverage Determinations (LCDs)/Local Coverage Articles (LCAs) exist and compliance with these policies is required where applicable.**" [Link](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/medadv-mp/pain-management-rehabilitation.pdf) → *Coverage Rationale*; *Applicable Codes*. |

**Critical bridge:** because MMP070.12 defers to LCD/LCA where applicable, **UHC Medicare Advantage members
in Arizona are held to Noridian L38801 / A58403** for facet work — including the 80% × 2 diagnostic block
requirement, the 1–2 levels per session cap, and the covered-diagnosis list in §3. For 64772 it defers to
**NCD 160.1**, i.e. case-by-case.

**Arizona Medicare Advantage — delegation to Optum, by plan and group number**

From dates of service beginning **1 January 2026**, **Optum Health Networks** (a UnitedHealthcare affiliate)
administers certain UHC MA plans in Arizona. Source: *Administrative updates for UnitedHealthcare Medicare
Advantage members in Arizona*, quick reference guide **PCA-4-26-00582-M&R-QRG_05132026**
([link](https://www.uhcprovider.com/content/dam/provider/docs/public/health-plans/medicare/2026/qrg/2026-MED-ADV-QRG-Optum-Care-Arizona.pdf)
→ *The following benefit plans will be administered by Optum Health Networks, effective Jan. 1, 2026*).

| Contract | PBP | Segment | Group number(s) |
|---|---|---|---|
| H5253 | 178 | 000 | 90451 |
| H2001 | 036 | 000 | 90927 |
| H2406 | 062 | 000 | 90920, 06362 |
| H2406 | 063 | 000 | 90811 |
| H2406 | 076 | 000 | 90823, 90990 |
| H2406 | 077 | 000 | 90824 |
| H2406 | 078 | 000 | 90922, 06372 |
| H5253 | 035 | 000 | 90653, 06453 |
| H5253 | 036 | 000 | 90974 |
| H0609 | 025 | 000 | 00345 |
| H0609 | 026 | 000 | 91038, 91041 |
| H0609 | 027 | 000 | 00340 |
| H0609 | 042 | 000 | 00337, 00339 |
| H0609 | 043 | 000 | 00335 |
| H0609 | 044 | 000 | 00332 |
| H0609 | 045 | 000 | 00330 |

- **Identify these members by payer ID `LIFE1` on the member ID card.**
- **HMO and HMO-POS** members delegated to Optum networks **need a PCP referral before the specialist
  visit**, submitted by the PCP to Optum in advance. Claim denial applies.
- Referral requirements do not apply to Institutional SNP plans or Erickson Advantage plans.
- PA requirements are published at **UHCprovider.com/priorauth › Advance Notification and Plan Requirement
  Resources**. A PA already approved by UnitedHealthcare for DOS from 1 Jan 2026 does not need resubmitting.
- **"If you are a network provider who is contracted directly with a delegated medical group/IPA, then you
  must follow the delegate's protocols"** — delegates use their own systems and forms.

---

### 2.5 Optum

**Coverage status: could not be verified. Treat as an open item.**

Optum appears in Arizona in three distinct roles, and they are easy to confuse:

1. **Optum Health Networks** — administers the UHC MA plans and group numbers listed in §2.4 from
   1 Jan 2026. Submissions via the **Optum Pro portal, `optumproportal.com`**. PA intake
   **877-370-2845** (TTY 711); `lcd_um@optum.com`.
2. **Optum Health Network Arizona (OHNAZ)** — appears in **AZ Blue's** Medicare Advantage authorisation
   workflows (portal `optumproportal.com`).
3. **Delegated medical groups / IPAs** contracted through Optum, which run their own UM with their own
   forms and protocols.

> ⚠️ **Unverified gap — this is the largest hole in this research.** I could **not** retrieve Optum's
> Arizona prior-authorization code lists. `www.optum.com` and `business.optum.com` are blocked by this
> environment's network egress policy, and `events.optumcare.com` does not resolve. **I have no verified
> answer on whether Optum requires prior authorization for 64772, 64633–64636 or 64625, or what criteria
> it applies.** The documents to obtain are:
> - `optum.com/…/forms/az-prior-authorization-list-bcbs.pdf` — OptumCare Network of Arizona PA list (BCBS)
> - `business.optum.com/en/support.hcp-resources.prior-authorization-list-arizona.html` — Arizona PA list
>
> Deanna/Bri should pull both from an unrestricted connection or request them from the Optum provider rep,
> **and separately confirm each delegated group's own protocol** — because per UHC's own guidance the
> delegate's rules govern, not UnitedHealthcare's.

---

### 2.6 AHCCCS (Arizona Medicaid) — included because plan type changes the answer

| Item | Finding |
|---|---|
| **Document** | **AHCCCS FFY26 Final Physician Fee Schedule**, sheet `FFY26 PFS 2026.09.10`, rate date **1 Oct 2025**. [Fee-For-Service Physician Fee Schedules](https://www.azahcccs.gov/PlansProviders/FeeForServiceHealthPlans/physicianrates.html) → *FY26_Final_PhysicianFeeSchedule.xlsx*. |
| **64772** | **Listed** — "TRANSECTION OR AVULSION OF OTHER SPINAL NERVE, EXTRADURAL." **$578.79** non-facility **and** facility (rate parity); lower tier **$405.15**. |
| **Contrast with Medicare** | AHCCCS publishes a **non-facility** rate for 64772; **Medicare does not** (`NA`). So the office is theoretically payable on AHCCCS but not on Medicare. |
| **64999** | **`BR` — by report.** Narrative required. |
| **64633 / 64635** | $439.67 / $443.51 non-facility; $197.70 facility. 64625: $476.28 / $202.23. |
| **Coverage caveat** | AHCCCS states expressly that "the appearance on this website of a code and rate is not an indication of coverage, nor a guarantee of payment." Coverage is established in the **AHCCCS Medical Policy Manual (AMPM)**, not the fee schedule. |
| **Plan-level PA** | AHCCCS contractor plans (incl. **Health Choice**, which AZ Blue administers) apply **their own** prior authorization. Rates questions: `FFSRates@azahcccs.gov`. |

> ⚠️ **Unverified gap.** I did not locate an AMPM section addressing 64772 or facet denervation. Fee-schedule
> presence is not coverage.

---

### 2.7 Summary matrix

| | Covered? | Prior auth | Vendor | Approved POS | Criteria published for 64772? |
|---|---|---|---|---|---|
| **Medicare — Noridian JF** | In principle (NCD 160.1), case-by-case | **None. Not required.** WISeR does not reach 64772 (Appendix A Table A2 = 64605/64610 only) | n/a | **ASC + HOPD only** — office not payable | **No** |
| **AZ Blue — Commercial** | Unlisted | **No eviCore precert** for facet codes; 64772 not on any list | eviCore (MA only) | Not published for 64772 | **No** |
| **AZ Blue — Med Advantage** | Unlisted | Facet codes **Y**; 64772 → AZ Blue internal UM | eviCore / OHNAZ / AZPC | Not published for 64772 | **No** |
| **Humana — MA & DSNP** | Unlisted | **Not required** (64772 absent from list); facet codes + 64999 **required** | **Cohere Health** | ASC/office/CAH may be exempt — verify per member | **No** |
| **UnitedHealthcare — Commercial/IE** | Unlisted; endoscopic rhizotomy & SI ablation **unproven** | Site-of-service review on thermal RFA | UHC internal (MP.12.22) | ASC only if MP.12.22 criteria met | **No** |
| **UHC — Medicare Advantage (AZ)** | Unlisted; defers to **L38801/A58403** and NCD 160.1 | Per UHCprovider.com/priorauth; **PCP referral** on HMO/HMO-POS | **Optum Health Networks** + delegates | Per LCD / delegate | **No** |
| **Optum (delegated)** | **Unverified** | **Unverified** | Optum / delegated IPA | **Unverified** | **Unverified** |
| **AHCCCS FFS** | On fee schedule ($578.79); coverage per AMPM | Contractor-specific | Plan-specific | Office **and** facility rates published | **No** |

**Not one payer reviewed publishes medical-necessity criteria for 64772.**

---

## Part 3 — Diagnosis and medical necessity

### 3.1 Does any payer publish a covered-dx list for 64772?

**No.** Specifically:

- **64772 does not appear in any LCD, LCA or NCD covered-diagnosis table I could find.** Verified absent
  from Noridian **L38801** and **A58403**. CMS's Medicare Coverage Database code-level search is a
  JavaScript application that returns no server-rendered results, so I could not run an exhaustive
  all-jurisdiction code query — **but** the Arizona-governing documents are confirmed clear, and the
  national policy that does cover the service (**NCD 160.1**) contains **no diagnosis table at all**.
- NCD 160.1 instead conditions payment on the MAC's **medical staff concurring** in "selected cases."
  **64772 is adjudicated case-by-case on the operative report, not against a dx list.**

### 3.2 The facet diagnoses will not carry over — and one of them is already invalid

**The Noridian covered-diagnosis list for facet interventions (A58403, Group 1) is, in full:**

`M47.812` `M47.813` `M47.814` `M47.815` `M47.816` `M47.817` · `M47.892` `M47.893` `M47.894` `M47.895`
`M47.896` `M47.897` · `M48.12` `M48.13` `M48.14` `M48.15` `M48.16` `M48.17` · `M53.82` `M53.83` `M53.84`
`M53.85` `M53.86` `M53.87`

`M53.8x` carries the footnote "**To be used for facet cyst injection/aspiration (not ablation)**."
The "ICD-10-CM Codes that DO NOT Support Medical Necessity" section is **N/A**.

Three findings, in order of urgency:

1. 🔴 **`M54.5` is not a billable code.** Validated against the **FY2026 ICD-10-CM** set: `M54.5`
   ("Low back pain") **exists but is a category header only and is not valid for HIPAA-covered
   transactions**. If it is on claims today it will reject as an invalid diagnosis. The billable children
   are **`M54.50`** (low back pain, unspecified), **`M54.51`** (vertebrogenic low back pain), **`M54.59`**
   (other low back pain). **This is a live problem independent of 64772 — worth checking the current claim
   file before the meeting.**
2. 🔴 **No `M54` code of any kind appears in the Noridian covered-dx list** — not `M54.50`, `M54.51`,
   `M54.59`, `M54.6`, `M54.2` or `M54.9`. `M54.6` ("Pain in thoracic spine") **is** a valid billable code,
   but it **will not support 64633–64636 in Jurisdiction F.** So the facet-dx exposure is bigger than the
   64772 question.
3. ⚠️ **`M47.81` (four characters) is also a non-billable header.** Only `M47.811`–`M47.819` are billable,
   and only `M47.812`–`M47.817` are on the covered list. `M47.811` (occipito-atlanto-axial),
   `M47.818` (sacral/sacrococcygeal) and `M47.819` (site unspecified) are **valid but not covered** for
   facet interventions in JF.

### 3.3 Which ICD-10 families would actually support 64772

If 64772 is genuinely being done on a **named peripheral or specific spinal nerve**, the diagnosis must
identify **that nerve and the underlying condition** — not a facet arthropathy. Candidate families
(all validated against FY2026):

| Family | Code | Description | Note |
|---|---|---|---|
| Other mononeuropathies | `G58` | Other mononeuropathies | ⚠️ **header — not billable** |
| | `G58.0` | Intercostal neuropathy | billable |
| | `G58.7` | Mononeuritis multiplex | billable |
| | `G58.8` | Other specified mononeuropathies | billable |
| | `G58.9` | Mononeuropathy, unspecified | billable |
| Lower-limb mononeuropathies | `G57.x` | e.g. sciatic, meralgia paraesthetica, tarsal tunnel — **requires laterality** | billable at full specificity |
| Neuralgia / neuritis | `M79.2` | Neuralgia and neuritis, unspecified | non-specific; weak on review |
| Post-surgical neuroma | see `G58.8`, plus injury-of-nerve (`S\*4\*`) and complication codes | — | pair with the causative history |

**Why the substitution matters.** Putting `M47.81x` or `M54.x` on a 64772 line creates a
**documentation contradiction on the face of the claim**: those codes describe facet-mediated axial
spine pain, which is precisely what 64633–64636 exist to treat. A facet diagnosis paired with an open
"other spinal nerve" transection code tells a reviewer the claim should have been the facet code. It is
the single most likely trigger for a records request, and then a recoupment.

### 3.4 Dx-to-CPT edits, and whether a narrative is needed regardless

- **There are no published dx-to-CPT edits for 64772** — because no LCD/LCA/NCD publishes a diagnosis
  table for it. This cuts both ways: there is no edit to fail, **and no published list to cite on appeal.**
  The operative report is the entire defence.
- **A narrative is effectively mandatory regardless of diagnosis**, for different reasons at each payer:
  - **64999** (the alternative code) is **`BR` — by report** at AHCCCS, **status `C`** (contractor-priced)
    at Medicare, and **PA-required** at Humana. All three require a narrative by rule.
  - **64772** is a valued code, so no fee-schedule rule compels a narrative — but because **no payer
    publishes criteria**, every payer will request the operative report on review. Submit the op note
    proactively with the first several claims rather than waiting for the request.

---

## Part 4 — Modifiers and other particularities

### 4.1 Anatomic site, laterality, and units

- **No payer reviewed publishes a laterality instruction for 64772.** Documentation must identify
  **the nerve, the level, and the side** in the operative report — this is the substitute for a
  published rule.
- **Modifier 50 buys nothing on Medicare.** 64772's **bilateral surgery indicator is `0`**: the 150%
  bilateral payment adjustment **does not apply**. Billed with modifier 50, or with RT and LT, payment is
  the **lower of the total actual charge for both sides or 100% of the fee schedule amount for a single
  code**. Bilateral 64772 pays essentially the same as unilateral.
- **This is exactly where Medicare and commercial diverge.** 64633, 64635, 64625, 64490 and 64493 all
  carry bilateral indicator **`1`** — 150% applies, modifier 50 is worth money. **64772 is the outlier in
  its own operating room.** Commercial payers frequently follow the MPFS indicator but are not bound to;
  none publishes a bilateral rule for 64772, so **get it in writing per payer** before booking bilateral cases.
- **Multiple units:** MUE **6**, MAI **3** — up to six units per date of service, and above six is
  appealable with documentation. Compare **64633 and 64635 at MUE 1 with MAI 2**: an **absolute** CMS
  policy limit that **no modifier and no appeal can exceed**. Practically: bilateral single-level facet RFA
  is **one unit with modifier 50**, never two lines — a second unit will deny and stay denied.
- **ASC bilateral reporting split (A58403):** for ASC-performed facet procedures the **physician** uses
  **modifier 50**, while the **ASC facility** reports the code on **two separate lines, one unit each,
  with RT and LT**. ⚠️ That instruction is written for 64490–64495. **There is no equivalent published
  instruction for 64772** — confirm with Noridian before the ASC bills its first case.

### 4.2 Same-session billing with 64633–64636

**Direct answer: there is no NCCI bundle between them, in either direction.** 64772 appears as Column 1 in
346 practitioner PTP edits and as Column 2 in **zero**, and **none** of those 346 pairs 64772 with 64633,
64634, 64635, 64636 or 64625 (NCCI v32.3, eff. 1 Oct 2026). So it is **not a hard bundle**, and no
modifier is needed to break an edit that does not exist.

That is not the same as "safe to bill together." Three things bite:

1. **Multiple-procedure reduction.** 64772 and 64633/64635 both carry **MULT PROC `2`** — standard
   100%/50% surgical reduction applies when reported in the same session.
2. **Audit exposure.** An **open nerve transection** and a **percutaneous facet RFA** in one session
   invites a records request, because the natural reading is that **one of the two is miscoded**. This
   risk is materially higher than the payment at stake.
3. **The global period swallows the follow-on.** See §4.5 — once 64772 is paid, the next 90 days are
   captured.

**What *is* a hard bundle with 64772** (modifier indicator `0`, unbreakable — see the table in §2.1):
**all facet blocks 64490–64495**, **all ESI codes 62320–62327**, and **all transforaminal ESI codes
64479/64480/64483/64484**. Operationally: **you cannot bill a same-day medial branch block or epidural
steroid injection with 64772 on any payer following NCCI.** That forecloses the common
"diagnostic block plus definitive procedure on one visit" pattern.

### 4.3 Assistant surgeon and co-surgeon

| | 64772 | 64633 / 64634 / 64635 / 64636 / 64625 |
|---|---|---|
| **Assistant at surgery** | **Indicator `2`** — **payable**, no supporting documentation required (modifiers 80/81/82, AS) | **Indicator `1`** — **statutory payment restriction; an assistant may NOT be paid** |
| **Co-surgeon** | **Indicator `1`** — **payable with supporting documentation** establishing the medical necessity of two surgeons (modifier 62) | **Indicator `0`** — **co-surgeons NOT permitted** |
| **Team surgeon** | `0` — not permitted | `0` — not permitted |

This is one of the few places 64772 is *more* permissive: it supports an assistant and a documented
co-surgeon where the facet codes support neither. ⚠️ **No commercial payer reviewed publishes an
assistant- or co-surgeon rule specific to 64772** — most follow the MPFS indicators, but confirm before
scheduling a two-surgeon case.

### 4.4 ASC vs HOPD — the scheduling determinant

| Code | On ASC covered list? | ASC indicator | ASC rate | HOPD APC | HOPD rate |
|---|---|---|---|---|---|
| **64772** | **Yes — Addendum AA** | **`A2`** (on ASC list in CY 2007; paid on OPPS weight) | **$948.66** | 5431 | **$1,765.76** |
| 64633 | Yes | `G2` (non office-based, added CY2008+) | $948.66 | 5431 | $1,765.76 |
| 64635 | Yes | `G2` | $948.66 | 5431 | $1,765.76 |
| 64625 | Yes | `G2` | $948.66 | 5431 | $1,765.76 |
| +64634 / +64636 | Yes | **`N1` — packaged, no separate payment** | — | — | — |
| **64999** | **No — Addendum EE, excluded from ASC payment** | — | **not payable in ASC** | — | — |

**Answers for scheduling:**

- **64772 can be booked at the ASC** on Medicare — it is on Addendum AA and separately payable.
- **The HOPD pays about 86% more than the ASC** for the same code ($1,765.76 vs $948.66) on the facility
  side. That is a site-of-service economics conversation, not a coverage one.
- **The office cannot be used on Medicare** — the physician side has no non-facility payment (`NA`).
- 🔴 **If the procedure is really 64999, the ASC is off the table entirely for Medicare** (Addendum EE).
  **This single fact may decide whether Deanna and Bri can book in-house or must send cases out**, and it
  turns on the code validation in Part 1. Resolve Part 1 before committing any ASC block time.
- **Commercial site-of-service review is a separate gate.** UHC **MP.12.22** subjects **64633 and 64635**
  to office-first review — the ASC is only medically necessary on one of the enumerated exceptions, and
  **"surgeon-preferred or proprietary instruments" is expressly excluded** as a reason. If the new
  equipment is the justification for the ASC, **UHC has pre-emptively rejected that argument.**

### 4.5 Post-operative global period — confirmed 90 days

**64772 carries a `090` global period** (PPRRVU2026: GLOB DAYS `090`; pre-op 0.11, intra-op 0.76,
post-op 0.13). What that bundles:

- The pre-operative visit on the day of or day before surgery.
- All intra-operative services that are a normal, necessary part of the procedure.
- **All typical post-operative care for 90 days** — follow-up visits, dressing changes, suture/staple
  removal, post-operative pain management by the surgeon, and related E/M.
- Complications **not** requiring a return to the operating room.

**The modifier consequences — this is the trap for the facet schedule:**

| Scenario inside the 90 days | Modifier |
|---|---|
| **Facet RFA (64633–64636) — unrelated to the 64772** | **`79`** — unrelated procedure by the same physician during the post-op period |
| Staged or related subsequent procedure | `58` |
| Return to the OR for a complication | `78` |
| Unrelated E/M visit | `24` |
| E/M on the day of surgery that led to the decision to operate | `57` (major surgery — **not** `25`) |

🔴 **Every patient who receives 64772 becomes a 90-day modifier-79 problem for the RFA schedule.**
Dr. Luke's facet population is exactly the group most likely to need an RFA inside that window. Today
this problem does not exist: **64633 and 64635 carry only a `010` global**, and the add-ons are `ZZZ`.
Adopting 64772 introduces a 90-day encumbrance that the current code set does not have — and a missing
modifier 79 means the RFA denies as included in the global.

### 4.6 Credentialing and specialty taxonomy

**NPPES verification — NPI 1437125846** ([NPPES registry](https://npiregistry.cms.hhs.gov/)):

| Field | Value |
|---|---|
| Name | **Timothy A Luke, M.D.** |
| Status | **Active** (enumerated 24 Feb 2006) |
| **Primary taxonomy** | **`207X00000X` — Orthopaedic Surgery** |
| Other taxonomies | **None on file — this is the only one** |
| License | **AZ 41183** |
| Primary practice | 8805 N 23rd Ave Ste 120, Phoenix, AZ 85021 · 602-265-8800 |
| Secondary location | 4860 E Baseline Rd Ste 103, Mesa, AZ 85206 |
| **Last NPPES update** | **20 January 2020** |

**Findings:**

- **No payer policy I reviewed restricts 64772 to a particular specialty taxonomy.** Neither the
  Noridian LCD/LCA, NCD 160.1, the UHC policies, the Humana PA list, nor the eviCore AZ Blue code list
  contains a specialty or taxonomy restriction for this code.
- ⚠️ **But three real credentialing risks follow from the record above:**
  1. **64772 is a facility-only open surgical code.** His payer contracts and privileging must cover
     **the facility where it is booked** — ASC credentialing and the specific procedure on his privilege
     list. An orthopaedic surgery taxonomy supports an open neurectomy well; it is the **site**
     credentialing, not the taxonomy, that will hold up scheduling.
  2. **Program scoping, not taxonomy, routes the review.** AZ Blue's eviCore MSK/interventional-pain
     program is **Medicare Advantage only**. The identical code, performed by the identical physician,
     routes to a different reviewer depending on the **member's plan type** — and for 64772, which is on
     no vendor list, to the health plan's internal UM. Expect inconsistent answers across members and
     document which entity gave each one.
  3. 🔴 **NPPES was last updated 20 January 2020.** If Dr. Luke has since added a pain-management, spine
     or interventional subspecialty taxonomy, **NPPES does not reflect it**, and payer credentialing
     files very likely do not either. An interventional-pain program built on an NPI that reads
     "Orthopaedic Surgery" alone invites specialty-edit denials at payers that do scope pain procedures
     by taxonomy. **Recommend refreshing NPPES and re-attesting with each payer before go-live.**

---

## Part 5 — What could delay scheduling or trigger a denial

For Deanna and Bri to raise in next week's meeting, highest impact first.

### Blockers — resolve before any case is booked

1. 🔴 **The code is very likely wrong.** If this is percutaneous medial branch rhizotomy, it is
   **64633–64636**. If it is open/endoscopic facet denervation, it is **64999**. 64772 fits neither
   unless the operative note documents open transection of a specifically named non-facet spinal nerve.
   Everything downstream depends on this. **Do not let auth or scheduling build workflow on 64772 until
   the operative technique is confirmed in writing.**
2. 🔴 **64999 cannot be paid in an ASC by Medicare** (Addendum EE). If Part 1 resolves to 64999, in-house
   ASC booking is dead for Medicare and cases must go to the HOPD. **This is the make-or-break scheduling fact.**
3. 🔴 **64772 has no office payment on Medicare** (`NA` non-facility PE). Office booking is unpayable —
   ASC or HOPD only.
4. 🔴 **No payer publishes medical-necessity criteria for 64772.** There is nothing to build a clean auth
   packet against and nothing to cite on appeal. Every claim is a medical-review claim decided on the
   operative report.

### Denial mechanics

5. 🔴 **Hard NCCI bundles, unbreakable by modifier:** 64772 + facet blocks **64490–64495**;
   64772 + **all** ESI codes **62320–62327**; 64772 + transforaminal **64479/64480/64483/64484**.
   All modifier indicator `0`. **No same-day diagnostic block or ESI with 64772, on any NCCI payer.**
6. 🔴 **`M54.5` is not a billable code** (FY2026 header). Check the current claim file — this may be
   generating rejections today, unrelated to 64772.
7. 🔴 **No `M54` code is on the Noridian covered-dx list for facet interventions.** `M54.6` is valid but
   not covered in JF. **The existing facet dx set needs an audit, not just a carry-over decision.**
8. 🔴 **90-day global on 64772** vs 10 days on 64633/64635. Any RFA inside the window needs **modifier 79**
   or it denies as global. Build this into the scheduling template now.
9. ⚠️ **Bilateral 64772 pays no premium** (bilateral indicator `0`). If the pro-forma assumes 150% for
   bilateral cases, it is overstated.
10. ⚠️ **64633/64635 are MUE 1 / MAI 2 — absolute.** Bilateral single-level = one unit with modifier 50.
    A second unit denies permanently, with no appeal.
11. ⚠️ **UHC has pre-empted the equipment argument for the ASC.** MP.12.22 expressly excludes
    "surgeon-preferred or proprietary instruments, instrument sets, and hardware sets" as grounds for
    ASC site-of-service. If the new equipment is the reason for the ASC, UHC will not accept it.
12. ⚠️ **UHC calls endoscopic rhizotomy "unproven and not medically necessary"** (2026T0107II), and
    eviCore CMM-208 says the same for the AZ Blue MA book. **If the technique is endoscopic, two of five
    payers deny it by written policy.** UHC also calls **SI joint ablation (64625) unproven** commercially.
13. ✅ **WISeR — cleared, no longer a risk.** Resolved 15 Sep 2026: the NCD 160.1 WISeR code set is
    **64605 and 64610 only** (trigeminal). 64772 is not in scope, so there is no voluntary-auth decision
    to make and no pre-payment review routing. Capture a dated Noridian PA Lookup screenshot for the file.
14. ⚠️ **AZ Blue commercial offers no pre-service approval** for these codes (eviCore precert `N`,
    MA only). There is no way to de-risk before the case; exposure is entirely post-service.
15. ⚠️ **UHC MA HMO/HMO-POS members delegated to Optum need a PCP referral before the specialist visit**,
    submitted by the PCP in advance, or the claim denies. That is a front-desk workflow item for the
    22 group numbers in §2.4.
16. ⚠️ **NPPES lists only Orthopaedic Surgery and was last updated in 2020.** Refresh before go-live.

### Open items — must be answered by a human, cannot be closed from published sources

| # | Question | Who to ask |
|---|---|---|
| ~~17~~ | ~~Is **64772** in the WISeR **NCD 160.1** code set for Arizona?~~ **CLOSED 15 Sep 2026 — No.** Operational Guide Appendix A Table A2 = 64605 and 64610 only. | — |
| 18 | Does **AZ Blue** require prior auth for 64772, and is there a medical policy for it? **Hard block — not retrievable here.** Their policy search is a JavaScript app that returns no server-rendered results; the PA code list (`edge.sitecorecloud.io`) and `provider.azblue.com` are both blocked by this environment's egress policy. Three access paths attempted, all failed. | [AZ Blue PA lookup](https://www.azblue.com/prior-authorization-lookup/providers) · `UtilMgmt@azblue.com` · **602-864-4320** · provider services **1-800-322-8670** |
| 19 | **Optum's Arizona PA code lists** — **hard block.** `www.optum.com` and `business.optum.com` are blocked by egress policy; `events.optumcare.com` does not resolve. Two further attempts after the first also failed. **No verified answer on Optum PA for 64772.** | Optum provider rep · Optum Pro portal `optumproportal.com` · **877-370-2845** (TTY 711) · `lcd_um@optum.com` |
| 20 | Each **delegated IPA's own protocol** — per UHC, "you must follow the delegate's protocols." | Each delegated group directly |
| 21 | **Humana** coverage policy for 64772, and whether the **commercial** book differs from MA/DSNP. Does Dr. Luke qualify for the 2026 **Gold Card**? | Humana provider rep · Cohere 833-283-0033 |
| 22 | **AHCCCS AMPM** coverage position on 64772 (fee-schedule presence is not coverage), plus Health Choice PA. | AHCCCS · `FFSRates@azahcccs.gov` |
| 23 | Is there an ASC facility bilateral-reporting instruction for **64772** (A58403's RT/LT split is written for 64490–64495 only)? | Noridian JF |

---

## Sources

**CMS — national data files**
- [PFS Relative Value Files](https://www.cms.gov/medicare/payment/fee-schedules/physician/pfs-relative-value-files) — *RVU26D* → `PPRRVU2026_Oct_nonQPP.csv`, eff. 1 Oct 2026 (global, bilateral, assistant, co-surgeon, facility indicators)
- [NCCI Procedure-to-Procedure Edits](https://www.cms.gov/medicare/coding-billing/national-correct-coding-initiative-ncci-edits/medicare-ncci-procedure-procedure-ptp-edits) — *Practitioner PTP Edits* `ccipra-v323r0` f1–f4, NCCI v32.3, eff. 1 Oct 2026
- [NCCI Medically Unlikely Edits](https://www.cms.gov/medicare/coding-billing/national-correct-coding-initiative-ncci-edits/medicare-ncci-medically-unlikely-edits) — `MCR_MUE_PractitionerServices_Eff_10-01-2026`
- [ASC Payment Rates Addenda](https://www.cms.gov/medicare/payment/prospective-payment-systems/ambulatory-surgical-center-asc/asc-payment-rates-addenda) — *July 2026 ASC Addenda*, sheets AA / DD1 / EE / FF, eff. 1 Jul 2026

**CMS — coverage**
- [NCD 160.1 Induced Lesions of Nerve Tracts](https://www.cms.gov/medicare-coverage-database/view/ncd.aspx?ncdid=19) — Pub. 100-3, longstanding
- [LCD L38801 Facet Joint Interventions for Pain Management](https://www.cms.gov/medicare-coverage-database/view/lcd.aspx?lcdid=38801&ver=23) — Noridian JF, rev. eff. 16 Apr 2026
- [LCA A58403 Billing and Coding: Facet Joint Interventions for Pain Management](https://www.cms.gov/medicare-coverage-database/view/article.aspx?articleid=58403&ver=27) — Noridian, rev. eff. 21 May 2026
- [LCD L39240 Epidural Steroid Injections for Pain Management](https://www.cms.gov/medicare-coverage-database/view/lcd.aspx?lcdid=39240) — Noridian JF
- [WISeR Model provider fact sheet](https://www.cms.gov/priorities/innovation/files/wiser-provider-fact-sheet.pdf) · [Noridian JF Part B WISeR page](https://med.noridianmedicare.com/web/jfb/cert-reviews/pre-claim/wiser-model)

**UnitedHealthcare**
- [Ablative Treatment for Spinal Pain, 2026T0107II](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/ablative-treatment-spinal-pain.pdf) — eff. 1 Feb 2026
- [Facet Joint and Medial Branch Block Injections for Spinal Pain, 2026T0004WW](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/facet-joint-injections-spinal-pain.pdf) — eff. 10 Sep 2026
- [Office-Based Procedures – Site of Service, MP.12.22](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/office-based-procedures-site-service.pdf) — eff. 1 Jul 2026
- [Outpatient Surgical Procedures – Site of Service, MP.11.27](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/outpatient-surg-procedures-site-service.pdf) — eff. 1 Aug 2026
- [Pain Management, MMP070.12 (Medicare Advantage)](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/medadv-mp/pain-management-rehabilitation.pdf) — eff. 1 Sep 2026
- [MA Arizona / Optum Health Networks QRG, PCA-4-26-00582-M&R-QRG_05132026](https://www.uhcprovider.com/content/dam/provider/docs/public/health-plans/medicare/2026/qrg/2026-MED-ADV-QRG-Optum-Care-Arizona.pdf) — eff. 1 Jan 2026

**AZ Blue / eviCore**
- [eviCore — Blue Cross Blue Shield of Arizona programs](https://www.evicore.com/resources/healthplan/blue-cross-blue-shield/arizona)
- [BCBSAZ MSK code list, eff. 1 Jan 2026](https://www.evicore.com/sites/default/files/resources/2025-12/BCBSAZ_MSK_CodeList_Eff01.01.26_Pub12.12.2025.pdf)
- [eviCore CMM-208 Ablations/Denervations of Facet Joints and Peripheral Nerves, V1.0.2025](https://www.evicore.com/sites/default/files/clinical-guidelines/2025-02/EviCore_CMM-208%20Ablat%20Denerv%20Nerves_Final_V1.0.2025_Pub02.28.2025.pdf)
- [AZ Blue Prior Authorization & Medical Policies](https://www.azblue.com/provider/resources/prior-authorization-and-medical-policies) · [PA lookup](https://www.azblue.com/prior-authorization-lookup/providers)

**Humana**
- [Medicare Advantage & DSNP Prior Authorization and Notification List, eff. 1 Jan 2026](https://assets.humana.com/is/content/humana/FINAL_Medicare%20and%20DSNP%20Prior%20Authorization%20and%20Notification%20List%20-%201-1-2026pdf)
- [Humana prior authorizations](https://provider.humana.com/coverage-claims/prior-authorizations) · [Cohere Health](https://www.coherehealth.com/news/modernize-prior-authorizations-musculoskeletal-treatment-humana)

**AHCCCS**
- [Fee-For-Service Physician Fee Schedules](https://www.azahcccs.gov/PlansProviders/FeeForServiceHealthPlans/physicianrates.html) — `FY26_Final_PhysicianFeeSchedule.xlsx`, sheet `FFY26 PFS 2026.09.10`, rates eff. 1 Oct 2025

**Coding references and registries**
- [NPPES NPI Registry](https://npiregistry.cms.hhs.gov/) — NPI 1437125846
- ICD-10-CM FY2026 code set (validity of `M54.5`, `M54.6`, `M47.81x`, `G58.x`)
- [KZA — Nerve Transection CPT 64772, 5 Mar 2026](https://www.kzanow.com/coding-coaches/nerve-transection-cpt-64772-03-05-26) (AIN/PIN neurectomy; MUE raised 2→6 Jan 2026)
- [AAPC — CPT 64772](https://www.aapc.com/codes/cpt-codes/64772) · [AAPC forum: 64772 vs 64635](https://www.aapc.com/discuss/threads/cpt-code-64772-or-64635-help-please.189179/) · [AAPC forum: endoscopic rhizotomy coding](https://www.aapc.com/discuss/threads/endoscopic-rhizotomy-compare-to-code.180883/)

---

*Payer policies change and effective dates in this memo are as-published on 15 September 2026. Items marked
⚠️ or listed in §5 Open Items are **not** verified from a published source and must be confirmed with the
payer before they are relied on for scheduling or billing.*
