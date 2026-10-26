---
title: User Stories and Tasks
---

# User Stories and Tasks — Digital Payment Solution

**Status:** Candidate stories derived from the supplied research report and application source. They are not a substitute for the team's actual Trello cards.

These stories describe the intended user value of PayTrader and provide a basis for checking the implementation. Reconcile each story with the current Trello board, the team's approved scope and the real behaviour before submitting.

## US-01 — Register as a trader

**User story:** As an informal trader, I want to register an account so that I can use the platform to receive and track simulated digital payments.

**Acceptance criteria to verify**
- The form collects the required name, surname, email, phone and password fields.
- An existing email address is rejected.
- The supplied source hashes the password before storage.
- Successful registration returns a session token and trader account information.
- The test result is recorded after actually running the flow.

**Candidate tasks**
- Confirm registration fields and validation rules.
- Verify frontend registration and API request.
- Verify duplicate email and password handling.
- Test successful and failed registration.
- Capture a genuine screenshot/test note.

**Source files to inspect:** `frontend/register.html`, `backend/controllers/authController.js`, `backend/models/User.js`.  
**Actual Trello card / owner / estimate / status:** [ADD from board]

## US-02 — Sign in securely

**User story:** As a registered trader, I want to sign in so that I can access my dashboard and account information.

**Acceptance criteria to verify**
- Valid credentials return a JWT session.
- Invalid credentials are rejected.
- Protected routes reject requests without a valid bearer token.
- Passwords are checked using the stored hash rather than plain-text comparison.

**Candidate tasks**
- Verify login form and API call.
- Verify JWT creation and verification.
- Test correct and incorrect credentials.
- Test access to protected routes with and without a token.
- Record actual results and defects.

**Source files to inspect:** `frontend/login.html`, `backend/controllers/authController.js`, `backend/middleware/auth.js`.  
**Actual Trello card / owner / estimate / status:** [ADD from board]

## US-03 — Generate and view a trader QR code

**User story:** As a trader, I want a unique trader ID and QR code so that customers can identify the trader when making a payment.

**Acceptance criteria to verify**
- Registration creates a trader ID and QR image.
- The dashboard displays the generated code and trader ID.
- The team verifies whether scanning the code on a real device reaches the correct payment flow.
- Any QR scanning limitation is documented accurately.

**Candidate tasks**
- Verify ID generation and QR-code creation.
- Verify the dashboard renders the QR image.
- Test the QR payload and scan behaviour.
- Record whether the QR contains a trader ID or a full payment URL.
- Capture a genuine screenshot.

**Source files to inspect:** `backend/controllers/authController.js`, `backend/controllers/traderController.js`, `frontend/dashboard.html`.  
**Actual Trello card / owner / estimate / status:** [ADD from board]

## US-04 — Make a simulated payment to a trader

**User story:** As a customer, I want to identify a trader and enter a payment amount so that I can experience the proposed digital-payment flow.

**Acceptance criteria to verify**
- The customer can look up a valid trader ID.
- Unknown trader IDs are rejected.
- The amount must be a positive number.
- The system records a simulated payment and reference.
- The confirmation page clearly represents a simulation, not a real bank transfer.

**Candidate tasks**
- Verify trader lookup.
- Verify customer form and payment method choices.
- Test valid and invalid amounts.
- Verify payment record creation and reference.
- Confirm dashboard/history reflects the test transaction.
- Label the feature as simulated in the documentation and demo.

**Source files to inspect:** `frontend/payment.html`, `backend/controllers/paymentController.js`, `backend/models/Payment.js`.  
**Important scope note:** the supplied payment controller explicitly states that no real money moves. Real payment-gateway integration is listed as future work.  
**Actual Trello card / owner / estimate / status:** [ADD from board]

## US-05 — View sales summary

**User story:** As a trader, I want to see my daily and total sales summaries so that I can review the activity recorded by the prototype.

**Acceptance criteria to verify**
- The dashboard shows daily and total payment figures and recent transactions.
- Displayed values are consistent with the test records.
- The team confirms how failed payments, if present, should be treated in totals.
- The summary is described as prototype data rather than verified settlement information.

**Candidate tasks**
- Verify dashboard endpoint and display.
- Create test records in a controlled test environment.
- Compare displayed totals with records.
- Check status filtering and date-boundary behaviour.
- Record actual results.

**Source files to inspect:** `backend/controllers/traderController.js`, `backend/models/Payment.js`, `frontend/dashboard.html`.  
**Actual Trello card / owner / estimate / status:** [ADD from board]

## US-06 — Review transaction history

**User story:** As a trader, I want to view my recorded transactions so that I can review customer names, amounts, methods and references.

**Acceptance criteria to verify**
- An authenticated trader can retrieve their own history.
- Results are ordered newest first as implemented.
- Search behaves as intended in the interface.
- One trader cannot retrieve another trader's history.

**Candidate tasks**
- Verify protected history route.
- Verify history rendering and search.
- Test empty and populated history.
- Test account-level access boundaries.
- Record results and any gaps.

**Source files to inspect:** `backend/routes/traderRoutes.js`, `backend/controllers/paymentController.js`, `frontend/history.html`.  
**Actual Trello card / owner / estimate / status:** [ADD from board]

## US-07 — Manage trader profile

**User story:** As a trader, I want to view and update my profile so that my contact information remains current.

**Acceptance criteria to verify**
- The profile page loads the authenticated trader's information.
- Supported fields can be updated.
- Account identity fields that should be fixed are not editable through the form.
- A successful update persists and is reflected on reload.

**Candidate tasks**
- Verify profile endpoint and form.
- Test a valid profile update.
- Test missing/invalid values and confirm intended validation.
- Verify the updated values persist.
- Record the actual result.

**Source files to inspect:** `backend/controllers/traderController.js`, `frontend/profile.html`.  
**Actual Trello card / owner / estimate / status:** [ADD from board]

## US-08 — View platform information as an administrator

**User story:** As an administrator, I want to view trader accounts and recorded payments so that I can monitor prototype activity.

**Acceptance criteria to verify**
- Admin endpoints require a valid token and admin role.
- A trader account cannot access admin-only endpoints.
- Password hashes are not included in the trader list response.
- The reported totals are checked against the stored test records.

**Candidate tasks**
- Verify admin route middleware.
- Create a test admin using the documented utility in a safe local environment.
- Test admin and non-admin access.
- Compare reported totals to test data.
- Record findings and limitations.

**Source files to inspect:** `backend/routes/adminRoutes.js`, `backend/middleware/auth.js`, `backend/controllers/adminController.js`, `frontend/admin.html`.  
**Actual Trello card / owner / estimate / status:** [ADD from board]

## Traceability summary

| Story | User value | Source evidence |
|---|---|---|
| US-01 | Trader can create an account | Registration page, auth controller, user model |
| US-02 | Trader can access an account | Login page, JWT creation and middleware |
| US-03 | Trader can identify their payment profile | Trader ID and QR code logic, dashboard |
| US-04 | Customer can try the payment journey | Payment page and simulated payment controller |
| US-05 | Trader can inspect recorded sales | Dashboard controller and page |
| US-06 | Trader can inspect recorded transactions | Protected history route and page |
| US-07 | Trader can maintain profile details | Profile controller and page |
| US-08 | Admin can inspect platform activity | Admin middleware, routes, controller and page |

## Actual board mapping — complete from Trello

| Story | Trello card/link | Owner | Estimate | Current status | Evidence or test result |
|---|---|---|---|---|---|
| US-01 | [ADD] | [ADD] | [ADD/N/A] | [CONFIRM] | [ADD] |
| US-02 | [ADD] | [ADD] | [ADD/N/A] | [CONFIRM] | [ADD] |
| US-03 | [ADD] | [ADD] | [ADD/N/A] | [CONFIRM] | [ADD] |
| US-04 | [ADD] | [ADD] | [ADD/N/A] | [CONFIRM] | [ADD] |
| US-05 | [ADD] | [ADD] | [ADD/N/A] | [CONFIRM] | [ADD] |
| US-06 | [ADD] | [ADD] | [ADD/N/A] | [CONFIRM] | [ADD] |
| US-07 | [ADD] | [ADD] | [ADD/N/A] | [CONFIRM] | [ADD] |
| US-08 | [ADD] | [ADD] | [ADD/N/A] | [CONFIRM] | [ADD] |

## Individual reflection — Paul Khumalo

Write about a user story or task you personally contributed to. Explain what requirement you worked from, what you did, how you verified the result, what changed after feedback and what you learned about turning a user need into testable work.

**Reflection:** [ADD Paul's first-person account using a real example and supporting evidence.]
