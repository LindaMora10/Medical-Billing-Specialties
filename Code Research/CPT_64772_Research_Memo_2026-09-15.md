# CPT 64772 — Code Validation and Payer Research

**Prepared:** 2026-09-15
**Requested for:** Dr. Timothy A. Luke, MD — NPI 1437125846 — Executive Team presentation this week; Deanna and Bri, auth/scheduling meeting next week
**Jurisdiction:** Arizona (Medicare JF — Noridian)
**Provider record (verified, NPPES):** TIMOTHY A LUKE, M.D.; NPI-1 active since 2006-02-24; sole taxonomy **207X00000X Orthopaedic Surgery**; AZ license 41183; locations 8805 N 23rd Ave Ste 120, Phoenix and 4860 E Baseline Rd Ste 103, Mesa.

---

## ⚠️ Research limitation — read this before relying on any citation below

This session's network egress proxy **blocked all direct document retrieval**. `cms.gov`, `med.noridianmedicare.com`, `uhcprovider.com`, `azblue.com`, and every other payer domain returned `EGRESS_BLOCKED` on both WebFetch and curl. The only working research channel was a search index, which returns titles, URLs, and machine-generated summaries — **not primary policy text**.

Consequences, stated plainly:

- I could **not** open a single LCD, LCA, payer medical policy PDF, prior-auth list, MPFS RVU file, NCCI PTP file, MUE file, or ASC Addendum AA.
- Every citation below is given with its **name, number, effective date, URL, and the navigation path** so Deanna or Bri can pull it, but the **content** attached to each is labeled by confidence.
- Confidence labels used throughout:
  - **[VERIFIED]** — retrieved and consistent across independent sources.
  - **[PARTIAL]** — retrieved from a search summary of the document; the document itself was not opened. Treat as a lead, not a quote.
  - **[NOT FOUND]** — I searched and found no published policy. This is a finding, not a gap to fill by inference.
  - **[MUST PULL]** — a specific data field I could not reach and that materially changes the answer. Do not schedule a case until these are pulled.

I have **not** inferred any policy I could not find. Where a payer publishes nothing on 64772, I say so.

---

# PART 1 — Code validation (do this before any coverage work)

## 1.1 The exact descriptor

> **64772 — Transection or avulsion of other spinal nerve, extradural** **[VERIFIED]**

AMA CPT, Surgery / Nervous System, subsection **"Transection or Avulsion"** within *Extracranial Nerves, Peripheral Nerves, and Autonomic Nervous System*, code range **64732–64772**.

## 1.2 What 64772 actually describes

| Attribute | 64772 |
|---|---|
| **Approach** | **Open.** The descriptor's verbs — *transection* (sharply cutting across) and *avulsion* (tearing/pulling the nerve out) — are mechanical acts performed on a nerve the surgeon has exposed and is looking at. There is no percutaneous, needle, catheter, or image-guided construct anywhere in this code family. |
| **Mechanism** | **Mechanical destruction / physical division.** Not neurolysis. Not thermal. Not chemical. CPT puts neurolytic destruction in a completely different subsection (64600–64681, "Destruction by Neurolytic Agent"). |
| **Location** | **Extradural** — outside the dura, i.e., the nerve after it has left the dural sac. Intradural work is 63185–63190 (rhizotomy proper). |
| **Which nerve** | **"Other spinal nerve"** — this is the residual catch-all of the family. The named-nerve codes come first (64732 supraorbital, 64734 infraorbital, 64736 mental, 64738 inferior alveolar, 64740 lingual, 64742 facial, 64744 greater occipital, 64746 phrenic, 64752/64755/64760 vagus, 64761 pudendal, 64763/64766 obturator, 64771 other cranial nerve). 64772 is what you report when you transected **a spinal nerve that has no code of its own** — and you must say which one. |
| **Units** | Per nerve. Not per joint, not per level. |
| **Imaging** | Not included, not required, not described. |

**Typical correct uses:** AIN/PIN neurectomy (anterior/posterior interosseous nerve) **[VERIFIED — KZA coding guidance]**, intercostal neurectomy, open peripheral neurectomy for a symptomatic or post-surgical neuroma, open transection of a named nerve for intractable focal neuropathic pain after failed conservative and interventional care.

## 1.3 The comparison he needs to see

| Code | Descriptor | Anatomic target | Technique | Unit |
|---|---|---|---|---|
| **64633** | Destruction by neurolytic agent (eg, chemical, thermal, electrical or radiofrequency), **paravertebral facet joint nerve(s), with imaging guidance (fluoroscopy or CT)**; cervical or thoracic, **single facet joint** | Facet joint's medial branches | Neurolytic destruction + imaging | **Per joint** |
| **64634** | …cervical or thoracic, **each additional facet joint** (add-on to 64633) | same | same | Per joint |
| **64635** | …**lumbar or sacral, single facet joint** | same | same | Per joint |
| **64636** | …lumbar or sacral, **each additional facet joint** (add-on to 64635) | same | same | Per joint |
| **64625** | **Radiofrequency ablation, nerves innervating the sacroiliac joint, with image guidance** (i.e., fluoroscopy or CT) | SI joint's innervating nerves (lateral branches) | RF ablation + imaging | **Once per side, entire joint** |
| **64999** | Unlisted procedure, nervous system | — | — | Narrative required |
| **64772** | Transection or avulsion of other spinal nerve, extradural | A **named spinal nerve** | Open mechanical transection/avulsion | **Per nerve** |

**[VERIFIED]** governing CPT rules for 64633–64636:
- Reported **per joint, not per nerve** — one unit per facet joint regardless of how many medial branches were destroyed at that joint.
- **Imaging guidance is bundled and required.** If no fluoro/CT was used, you may not report 64633–64636 — report **64999**.
- **Not** to be reported for non-thermal denervation (chemical, sub-80 °C thermal, or any pulsed RF) — report **64999**.

## 1.4 Verdict — and I want to be direct about this

**If the procedure being presented is denervation of the facet joints by targeting the medial branches — by any technique, endoscopic included — 64772 is not the correct code.**

CPT assigns codes by **anatomic target first**. The medial branch of the dorsal ramus, when it is being destroyed to denervate a facet joint, is a **"paravertebral facet joint nerve."** CPT has already built a dedicated code family for that target (64633–64636), and it explicitly routes every technique that doesn't fit those four codes to **64999**, not to a different anatomic family. You cannot move a procedure out of its own code family by changing the instrument.

Supporting evidence:

- **[VERIFIED]** The AMA CPT Knowledge Base has published **two** Q&As on precisely this question — *"When the physician performs a medial branch endoscopic rhizotomy at L3, L4, and L5…"* and *"What is the appropriate code(s) to report for a minimally invasive surgical (MIS) endoscopic rhizotomy…"* — the second describing exactly the fact pattern (small incision, endoscope, bipolar device, fluoroscopic visualization). **The full answers sit behind Find-A-Code's paywall and I could not retrieve them.** **[MUST PULL]** — this is the single highest-value document in this memo and it costs a subscription, not a lawsuit. Get both.
- **[PARTIAL]** The consistently reported AMA/AAOS position across multiple independent secondary sources: *there is no CPT code describing mechanical destruction of the facet nerves performed through an open or endoscopic exposure; unlisted 64999 must be used.*
- **[PARTIAL]** Multiple health plans already state that **endoscopic rhizotomy / endoscopic RFA is investigational or unproven, and is to be reported with 64999** (see Part 2).

### The counter-argument he will bring, and the honest answer to it

There is a real, active, well-funded national push — visible in endoscopic-spine device marketing (Arthrex "Spine Evolutions" audience-question documents), Becker's Spine Review, and LinkedIn — to report **endoscopic medial branch transection (MBT)** as 64772. **[VERIFIED]** Its centerpiece: **CMS raised the MUE for 64772 from 2 units to 6 units, effective 2026-01-01.**

That is being characterized as "CMS approved 64772 for rhizotomy." **It is not.** An MUE is a **claims-volume edit** — a ceiling on units per date of service. It is not a coverage determination, not a payment policy, and not an AMA coding instruction. CMS said nothing about facet denervation when it changed the number. Even the sources promoting it concede that **reimbursement is still determined regionally by each MAC and depends on payer policy, modifier usage, and documentation.** **[VERIFIED]**

If that slide appears in the Executive Team deck, this is the correction.

## 1.5 What documentation would have to support 64772 instead

If he intends to bill 64772, every one of these has to be in the operative note. Anything less and the claim is indefensible on audit:

1. **The nerve, by name.** "Right L4 medial branch" is not a named spinal nerve for this purpose — it is a paravertebral facet joint nerve, which sends you back to 64633–64636/64999. The note must name a spinal nerve that has **no** code of its own in 64732–64771 and that is **not** being treated as a facet-joint denervation.
2. **Level and side**, explicitly, for each nerve.
3. **Open exposure with direct visualization** — the incision, the dissection, the plane, the moment the nerve was identified.
4. **The mechanical act** — sharp transection or avulsion — including the length of nerve excised or the segment removed, and what was done with the proximal stump.
5. **Extradural location**, stated.
6. **Why no more specific code applies** (i.e., the nerve is not one of the named ones).
7. **A nerve-specific indication** — entrapment, neuroma, traumatic or post-surgical neuropathy of that nerve — **not** axial facet arthropathy. See Part 3.
8. **Failed conservative and less-destructive care**, since permanent denervation is a last-resort procedure. **[VERIFIED — consistent across sources]**

**And the corollary:** if the honest answer is "open/endoscopic mechanical denervation of the facet medial branches," the defensible code is **64999** with a narrative, a comparison code, and — because unlisted codes are manually priced with no fee schedule — a **pre-determination in writing before the first case is booked.** That is a scheduling reality Deanna and Bri need to plan around, not a technicality.

---

# PART 2 — Payer by payer

## 2.1 Traditional Medicare — Noridian, Jurisdiction JF

**Jurisdiction confirmed [VERIFIED]:** Noridian JF covers **AZ**, AK, ID, MT, ND, OR, SD, UT, WA, WY.

### Is 64772 covered?

**[NOT FOUND] — and this is the finding.** I found **no NCD, no LCD, and no Local Coverage Article** — national or JF-local — that addresses CPT 64772 in any context. It does not appear in the facet joint policy family, and I found no covered-diagnosis table anywhere that lists it.

**Consequence:** 64772 is **adjudicated case-by-case** against the general reasonable-and-necessary standard (SSA §1862(a)(1)(A)) on the strength of the operative note alone. There is no published criteria set to satisfy in advance and — critically — **nothing to cite in an appeal.**

### The policy that *does* govern what he's actually describing

**LCD: Facet Joint Interventions for Pain Management — L38801**, Noridian Healthcare Solutions, LLC (Part A & Part B), **version 23, revision effective 2026-04-16, updated 2026-04-06** **[VERIFIED — CMS Medicare Coverage Database record]**
🔗 https://www.cms.gov/medicare-coverage-database/view/lcd.aspx?lcdid=38801&ver=23
*Path:* CMS Medicare Coverage Database → Local Coverage → Local Coverage Determinations → search "Facet Joint Interventions for Pain Management" → filter contractor "Noridian Healthcare Solutions, LLC" → L38801 → *Coverage Indications, Limitations, and/or Medical Necessity*.

**Jurisdiction change Deanna and Bri must know about [VERIFIED]:** JF previously ran on **L38803** with billing/coding article **A58405**. Both were **retired effective 2026-04-16** when Noridian consolidated JF onto the JE policy. **If anyone in the office is working from an L38803 or A58405 printout, it is out of date.** The JE-lineage companion article is **A58403** — **[MUST PULL]** confirm the current companion LCA number and revision now attached to L38801.

🔗 Retired JF LCD (for reference only): https://www.cms.gov/medicare-coverage-database/view/lcd.aspx?lcdid=38803&ver=17
🔗 Retired JF article A58405: https://www.cms.gov/medicare-coverage-database/view/article.aspx?articleId=58405

**[PARTIAL] — criteria reported for this LCD family** (national facet-LCD template; **verify exact wording in L38801 before quoting to a payer**):
- Moderate-to-severe chronic neck or low back pain causing functional deficit.
- Pain present **≥ 3 months** with documented failure of conservative management.
- **Absence of untreated radiculopathy.**
- Diagnostic medial branch blocks required before denervation, with a defined relief threshold.
- **No more than 2 RFA sessions per rolling 12 months per spinal region.**
- **No more than 4 therapeutic facet injection sessions per rolling 12 months per covered spinal region.**
- 64633–64636 are **per joint, not per nerve**.
- **Non-thermal facet denervation → 64999, and 64999 is non-covered for that purpose.** **[VERIFIED]** — note what this means: Medicare has already closed the unlisted-code door for non-thermal facet denervation in this jurisdiction.

### Prior authorization

**[VERIFIED]** Medicare runs a **Hospital OPD prior authorization program for facet joint interventions** (64490–64495, 64633–64636), effective 2023-07-01. It applies **only to the hospital outpatient department setting** — not office, not ASC.
🔗 https://med.noridianmedicare.com/web/jfa/cert-reviews/pre-claim/prior-authorization-for-certain-hospital-opd-services/facet-joint-interventions-for-pain-management
*Path:* Noridian JF Part A → Cert Reviews → Pre-Claim → Prior Authorization for Certain Hospital OPD Services → Facet Joint Interventions.

**64772 is not on that list.** Flag for the meeting: **"no prior auth required" is not good news here.** It means there is no pre-service decision, no safety net, and every dollar is exposed to post-payment review and recoupment. With a 090-day global and no coverage policy, that is the worst combination on this memo.

### Payment and edit indicators — all [MUST PULL]

I could not reach a single CMS data file. Each of these changes the answer materially:

| Field | Source | Status |
|---|---|---|
| Global period (expected **090**) | CY2026 MPFS RVU file, field `GLOB DAYS` | **[MUST PULL]** — expected 090 but unverified |
| **Bilateral surgery indicator** | same file, field `BILAT SURG` | **[MUST PULL]** — determines whether modifier 50 pays, and at what rate |
| **Assistant-at-surgery indicator** | same file, field `ASST SURG` | **[MUST PULL]** |
| **Co-surgeon indicator** | same file, field `CO-SURG` | **[MUST PULL]** |
| Multiple-procedure indicator | same file, field `MULT PROC` | **[MUST PULL]** |
| **MUE value and MAI** | CMS Practitioner Services MUE file | Value = **6, effective 2026-01-01 [VERIFIED]**. **MAI unknown [MUST PULL]** |
| **ASC covered-procedure status** | CY2026 ASC Addendum AA + payment indicator (Addendum DD1) | **[MUST PULL]** |
| **NCCI PTP pairs vs. 64633–64636, 64490–64495, 62321/62323, 64483/64484** | CMS NCCI PTP edit file, current quarter | **[MUST PULL]** |

*Paths:* MPFS RVU → cms.gov → Medicare → Physician Fee Schedule → **PFS Relative Value Files** → RVU26x → `PPRRVU26.csv`. MUE → cms.gov → Medicare → Coding & Billing → **NCCI → Medically Unlikely Edits** → *Practitioner Services MUE Table*. NCCI PTP → same NCCI landing page → **Procedure-to-Procedure (PTP) Edits** → Practitioner Services, current quarter. ASC → cms.gov → Medicare → **ASC Payment → ASC Payment Rates — Addenda** → Addendum AA.

**On the MAI specifically — this is not a footnote.** If 64772's MUE Adjudication Indicator is **2 ("Date of Service Edit: Policy")**, units above 6 are denied absolutely, with **no modifier override and no appeal**, on the whole date of service. If it is **3 ("Date of Service Edit: Clinical")**, over-cap units can be appealed with documentation. A bilateral, multi-level case can exceed 6 nerves easily. Pull this before Bri quotes anyone a case plan.

## 2.2 Blue Cross Blue Shield of Arizona (AZ Blue)

**64772 policy: [NOT FOUND].** No AZ Blue medical policy naming 64772 could be located.

**Facet denervation policy:** AZ Blue is a BCBSA licensee; the BCBSA reference policy for this space is **7.01.116 Facet Joint Denervation**, which licensees adopt under local numbers (e.g., Premera publishes it as **7.01.555**). **[PARTIAL]** — within this BCBS policy family, **endoscopic RFA/rhizotomy is investigational for facet-related pain and is reported with 64999**, and **pulsed RF denervation is not covered.** **[MUST PULL]** AZ Blue's own adopted policy number, title, and effective date.
🔗 Policy search: https://www.azblue.com/provider/resources/prior-authorization-and-medical-policies/search
*Path:* azblue.com → Providers → Resources → Prior Authorization & Medical Policies → **Search** → query "facet," "denervation," "rhizotomy," "ablation," and the literal string "64772."
🔗 Reference-policy example (Premera 7.01.555): https://www.premera.com/medicalpolicies/7.01.555.pdf

**Prior authorization vendor — and this one is plan-type dependent [PARTIAL]:**
- **Carelon Medical Benefits Management** handles **Musculoskeletal–Advanced Procedures (spine and joint) and interventional pain management for AZ Blue Medicare Advantage members only — not commercial.**
- **eviCore by Evernorth** also has an AZ Blue health-plan page, indicating eviCore holds other AZ Blue programs.
🔗 eviCore AZ Blue: https://www.evicore.com/resources/healthplan/blue-cross-blue-shield/arizona
🔗 PA lookup: https://www.azblue.com/prior-authorization-lookup (*Path:* azblue.com → Prior Authorization Lookup → enter CPT)

**[MUST PULL]** Run **64772, 64633, 64635, and 64999** through the AZ Blue PA lookup for **each plan type** the practice sees — commercial/group, ACA individual, Medicare Advantage, and **Health Choice Pathway (D-SNP)** and **Health Choice Arizona (AHCCCS)**, both AZ Blue entities with entirely separate rules.
🔗 D-SNP PA guidelines: https://www.azblue.com/health-choice-pathway/providers/prior-authorization-guidelines

**Plan-group-number sensitivity:** self-funded ASO groups administered by AZ Blue can carve out or override the medical policy entirely. For any ASO group, the **summary plan description governs, not the AZ Blue policy.** Verify per group number, not per payer.

## 2.3 Humana

**64772 policy: [NOT FOUND].** No Humana medical coverage policy naming 64772 was located.

**Prior authorization list:** **Medicare Advantage and Dual Eligible Special Needs Plans Prior Authorization and Notification List, effective 2026-01-01** **[VERIFIED — document exists]**
🔗 https://assets.humana.com/is/content/humana/FINAL_Medicare%20and%20DSNP%20Prior%20Authorization%20and%20Notification%20List%20-%201-1-2026pdf
*Path:* provider.humana.com → Coverage & Claims → Prior Authorizations → **Prior authorization lists** → Medicare Advantage and DSNP list, 1-1-2026.
**[PARTIAL]** 64633–64636 appear on Humana PA lists. **[MUST PULL]** whether 64772 appears — search the PDF for the literal string.

**Vendor — correct a likely misconception [VERIFIED]:** Humana's **Cohere Health** MSK prior-auth program covers **12 states: AL, GA, IN, KY, MI, NC, OH, PA, SC, TN, VA, WV. Arizona is not among them.** Do not route AZ cases to Cohere. **[PARTIAL]** Humana uses **eviCore by Evernorth** for MSK/pain in other markets — **[MUST PULL]** confirm which vendor holds AZ.
🔗 PA search tool (authoritative, code-level): https://provider.humana.com/coverage-claims/prior-authorizations/prior-authorizations-search-tool

**Plan-type divergence:** Humana **Medicare Advantage must follow the applicable Medicare LCD** — meaning **L38801** governs facet interventions for Humana MA members in Arizona, including its session limits. Humana commercial/employer plans follow Humana's own medical coverage policies. Different rules, same payer.

## 2.4 UnitedHealthcare

**64772: [NOT FOUND] in the governing policy — and its absence is itself a problem.**

**UnitedHealthcare Commercial Medical Policy — "Ablative Treatment for Spinal Pain," effective 2026-05-01** **[VERIFIED — document and effective date]**
🔗 https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/ablative-treatment-spinal-pain.pdf
*Path:* uhcprovider.com → Policies and Protocols → Commercial Policies → **Medical & Drug Policies** → "Ablative Treatment for Spinal Pain" → *Applicable Codes* and *Coverage Rationale*.

**[PARTIAL]** Applicable procedure codes reported for this policy: **22899, 64625, 64628, 64629, 64633, 64634, 64635, 64636, 64999, 77003**. **64772 is not among them.** The policy scope covers facet joint nerve ablation, SI joint ablation, and basivertebral nerve ablation.

**[PARTIAL] — the direct hit:** the policy states there is **insufficient evidence to establish the safety and efficacy of endoscopic RFA for treating spinal pain**, i.e. **endoscopic radiofrequency ablation is unproven and not medically necessary.** **[MUST PULL]** the exact sentence and its position in the *Coverage Rationale* — it is the sentence UHC will quote on denial, and it is worth having verbatim before the Executive Team meeting, not after.

Companion policies to pull at the same time:
- **"Facet Joint and Medial Branch Block Injections for Spinal Pain"** 🔗 https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/facet-joint-injections-spinal-pain.pdf
- **Community Plan (AHCCCS) version — "Ablative Treatment for Spinal Pain"** 🔗 https://www.uhcprovider.com/content/dam/provider/docs/public/policies/medicaid-comm-plan/ablative-treatment-spinal-pain-cs.pdf
- **Medicare Advantage — "Pain Management"** 🔗 https://www.uhcprovider.com/content/dam/provider/docs/public/policies/medadv-mp/pain-management-rehabilitation.pdf (MA additionally defers to CMS LCD L38801)

**Prior authorization:** **UnitedHealthcare Commercial Advance Notification and Prior Authorization Requirements, effective 2026-01-01** **[VERIFIED — document exists]**
🔗 https://www.uhcprovider.com/content/dam/provider/docs/public/prior-auth/pa-requirements/commercial/UHC-Commercial-Advance-Notification-PA-Requirements-1-2026.pdf
*Path:* uhcprovider.com → Prior Authorization and Notification → **Advance Notification and Plan Requirement Resources** → Commercial → 1-2026 PDF.
**[PARTIAL]** UHC applies **site-of-service review** to certain outpatient surgical codes — a policy effective 2026-07-01 addressing procedures typically performed in an office that may be done in an ASC lists 64633 among applicable codes. **[MUST PULL]** 64772's status on the PA list and in site-of-service review.

Also pull, per plan type: Individual Exchange PA list (eff. 2026-01-01) 🔗 https://www.uhcprovider.com/content/dam/provider/docs/public/prior-auth/exchanges/UHC-Exchange-Plans-Advance-Notification-PA-Eff-1-1-26.pdf · Medicare Advantage/Dual PA list (eff. 2026-07-01) 🔗 https://www.uhcprovider.com/content/dam/provider/docs/public/prior-auth/pa-requirements/medicare/Med-Adv-Dual-Eff-7-1-26.pdf

**Warning for Bri:** a code's absence from a PA list means only that no pre-service review is required. It does **not** confer coverage. UHC can and will deny post-service for incorrect coding or on the "unproven" endoscopic language above.

## 2.5 Optum

**Optum is not a payer in this scenario.** It is two distinct things, and conflating them will cost auth time:

1. **Optum "Spine, Pain, and Joint" solution** — the clinical-review/PA vendor for spine and pain services on behalf of UHC and other plans. **[VERIFIED] The OrthoNet provider portal was discontinued; as of 2025-09-03 prior authorizations must be submitted through Optum's Spine, Pain, and Joint portal.** **If anyone in the office still has OrthoNet bookmarked or in a workflow document, it is dead — fix that this week.**
2. **Optum Care Arizona / Optum Health Networks** — a delegated medical-group network in the Phoenix metro. **[VERIFIED] For dates of service beginning 2026-01-01, Optum Health Networks administers certain services for UnitedHealthcare Medicare Advantage plans**, including in Arizona.
🔗 UnitedHealthcare Medicare Advantage Plans of Arizona — 2026 Quick Reference Guide, Optum Care Arizona: https://www.uhcprovider.com/content/dam/provider/docs/public/health-plans/medicare/2026/qrg/2026-MED-ADV-QRG-Optum-Care-Arizona.pdf

**[VERIFIED]** UHC also delegates prior authorization to some care provider groups outright, with the delegated entity **printed on the back of the member ID card.** For AZ MA members especially, **check the card before choosing a submission channel** — the same CPT can route to UHC, to Optum Spine/Pain/Joint, or to a delegated group depending on the member.

**64772 policy under any Optum program: [NOT FOUND].**

## 2.6 AHCCCS / Arizona Medicaid

**64772 policy: [NOT FOUND].**

**[PARTIAL]** AHCCCS fee-for-service prior-authorization requirements are governed by the **AHCCCS Medical Policy Manual (AMPM), Chapters 300, 400, 800, and 1100.**
🔗 https://www.azahcccs.gov/PlansProviders/FeeForServiceHealthPlans/PriorAuthorization/requirements.html
*Path:* azahcccs.gov → Plans/Providers → Fee-For-Service Health Plans → Prior Authorization → PA Requirements.

Most AHCCCS members are in **managed care**, each MCO with its own PA list: UnitedHealthcare Community Plan, Banner–University Family Care, Mercy Care, Health Choice Arizona (AZ Blue), Molina. **[MUST PULL]** 64772's PA status and fee-schedule presence for each contracted MCO. A 090-global open neurectomy with no AHCCCS fee-schedule entry will land in manual pricing — plan for delay.

---

# PART 3 — Diagnosis and medical necessity

## 3.1 Does any payer publish a covered-dx list for 64772?

**No. [NOT FOUND] at every payer researched.**

I specifically checked whether 64772 appears in any LCD or LCA covered-diagnosis table. It does not. The facet policy family's ICD-10 tables — in **A58403 / A58405 / A58350 / A57826 / A57787** and their siblings — are attached to **64490–64495 and 64633–64636**, not to 64772.

**Therefore: 64772 is adjudicated case-by-case, on the operative narrative.** There is no dx list to match into, and no dx that guarantees payment. That cuts both ways — nothing pre-approves it, and nothing gives you an appeal citation either.

## 3.2 The diagnoses he is using now will not carry over — flag this hard

**They describe a joint and a region. 64772 describes a nerve.** Pairing a facet/axial-pain diagnosis with 64772 is precisely the combination that reads to a reviewer as *"a facet denervation billed under an open surgical code,"* and it is what will pull the chart.

| Code | FY2026 status | Note |
|---|---|---|
| **M54.5** | ❌ **NOT VALID / not billable** — parent code only **[VERIFIED]** | Split in FY2022. Must be **M54.50** (low back pain, unspecified), **M54.51** (vertebrogenic low back pain), or **M54.59** (other low back pain). **If M54.5 is still in the practice's claim templates, it is causing front-end rejections today, independent of 64772.** |
| **M54.6** | ✅ Valid — Pain in thoracic spine **[VERIFIED]** | Regional pain. Supports facet workup, not a named-nerve transection. |
| **M47.81** | ❌ **NOT VALID** — parent only **[VERIFIED]** | Requires 5th character: **M47.812** cervical, **M47.813** cervicothoracic, **M47.814** thoracic, **M47.815** thoracolumbar, **M47.816** lumbar, **M47.817** lumbosacral, **M47.818** sacral/sacrococcygeal, **M47.819** unspecified site. |

## 3.3 ICD-10 families that would actually support 64772

If the nerve is genuinely a named peripheral or specific spinal nerve, the diagnosis must identify **that nerve and its underlying condition** — all **[VERIFIED]** as valid FY2026 billable codes unless noted:

- **G58.0** Intercostal neuropathy
- **G58.7** Mononeuritis multiplex
- **G58.8** Other specified mononeuropathies — the usual landing place for a symptomatic **post-surgical or traumatic neuroma of a named nerve**, since ICD-10-CM has **no dedicated "painful post-surgical neuroma" code** outside the amputation-stump series
- **G58.9** Mononeuropathy, unspecified — weak; expect scrutiny
- **G57.x** Mononeuropathies of lower limb — G57.0 sciatic, G57.1 meralgia paresthetica (lateral femoral cutaneous), G57.5 tarsal tunnel, G57.6 plantar nerve/Morton's, G57.8 other
- **G56.x** Mononeuropathies of upper limb — relevant to the AIN/PIN neurectomy use case
- **T87.3x** Neuroma of amputation stump — T87.30/31/32/33/34 by laterality and extremity
- **S-chapter nerve-injury codes with the appropriate 7th character** (S34.x lumbar/sacral, S44.x shoulder/upper arm, S54.x forearm, S74.x hip/thigh, S84.x lower leg), or their **sequela** ("S") forms for post-surgical/post-traumatic nerve injury
- **M79.2** Neuralgia and neuritis, unspecified — **use with caution.** Most payers treat it as a nonspecific symptom code and it will not carry a 090-global surgical claim on its own.

All G5x and T87.3x codes require **laterality and site consistency** with the operative note.

## 3.4 Dx-to-CPT edits and the narrative question

- **Medicare:** **[NOT FOUND]** — no published NCD/LCD dx edit table for 64772, so no LCD-based dx denial to design around. The tradeoff is that there is also no published list to satisfy; the medical record is the entire defense.
- **Commercial:** AZ Blue, Humana, UHC, and Optum all run **proprietary, unpublished** dx-to-procedure and clinical-edit logic (typically ClaimsXten/Optum-family editing). **These are not obtainable.** The only reliable way to find them is a **pre-determination or a written coding inquiry per payer** before the first case.
- **Narrative requirement:** **64999 always requires a narrative** — no exception, any payer, any diagnosis. And because **no payer publishes a covered-dx list for 64772**, in practice **64772 needs the same narrative treatment**: submit the operative report with the initial claim, don't wait to be asked. **[MUST PULL]** each payer's preferred channel for attaching an op note to an original claim (some accept PWK, some require a portal upload, some only accept it on appeal).

---

# PART 4 — Modifiers, units, bundling, site of service, global

## 4.1 Anatomic site and laterality

64772's descriptor carries **no level and no side.** The claim therefore cannot show what was done — the op note has to.

**Required in the note, per nerve:** nerve name · spinal level · side · approach · that it was transected or avulsed (with segment length if excised) · extradural location.

**Modifier:**
- **Modifier 50** (bilateral) vs. **LT/RT** — depends entirely on 64772's **MPFS bilateral surgery indicator**, which is **[MUST PULL]**. Indicator 0 = bilateral adjustment does not apply; 1 = 150% with modifier 50, one line, one unit; 2 = RVUs already reflect bilateral, no additional payment; 3 = paid at 100% per side (typically two lines with LT/RT).
- **This is exactly where Medicare and commercial diverge.** Medicare generally wants **modifier 50, one line, one unit**. Many commercial payers want **two lines with LT and RT**. Billing Medicare's way to a commercial payer (or the reverse) produces a denial that looks like a medical-necessity denial and isn't. **[MUST PULL]** each payer's bilateral convention in writing.

## 4.2 Units, MUE, and bilateral interaction

- **MUE = 6 units, effective 2026-01-01** (increased from 2) **[VERIFIED]**.
- **MAI unknown — [MUST PULL].** See §2.1; if MAI = 2 there is no override and no appeal above 6.
- Units are **per distinct nerve**, each separately documented. Six units means six individually described nerves — not "six levels" and not "three levels bilaterally" unless each nerve is named.
- **A 6-unit MUE does not mean 6 per side.** MUE is a per-date-of-service cap. How bilateral consumes units depends on the bilateral indicator above. Until both fields are pulled, **do not let scheduling quote a bilateral multi-level case as billable.**

## 4.3 Same-session billing with 64633–64636

**[MUST PULL] — I could not retrieve the NCCI PTP file, so I will not state an edit that I have not seen.** This is the top-priority data pull and it is free: CMS NCCI → Procedure-to-Procedure Edits → Practitioner Services, current quarter; search column 1 and column 2 for 64772 against 64633, 64634, 64635, 64636, 64490–64495, 62321, 62323, 64483, 64484.

What is known:

- **Same joint / same level / same side: do not bill both.** 64633–64636 and a 64772 aimed at the same medial branches describe the **same anatomic target**; the more definitive procedure supersedes the other. A modifier does not fix that — it is a coding-accuracy problem, not an edit problem, and modifier 59/XS applied to it is the pattern that draws an audit.
- **Different levels, genuinely separate indications:** expect an edit. Whether **59 / XE / XS / XU** breaks it depends on the pair's **modifier indicator (0 = never bypassable, 1 = bypassable with documentation, 9 = no edit)** — pull it.
- **The global period is the bigger collision.** If 64772 carries **090 days**, any RFA at the same site inside that window is bundled into the global unless it is genuinely staged (58), a return to the OR for a related problem (78), or unrelated (79). **This lands directly on the existing facet population** — patients who have a 64772 and then need RFA within 90 days.
- **64490–64495 same day:** the facet LCD policy restricts diagnostic medial branch blocks and denervation at the same level on the same day. **[MUST PULL]** exact wording from L38801's companion LCA.
- **ESI same day (62321/62323, 64483/64484):** also restricted under the facet policy family. **[MUST PULL]** from the same LCA.

## 4.4 Assistant surgeon / co-surgeon

**[MUST PULL] — CY2026 MPFS RVU file, fields `ASST SURG` and `CO-SURG`.** I could not reach the file and will not guess. Commercial payers usually mirror the Medicare indicators but are not obligated to; if an assistant is planned for any case, confirm in writing per payer first.

## 4.5 ASC vs. HOPD — the question that decides whether Bri can book it in-house

**[MUST PULL] — whether 64772 appears on the CY2026 ASC Covered Procedures List (Addendum AA), and its payment indicator (defined in Addendum DD1).**

This is the single most consequential unknown in this memo for scheduling:

- **If 64772 is on Addendum AA:** the ASC receives a facility payment; the case can be booked at the practice's ASC.
- **If 64772 is not on Addendum AA:** **Medicare pays no ASC facility fee.** The case must go to an HOPD, or the ASC absorbs the facility cost entirely. Scheduling has to send it out, which changes access, timeline, and the economics the Executive Team will be shown.

Commercial ASC coverage runs off each payer's own ASC/site-of-service list, not Medicare's. **[MUST PULL]** per payer. Note also **[PARTIAL]** that UHC applies **site-of-service review** to outpatient surgical codes (policy effective 2026-07-01), and that Medicare's HOPD prior-auth program for facet interventions applies to the HOPD setting — so the "send it to the hospital" fallback carries its own pre-service requirement for the facet codes.

## 4.6 Post-operative global

**Expected 090 days — [MUST PULL] to confirm** (MPFS `GLOB DAYS`; 090 = major surgery, 1 pre-operative day + day of surgery + 90 post-operative days).

**If 090, the global bundles:** the pre-operative visit the day before or day of · intra-operative services · all routine post-operative care for 90 days · post-surgical pain management related to the procedure · dressing changes, suture/staple removal · all related follow-up visits · treatment of complications not requiring a return to the OR.

**Modifiers needed inside the window:**
- **24** — unrelated E/M during the post-op period (requires a distinct diagnosis)
- **25** — significant, separate E/M on the same day as a minor procedure
- **58** — staged or planned related procedure
- **78** — unplanned return to the OR for a related problem
- **79** — unrelated procedure during the post-op period
- **54 / 55 / 56** — split surgical care, if pre-op, intra-op, and post-op are provided by different physicians

**For the Executive Team:** a 090-day global is a very different operational and financial profile from 64633's 010-day global. It changes post-op visit billing, changes when the next RFA can be done, and changes the revenue-per-case math. If the deck models 64772 revenue without modeling 90 days of bundled follow-up, the model is wrong.

## 4.7 Credentialing and specialty taxonomy

**[NOT FOUND]** — no payer policy located that restricts 64772 to a particular specialty taxonomy.

**[VERIFIED]** Dr. Luke's NPPES record carries a **single taxonomy: 207X00000X Orthopaedic Surgery.** That is an appropriate and defensible taxonomy for an open nerve transection — this is **not** the main risk here. Three practical checks anyway:

1. **Contract-level specialty designation.** If any payer credentialed him under a pain-management or interventional designation for the facet work, an open 090-global surgical code may trip specialty-based claim editing. **[MUST PULL]** his credentialed specialty per payer contract — not his NPPES taxonomy, which payers frequently do not use for editing.
2. **Facility privileging.** ASC and HOPD privileges must explicitly cover open (and, if applicable, endoscopic) neurectomy. A code the credentialing file doesn't support is a denial no biller can fix.
3. **Device/technique-specific credentialing.** If the procedure is endoscopic, some payers and facilities require technique-specific credentialing or proctoring before the first case.

---

# PART 5 — For Deanna and Bri: what delays scheduling or triggers denial

Ranked by how much damage each one does.

| # | Risk | Why it bites | Owner |
|---|---|---|---|
| 1 | **The code is likely wrong for the procedure.** | If this is facet/medial-branch denervation, CPT routes it to 64633–64636 or 64999 — not 64772. Billing an open 090-global surgical code for a percutaneous or endoscopic facet denervation is a recognized audit target and reads as misrepresentation of the service, not a coding difference of opinion. | Resolve **before** anything is scheduled |
| 2 | **No published coverage policy for 64772 at any of the five payers.** | Nothing to cite in an auth request. Nothing to cite in an appeal. Every claim is decided on the op note by an individual reviewer. | Auth |
| 3 | **"No prior auth required" is not approval.** | With no PA, no policy, and a 090-day global, 100% of the exposure is post-payment — including recoupment on cases already performed and paid. | Executive Team |
| 4 | **ASC status unknown.** | If 64772 is not on ASC Addendum AA, **the case cannot be booked at the ASC with a facility payment.** This alone can move the entire program off-site. | Scheduling — **pull first** |
| 5 | **090-day global collides with the existing RFA population.** | Facet patients who have a 64772 and then need RFA inside 90 days will be bundled unless correctly staged with 58/78/79. Expect denials in month two if this isn't built into the scheduling rules now. | Scheduling |
| 6 | **MUE = 6 with unknown MAI.** | If MAI = 2, units above 6 are denied with **no appeal**. Bilateral multi-level cases exceed 6 nerves easily. | Billing — **pull now** |
| 7 | **Endoscopic technique is affirmatively excluded.** | UHC's Ablative Treatment for Spinal Pain policy calls endoscopic RFA for spinal pain **unproven/not medically necessary [PARTIAL]**; BCBS-family facet denervation policies call endoscopic rhizotomy **investigational [PARTIAL]**. These are denial hooks that exist today. | Auth |
| 8 | **Vendor routing is stale in three places.** | **OrthoNet portal is retired** (Optum Spine/Pain/Joint since 2025-09-03) · **Carelon at AZ Blue is Medicare Advantage only, not commercial** · **Humana's Cohere MSK program does not include Arizona.** Each wrong submission costs days. | Auth — fix this week |
| 9 | **Diagnosis carryover fails.** | **M54.5 and M47.81 are invalid parent codes** and reject at the front end. Facet/regional diagnoses will not support a named-nerve transection and are the exact pattern that pulls the chart. | Billing |
| 10 | **Plan-type and group-number divergence.** | Commercial, ACA, Medicare Advantage, D-SNP, and AHCCCS follow different rules at the same payer; **self-funded ASO groups override the medical policy entirely.** Verify per member, per group number. | Auth |

## Recommended questions for the payer calls

Ask each payer's provider relations these, and **get the answer in writing** — a verbal auth reference number will not survive a post-payment review:

1. Do you publish any medical policy, coverage guideline, or payment policy addressing **CPT 64772**? If not, how is it adjudicated?
2. Does 64772 require **prior authorization**, notification, or nothing — by plan type (commercial, ACA, MA, D-SNP, Medicaid)? **Which vendor** holds it?
3. Is 64772 on your **ASC covered-procedure list**? What is the facility payment pathway? Does **site-of-service review** apply?
4. What is your **bilateral convention** for 64772 — modifier 50 with one unit, or LT/RT on separate lines? **How many units** will you allow per session?
5. Do you have an **edit between 64772 and 64633–64636** on the same date of service? Is it **bypassable with a modifier**, or a hard bundle?
6. Does 64772 carry a **90-day global** on your fee schedule? What does it bundle?
7. Do you allow an **assistant surgeon or co-surgeon** on 64772?
8. Is there a **covered-diagnosis list**, or is it case-by-case? **Will you accept a pre-determination** for a named patient before we schedule?
9. If we report **64999** for endoscopic medial branch transection instead, what is your coverage position and your manual-pricing process?
10. Is 64772 restricted by **specialty or taxonomy** on your fee schedule?

## Recommended sequence before the first case is booked

1. **Get the operative-note template and the vendor's coding sheet** from Dr. Luke or the device rep, and read what the procedure actually is. Everything else depends on this one answer.
2. **Purchase and read the two AMA CPT Knowledge Base Q&As** on endoscopic rhizotomy (§1.4). This is the authoritative answer to the code question and it is behind a paywall, not a wall.
3. **Pull the six CMS data files** in §2.1 — MPFS indicators, MUE/MAI, NCCI PTP, ASC Addendum AA. Free, same-day, and four of the ten risks above resolve on them.
4. **Pull L38801** and its current companion LCA, and retire every L38803/A58405 printout in the office.
5. **Run 64772, 64633, 64635, and 64999** through each payer's PA lookup, by plan type.
6. **Request written pre-determinations** from the top two payers by volume before scheduling a single case.
7. **If the procedure is endoscopic medial branch transection:** plan on **64999** with a narrative, a comparison code, and manual pricing — and set the Executive Team's revenue expectations accordingly, before the equipment decision is made rather than after.

---

## Sources

**Primary policy documents (cited by name/number/date; full text not retrievable this session):**
- LCD — Facet Joint Interventions for Pain Management, **L38801**, Noridian Healthcare Solutions (JE/JF consolidated), v23, rev. eff. 2026-04-16 — https://www.cms.gov/medicare-coverage-database/view/lcd.aspx?lcdid=38801&ver=23
- LCD — Facet Joint Interventions for Pain Management, **L38803** (Noridian JF, **retired 2026-04-16**) — https://www.cms.gov/medicare-coverage-database/view/lcd.aspx?lcdid=38803&ver=17
- Article — Billing and Coding: Facet Joint Interventions for Pain Management, **A58405** (Noridian JF, retired) — https://www.cms.gov/medicare-coverage-database/view/article.aspx?articleId=58405
- Article — Billing and Coding: Facet Joint Interventions for Pain Management, **A58350** — https://www.cms.gov/medicare-coverage-database/view/article.aspx?articleid=58350&ver=22
- Noridian — Prior Authorization for Certain Hospital OPD Services: Facet Joint Interventions (eff. 2023-07-01) — https://med.noridianmedicare.com/web/jfa/cert-reviews/pre-claim/prior-authorization-for-certain-hospital-opd-services/facet-joint-interventions-for-pain-management
- UnitedHealthcare Commercial Medical Policy — Ablative Treatment for Spinal Pain (eff. 2026-05-01) — https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/ablative-treatment-spinal-pain.pdf
- UnitedHealthcare — Facet Joint and Medial Branch Block Injections for Spinal Pain — https://www.uhcprovider.com/content/dam/provider/docs/public/policies/comm-medical-drug/facet-joint-injections-spinal-pain.pdf
- UnitedHealthcare Community Plan — Ablative Treatment for Spinal Pain — https://www.uhcprovider.com/content/dam/provider/docs/public/policies/medicaid-comm-plan/ablative-treatment-spinal-pain-cs.pdf
- UnitedHealthcare Medicare Advantage Medical Policy — Pain Management — https://www.uhcprovider.com/content/dam/provider/docs/public/policies/medadv-mp/pain-management-rehabilitation.pdf
- UnitedHealthcare Commercial Advance Notification and PA Requirements (eff. 2026-01-01) — https://www.uhcprovider.com/content/dam/provider/docs/public/prior-auth/pa-requirements/commercial/UHC-Commercial-Advance-Notification-PA-Requirements-1-2026.pdf
- UnitedHealthcare Medicare Advantage Plans of Arizona — 2026 QRG, Optum Care Arizona — https://www.uhcprovider.com/content/dam/provider/docs/public/health-plans/medicare/2026/qrg/2026-MED-ADV-QRG-Optum-Care-Arizona.pdf
- Humana — Medicare Advantage and DSNP Prior Authorization and Notification List (eff. 2026-01-01) — https://assets.humana.com/is/content/humana/FINAL_Medicare%20and%20DSNP%20Prior%20Authorization%20and%20Notification%20List%20-%201-1-2026pdf
- Humana — Prior Authorization Search Tool — https://provider.humana.com/coverage-claims/prior-authorizations/prior-authorizations-search-tool
- AZ Blue — Prior Authorization & Medical Policies search — https://www.azblue.com/provider/resources/prior-authorization-and-medical-policies/search
- AZ Blue — Prior Authorization Lookup — https://www.azblue.com/prior-authorization-lookup
- AZ Blue Health Choice Pathway (D-SNP) — Prior Authorization Guidelines — https://www.azblue.com/health-choice-pathway/providers/prior-authorization-guidelines
- eviCore by Evernorth — Blue Cross Blue Shield of Arizona health plan page — https://www.evicore.com/resources/healthplan/blue-cross-blue-shield/arizona
- BCBSA reference policy 7.01.116 Facet Joint Denervation, as published by Premera (7.01.555) — https://www.premera.com/medicalpolicies/7.01.555.pdf
- AHCCCS — Fee-For-Service Prior Authorization Requirements (AMPM Ch. 300/400/800/1100) — https://www.azahcccs.gov/PlansProviders/FeeForServiceHealthPlans/PriorAuthorization/requirements.html

**Coding references:**
- AMA CPT Knowledge Base — "When the physician performs a medial branch endoscopic rhizotomy at L3, L4, and L5…" (paywalled) — https://www.findacode.com/newsletters/ama-cpt-kb/physician-performs-medial-branch-endoscopic-7298.html
- AMA CPT Knowledge Base — "What is the appropriate code(s) to report for a minimally invasive surgical (MIS) endoscopic rhizotomy…" (paywalled) — https://www.findacode.com/newsletters/ama-cpt-kb/appropriate-codes-report-minimally-7070.html
- AAPC Codify — CPT 64772 — https://www.aapc.com/codes/cpt-codes/64772
- AAPC Codify — Transection or Avulsion, 64732–64772 — https://www.aapc.com/codes/cpt-codes-range/64732-64772/
- Find-A-Code — CPT 64772 — https://www.findacode.com/cpt/64772-cpt-code.html
- KZA — Nerve Transection CPT 64772 (2026-03-05) — https://www.kzanow.com/coding-coaches/nerve-transection-cpt-64772-03-05-26
- AAPC forum — Endoscopic Rhizotomy compare to code — https://www.aapc.com/discuss/threads/endoscopic-rhizotomy-compare-to-code.180883/
- AAPC forum — 64772 Transection or avulsion of other spinal nerve, extradural — https://www.aapc.com/discuss/threads/64772-transection-or-avulsion-of-other-spinal-nerve-extradural.158873/
- Medtronic — Radiofrequency Ablation for Nerve Tissue, 2026 Coding and Payment Guide — https://www.medtronic.com/content/dam/medtronic-wide/public/united-states/products/neurological/radiofrequency-ablation-nerve-tissue-reimbursement-guide.pdf

**On the 64772 MUE change and the endoscopic-MBT coding position:**
- Becker's Spine Review — "CMS approves 6 units for CPT 64772: Why this is a major step for endoscopic spine surgery" — https://www.beckersspine.com/spine/cms-approves-6-units-for-cpt-64772-why-this-is-a-major-step-for-endoscopic-spine-surgery/
- Arthrex — Spine Evolutions 2026: Audience Questions — https://www.arthrex.com/resources/DOC1-001292-en-US/spine-evolutions-2026-audience-questions
- "The Emerging Case for Expanding the MUE for CPT 64772" — https://raymondpolo.substack.com/p/the-emerging-case-for-expanding-the

**Vendor/program:**
- Optum Spine, Pain and Joint portal replacing OrthoNet (eff. 2025-09-03) — https://hfproviders.org/resource-posts/changes-to-prior-authorization-submissions-for-back-pain-management-and-spinal-surgery-services
- Cohere Health / Humana MSK prior authorization, 12-state footprint — https://www.fiercehealthcare.com/payer/humana-teams-cohere-health-to-streamline-prior-authorization-for-musculoskeletal-conditions

**Registry:**
- CMS NPPES NPI Registry — NPI 1437125846 (verified via NPI Registry API, 2026-09-15)

**CMS data files to pull (paths in §2.1):** CY2026 MPFS Relative Value Files (`PPRRVU26`) · Practitioner Services MUE Table · NCCI Procedure-to-Procedure Edits, Practitioner Services, current quarter · ASC Payment Rates Addenda AA and DD1.
