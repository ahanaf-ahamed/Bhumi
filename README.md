BhumiShield — Citizen Land Security Portal

BhumiShield is an independent, citizen-facing prototype for Bangladesh focused on P3: Catch Fraud & Double-Selling. It helps people identify inconsistencies in manually entered sample land information before paying for or proceeding with a transaction. It is not a government portal and does not establish legal ownership.

Website files

• index.html — page structure, forms and accessible interface.
• styles.css — responsive government-service-inspired theme.
• app.js — bilingual interface, rule-based demonstration checks, review queue and exports.

These are the three website source files.

Run locally

1. Extract the ZIP archive.
2. Open a terminal in the extracted folder.
3. Run python -m http.server 8080.
4. Open http://localhost:8080 in a browser.

No build step is required. An internet connection may be needed for externally hosted fonts or other CDN-hosted visual resources.

Main features

1. Possible double-selling check: compares location and parcel references (division, district, upazila, mouza, khatian and dag/plot) against a small fictional sample registry. The sample deliberately includes a duplicate scenario to demonstrate a warning.
2. Registration versus mutation comparison: compares entered deed reference, khatian, dag/plot, buyer/owner reference and area, and flags a pending or unknown mutation status for review.
3. Deed warning signals: checks missing fields, date order, same seller/buyer reference, non-positive area and duplicate deed references within the sample data. It cannot authenticate a signature or prove that a deed is genuine.
4. Review queue: allows findings to be saved for review, status to be changed, entries to be removed and the queue to be exported as JSON/CSV. Queue data is stored in this browser using localStorage.
5. Citizen due-diligence checklist: provides reminders about checking deed registration, khatian, dag, land area, mutation, tax, possible disputes, mortgage/encumbrance and physical boundaries with the appropriate authorities.
6. Bangla and English: language toggle and responsive forms.
7. Official service links: links to government portals as external destinations; it does not submit applications or payments.

Data used

• All in-app transaction and parcel examples are fictional demonstration data, including the duplicate-sale example.
• No live government land records are queried, scraped or bulk-downloaded.
• The prototype does not include verified cadastral parcel geometry or a live ownership database.
• Do not enter real NID numbers, phone numbers, private documents or confidential personal data.

Official destinations

• Ministry of Land: https://land.gov.bd/
• e-Mutation: https://mutation.land.gov.bd/
• Land Development Tax: https://ldtax.gov.bd/
• Department of Land Records and Surveys: https://dlrs.gov.bd/

Check the current instructions directly with the relevant authority. These links do not mean BhumiShield is integrated with those systems.

Technology and architecture

• Frontend: HTML5, CSS3 and vanilla JavaScript.
• Rule checks: client-side comparisons and validation rules over entered values and synthetic examples.
• Review queue: browser localStorage; JSON/CSV export generated in the browser.
• Deployment: static website, suitable for local demonstration or static hosting.
• Current limitation: no backend, user account service, official API integration, digital-signature validation, OCR or authoritative ownership verification.

AI tools disclosure

ChatGPT (OpenAI) was used to assist with drafting, design iteration and code development. The team must review, test and understand the code before publishing or presenting it.

Test checklist

• Switch between Bangla and English; test the layout on mobile and desktop.
• In the double-selling check, try the fictional sample location and parcel references shown in the interface or demo example.
• Compare matching and mismatching registration/mutation fields.
• Test blank fields, date order, same seller/buyer and invalid area.
• Add a finding to the review queue, change its status, remove it, refresh the page and export JSON/CSV.
• Confirm that all warnings are explained as screening signals and do not claim official verification.

Privacy, safety and field deployment

A match or warning is not a legal conclusion, and no match in this sample data does not mean a plot is safe. Citizens should verify original documents and relevant records through the appropriate Sub-Registry Office, Land Office and official services, and consult a qualified professional when necessary.

A field deployment would require authorized data-sharing agreements, authenticated official APIs, secure backend storage, access controls, audit logs, encryption, privacy review, legal validation, security testing and an operational support process. Do not scrape or bulk-download government websites.

Team and mentors

• Team leader: Ahanaf Ahamed — Student ID: 252-15-024
• Second student: Md. Riyazul Islam Riyad — Student ID: 252-15-312
• Faculty mentor: Md. Abdullah-Al-Kafi
• Industry mentor: Pritam Biswas

Repository URL:https://github.com/ahanaf-ahamed/Bhumi
Optional live URL :https://ahanaf-ahamed.github.io/Bhumi/