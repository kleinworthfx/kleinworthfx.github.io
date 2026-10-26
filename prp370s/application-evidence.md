---
title: Digital Payment Solution — Application Evidence
---

# Application Evidence — PayTrader

**Source reviewed:** `DigitalPaymentSolution.zip`, including its README, HTML pages, JavaScript, Express routes, controllers, models and configuration.

This page records what is visible in the supplied source archive. It is not a claim that the application has been run, fully tested, deployed or accepted by users.

## 1. Problem and proposed value

The submitted Professional Practice 3 report (13 March 2026) describes informal traders in busy Cape Town trading areas who may lose sales when customers cannot pay digitally and who face risks from carrying cash. The proposed value proposition is a simple, affordable phone-based way to accept digital payments, reducing dependence on cash and avoiding the need for a trader to purchase an expensive card machine.

The report says the team conducted eight short interviews and includes a summary of their feedback. Use that report as the evidence source for the interview findings; do not claim the interviews establish the views of all informal traders.

## 2. Features visible in the source archive

| Feature area | Evidence in the supplied code | Important qualification |
|---|---|---|
| Trader registration | `frontend/register.html`, `backend/controllers/authController.js` | Source contains registration logic; successful end-to-end testing is not confirmed here |
| Trader login | `frontend/login.html`, `backend/controllers/authController.js` | Uses bcrypt password hashing and JWT creation in source |
| Unique trader ID and QR code | `authController.js`, `dashboard.html` | The QR payload encodes the trader ID; verify how scanning is handled in the actual app |
| Customer payment flow | `frontend/payment.html`, `backend/controllers/paymentController.js` | Explicitly simulated; no real funds move |
| Trader dashboard | `traderController.js`, `dashboard.html` | Source calculates daily and total payment figures and recent transactions |
| Transaction history | `traderRoutes.js`, `paymentController.js`, `history.html` | Source supports retrieval of a trader's payment history |
| Profile management | `traderController.js`, `profile.html` | Source includes profile read/update handlers |
| Admin overview | `adminRoutes.js`, `adminController.js`, `admin.html` | Source includes protected endpoints for trader list, payment list and totals |
| Persistence | `backend/config/db.js` | The supplied configuration uses JSON files, not a configured production database |
| Authentication and role checks | `backend/middleware/auth.js` | Source verifies JWTs and restricts admin routes to the admin role |

## 3. Architecture and technology

The supplied source archive describes a browser-based application with:

- **Frontend:** HTML, CSS, vanilla JavaScript, Bootstrap 5 and Font Awesome.
- **Backend:** Node.js and Express.
- **Authentication:** JSON Web Tokens (JWT) and bcryptjs password hashing.
- **QR code generation:** the `qrcode` npm package.
- **Data storage:** JSON files created by the backend's database helper.
- **API structure:** separate route/controller modules for authentication, trader functions, payments and administration.

These are source-derived technology descriptions. They do not establish production readiness, deployment or security certification.

## 4. Payment limitation — important

The payment controller contains a comment stating that the flow is simulated and no real money moves. The code validates a positive amount, records a payment with a successful status, creates a reference and updates the trader's stored wallet balance. Those records represent a prototype simulation, not a verified bank transfer or settled payment.

The project README lists real payment gateway integration, QR scanning through the device camera, notifications and bank settlement as future improvements. Do not claim these are implemented in the supplied source.

## 5. Suggested evidence to capture

Capture only after opening and using the actual app. Keep screenshots free of passwords, tokens and real personal/payment data.

- [ ] Landing page describing the problem and proposed value.
- [ ] Trader registration form and a successful test account creation.
- [ ] Trader dashboard showing the generated trader ID and QR code.
- [ ] Customer payment flow with an explicitly labelled simulated payment.
- [ ] Transaction history after a test payment.
- [ ] Profile page and a verified profile update.
- [ ] Admin overview using a test admin account.
- [ ] Test notes for invalid login, duplicate email, unknown trader ID, invalid amount and role-restricted admin access.
- [ ] Record the test date, steps, expected result, actual result and any defect for each test performed.

**Testing status:** Not independently executed during this source review. Add test outcomes only after running the application.

## 6. Quality and risk observations from code inspection

These are review observations, not proof that an exploit occurred:

- The QR code payload is the trader ID. The source comment describes a URL shape, but the QR payload itself is not a complete URL; test real-device scanning before claiming scan-to-pay works directly.
- Trader IDs and payment references are generated using random numbers; the source does not show a uniqueness check for these generated values.
- The JSON file storage is described as a zero-setup prototype and is not a production-grade database for concurrent writes.
- The public payment endpoint records a simulated success rather than verifying a real provider's payment confirmation.
- The `getStats` controller sums all stored payment amounts without filtering by payment status. Verify intended reporting behaviour before treating the totals as authoritative.
- The supplied source uses `JWT_SECRET` from the environment; a strong, private secret must be configured before local use. Never publish a real `.env` file or token.
- The presence of authentication middleware does not by itself prove that the full application has been security-tested.

## 7. Reflection prompt — Paul Khumalo

Complete this section in your own words after confirming your actual contribution:

1. Which part of the application did you personally research, design, code, document or test?
2. What requirement did that work address for informal traders?
3. What evidence can you show (commit, code file, Trello card, screenshot, test record or report section)?
4. What technical or teamwork challenge did you personally encounter?
5. What did you learn, and what would you change in a future iteration?

**Personal reflection:** [ADD a first-person account based on your actual work. Do not claim authorship of code or testing without confirming it.]
