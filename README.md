# Consent, by Design — YouTube × DPDP Prototype

A clickable prototype for Vedantu's Product Management Intern assignment: designing a DPDP Act (2023)–compliant parental-consent experience for YouTube's under-18 users in India — without driving families away with friction.

**🔗 Live demo:** _add your GitHub Pages link here after deployment_
**📊 Product Thinking Deck:** `YouTube_DPDP_Consent_Deck.pptx` (in this repo)

---

## What this is

India's Digital Personal Data Protection (DPDP) Act, 2023 and its 2025 Rules require **verifiable parental consent** before processing any data belonging to a user under 18 — the strictest age threshold globally. This prototype reimagines YouTube's sign-up flow around that requirement, treating consent as a product experience rather than a legal checkbox.

## Try it

Open the live link above, or run it locally — it's a single self-contained HTML file with no dependencies or build step.

From the left-hand panel, choose a scenario:

| Scenario | What it shows |
|---|---|
| ▶ Happy path — teen (13–17) | Full flow: sign-up → age gate → parent invited → hand-off to parent's phone → DigiLocker verification → plain-language notice (EN/हिंदी) → granular consent → account activated with a live audit trail |
| Child under 13 | Routes into a supervised-account setup instead of the standard teen flow |
| Verification fails | Shows the fallback path (Aadhaar OTP) when DigiLocker verification doesn't complete |
| Consent declined | Safe, no-data outcome — nothing is processed, logged in the audit trail |
| Withdraw consent | Demonstrates that withdrawal is as easy as granting consent, per DPDP Rule requirements |
| Delete child's data | Simulates a data-erasure request and confirmation |
| Adult (18+) — no gate | Shows the flow quietly bypassing the parental-consent detour for adult users |

## Design highlights

- **Two-phone hand-off** — the interface visibly switches from the teen's device to the parent's device, making the "who does what" of parental consent legible at a glance.
- **Live consent audit trail** — every consent action is timestamped and logged, mirroring DPDP's requirement for verifiable, auditable consent records.
- **Bilingual notice screen (EN/हिंदी)** — reflecting DPDP's expectation that consent notices be genuinely understandable, not just present.
- **Law-locked toggles** — targeted ads and behavioural tracking are shown as permanently off for under-18 accounts, not just unchecked, reflecting a legal prohibition rather than a user preference.

## Tech

Plain HTML/CSS/JavaScript — no framework, no build step, no external runtime dependencies (only a Google Fonts import). Built to be inspected, hosted, and read in about the same time it takes to read this file.

## Context

Built for Vedantu's Product Management Intern hiring assignment (July 2026). The accompanying deck (`YouTube_DPDP_Consent_Deck.pptx`) covers the full product-thinking process: problem framing, user personas, current-state gaps, proposed solution, success metrics, diagnostic thinking, a monitoring dashboard, rollout plan, and risk trade-offs.

---

*This is a design prototype for a hiring exercise, not an official YouTube or Google product, and is not affiliated with either company.*
