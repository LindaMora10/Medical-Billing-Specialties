# AZ Blue & Optum — Coverage and Authorization Routing Guide

**Prepared:** 15 September 2026 · **For:** Deanna, Bri, and the billing department
**Scope:** Where to get **coverage criteria** and **prior authorization** for every AZ Blue and Optum
plan family, keyed to the payer names as they appear in your AR.

> **The core problem this solves:** neither "BCBS AZ" nor "Optum" is one payer. **AZ Blue runs nine plan
> families**, each with its own vendor, code list and phone number. **Optum Care Arizona maintains a
> separate prior-authorization list per health plan** — one for UnitedHealthcare members, a different one
> for Blue Cross members. Calling the wrong one gets you a confidently wrong answer.

Companion documents: **[CPT 64772 Billing Playbook](../Code%20Research/CPT_64772_Billing_Playbook_2026-09-15.md)** ·
**[CPT 64772 Payer Research](../Code%20Research/CPT_64772_Payer_Research_2026-09-15.md)**

---

## 1. Routing decision tree — do this before you call anyone

Work top to bottom. Stop at the first match.

| Step | Look at | If you see… | Route to |
|---|---|---|---|
| 1 | **Payer ID on the card / in the clearinghouse** | **`LIFE1`** | **Optum Medical Network AZ** (§3) — *not* the health plan, even though the card says UnitedHealthcare or Blue Cross |
| 2 | **AZ Blue alpha prefix** (first 3 chars of member ID) | `M2K` | AZ Blue **Medicare Advantage** (§2.5) |
| 3 | | **`HCIA`** or `IAZ` | AZ Blue **Health Choice family** (§2.2) — then split by payer ID: `RP105` = ACA StandardHealth · `62179` = Health Choice Arizona Medicaid |
| 4 | | `R` | **FEP** (§2.4) |
| 5 | | `XBS` | **Medicare Supplement** (§2.9) |
| 6 | | `AOZ` `AZI` `AZK` `IVR` | **Strategic Hub** — another Blue plan administers (§2.6) |
| 7 | | Any other prefix, member lives out of state | **BlueCard** — the member's home Blue plan owns the rules (§2.3) |
| 8 | **Card says a TPA / third-party administrator** | e.g. Meritain, Summit, UMR | **CHS or jointly-administered** (§2.7, §2.8) — call the number on the back of the card |
| 9 | Nothing above matches | — | AZ Blue **commercial** (§2.1) |

🔴 **Step 1 outranks everything.** A delegated member's card can carry UnitedHealthcare or Blue Cross
branding while every authorization decision is made by Optum. `LIFE1` is the tell.

> 🔴 **Why misrouting is now expensive.** Per `Carrier_Timely_Filing_Reference.xlsx`, **AZ Blue's initial
> filing limit dropped from 365 days to 90 days for dates of service on or after 1 January 2026.** Time
> spent bouncing between the wrong entity and the right one used to be absorbed by a year-long window;
> it no longer is. Health Choice lines run on **6–7 month** windows (12 months non-contracted on the ACA
> line), and **Optum is 90 days.** Route right the first time.

---

## 2. AZ Blue — nine plan families

Source: [AZ Blue Prior Authorization & Medical Policies](https://www.azblue.com/provider/resources/prior-authorization-and-medical-policies)
(resources are organised by benefit plan type) and
[Medicare PA & Medical Policies](https://www.azblue.com/medicare/resources/prior-authorization-and-medical-policies).

### 2.1 AZ Blue Plans — commercial
| | |
|---|---|
| **Prefix** | Everything not listed below |
| **Auth vendor** | **Availity Essentials** + **eviCore** |
| **Submit via** | Availity Essentials portal · eviCore request system · fax/online forms (separate forms for Healthcare Services vs Medications/DME) · pharmacy via Cover My Meds or Surescripts |
| **Code list** | `az-blue-prior-auth-code-lists.xlsx` — see §5 for the live link |
| **Coverage criteria** | [AZ Blue proprietary medical policies](https://www.azblue.com/provider/resources/prior-authorization-and-medical-policies/search#tab=all) · MCG Care Guidelines (login) · eviCore guidelines · chiropractic guidelines |
| **UM contact** | `UtilMgmt@azblue.com` · **602-864-4320** (24/7 clinical) · provider services **1-800-322-8670** |
| ⚠️ **For 64772 / pain** | **eviCore's MSK–Interventional Pain program does NOT apply to commercial members** — Medicare Advantage only. So there is **no eviCore precert pathway** here, and no pre-service approval to obtain. Confirm whether AZ Blue's own UM requires PA. |

### 2.2 Health Choice family — three separate lines of business

**Prefixes: `HCIA` and `IAZ`.**

> ⚠️ **On `HCIA`:** added at the practice's direction — this is what we see on cards and in our AR. I could
> **not** confirm it from a published AZ Blue source: six AZ Blue / Health Choice pages were checked (the
> provider PA-and-policies hub, both ACA PA-guidelines pages, the Medicaid PA page, and both claims pages)
> and none of them publishes a prefix list. AZ Blue's provider hub names only **`IAZ`** for the ACA
> Health Choice Network line. **Treat both as in use**, and see §7 for the ask that gets the full,
> authoritative prefix list in writing.

🔴 **Do not route on the prefix alone here — "Health Choice" is three different plans.** The **payer ID**
is the reliable discriminator:

| | **ACA StandardHealth with Health Choice** | **Health Choice Arizona** | **Health Choice Pathway** |
|---|---|---|---|
| **Line of business** | ACA / marketplace | **AHCCCS Medicaid** | **D-SNP** (Medicare + Medicaid) |
| **Payer ID** | **`RP105`** | **`62179`** | *(confirm — see §7)* |
| **Also known as** | "Standard Health" on forms | — | Health Choice Generations |
| **PA phone** | **1-800-322-8670** (Maricopa 480-968-6866) | **1-800-322-8670** | **1-800-656-8991** |
| **PA fax** | **602-864-5308** · BH out-of-home **480-760-4732** | **1-877-422-8120** · referrals 1-855-432-2494 · Rx 877-422-8130 | **1-877-424-5680** · Rx **1-877-424-5690** |
| **Portal** | [providerportal.healthchoiceaz.com](https://providerportal.healthchoiceaz.com/Account/Login) | same | secure provider portal |
| **PA grid** | Standard Health PA Grid, eff. **5/1/2026** | PA Grid, eff. **5/1/2026** | PA Grid, eff. **5/1/2026** |
| **Coverage criteria** | [Clinical guidelines](https://www.azblue.com/medicaid/providers/clinical-guidelines) · **eviCore** for radiology / cardiac imaging | [Clinical guidelines](https://www.azblue.com/health-choice-az/providers/clinical-guidelines) · AHCCCS AMPM | **InterQual · UpToDate · NCDs/LCDs · NCCN** |
| **Timely filing** | 6 mo contracted / **12 mo non-contracted** | 6 mo (7 mo if HCP primary) | 6 months |
| **Claims address** | ACA StandardHealth with Health Choice, PO Box 52033, Phoenix AZ 85072-2033 | BCBSAZ Health Choice, PO Box 52033, Phoenix AZ 85072-2033 | — |

**Clearinghouse for all three:** Availity (800-282-4548). Dental PA by email: `HCHDentalDeptHCA@azblue.com`.

**Notes that matter for 64772:**
- **Pathway is a D-SNP** — it applies **NCDs and LCDs**, so the Medicare analysis governs: **NCD 160.1**,
  no published criteria, decided on the operative report.
- **eviCore on the ACA line covers radiology and cardiac imaging only** — not MSK or interventional pain.
  So there is no eviCore pathway for 64772 here either.
- "Many of the items on our abbreviated prior authorization list ask for **notification only**" (Health
  Choice Arizona) — worth asking whether 64772 falls in that category rather than full PA.
- **All non-contracted providers must obtain authorization for any service**, on every Health Choice line.

### 2.3 BlueCard — out-of-area Blue members
| | |
|---|---|
| **Who decides** | **The member's home Blue plan**, not AZ Blue |
| **Submit via** | [Availity BlueCard authorization request](https://essentials.availity.com) → Authorizations & Referrals |
| **Coverage criteria** | [BlueCard Medical Policy Router](https://www.azblue.com/provider/resources/prior-authorization-and-medical-policies/bluecard-medical-policy-router) — enter the prefix, it routes you to that plan's policy |
| ⚠️ **For 64772** | Every home plan has its own position. **Check the router per member.** Do not assume AZ Blue's answer applies. |

### 2.4 Federal Employee Program (FEP)
| | |
|---|---|
| **Prefix** | **`R`** |
| **Auth vendor** | Availity Essentials · Caremark (pharmacy) |
| **Code list** | **FEP tab** of the AZ Blue code list workbook (§5) |
| **Coverage criteria** | [FEP medical policies](https://www.fepblue.org/legal/policies-guidelines) · [FEP utilization guidelines](https://www.fepblue.org/legal/utilization-guidelines) · MCG (login) |
| **Contacts** | **602-864-4102** · **1-800-345-7562** · pharmacy **1-877-727-3784** |
| ⚠️ | FEP uses its **own** policy set — AZ Blue proprietary policies do not govern. |

### 2.5 Medicare Advantage — 🔴 three different vendors
| | |
|---|---|
| **Prefix** | **`M2K`** |
| **Code list** | **Medicare Advantage tab** of the AZ Blue code list workbook (§5) |
| **Coverage criteria** | **CMS NCDs and LCDs first** (for 64772 that means **NCD 160.1**; for facet work, **Noridian L38801 / A58403**) · eviCore guidelines · MCG · Part B step therapy list |
| **Submit via** | Availity Essentials · eviCore · fax request form · **OHNAZ or AZPC portals** · Part D via Cover My Meds/Surescripts |

**Which of the three owns the member:**

| Sub-plan | Vendor | Phone | Prior auth list |
|---|---|---|---|
| **AZ Blue** (retained) | AZ Blue | **1-800-446-8331** | AZ Blue code list workbook, MA tab (§5) |
| **OHNAZ** — Optum Health Network Arizona | **Optum** | **1-877-370-2845** | **BCBS-specific Optum list** (§5) — a *different document* from the UHC one |
| **AZPC** — Arizona Priority Care | Arizona Priority Care | **480-499-8720** | AZPC "Services That Do Not Require Authorization" attachment (§5) |

⚠️ **For 64772 / pain:** eviCore's MSK–Interventional Pain program **does** apply to MA. But **64772 is not
on the eviCore code list at all**, so it routes to AZ Blue's internal UM (or OHNAZ/AZPC if the member is
delegated). **Ask explicitly which entity adjudicates a code that is absent from the eviCore list.**

### 2.6 Strategic Hub Plans
| | |
|---|---|
| **Prefixes** | **`AOZ` `AZI` `AZK` `IVR`** |
| **Who decides** | A partner Blue plan |
| **Submit via** | ["My Insurance Manager" (BCBS SC)](https://provider.bcbssc.com/wps/portal/nhcp/providers/home/) |
| **Coverage criteria** | [Strategic Hub medical policies](https://member.myhealthtoolkitaz.com/web/public/brands/az/manage-your-plan/understanding-insurance/medical-policies/) |

### 2.7 Corporate Health Services (CHS) group plans
| | |
|---|---|
| **Who decides** | The group's **TPA** |
| **Find the TPA** | CHS Group/TPA contact list via Availity (login required) |
| **Submit via** | Number on the back of the member's card |
| ⚠️ | Coverage criteria are the **TPA's**, not AZ Blue's. Get the policy from the TPA in writing. |

### 2.8 AZ Blue & TPA jointly administered plans
| | |
|---|---|
| **Who decides** | Split between AZ Blue and a TPA — **varies by group** |
| **Find the TPA** | **2026 AZ Blue TPA Jointly Administered Plans** contact list (§5) |
| ⚠️ | This is where "we called BCBS and they said no auth needed" goes wrong. Confirm **which half** of the administration owns utilisation review for this group. |

### 2.9 Medicare Supplement
| | |
|---|---|
| **Prefix** | **`XBS`** |
| **Who decides** | **CMS** — the plan follows the Medicare determination |
| **Practical effect** | Get it right with **Noridian** and the supplement follows. AZ Blue makes its own determination only for foreign-travel emergencies. |

**AZ Blue general inquiries:** **1-844-995-2583**

---

## 3. Optum — routing by health plan, not by "Optum"

**Optum Medical Network of Arizona** (formerly **LifePrint**; also appears as *Optum Care Medical Network
of Arizona, Utah & Washington*) is a **delegated risk network**. It takes over utilisation management for
members assigned to it from **multiple different health plans** — and it publishes a **separate prior
authorization list for each one.**

| Fact | Value |
|---|---|
| **Payer ID** | **`LIFE1`** |
| **Provider portal** | `secure.optummedicalnetwork.com` (register at `/provider/account/register`) · also **Optum Pro portal**, `optumproportal.com` → *Medical Management* |
| **PA intake** | **1-877-370-2845** (TTY 711) — urgent and routine |
| **PA email** | `lcd_um@optum.com` |
| **Pharmacy (UHC members)** | **1-800-711-4555** · fax **1-800-527-0531** · `optumrx.com` |

### 3.1 The two lists — use the right one

| Member's health plan | Which Optum list applies | Where |
|---|---|---|
| **UnitedHealthcare** members delegated to Optum | **Optum Care–Arizona prior authorization list (UHC)** | §5 |
| **Blue Cross Blue Shield of Arizona** members delegated to Optum (**OHNAZ**) | **Optum Care–Arizona prior authorization list (BCBS)** — *a different document* | §5 |

🔴 **These lists are not interchangeable.** A code that needs PA for a UHC-delegated member may not for a
BCBS-delegated one, and vice versa. Always confirm which health plan issued the card before pulling a list.

### 3.2 UnitedHealthcare Medicare Advantage plans delegated to Optum in Arizona

From **1 January 2026**, Optum Health Networks administers these UHC MA plans in Arizona. Source:
[UHC MA Arizona QRG, PCA-4-26-00582-M&R-QRG_05132026](https://www.uhcprovider.com/content/dam/provider/docs/public/health-plans/medicare/2026/qrg/2026-MED-ADV-QRG-Optum-Care-Arizona.pdf).

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

🔴 **Referral requirement.** HMO and HMO-POS members delegated to Optum **must have a PCP referral
submitted to Optum before the specialist visit**, or the claim denies. Does not apply to Institutional SNP
or Erickson Advantage plans. **This is a front-desk workflow item, not a billing one** — by the time it
reaches billing it is too late.

**Other rules from the QRG:** a PA already approved by UnitedHealthcare for DOS from 1 Jan 2026 does not
need resubmitting to Optum · notify Optum of hospital admissions within 1 business day · UHC publishes PA
requirements at **UHCprovider.com/priorauth → Advance Notification and Plan Requirement Resources**.

### 3.3 🔴 Delegated groups and IPAs override everything above

UHC's own guidance: **"If you are a network provider who is contracted directly with a delegated medical
group/IPA, then you must follow the delegate's protocols"** — delegates use their own systems and forms.

**So there is a third layer:** health plan → Optum → the specific IPA. Ask, per contract, which layer owns
utilisation review for Dr. Luke's patients. A correct answer from Optum can still be the wrong answer for
an IPA-contracted member.

---

## 4. Your AR payer names → where to go

Mapped to the primary payers in `Specialty Claims Pending 2026-S1.xlsx` (1,086 claim lines).

| Payer name in your system | Lines | Family | Coverage criteria | Authorization |
|---|---|---|---|---|
| **Blue Cross Blue Shield of Arizona (BCBS AZ)** | 95 | 🔴 **Ambiguous — resolve by prefix.** Could be commercial, MA (`M2K`), FEP (`R`), BlueCard or Strategic Hub | Per §2 family | Per §2 family |
| **Optum Care Medical Network of AZ, UT & WA (LifePrint)** | 65 | Optum delegated | §3 — **and identify the underlying health plan first** | 1-877-370-2845 · `optumproportal.com` |
| **Health Choice Arizona** | 8 | AZ Blue **Medicaid (AHCCCS)** · prefix `HCIA`/`IAZ` · payer ID **62179** | [Clinical guidelines](https://www.azblue.com/health-choice-az/providers/clinical-guidelines) · AHCCCS AMPM | Portal · **1-800-322-8670** · fax **1-877-422-8120** |
| **Health Choice Pathway (Health Choice Generations)** | 2 | AZ Blue **D-SNP** | InterQual · UpToDate · **NCDs/LCDs** · NCCN | **1-800-656-8991** · fax **1-877-424-5680** |
| *(ACA StandardHealth with Health Choice)* | — | AZ Blue **ACA** · prefix `HCIA`/`IAZ` · payer ID **RP105** | [Clinical guidelines](https://www.azblue.com/medicaid/providers/clinical-guidelines) · eviCore (imaging only) | Portal · **1-800-322-8670** · fax **602-864-5308** |
| **UHC Group Medicare Advantage** | 36 | UHC MA | UHC MA policies + **LCD/LCA** | 🔴 Check for `LIFE1` → Optum, else UHCprovider.com/priorauth |
| **United HealthCare Dual Complete** | 30 | UHC D-SNP | UHC MA policies + LCD/LCA | Same — check `LIFE1` |
| **AARP MedicareComplete (SecureHorizons & Oxford)** | 15 | UHC MA | UHC MA policies + LCD/LCA | Same — check `LIFE1` |
| **United Healthcare** | 60 | UHC commercial | UHC commercial policies (2026T0107II, 2026T0004WW, MP.12.22) | UHCprovider.com/priorauth |
| **UnitedHealthcare Community Plan / AZ Long Term Care** | 104 | UHC **AHCCCS ALTCS** | UHC Community Plan AZ policies + AHCCCS AMPM | UHC Community Plan — **separate from commercial** |
| **UMR Wausau / UHIS** | 23 | UHC **TPA** | 🔴 **Plan document governs** — UMR administers self-funded groups | Per group; UMR medical policies at uhcprovider.com |
| **Surest (formerly BIND)** | 2 | UHC | **Surest-specific policy set** — different from UHC commercial | Surest policies at uhcprovider.com |
| **Humana Gold Plus HMO** / **Humana** | 49 / 12 | Humana MA | Humana coverage policies | **64772 not on the PA list**; facet codes are. Cohere **833-283-0033** |
| **Arizona Priority Care Plus** | 6 | AZ Blue MA delegate (**AZPC**) | §2.5 | **480-499-8720** |
| **Medicare Part B Arizona** | 246 | Traditional Medicare | **NCD 160.1** for 64772; L38801/A58403 for facet | **No PA required** |

*Other payers in your AR (Aetna, Banner, Alignment, Devoted, Mercy Care, Gold Kidney, SCAN, Cigna/
HealthSpring, Ambetter, Imperial, Oscar, TriWest, Tricare) fall outside this guide's scope — AZ Blue and
Optum only, as asked.*

---

## 5. 🔴 Links to open from an office machine

These are the documents that decide the 64772 answer. **All five domains below are blocked from the
environment this research ran in** — every access path was tried and refused at the network layer. The URLs
are correct and current; they just have to be opened from your network.

| Document | URL | What to look for |
|---|---|---|
| **AZ Blue PA code lists** (eff. **April 2026**) | `assets.azblue.com/asset/1b2ef17e-2036-48a4-b0d7-cb49806d433a/AZ-BluePriorAuth-CodeListsEffective202604.xlsx` | Tabs by plan family. Search **64772**, then 64633–64636, 64625 |
| *(older mirror of the same workbook)* | `edge.sitecorecloud.io/bluecross-6f8ea2ea/media/project/bcbs-az/azblue/data/media/files/providers/resources/code-lists/az-blue-prior-auth-code-lists.xlsx` | Fallback if the above 404s |
| **Optum Care–Arizona PA list — BCBS members** | `optum.com/content/dam/o4-dam/resources/pdfs/forms/az-prior-authorization-list-bcbs.pdf` | Search **64772** |
| **Optum Care–Arizona PA list — UHC members** | `business.optum.com/content/dam/noindex-resources/consumers/pdfs/forms/prior-authorization-requirements-arizona-uhc.pdf` (doc `OHNC-1-24-00647`) | Search **64772** |
| **Optum Care–Arizona PA landing pages** | `business.optum.com/en/support.hcp-resources.prior-authorization-list-arizona.html` (UHC) · `…-arizona-bcbs.html` (BCBS) | Confirms current list versions |
| **OptumCare AZ Quick Reference Guide** | `campaign.optum.com/content/dam/optumcare/resources/references/OptumCare-AZ-Quick-Reference-Guide.pdf` | Full contact/claims/eligibility reference |
| **AZPC no-auth-required list** | `azprioritycare.com/wp-content/uploads/2024/08/AZPC-2024-Services-That-Do-Not-Require-Authorization_Attachment-A_Effective-8.8.2024.pdf` | If 64772 is absent, auth is required |
| **AZ Blue 2026 TPA jointly administered plans** | `edge.sitecorecloud.io/.../2026/2026-az-blue-tpa-jointly-administered-plans.pdf` | Which TPA owns which group |

**Also note:** the [AZ Blue PA lookup tool](https://www.azblue.com/prior-authorization-lookup/providers)
requires a **date of service, a CPT code, and a live Member ID** — it is member-specific, so you cannot
check 64772 generically. Run it against a real scheduled patient and **screenshot the result** for the file.

---

## 6. Call script for 64772

Ask these five, in this order, and **write down who answered and when**. A verbal "no auth needed" is worth
nothing at appeal without a reference number.

1. *"For a member with prefix ___ / group ___, who performs utilisation review for CPT **64772** — you, eviCore, Optum/OHNAZ, AZPC, or a delegated IPA?"*
2. *"Does 64772 require prior authorization for this plan? Reference number for that answer, please."*
3. *"64772 is not on the eviCore MSK list. **What criteria set do you apply to a code that isn't on a vendor list?**"* — this is the question that exposes whether anyone has a policy at all
4. *"Is there a published medical policy for 64772? Please send it, or confirm in writing that none exists."*
5. *"Is 64772 approved in an **ASC (POS 24)**, and is there a site-of-service review?"* — remember it is **not payable in an office** on Medicare

**Log every answer** — plan family, prefix, entity, answer, reference number, date, representative. Where
no published policy exists (which is the case for 64772 at every payer researched), **that call log becomes
your appeal evidence.**

---

## 7. What is settled vs what still needs a call

| ✅ Settled | |
|---|---|
| Traditional Medicare | **No PA.** WISeR does not reach 64772 — NCD 160.1's WISeR code set is 64605/64610 only |
| Humana MA & DSNP | **No PA** — 64772 absent from the list eff. 1 Jan 2026 (facet codes and 64999 *do* require it) |
| AZ Blue commercial | **No eviCore precert** — that program is MA-only |
| AZ Blue MA | Facet codes need eviCore precert; **64772 is not on the eviCore list**, so it routes elsewhere |
| Optum structure | Separate PA lists per health plan; payer ID **`LIFE1`**; 22 UHC MA group numbers delegated |

| ⚠️ Still needs a call | Who | Priority |
|---|---|---|
| Does AZ Blue require PA for 64772, and is there a policy? | **602-864-4320** · `UtilMgmt@azblue.com` | 🔴 Highest |
| **Confirm the full alpha-prefix list for the Health Choice family** — we use `HCIA`, AZ Blue publishes only `IAZ`. Ask which prefix maps to which line (ACA StandardHealth `RP105` / Health Choice Arizona Medicaid `62179` / Pathway D-SNP), and get Pathway's payer ID. | Health Choice provider services **1-800-322-8670** | ⚠️ Medium — fixes routing at step 3 |
| Does Optum require PA for 64772 — **on each list, UHC and BCBS**? | **1-877-370-2845** · `lcd_um@optum.com` | 🔴 Highest |
| Which entity adjudicates a code absent from the eviCore list? | AZ Blue MA **1-800-446-8331** | 🔴 High |
| Each delegated IPA's own protocol | Each IPA directly | 🔴 High |
| AZPC position on 64772 | **480-499-8720** | ⚠️ Medium |
| Health Choice (Medicaid) and Pathway (D-SNP) positions | **1-800-322-8670** / **1-800-656-8991** | ⚠️ Medium |

---

*Plan structures, vendors and contacts as published 15 September 2026. Alpha prefixes and delegation
assignments change at plan-year boundaries — re-verify each January. Nothing here is a coverage guarantee;
AZ Blue states expressly that prior authorization "is not a guarantee of payment."*
