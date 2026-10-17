# BhumiShield — Citizen Land Security Portal

BhumiShield is an independent, citizen-facing prototype for Bangladesh focused on **P3: Catch Fraud & Double-Selling**. The portal helps a citizen spot inconsistencies in manually entered sample land data before they pay or proceed with a transaction. It is not a government portal and does not establish legal ownership.

## Files

- `index.html` — page structure, forms and accessible interface
- `styles.css` — responsive government-service-inspired visual theme
- `app.js` — bilingual interface, rule-based demo checks, review queue and exports

These are the three website source files.

## Run locally

1. Extract the ZIP.
2. Open a terminal in the extracted folder.
3. Run `python -m http.server 8080`.
4. Open `http://localhost:8080`.

Internet access is needed for Google Fonts. The website itself does not need a build step.

## P3 features

1. **Possible double-selling check:** compares division, district, upazila, mouza, khatian and dag against a tiny, fictional in-code sample registry. The sample intentionally contains two transactions for one sample parcel to demonstrate a warning.
2. **Registration vs mutation comparison:** compares deed reference, khatian, dag, buyer/owner reference and entered area, and flags pending/unknown mutation status.
3. **Deed warning signals:** checks missing fields, registration/deed date order, same seller/buyer reference, non-positive area and deed-number matches in the sample data. It cannot authenticate signatures or determine whether a deed is genuine.
4. **Review queue:** adds findings, changes review status, removes entries and exports JSON/CSV. Queue data is stored locally in this browser using localStorage.
5. **Citizen checklist and official links:** provides practical due-diligence reminders and external links to official services.
6. **Bangla/English:** interface toggle, responsive forms and keyboard-friendly controls.

## Data, privacy and limits

- All in-app transaction records are invented demonstration data. No live government land records are queried.
- Do not enter real NID numbers, phone numbers, private records or confidential personal data.
- A match or warning is not a legal conclusion. No match in demo data does not mean a plot is safe.
- Government land-service links open external websites; no applications or payments are submitted here.
- The review queue is browser-local and is not backed up or transmitted to a server.
- Real deployments would require authorized data-sharing agreements, authenticated official APIs, role-based access, audit logs, encryption, security review and legal validation. Do not scrape or bulk-download government websites.

## Official destinations

- Ministry of Land: https://land.gov.bd/
- e-Mutation: https://mutation.land.gov.bd/
- Land Development Tax: https://ldtax.gov.bd/
- Department of Land Records and Surveys: https://dlrs.gov.bd/

Check current official instructions directly with the relevant authority before relying on them.

## AI and tools disclosure

ChatGPT (OpenAI) was used to assist with drafting and code iteration. The team should review, test and understand all code before publishing.

## Suggested testing

- Toggle Bangla/English and test mobile navigation.
- In double-selling check, try `Dhaka / Gazipur / Kaliakair / Demo Mouza 07 / 12 / K-104 / D-778` to see the fictional duplicate signal.
- Compare matching and mismatching registration/mutation fields.
- Check date order, blank fields and same buyer/seller in the deed form.
- Add a result to the review queue, change status, delete it, refresh the page, and export JSON/CSV.
- Confirm every warning clearly states that official records were not checked.
