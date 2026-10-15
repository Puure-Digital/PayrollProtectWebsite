# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

**Primary — Finance & HR teams at UK construction companies.** Two-role workflow: finance/commercial managers own the payment decision and need verified evidence before approving an invoice; HR or site managers supply the attendance records and are accountable for the data quality. Both roles interact with the product before a single payment clears.

**Secondary — Project and contract managers** who oversee multi-trade subcontractor packages and need a single view of claimed vs. verified labour across trades.

## Product Purpose

PayRoll Protect is the financial verification layer between a subcontractor's labour invoice and the payment approval. It cross-references every invoice claim against verified site attendance — worker by worker, trade by trade — so finance teams can approve what they can prove and dispute what they cannot.

Success means: zero unverified payments leaving the account. A finance team using PayRoll Protect can demonstrate, for any invoice line, what attendance evidence was checked before approval.

## Positioning

PayRoll Protect matches verified site attendance to invoice claims **line by line** — individual worker, individual day, individual trade — not just aggregated totals. General payroll tools and contract management platforms operate at summary level; they cannot detect a three-worker discrepancy inside a 100-worker invoice across three trades. That granularity is the product's unmatchable mechanism.

## Operating Context

- UK construction industry; primary document types: CIS invoices, attendance registers, gate access logs, induction records, QR-code attendance systems.
- Finance teams receive weekly or fortnightly subcontractor payroll invoices covering multiple trades (groundworks, structural, fit-out, M&E, etc.).
- Current verification is manual or absent — site records are fragmented across paper, email, and separate access-control systems.
- The commercial risk is unverified labour claims inflating payroll spend; the recovery window closes once payment is made.
- Product is used inside a desktop browser by finance and HR staff, not on-site on mobile by workers.

## Capabilities and Constraints

- **Confirmed capabilities:** Invoice upload and line-item parsing; attendance record import; cross-referencing engine; discrepancy reporting; audit trail per invoice; booking/enquiry flow for onboarding.
- **Calculator:** A savings calculator on the homepage and at `/calculator.html` models projected overpayment recovery based on annual payroll size and historical discrepancy rate.
- **Current implementation:** Single-file static HTML (`index.html`) with inline CSS and vanilla JS. No build step, no framework. Contact/booking at `contact.html`. Privacy policy and terms at `/privacy-policy/` and `/terms/`.
- **Undecided:** Pricing model and tiers; whether the platform becomes a logged-in SaaS product or remains a verification-as-a-service engagement.

## Brand Commitments

- **Name:** PayRoll Protect (two capitalised words, no space alternative).
- **Tagline register:** Financial precision, not tech enthusiasm. Language is specific and evidence-led — "verified attendance", "invoice discrepancy", "disputed claim" — not startup jargon.
- **Visual identity:** Dark, austere. Lime accent (`oklch(0.770 0.206 151)`) reserved for verified/approved states only. See DESIGN.md for the full system.
- **Logo assets:** `assets/pp-logo-hero.webp`, `assets/pp-logo-light-transp.webp`, `assets/favicon-light-sm.png`.

## Evidence on Hand

- Homepage copy with worked financial examples (£47,200 invoice; 3-worker discrepancy; £1,336 unrecoverable loss; £30,000 annual exposure on a 3% discrepancy rate on a £1M payroll).
- Before/after comparison widget demonstrating verified vs. unverified states.
- Calculator with configurable payroll size and discrepancy rate.
- FAQ section addressing common objections.
- No real customer testimonials or case studies in the current build — must not be fabricated.

## Product Principles

1. **Prove it before you pay it.** Every payment approval must be traceable to a specific piece of verified attendance evidence. The system exists to make "I checked" mean something.
2. **Granularity is the defence.** Total-level matching is not enough. The product's value lives in the individual line — the worker whose name appears on an invoice but not on a site record.
3. **Finance teams are the customer.** The product speaks to commercial risk and budget protection, not HR administration or workforce management. Every interface decision serves the person who signs off the invoice.
4. **Restraint signals rigour.** A product that verifies financial claims should look like it operates with discipline. Decoration is evidence of the wrong priorities.
5. **Recovery window is short.** Once money moves, it is gone. The product's urgency is pre-payment, not post-dispute.

## Accessibility & Inclusion

WCAG 2.1 AA. Minimum contrast 4.5:1 for normal text, 3:1 for large text and UI components. Keyboard navigation throughout. Focus indicators visible (current: 2px lime outline). All interactive elements have accessible labels. `prefers-reduced-motion` respected for all animations.
