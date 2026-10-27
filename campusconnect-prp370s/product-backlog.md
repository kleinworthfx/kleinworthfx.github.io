---
title: CampusConnect — Product Backlog
---

# Product Backlog — CampusConnect Marketplace

**Status:** Candidate backlog based on the documented requirements. This ordering is a proposed starting point, not proof of the team's historical prioritisation. Replace it with the actual Trello backlog order, estimates and status before final submission.

## Prioritisation rationale

The draft ordering prioritises account access and core listing discovery before communication, trust and moderation flows. The actual sequence should reflect the team's agreed dependencies, risk, time and stakeholder feedback.

| Candidate priority | Item | User value / rationale | Dependencies | Actual Trello priority / status |
|---:|---|---|---|---|
| 1 | University email registration and validation | Establishes the intended university-only access boundary. | Agreed email-domain rule; user data model | [CONFIRM] |
| 2 | Login, authentication and role checks | Protects user accounts and restricted functions. | User model; session/token approach | [CONFIRM] |
| 3 | Listing create, edit and delete | Enables the marketplace's core seller workflow. | Authentication; listing/category model | [CONFIRM] |
| 4 | Listing search and filters | Helps buyers find items by name, category and price range. | Listing data; agreed filter rules | [CONFIRM] |
| 5 | Profiles and seller information | Provides context for marketplace participants. | User/profile model | [CONFIRM] |
| 6 | Buyer–seller messaging | Supports questions and handover coordination. | Authentication; listing ownership/association | [CONFIRM] |
| 7 | Collection-point selection | Supports safer, structured campus handovers. | Approved collection-point data | [CONFIRM] |
| 8 | Reviews and ratings | Supports trust and accountability. | Review eligibility rule; listing/user relationships | [CONFIRM] |
| 9 | Admin moderation and action log | Supports removal of inappropriate content and accountability. | Admin role; listing status; audit fields | [CONFIRM] |
| 10 | Responsive layout and accessibility refinement | Improves usability on desktop and mobile browsers. | Main user journeys | [CONFIRM] |
| 11 | Notifications and richer transaction workflow | Possible improvement beyond the initial core scope. | Event model; agreed scope | [CONFIRM whether in scope] |

## Backlog item template

For each actual Trello card, record:

- **ID / title:** [ADD exact card details]
- **User story:** [LINK or paste]
- **Priority:** [COPY actual priority]
- **Estimate:** [COPY actual estimate or state not estimated]
- **Owner:** [CONFIRM]
- **Acceptance criteria:** [ADD agreed criteria]
- **Dependencies:** [ADD]
- **Status:** [COPY current actual status]
- **Evidence:** [LINK to code, design, screenshot or test]
- **Change history:** [ADD only if supported by board activity]

## Backlog quality checks

- Is each item understandable and valuable to a user?
- Are acceptance criteria observable and testable?
- Are dependencies and security requirements identified?
- Are estimates and priorities taken from the actual team process?
- Are out-of-scope ideas labelled as future enhancements?
- Is completed work supported by evidence rather than a card label alone?

## Scope notes from the supplied documentation

The project documents include university email access, listings, search/filtering, messaging, ratings/reviews, moderation and approved collection points. They exclude a native mobile app and an integrated payment gateway from the initial scope. Do not add payment processing as a required initial backlog item unless a later, documented team decision changed the scope.

## Individual reflection — Paul Khumalo

**Prompt:** Describe one real prioritisation decision. What did you or the team choose, what information informed the choice, what trade-off was involved, and what did you learn? Link the actual board history or decision record.

**[PAUL REFLECTION — complete using a true event.]**

## Evidence checklist

- [ ] Actual product backlog screenshot/link.
- [ ] Confirmed order, labels, estimates and status.
- [ ] Evidence of changes to priority over time, if any.
- [ ] Rationale grounded in an actual decision or documented requirement.
- [ ] Individual reflection based on real evidence.
