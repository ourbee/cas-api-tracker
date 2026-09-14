# CAS API Tracker — User Guide

A step-by-step guide to building your **CAS promotion file** with the CAS API Tracker.

**App:** https://ourbee.github.io/cas-api-tracker/
**For:** teachers in West Bengal Government-aided colleges applying for CAS promotion under G.O. 1373-Edn(CS) / UGC Regulations 2016 (4th Amendment).

You do not need any technical knowledge. If you can fill in a form and choose a file, you can use this app.

> **The golden rule: back up after every sitting.** Your data is saved inside your browser, not on a server. Dashboard → **Download backup** takes five seconds.

The tabs along the top: **Dashboard · Upload · Annexures · Sessions · Days · Evidence · Research (Cat III) · Dossier · Proforma · Summary**, with the **⚑ flags** count on the right.

---

## Step 1 — Dashboard: who you are and your period

1. Fill in your **name, department, college and designation**.
2. Choose the **promotion sought** (Stage 1→2, 2→3, 3→4).
3. Enter your **date of joining** (for Stage 1→2) or the **date of your last promotion** (later stages), and your **service track**.

The app now shows your **assessment period** and builds its **sessions** (1 July – 30 June; the first starts on your joining date and the last ends on the period's end). You never add sessions by hand.

## Step 2 — Upload: the whole Yellow Book

If you keep a day-by-day register workbook (the "Yellow Book"), start here.

1. In Google Sheets: **File → Download → Microsoft Excel (.xlsx)**.
2. Open the **Upload** tab. Under **Option 1 · all categories**, click **Upload the Yellow Book (.xlsx)** and choose the file.
3. The **review** shows each sheet, the session it goes to, the class length it found, and — in the last column — any place where the sheet's own **TOTAL row** doesn't match its daily values (for example a SUM that starts halfway down the year).
4. Below, the proposed rows are sorted into **Ready**, **Ask me**, **Couldn't read** and **Skipped**. Check the *Ask me* ones: choose an annexure to include a row, or leave it out. (Optional: *Sort unclear items with AI* uses Gemini with your own key.)
5. Click **Accept and create … rows**. The **upload report** links every row back to its cell.

**To remove an upload:** Upload tab → **Your uploads** (also on the Annexures page, and on each annexure page under *Uploads with rows in …*) → **Remove upload**. It deletes the rows that upload created (including any edits you made to them) and brings back anything it had set aside. You can upload the file again afterwards.

Uploading the same workbook again later only proposes what is new.

## Step 3 — Upload: individual annexures (they override the Yellow Book)

Where you have a fuller or more accurate record for one category — an invigilation annexure, an evaluation list, an OIC duty list — upload it on its own.

1. **Upload** tab → **Option 2 · one category at a time**.
2. **Which annexure is this file?** Pick it (e.g. *B-3 Invigilation*), or leave *Work it out from the file*. Files can be:
   - SP's Word formats (a table with *Session · Type of Examination Duty · Exam Details · Date · Hours*);
   - an Excel or CSV table;
   - the app's own **templates** (Upload tab → *Annexure templates*, or **Excel template** on any annexure page) — these map themselves;
   - a workbook with one sheet per annexure, sheets named like "B-3 Invigilation".
3. Click **Upload an individual annexure** and choose the file. (Shortcut: on any annexure page, **Upload a file for this annexure**.)
4. In the review, check each table's **Annexure** and, if needed, its **Columns**.
5. Under **What this file overrides in the Yellow Book**, choose:
   - **Only the annexures in this file** — e.g. an invigilation list replaces only the Yellow Book's B-3 rows; or
   - **The whole category** — every annexure of that category (e.g. all of I(b) Examination duties), when the file is your complete record for it.

   Each session is listed with how many Yellow Book rows will be **set aside**. Untick a session to add the file's rows alongside the Yellow Book instead.
6. **Accept**. Set-aside rows are not counted and not deleted — **Remove upload** on this file (Upload tab → *Your uploads*) makes them count again. Rows you typed by hand are never set aside.

**Annexures** tab → **Sources in use** shows, for every annexure and session, whether it is counted from the Yellow Book, an annexure file, typed rows or evidence.

## Step 4 — Class length

On the **Dashboard**, the sessions table has a **Class length (h)** for each session.

- If the Yellow Book's own hours show a different length — or a change during the year, such as 45-minute classes and then 1-hour online classes from the lockdown — it says *sheet hours suggest …* with a **use** button.
- **+ changes from a date** lets you add such a change yourself.
- Tick **Confirmed** once it is right. Until then the session carries a flag.

## Step 5 — Annexures: check and complete your rows

Open **Annexures** and any annexure. Rows are grouped by session; every change saves as you type.

- **Hours** shows where the figure comes from: *rule*, *time* (a recorded time slot), *sheet* (hours written in the upload), *default*, *rest of day* (see Days), or *typed* (your own number, which always wins).
- **Details** holds the evidence reference, status (pending / attached / verified), *Estimated*, a note, where it came from, and **Where the work was done** (on campus / off campus or outside college hours / online) — used by the Days check.
- Flags on a row: hours missing, outside the period, sheet ≠ rule, duplicate, on a leave day, set aside.
- **Hour rules** (link on the Annexures page) holds every convention, the mismatch threshold and the two Days settings.

## Step 6 — Sessions: where each year stands

Pick a session. **Category I** shows each head as *"(a) Direct teaching · 117.25h ÷ 7.5 = 15.63 · cap 70 · floor 50 · short by …"* with the annexures behind it.

- **Set aside — not counted:** a *direct entry* typed before the annexures existed (for example a year's class total) is not counted once annexure rows cover the same head, so nothing is counted twice. Choose **Count as well** only if it is genuinely different work, or **Delete it**.
- **Why the Yellow Book's TOTAL row shows a different figure** explains the sheet's own mistakes.
- **Category II** and **Category III** work the same way; **Flags** lists the session's flags.

## Step 7 — Days: time on campus

**Days** lists each day of a session: arrival–departure, classes, every activity with its hours, and the balance.

- A **meeting with no recorded duration gets the rest of the day**: time on campus minus classes and everything else recorded that day. Classes allotted but not taken that day are read as missed because of the meeting.
- **Needs review** shows days with **unaccounted time** (from 1 h, adjustable) and days with **more work than time on campus**. On a day with unaccounted time and an activity that has no hours, a button offers to give it that time.
- Evaluation, question setting, presentations, and anything marked off campus or online are not held against campus time.
- **Teaching-mode periods — online / hybrid:** add the dates teaching went online (COVID) and any hybrid stretch. Online days are never flagged as *more than time on campus*. *Month by month* shows what your records say, to help set the dates.

## Step 8 — Evidence: messages, e-mails, minutes, flyers

Much of your work is recorded only in WhatsApp groups, e-mails, minutes and notices. The **Evidence** tab brings it in and checks it.

1. Bring the annexures in first (Steps 2–3).
2. **Download the brief for the Claude project.** It lists what is recorded, where the file is thin (shortfalls, years with little recorded, work recorded one year but missing another, days with unaccounted time) and the exact **evidence ledger** format.
3. In Claude, open your CAS Promotion project, attach the brief and your sources (WhatsApp chat exports, screenshots, e-mails, minutes), and ask: *"Prepare the evidence ledger from these sources, following the brief."* (Set-up text for the project: `docs/CLAUDE-PROJECT.md` in the development folder.)
4. Back in the app, **Choose the ledger file** (or paste Claude's table) → **Add … and check them**.
5. Each item gets a verdict — **Not recorded** (add it as a row), **Recorded, not fully** (the row lacks a time, paper or body the source gives), **More than the source shows**, **On another date?**, **Recorded** (use it as the row's evidence). **Dismiss** anything irrelevant.

For a few items at a time, **Read a few messages, screenshots or flyers with Gemini** does the extraction inside the app with your own key. **Work recorded in some years but missing, rarer or briefer in others** lists patterns worth looking for.

## Step 9 — Research (Cat III)

Publications, projects, guidance, awards, and talks or papers presented are scored cumulatively on the points table, with impact-factor bands and authorship shares. Verify journals against the UGC list and confirm e-learning modules with IQAC.

## Step 10 — Documents

- **Annexures:** on any annexure page, print (Save as PDF) or download Word, in the session-grouped format with signature lines for the Incumbent, IQAC Coordinator and Principal.
- **Proforma** (Annexure B) and **Summary** of API scores: print or Word.
- **Dossier:** the checklist of documents to attach, in order.

## Step 11 — Flags

**⚑ flags** (top right) lists everything that needs a look, each linked to its row, session or day. Red stops hours counting (missing hours, outside the period); amber asks you to check a number; blue is information.

---

## Troubleshooting

**My Yellow Book rows for an annexure aren't counted.** An individual annexure you uploaded overrides them. See Annexures → *Sources in use*; to restore them, remove that upload (Upload tab → *Your uploads* → **Remove upload**).

**How do I clear an upload?** Upload tab → *Your uploads* → **Remove upload** next to the file. The same list is on the Annexures page, and each annexure page lists the uploads that touched it.

**A session's score fell after the update.** Look for *Set aside — not counted* on the session page: an old lump-sum entry is no longer added on top of the annexure rows. Count it as well only if it is different work.

**Days shows nothing to check.** The session has no arrival/departure times. Upload the Yellow Book again to bring them in, or add them in Annexure H-7.

**My data disappeared.** Browser data is cleared by clearing browsing data, private windows, or another browser or computer. Restore your latest backup.

**"Save failed — edit to retry".** Make a small edit; if it persists, download a backup and reload.

**Is this official?** No — it follows the published rules; your college's committee certifies the final score.

---

*Created by Ritwik Balo. Based on G.O. 1373-Edn(CS) dt. 07.12.2017 and UGC Regulations 2016 (4th Amendment).*
