# CAS API Tracker — User Guide

A step-by-step guide to building your **CAS promotion file** with the CAS API Tracker.

**App:** https://ourbee.github.io/cas-api-tracker/
**For:** teachers in West Bengal Government-aided colleges applying for CAS promotion under G.O. 1373-Edn(CS) / UGC Regulations 2016 (4th Amendment).

You do not need any technical knowledge. If you can fill in a form and choose a file, you can use this app.

> **The golden rule: back up after every sitting.** Your data is saved inside your browser, not on a server. Home → Setup → **Backup & restore** → *Download backup* takes five seconds, and Home reminds you when it has been a while.

The tabs along the top: **Home · Bring in records · To check · Annexures · Scores · Print & submit**. The number beside *To check* is how many cards are open; it turns red when some hours can't count yet.

---

## Step 1 — Home: who you are and your period

Home starts with **Setup** — the things you set once — and below it **Where you stand**: **Next steps**, what needs you now, and the **score overview**.

1. Open **Setup → Profile & assessment period**. Fill in your **name, department, college and designation**.
2. Choose the **promotion sought** (Stage 1→2, 2→3, 3→4).
3. Enter your **date of joining** (for Stage 1→2) or the **date of your last promotion** (later stages), and your **service track**.

4. Add your **initials** as they appear in routines, duty lists and notices (e.g. RB).
5. If you have been Head of Department, open **Setup → Headship** and add the period. While you were head, a notice calling all HoDs to a meeting counts as a meeting you attended (ex officio). Other cells and committees you belong to go in Annexure D-1.

The app shows your **assessment period** and builds its **sessions** (1 July – 30 June; the first starts on your joining date and the last ends on the period's end). You never add sessions by hand.

## Step 2 — Bring in records: the Yellow Book

If you keep a day-by-day register workbook (the "Yellow Book"), start here.

1. In Google Sheets: **File → Download → Microsoft Excel (.xlsx)**.
2. **Bring in records → Upload files → Option 1** → *Upload the Yellow Book (.xlsx)*.
3. The review shows each sheet, the session it goes to, the class length it found, and any place where the sheet's own **TOTAL row** doesn't match its daily values.
4. The proposed rows are sorted into **Ready**, **Ask me**, **Couldn't read** and **Skipped**. Check the *Ask me* ones: choose an annexure to include a row, or leave it out. When you choose a different annexure from the app's guess, it remembers your choice for that text in later uploads. (Optional: *Sort unclear items with AI* uses Gemini with your own key.)
5. Click **Accept and create … rows**. The **upload report** links every row back to its cell.

Uploading the same workbook again later only proposes what is new — so when you fill the Yellow Book for more years, upload it again.

**To remove an upload:** Bring in records → **Your uploads** → **Remove upload**. It deletes the rows that upload created and brings back anything it had set aside.

## Step 3 — Individual annexures and spreadsheets of work

**An individual annexure replaces the Yellow Book** for one category where you have a fuller or more accurate record — an invigilation annexure, an evaluation list, an OIC duty list.

1. **Upload files → Option 2**. Pick the annexure (e.g. *B-3 Invigilation*), or leave *Work it out from the file*. SP's Word formats, Excel/CSV tables and the app's **templates** (*Annexure templates* below the options, or **Excel template** on any annexure page) all work.
2. In the review, check each table's **Annexure** and **Columns**.
3. Under **What this file overrides in the Yellow Book**, choose *Only the annexures in this file* or *The whole category*. Untick a session to add the file's rows alongside instead.

**A spreadsheet of work adds alongside** and replaces nothing — use it for a list of work from any year, a few rows or many (for example work from 2023-24 onwards). **Upload files → Option 3**. Each row needs a date and a description; the app sorts every row into its annexure from its text, and you review before anything is added.

**A pasted list** (for example a TickTick export, one activity per line with the date in brackets) also adds rows.

**Annexures → *Where each annexure's rows come from*** shows, for every annexure and session, the rows and hours from each source, and marks sessions with nothing yet.

## Step 4 — To check: work through the cards

Every flag is a **card** that says, in plain words:

- **what was found** — e.g. *Invigilation on Thu 03 Sep 2020 has no hours — not counted yet*;
- **where each figure comes from** — *your Yellow Book (sheet "2020-2021", cell V70)* — with a link that opens the cell in Google Sheets once you add the sheet links (Home → Setup → **Yellow Book links**);
- **which rule applies** — e.g. *the JDPI rule for setting a question paper — UG 5 h per paper for up to 50 candidates, 8 h above*;
- **what it probably means and what you can do**, with the fixes right on the card.

Cards come in three groups:

- **Not counted yet** — hours missing, no date, dated outside the period. Type the time or the hours; use **your usual time** for that work (worked out from your other records, marked *estimated*); use **the day's unexplained time on campus**; or **leave the row out**.
- **Worth checking** — two figures differ (the sheet's hours against a rule or a written time), a possible duplicate, work on a leave day, a class length to confirm, an earlier total that isn't counted, a day with more work than time on campus, days with time no record explains.
- **For your information** — rows replaced by an annexure file, the 75% cut-off, a committee with nothing recorded, an IQAC confirmation.

Fixing a row clears its card. **Mark as checked** (or *Keep 5 h*, *Both are right*, *They're different — keep both*) puts a card away; it comes back by itself if its figures change. **Checked** at the top shows the cards you've put away, each with **Reopen**. Filter by session or by kind of card.

## Step 5 — Class length

Home → Setup → **Sessions & class length** (or the *Class length* card on To check).

- If the Yellow Book's own hours show a different length — or a change during the year, such as 45-minute classes and then 1-hour online classes from the lockdown — it says *sheet hours suggest …* with a **use** button.
- **+ changes from a date** lets you add such a change yourself.
- Tick **Confirmed** once it is right.

## Step 6 — Annexures: check and complete your rows

Open **Annexures** and any annexure. Rows are grouped by session; every change saves as you type.

- **Hours** shows where the figure comes from: *rule*, *time* (a recorded time slot), *sheet* (hours written in the upload), *default*, *rest of day* (see Days), or *typed* (your own number, which always wins). A row with no hours offers **your usual** time for that work.
- **College work with no written time** (Annexure D-3) gets **your default hours** for its kind of work — a notice 1 h, a Google Form 1.5 h, minutes 1.5 h, a report 3 h, scholarship applications 2 h and so on; a lesson plan (C-4) 1 h. The app works the kind out from the text, or choose it in the row's *Kind of work*. Change the figures in Home → Setup → Hour rules.
- Each row says where it **counts** — e.g. *counts in I(b) Examination duties* (hover for how that head is scored) — and links to the Yellow Book cell it came from.
- **Details** holds the **proof** (link or reference), status (pending / attached / verified), *Estimated*, **Don't count this row** (kept for the record, counted nowhere), a note, **Where the work was done** (on campus / off campus / online), and **Belongs in another annexure?** — move the row; its date, hours, proof and source stay, and later uploads send the same text to the new annexure.
- **The day of the week** is shown with every date — *Wed 18 Aug 2021* in lists and tables, and above each date box as *DATE · WED* — so you can place a record at a glance. The assessment period and the session windows stay plain dates.
- **Hour rules** are in Home → Setup.

## Step 7 — Scores

**Whole period** shows Category I in every session (hours → points per head, and whether each session clears), Category II added up over the period, **Category III** (publications, projects, guidance, awards, talks — scored on the points table and added up over the period, with the lecture cap, UGC-list and IQAC checks), Category II + III, and work that is counted once.

Pick a **session** for its own page: **Category I** (each head as *"(a) Direct teaching · 117.25h ÷ 7.5 = 15.63 · cap 70 · floor 50 · short by …"* with the annexures behind it, and why the Yellow Book's TOTAL row differs), **Category II**, **Category III**, **Days** and **To check** for that session.

## Step 8 — Days: time on campus

Scores → a session → **Days** lists each day: arrival–departure, classes, every activity with its hours, and the balance.

- A **meeting with no recorded duration gets the rest of the day**: time on campus minus classes and everything else recorded that day. Classes allotted but not taken that day are read as missed because of the meeting.
- **Needs review** shows days with **unaccounted time** (from 1 h, adjustable in Hour rules) and days with **more work than time on campus**.
- Evaluation, question setting, presentations, and anything marked off campus or online are not held against campus time.
- **Teaching-mode periods — online / hybrid** are set in Home → Setup: add the dates teaching went online (COVID) and any hybrid stretch. *Month by month* shows what your records say, to help set the dates.

## Step 9 — Evidence Ledger: messages, e-mails, minutes, flyers

Much of your work is recorded only in WhatsApp groups, e-mails, minutes and notices. **Bring in records → Evidence Ledger** brings it in and checks it.

1. Bring the Yellow Book and any annexure files in first.
2. **Download the brief for the Claude project.** It lists what is recorded, where the file is thin (shortfalls, years with little recorded, work recorded one year but missing another, days with unaccounted time) and the exact **evidence ledger** format.
3. In Claude, open your CAS Promotion project, attach the brief and your sources, and ask: *"Prepare the evidence ledger from these sources, following the brief."* (Set-up text for the project: `docs/CLAUDE-PROJECT.md` in the development folder.)
4. Back in the app, **Choose the ledger file** (or paste Claude's table) → **Add … and check them**. Bring in more ledger files whenever you like — items already in the ledger are skipped.
5. Each item gets a verdict — **Not recorded** (add it as a row), **Recorded, not fully**, **More than the source shows**, **On another date?**, **Recorded** (use it as the row's proof). **Dismiss** anything irrelevant. A notice calling all HoDs to a meeting while you were head is marked **HoD then — presumed present**; adding it records the meeting with that note.

For a few items at a time, **Read a few messages, screenshots or flyers with Gemini** does the extraction inside the app with your own key.

## Step 10 — Print & submit

- **Checklist & complete file:** the dossier checklist, all annexures, or the complete file (proforma, summary, then every annexure).
- **Proforma** (Annexure B) and **Summary of API scores**: print (Save as PDF) or download Word.
- Any single annexure prints from its own page, with signature lines for the Incumbent, IQAC Coordinator and Principal.

---

## Troubleshooting

**My Yellow Book rows for an annexure aren't counted.** An individual annexure you uploaded overrides them. See Annexures → *Where each annexure's rows come from*; to restore them, remove that upload (Bring in records → *Your uploads* → **Remove upload**).

**A session's score fell after an update.** A total typed before the annexures existed is kept but not counted where annexure rows hold the same head. Its *Earlier total* card on To check lets you count it as well — only if it is different work — or delete it.

**Days shows nothing to check.** The session has no arrival/departure times. Upload the Yellow Book again to bring them in, or add them in Annexure H-7.

**My data disappeared.** Browser data is cleared by clearing browsing data, private windows, or another browser or computer. Restore your latest backup.

**"Save failed — edit to retry".** Make a small edit; if it persists, download a backup and reload.

**Is this official?** No — it follows the published rules; your college's committee certifies the final score.

---

*Created by Ritwik Balo. Based on G.O. 1373-Edn(CS) dt. 07.12.2017 and UGC Regulations 2016 (4th Amendment).*
