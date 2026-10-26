---
title: User Stories and Tasks
---

# User Stories and Tasks — CampusConnect Marketplace

**Status:** Candidate stories derived from documented requirements; not yet confirmed as the team's actual or approved stories.

These stories translate the available project requirements into user-centred work. Before submission, compare them with the real project backlog and Trello cards. Keep, change or remove items according to the team's agreed scope.

## Story map and candidate tasks

### US-01 — University account access

**User story:** As an eligible university user, I want to register and sign in using my university email so that access to the marketplace is restricted to the intended community.

**Acceptance criteria**
- Registration requires the documented mandatory fields.
- The system rejects an email address already associated with an account.
- Authentication is required before protected marketplace functions can be used.
- Passwords are not stored as plain text.
- The team records the actual tests performed and their results.

**Candidate tasks**
- Confirm the allowed university email rule and validation behaviour.
- Design or verify the registration and sign-in flow.
- Implement or verify server-side validation and authentication.
- Test valid, invalid and duplicate registration scenarios.
- Document the test outcome and any unresolved issues.

**Priority proposal:** High, because access control supports the intended university-focused marketplace.  
**Estimate / owner / actual status:** [CONFIRM]

### US-02 — Create and manage a listing

**User story:** As a seller, I want to create and manage a listing so that other users can discover an item I offer.

**Acceptance criteria**
- A listing records the required seller, title, description, price and category.
- Price validation prevents negative values.
- Users can manage only listings permitted by the implemented authorisation rules.
- Removed or inactive listings do not appear as ordinary active results.
- Actual behaviour is verified against the implementation.

**Candidate tasks**
- Confirm required listing fields and validation rules.
- Implement or verify listing creation and editing.
- Implement or verify deletion/removal and listing status.
- Test ownership and validation rules.
- Capture a genuine test result or screenshot.

**Priority proposal:** High, because listings are central to the marketplace.  
**Estimate / owner / actual status:** [CONFIRM]

### US-03 — Search and filter listings

**User story:** As a buyer, I want to search and filter listings by relevant attributes so that I can find suitable items efficiently.

**Acceptance criteria**
- A user can search by item name or title as supported by the implementation.
- Available category and price filters return matching listings.
- Empty or unmatched searches produce a clear result state.
- Inactive or removed listings are excluded from normal active results.

**Candidate tasks**
- Confirm which search fields and filters are in the approved scope.
- Implement or verify search and filtering.
- Test matching, no-match and filter-combination scenarios.
- Record actual test outcomes.

**Priority proposal:** High.  
**Estimate / owner / actual status:** [CONFIRM]

### US-04 — Contact a seller

**User story:** As a buyer, I want to message a seller about a listing so that I can clarify item details before arranging an exchange.

**Acceptance criteria**
- A message is associated with the relevant listing and sender/recipient.
- Only permitted users can access the relevant conversation.
- The implementation avoids unnecessarily exposing personal contact information.
- Message handling and authorisation are tested.

**Candidate tasks**
- Confirm the messaging workflow and privacy requirements.
- Design or verify the message data structure.
- Implement or verify message creation and retrieval.
- Test access restrictions and listing association.
- Document known limitations.

**Priority proposal:** Medium to high; confirm dependencies and actual project scope.  
**Estimate / owner / actual status:** [CONFIRM]

### US-05 — Review and rate a user

**User story:** As a marketplace user, I want to submit a rating and review associated with an exchange so that other users can make more informed trust decisions.

**Acceptance criteria**
- Ratings are restricted to the documented 1–5 range.
- A review records the reviewer, reviewed user and associated listing.
- Invalid rating values are rejected.
- The team verifies any eligibility rules for submitting a review.

**Candidate tasks**
- Confirm when a review is permitted.
- Implement or verify rating validation and review storage.
- Test valid and invalid rating values.
- Verify that review details are associated with the correct listing and users.

**Priority proposal:** Medium; confirm dependencies and planned release.  
**Estimate / owner / actual status:** [CONFIRM]

### US-06 — Moderate reported or inappropriate content

**User story:** As an administrator, I want to review and moderate inappropriate listings so that the marketplace can be managed responsibly.

**Acceptance criteria**
- Administrative actions are restricted to accounts with the required role.
- The system records the moderation action and reason where required by the documented rules.
- Removed or inactive listings are no longer shown as normal active results.
- Access-control and moderation behaviour are tested.

**Candidate tasks**
- Confirm the moderation workflow and administrator permissions.
- Implement or verify the protected moderation interface and actions.
- Record action details as supported by the design.
- Test administrator and non-administrator access.
- Document the actual results and any gaps.

**Priority proposal:** Medium to high because it supports trust and control; confirm with the team.  
**Estimate / owner / actual status:** [CONFIRM]

### US-07 — Choose an approved collection point

**User story:** As a buyer or seller, I want to identify an approved collection point where supported so that the handover can be coordinated around an accepted location.

**Acceptance criteria**
- Only collection points approved and active in the system can be selected for supported handovers.
- The chosen point corresponds to the intended collection location.
- The actual workflow and limitations are documented.

**Candidate tasks**
- Confirm the collection-point workflow and locations in scope.
- Verify the data model and active/inactive rules.
- Implement or verify selection behaviour.
- Test invalid or inactive collection points.

**Priority proposal:** Medium; confirm dependencies and scope.  
**Estimate / owner / actual status:** [CONFIRM]

## Traceability to project requirements

| Story | Documented requirement area |
|---|---|
| US-01 | University email access, unique accounts, authentication and password security |
| US-02 | Listing fields, seller ownership, price validation and listing status |
| US-03 | Search, filtering and active listing results |
| US-04 | Buyer–seller messaging and privacy |
| US-05 | Reviews and 1–5 rating range |
| US-06 | Role-restricted administration and moderation records |
| US-07 | Approved collection points |

## Task tracking fields to complete from the real board

| Story ID | Actual Trello card / link | Task owner | Estimate | Current status | Evidence |
|---|---|---|---|---|---|
| US-01 | [ADD] | [ADD] | [ADD or N/A] | [CONFIRM] | [ADD] |
| US-02 | [ADD] | [ADD] | [ADD or N/A] | [CONFIRM] | [ADD] |
| US-03 | [ADD] | [ADD] | [ADD or N/A] | [CONFIRM] | [ADD] |
| US-04 | [ADD] | [ADD] | [ADD or N/A] | [CONFIRM] | [ADD] |
| US-05 | [ADD] | [ADD] | [ADD or N/A] | [CONFIRM] | [ADD] |
| US-06 | [ADD] | [ADD] | [ADD or N/A] | [CONFIRM] | [ADD] |
| US-07 | [ADD] | [ADD] | [ADD or N/A] | [CONFIRM] | [ADD] |

## Individual reflection — Paul Khumalo

**Drafting status: Not written because personal experience has not yet been confirmed.**

Reflect on which story or task you personally contributed to, how you helped define or test acceptance criteria, what changed after feedback, and what you learned about breaking requirements into manageable work. Include one specific example supported by actual evidence.

**Reflection to complete:** [ADD your own account; do not claim ownership of tasks without confirmation.]
