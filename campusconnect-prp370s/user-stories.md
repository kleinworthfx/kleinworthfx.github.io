---
title: CampusConnect — User Stories and Tasks
---

# User Stories and Tasks — CampusConnect Marketplace

**Status:** Candidate stories derived from the supplied functional requirements. Reconcile them with the actual Trello cards before claiming these were approved, estimated or completed by the team.

## Story format

A user story describes a capability from an end user's perspective. Tasks break the story into actionable work. Acceptance criteria describe observable conditions for acceptance; they are not test results.

## Candidate user stories

### US-01 — University account registration

**As a** student, **I want** to register using a valid university email address, **so that** access is restricted to the intended university community.

**Candidate acceptance criteria**
- Required fields are validated.
- An email address cannot be used to create duplicate accounts.
- Non-university email addresses are rejected according to the agreed rule.
- Passwords are not stored as plain text.

**Candidate tasks**
- Confirm the allowed university email-domain rule.
- Design the registration form and validation messages.
- Implement server-side validation and unique-email enforcement.
- Test valid, invalid, duplicate and incomplete submissions.

**Status / owner / Trello card:** [CONFIRM]

### US-02 — Sign in and protected access

**As a** registered user, **I want** to sign in and access permitted functions, **so that** my account and activity are protected.

**Candidate acceptance criteria**
- Valid credentials allow access.
- Invalid credentials are rejected without exposing sensitive details.
- Protected functions require authentication.
- Administrative functions require the administrator role.

**Candidate tasks**
- Implement login and logout flow.
- Apply authentication checks to protected routes.
- Apply role checks to administrator functions.
- Test valid, invalid and unauthorized access.

**Status / owner / Trello card:** [CONFIRM]

### US-03 — Create and manage a listing

**As a** seller, **I want** to create, edit and remove my own item listings, **so that** other students can discover items I offer.

**Candidate acceptance criteria**
- A listing requires a title, description, price and category.
- Price is a non-negative monetary value.
- The listing is associated with its seller.
- A user cannot edit or remove another user's listing unless an authorized administrative rule permits it.

**Candidate tasks**
- Define listing fields and database relationships.
- Build create/edit form validation.
- Implement ownership checks.
- Test required fields, invalid prices and unauthorized edits.

**Status / owner / Trello card:** [CONFIRM]

### US-04 — Search and filter listings

**As a** buyer, **I want** to search and filter listings by item name, category and price range, **so that** I can find relevant items efficiently.

**Candidate acceptance criteria**
- Search results match the agreed search fields.
- Category and price filters can be applied.
- Invalid price ranges are handled clearly.
- Removed or inactive listings do not appear as normal active results.

**Candidate tasks**
- Confirm filter combinations and sorting rules.
- Implement search/filter controls.
- Implement corresponding query logic.
- Test empty results, boundary prices and combined filters.

**Status / owner / Trello card:** [CONFIRM]

### US-05 — Communicate about a listing

**As a** buyer or seller, **I want** to message the other party about a listing, **so that** I can arrange the exchange without unnecessarily exposing personal contact details.

**Candidate acceptance criteria**
- Messages are associated with the relevant listing and sender/receiver.
- Only authorized participants can access a conversation.
- Empty messages are rejected.
- Message content is displayed safely.

**Candidate tasks**
- Define the message data model.
- Build the conversation UI.
- Implement authorization checks.
- Test access by unrelated users and invalid submissions.

**Status / owner / Trello card:** [CONFIRM]

### US-06 — Rate and review a transaction participant

**As a** user, **I want** to leave a rating and review associated with a listing, **so that** other users can make more informed decisions.

**Candidate acceptance criteria**
- Ratings remain within the defined 1–5 range.
- A review is associated with a reviewer, reviewed user and listing.
- Invalid rating values are rejected.
- The team defines and enforces whether a completed transaction is required before review.

**Candidate tasks**
- Confirm the review eligibility rule.
- Implement review form and validation.
- Store and display reviews.
- Test rating boundaries and invalid associations.

**Status / owner / Trello card:** [CONFIRM]

### US-07 — Moderate reported content

**As an** administrator, **I want** to review and moderate inappropriate listings, **so that** the marketplace remains accountable and safer to use.

**Candidate acceptance criteria**
- Only authorized administrators can access moderation actions.
- A moderation action records the affected listing, action type, reason and date.
- Inactive or removed listings are not shown as normal active results.

**Candidate tasks**
- Define moderation actions and permissions.
- Build the moderation view.
- Record the action and reason.
- Test role restrictions and listing status changes.

**Status / owner / Trello card:** [CONFIRM]

### US-08 — Choose an approved collection point

**As a** buyer and seller, **I want** to select an approved campus/library collection point, **so that** we can coordinate a practical handover.

**Candidate acceptance criteria**
- Only active approved collection points are selectable.
- The selected point is associated with the relevant workflow or listing/transaction record.
- Unavailable collection points cannot be selected.

**Candidate tasks**
- Confirm the supported campus and collection-point list.
- Define the data relationship.
- Implement selection and validation.
- Test inactive and missing collection points.

**Status / owner / Trello card:** [CONFIRM]

## Task decomposition and evidence register

| Story | Actual Trello card / task | Owner | Actual status | Evidence / test result |
|---|---|---|---|---|
| US-01 | [ADD] | [CONFIRM] | [CONFIRM] | [LINK / RESULT] |
| US-02 | [ADD] | [CONFIRM] | [CONFIRM] | [LINK / RESULT] |
| US-03 | [ADD] | [CONFIRM] | [CONFIRM] | [LINK / RESULT] |
| US-04 | [ADD] | [CONFIRM] | [CONFIRM] | [LINK / RESULT] |
| US-05 | [ADD] | [CONFIRM] | [CONFIRM] | [LINK / RESULT] |
| US-06 | [ADD] | [CONFIRM] | [CONFIRM] | [LINK / RESULT] |
| US-07 | [ADD] | [CONFIRM] | [CONFIRM] | [LINK / RESULT] |
| US-08 | [ADD] | [CONFIRM] | [CONFIRM] | [LINK / RESULT] |

## Individual reflection — Paul Khumalo

**Prompt:** Choose one story or task you personally worked on. Explain the requirement, your specific contribution, one technical or coordination challenge, how you addressed it, the outcome and the evidence that supports your account.

**[PAUL REFLECTION — do not submit the prompt as a completed reflection.]**

## Evidence checklist

- [ ] Actual Trello story and task cards linked.
- [ ] Priority, estimate, owner and status copied from real records.
- [ ] Acceptance criteria checked against the agreed implementation.
- [ ] Genuine test results or screenshots linked.
- [ ] Individual contribution and reflection confirmed.
