# CAS API Tracker

A free, single-page web app that helps college teachers in **West Bengal Government-aided colleges** calculate their **API (Academic Performance Indicator) score** for **CAS promotion** — and assemble a print-ready dossier — without spreadsheets, logins, or installation.

**▶ Use it now: https://ourbee.github.io/cas-api-tracker/**

Built to the rules in **G.O. 1373-Edn(CS) dated 07.12.2017** and the **UGC Regulations 2016 (4th Amendment)**.

---

## What it does

CAS (Career Advancement Scheme) promotions require you to score your teaching, co-curricular, administrative and research work against a fixed points system, session by session, and present it in a specific committee format. Doing this by hand is slow and easy to get wrong — especially the rules about what may *not* be counted twice.

This app does the arithmetic for you and keeps the format correct. You type in what you did; it works out the API score live, flags anything counted twice, and lays everything out as the proforma the Screening-cum-Evaluation Committee and Governing Body expect.

It covers:

- **Category I** (assessed each year) — direct teaching, examination duties, and innovative/ICT-aided teaching.
- **Category II** (cumulative) — student co-curricular and extension activities, committee and administrative work, and professional development.
- **Category III** (cumulative) — research, publications, paper presentations, and academic lectures, with impact-factor (IF) augmentation.
- **All promotion stages** — Stage 1→2, Stage 2→3, and Stage 3→4 (to Associate Professor).
- **Double-count reconciliation** — the same activity (e.g. remedial classes, mentoring, a lecture) can qualify under more than one head; the app makes sure it is counted **once only**, as the rules require.
- **A printable dossier** — Part A (general information), Part B (Category I & II sheets, one per academic session, plus the Category III cumulative sheet), Part C (for the Screening-cum-Evaluation Committee), and Part D (for the Governing Body), with an annexure checklist for your evidence.

## Why you might want it

- **Nothing to install.** It runs in any modern web browser (Chrome, Edge, Firefox, Safari). You can also save the single `index.html` file and open it offline by double-clicking it.
- **Your data stays with you.** Everything you enter is stored **only in your own browser** (in "local storage"). Nothing is uploaded to any server — there is no account and no cloud. See *Privacy* below.
- **Backup and restore built in.** Download your work as a small backup file at any time, and restore it later or on another computer. Backups from every earlier version of the app still import.
- **Live scoring.** Your API totals update as you type, with the per-head caps applied automatically, so you always know where you stand against the requirement.

## How to use it (quick version)

1. Open **https://ourbee.github.io/cas-tracker/**.
2. On the **Dashboard**, add at least one **assessment window / academic session** (the app anchors sessions to your Date of Joining; each runs **1 July – 30 June**).
3. Fill in **Part A** — your general and service information (name, college, designation, date of joining, promotion sought).
4. For each session, complete the **Category I & II** sheet; then complete the **Category III** cumulative sheet.
5. Watch the **score overview** and the **double-count watchers** as you go — they tell you your running total and warn if an activity is being claimed twice.
6. **Download a backup** whenever you finish a session's worth of entries.
7. When you're ready, use **Print** to produce Parts A–D and save them as a PDF (in the print dialog choose "Save as PDF").

A full, screen-by-screen walkthrough is in **[USER-GUIDE.md](USER-GUIDE.md)**.

## Backup and restore

Because your data lives in the browser, clearing your browser history or switching computers can lose it. To stay safe:

- Click **Download backup** after each working session. You'll get a small `.json` file — keep it somewhere safe (email it to yourself, or save it to cloud storage).
- To continue on another computer or after clearing your browser, open the app and use **Restore from backup**, then choose your `.json` file.
- Old backups from earlier versions of the app import automatically.

## The scoring rules it applies

For **Stage 1→2** the app applies the following (from the G.O. / UGC 4th-Amendment method), and does not let you change the maths:

- **Direct teaching** — divided by 7.5, capped at 70 points.
- **Examination duties** — divided by 10, capped at 20 points.
- **Innovative / ICT-aided teaching** — divided by 10, capped at 10 points.
- **Category II sub-heads** — divided by 10, capped at 15 points.
- **Category III** — scored on the points table, with **impact-factor augmentation applied before the authorship split**, a cap on invited/academic lectures, and a yearly Category I gate.
- **Impact-factor bands** — IF 1–2 adds +10, IF 2–5 adds +15, IF 5–10 adds +20.

The other stages use their own thresholds; the on-screen **score overview** always shows the target for the stage you've selected. Treat the app's totals as your working estimate — the **final, official** score is whatever the Screening-cum-Evaluation Committee and Governing Body certify.

## Privacy

- No account, no login, no tracking.
- All data is stored locally in your browser only.
- The only way data leaves your computer is if **you** download a backup file and share it, or print/export the dossier.

## Frequently asked

**Is this an official Government or UGC tool?**
No. It is an independent helper built to follow the published rules. It does the calculations and formatting; your institution's committee makes the final decision.

**Can I use it offline?**
Yes. Save the `index.html` file to your computer and double-click it to open — no internet needed. (Your backups still work.)

**I entered a lot of data and it's gone!**
Local-storage data can be cleared by clearing browser history, using private/incognito mode, or switching browsers/computers. Always keep a downloaded backup — see *Backup and restore*.

**Which browser should I use?**
Any current version of Chrome, Edge, Firefox, or Safari. A laptop/desktop is best for the print layout.

## For future development

The deployable app is the single **`index.html`** file — that is all an end user needs. The source (React UI, a pure-JavaScript scoring engine with the canonical schema and migrations, a storage seam, and a regression test suite that checks the new engine against the original app's own maths) lives alongside it for future work, including planned Google-Sheet (Apps Script) and Supabase versions. **The Stage 1→2 scoring maths must never be changed** — the test suite enforces parity with the original.

## Credits

Created by **Ritwik Balo**.

Licensed for use by colleagues and CAS applicants. If it saved you time, an optional "buy me a coffee" / UPI contribution can be enabled in the app.
