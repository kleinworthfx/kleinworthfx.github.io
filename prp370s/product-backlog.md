---
title: Product Backlog
---

# Product Backlog — Digital Payment Solution

**Status:** Candidate backlog derived from the submitted research report and supplied PayTrader source archive. The order below is a proposal, not a claim about the team's actual Trello priorities.

## Product vision

Provide informal traders with an accessible way to try accepting digital payments through a phone-based platform, reducing reliance on cash and avoiding the need for a conventional card machine. The 13 March 2026 report proposes QR codes/payment links and a small transaction fee. The supplied source is a prototype with simulated payments, not a live payment processor.

## Candidate product backlog

| ID | Product backlog item | User value / rationale | Proposed priority | Dependency / acceptance focus | Actual team priority and status |
|---|---|---|---|---|---|
| PB-01 | Trader registration | Allows a trader to create an account | High | Required fields, duplicate email handling, password hashing | [CONFIRM from Trello] |
| PB-02 | Trader login and protected access | Keeps account pages restricted | High | JWT creation, token validation, role/access checks | [CONFIRM from Trello] |
| PB-03 | Trader ID and QR-code generation | Gives each trader a payment identifier | High | ID creation, QR payload, display and scan test | [CONFIRM from Trello] |
| PB-04 | Customer trader lookup | Identifies the intended recipient | High | Valid and unknown trader IDs | [CONFIRM from Trello] |
| PB-05 | Simulated payment flow | Demonstrates the proposed customer journey | High for prototype demonstration | Positive amount validation, record/reference creation; clearly label as simulation | [CONFIRM from Trello] |
| PB-06 | Trader dashboard | Helps trader review recorded activity | High | Daily/total summary, recent records and correct calculations | [CONFIRM from Trello] |
| PB-07 | Transaction history | Helps trader review recorded transactions | Medium–high | Protected access, ordering, search and account boundaries | [CONFIRM from Trello] |
| PB-08 | Profile management | Lets trader maintain supported details | Medium | Correct account association and persistence | [CONFIRM from Trello] |
| PB-09 | Admin trader/payment overview | Helps administrator inspect prototype activity | Medium | Admin-only access, safe data output, correct totals | [CONFIRM from Trello] |
| PB-10 | Stronger data persistence | Improves reliability beyond local JSON files | Future improvement | Evaluate database choice and concurrent writes | [CONFIRM scope] |
| PB-11 | Real payment gateway integration | Would support actual payment processing | Future / out of current supplied prototype | Provider integration, verified payment callbacks, security and compliance review | [CONFIRM if scope changes] |
| PB-12 | Camera-based QR scanning and direct URL payload | Makes scan-to-pay easier | Future improvement / verify current behaviour first | Test on real devices and confirm the QR destination | [CONFIRM scope] |
| PB-13 | Receipts and notifications | Improves payment communication | Future improvement | Email/SMS provider and privacy requirements | [CONFIRM scope] |

**Priority note:** This table orders candidate work by the apparent core prototype journey. Replace the proposed order with the actual priorities and reasoning shown on the team's Trello board.

## Why the proposed order starts with access and payment flow

Registration, authentication, trader identity and payment flow form a coherent demonstration path: a trader creates an account, receives an identifier, a customer identifies the trader, and the prototype records a simulated payment. The dashboard and history then allow the trader to inspect that recorded activity. This is a suggested planning rationale, not a verified historical team decision.

## Scope and implementation boundaries

Based on the supplied source archive and README:

- The prototype includes trader registration/login, QR-code generation, a customer-facing simulated payment flow, dashboard summaries, transaction history, profile management and an admin overview.
- The source uses JSON-file persistence in `backend/data` via `backend/config/db.js`.
- The payment controller explicitly says that no real money moves.
- The README lists real payment gateway integration, camera-based QR scanning, SMS/email notifications and bank settlement as future improvements.

Do not describe future improvements as completed features. Confirm the approved scope from Trello before treating any proposed backlog item as accepted.

## Backlog refinement history

| Date | Item(s) reviewed | Actual change | Reason / evidence | Decision owner |
|---|---|---|---|---|
| [ADD actual date] | [ADD from Trello activity] | [ADD] | [ADD] | [ADD] |

Do not invent historical refinement events. If Trello does not preserve the history, note that limitation.

## Estimates and task ownership

The current supplied source and research report do not establish actual story-point estimates or task owners for software development. Populate those fields from the board rather than guessing.

| Backlog ID | Actual estimate | Actual owner(s) | Actual status | Trello card |
|---|---|---|---|---|
| PB-01 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |
| PB-02 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |
| PB-03 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |
| PB-04 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |
| PB-05 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |
| PB-06 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |
| PB-07 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |
| PB-08 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |
| PB-09 | [ADD/N/A] | [ADD] | [CONFIRM] | [ADD] |

## Individual reflection — Paul Khumalo

Reflect on a real prioritisation decision you were involved in. What user need did it address? What dependency or constraint affected the decision? Did the team change its mind after feedback or testing? What did you personally learn about prioritising an MVP?

**Reflection:** [ADD first-person reflection grounded in an actual board item or project decision.]
