# Payer Routing

Where to get **coverage criteria** and **prior authorization** for each payer, by plan family —
so a question gets asked of the entity that can actually answer it.

| File | Covers | Date |
|---|---|---|
| `AZBlue_Optum_Auth_Routing_2026-09-15.md` | AZ Blue (9 plan families) and Optum Medical Network AZ, plus a map from the payer names in our AR to the right route | 15 Sep 2026 |

## Why this exists

Neither "BCBS AZ" nor "Optum" is a single payer:

- **AZ Blue** runs nine plan families — commercial, ACA/Health Choice (`IAZ`), BlueCard, FEP (`R`),
  Medicare Advantage (`M2K`), Strategic Hub (`AOZ`/`AZI`/`AZK`/`IVR`), CHS group, TPA jointly
  administered, and Medicare Supplement (`XBS`) — each with its own vendor, code list and phone number.
- **Optum Medical Network AZ** (formerly LifePrint, payer ID `LIFE1`) is a delegated risk network that
  publishes a **separate prior-authorization list per health plan** — one for UnitedHealthcare members,
  a different one for Blue Cross members.
- A **delegated IPA** can override both.

Routing by the name on the card produces wrong answers. Route by **prefix and payer ID** — §1 of the guide.

## Conventions

- 🔴 blocker or high-risk · ⚠️ unverified, needs a call
- Prefixes and payer IDs observed by the practice but not published by the payer are marked as such —
  `HCIA` is one of these. They are used for routing, and flagged for written confirmation.
- Where a document could not be retrieved, the guide gives the **exact URL** to open rather than an
  inference about its contents.
- Verbal authorization answers are logged with a reference number, date and representative — §6.
