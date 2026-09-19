# CAS API Tracker

A free, single-page web app that helps college teachers in **West Bengal Government-aided colleges** work out their **API (Academic Performance Indicator) score** for **CAS promotion**, keep every claim tied to its evidence, and print the dossier — without spreadsheets, logins or installation.

**▶ Use it now: https://ourbee.github.io/cas-api-tracker/**

Built to **G.O. 1373-Edn(CS) dated 07.12.2017** and the **UGC Regulations 2016 (4th Amendment)**, with the DPI office's working conventions (JDPI, T.K. Ghara) for turning duties into hours.

A screen-by-screen walkthrough is in **[USER-GUIDE.md](USER-GUIDE.md)**.

The tabs: **Home · Bring in records · To check · Annexures · Scores · Print & submit**.

---

## What it does

- **Annexures are the record.** Everything you did goes into an annexure — class log, exam duties (question setting, invigilation, evaluation, scrutiny, marks upload, OIC/JOIC work), presentations and videos, meetings, committee and college work, student events, seminars, research, leave, and time on campus. Each row has a date, its details, a proof reference and a verification status.
- **Hours from the rules.** Evaluation 0.3/0.5 h per script (UG) and 0.5/0.75 (PG), question setting 5–8 h, moderation 3–4 h, scrutiny 5 min per script, marks upload 30 s per script, meetings 2 h when no time is recorded, presentations 5 h, a full day 8 h — every number editable. Recorded times ("10AM–1PM") win over defaults. College work that rarely has a written time — notices, Google Forms, minutes, reports, scholarship applications, magazine editing, lesson plans — gets your own default hours (editable, and shown as a default on the row).
- **Sessions made for you.** From your date of joining, the app builds the assessment period and its academic sessions (the first and last clipped to the period), sorts every dated row into its session, and scores Category I per session, Category II and III over the whole period, with "floor · short by" readings on every head.
- **Bring in records — one place for everything.**
  - **The Yellow Book** (your day-by-day register workbook) is read into all annexures at once, with the cell each row came from. The app explains where the sheet's own TOTAL row is wrong and reads class lengths that change mid-year.
  - **An individual annexure** — SP's Word formats, an evaluation list, or the app's own Excel templates — replaces the Yellow Book for that annexure, or its whole category, in the sessions it covers.
  - **A spreadsheet of work done** — a few rows or many, from any year — is sorted into annexures row by row and added alongside the Yellow Book.
  - **The Evidence Ledger** brings in work found in WhatsApp messages, e-mails, minutes, notices and flyers — prepared by a Claude project from a brief the app writes, or read in the app by Gemini — and checks every item against your rows: recorded · recorded, not fully · more than the source shows · on another date? · not recorded.
  - Upload as often as you like: each upload adds only what is new, and any upload can be removed. When you choose a different annexure for a piece of text, the app remembers it for later uploads.
- **The review's cards don't disappear.** Every cell an upload did not turn into a row is kept with that upload, so the cards survive pressing *Accept*, a browser refresh and a restore from backup. **Your uploads** says how many cells are still undecided; opening an upload brings the same cards back, grouped as *Set aside · Not sure · Couldn't read · Left out*, each with **Bring it in now** (creates the row as part of that upload — or *as a second row*, with a warning, where the work is already recorded) and **Leave it out** (put away under *Decided*, reopenable). Nothing closes itself; a card waits until you decide.
- **Nothing is set aside without an explanation.** Every cell the app doesn't make a row of gets its own card saying why, showing the record that already carries the work (cited and linked — the row this very cell made before, or whatever else is on that day), and listing what this file says that the record doesn't: a remark, a written time, an hours figure, a committee, a paper code, a proof link. Each of those carries a button that puts it on the row that already exists rather than creating a second one, and the row's note then records which file and cell it came from. The tab leads with the number worth acting on — *2 of these 59 set-aside cells say something your records don't have* — and a figure the two record differently is called a disagreement, not an addition. The same reading warns, before a row is created, when the day it lands on already carries that work.
- **To check.** Everything that needs a look is a card, and every card reads the same way: **Record** (the whole record — particulars, note, proof, and the source's own words), **Source** (who says so, name and cell both live links), **Issue** (what was found and which rule says so), **Likely** (what it probably is, reasoned from records already in the file — the same work on other dates, the day's unaccounted time, the Evidence Ledger, your usual hours, a possible misfiling), and **Do** (the fixes, with ★ on the one your records point to). Where only a raw source can settle it, the card offers the question to put to the Claude project, and the whole set can be downloaded as a numbered questions pack. A card marked as checked stays away until its figures change.
- **Who says what.** Every card, row, day and score list cites its source in full — *your Yellow Book (sheet “2019-2020”, cell O93)*, *the annexure file “B-3.xlsx” (cell A5)*, *the Evidence Ledger (WhatsApp, msg 14)* — with the cell always as a link (the exact cell once that year's tab address is in Setup, the workbook otherwise) and a way back to the upload report. When two uploads describe the same work and disagree, or one says more than the other, the card quotes each source side by side and offers a way to settle it; an *Hours missing* card always says how much of that day is still unaccounted.
- **Scores.** The whole period — Category I in every session, Category II and III added up, and work that is counted once — and each session's heads, its days against time on campus, and its cards to check.
- **Days.** Each day's recorded work is set against your time on campus. A meeting with no recorded duration is given the rest of the day; days with unaccounted time, or more work than time on campus, are flagged; online teaching periods (COVID) are exempt.
- **Headship.** While you were Head of Department, a notice calling all Heads of Departments to a meeting counts as a meeting attended (ex officio); the Evidence Ledger, the brief and Gemini all apply it.
- **Counted once.** Remedial classes, mentoring, and talks that could sit under two heads are counted in one place only. Totals typed before the annexures existed are annexure rows now; one that overlaps annexure rows for the same head is kept but not counted, so nothing is counted twice.
- **Documents.** Every annexure in the session-grouped format, the Annexure-B proforma, the summary of API scores, or the complete file — printed (Save as PDF) or downloaded as Word.

## Why you might want it

- **Nothing to install.** Runs in any current browser. You can also save `index.html` and open it offline.
- **Your data stays with you.** Everything is stored in your own browser. Files you upload are read on your computer and never sent anywhere. The only optional exception is Gemini, which you switch on with your own key.
- **Backup and restore.** Download one small backup file after each sitting; restore it on any computer. Backups from every earlier version still import.

## Quick start

1. Open **https://ourbee.github.io/cas-api-tracker/** on a laptop or desktop.
2. **Home → Setup → Profile** — fill in your profile, the promotion sought and your date of joining. Sessions appear.
3. **Bring in records → Upload files** — upload the Yellow Book. Review, then accept.
4. Upload individual annexures or spreadsheets of work where you have them.
5. **To check** — work through the cards, starting with *Not counted yet*.
6. **Bring in records → Evidence Ledger** — download the brief and the open questions, prepare the ledger in Claude, bring it back, act on the verdicts.
7. **Scores** — see where each session and the whole period stand.
8. **Home → Setup → Backup & restore** after each sitting. When ready, **Print & submit**.

## Backup and restore

Browser data can be lost by clearing browsing data, private windows, or a change of browser or computer. Click **Download backup** (Home → Setup → Backup & restore; Home also reminds you) after each sitting and keep the `.json` file safe; **Restore from backup** loads it back.

## The scoring rules

For **Stage 1→2** the maths is fixed: direct teaching hours ÷ 7.5 (cap 70); examination duties ÷ 10 (cap 20); innovative teaching ÷ 10 (cap 10); Category II sub-heads ÷ 10 (cap 15 each); Category III on the points table with impact-factor augmentation before the authorship split and the cap on lectures. Category I must reach 80 in every session (or, as an alternative reading, on average — you choose). Treat the totals as a working estimate: the Screening-cum-Evaluation Committee certifies the official score.

## Privacy

No account, no login, no tracking. Data lives in your browser. It leaves your computer only if you share a backup, print or download documents, or use the optional Gemini features with your own key.

## Frequently asked

**Is this an official tool?** No. It is an independent helper that follows the published rules and the DPI office's conventions.

**The numbers differ from my Yellow Book's TOTAL row.** The app counts each day's own value. Open the session in Scores — it explains which rows the TOTAL formula leaves out.

**I uploaded an annexure file and my Yellow Book rows disappeared.** They are set aside, not deleted: the file overrides them for that annexure in those sessions. Remove the upload (Bring in records → *Your uploads* → **Remove upload**) to bring them back, or untick a session when uploading.

**A total I typed in an earlier version isn't counted.** It is an annexure row now, kept but not counted because annexure rows hold the same head. Its card on To check lets you count it as well or delete it.

## For development

The deliverable is the single `index.html`. Source lives in the development folder:

- `src/engine.js` — scoring engine, sessions and period, schema and migration (the Stage 1→2 maths must never change; `npm test` checks it against the original app)
- `src/annex.js` — annexure definitions, hour rules, head names, time-slot parser, class-length changes, moving a row between annexures
- `src/model.js` — rows → engine entries, precedence (annexure files over the Yellow Book), flags with ids, retiring direct entries into rows
- `src/importer.js` — Yellow Book, list, spreadsheet and annexure-file (.xlsx / .csv / .docx) reading, remembered annexure choices
- `src/days.js` — the day view; `src/evidence.js` — ledger, verdicts, patterns, the brief; `src/checks.js` — usual hours, cell links
- `src/ai.js` — optional Gemini; `src/docmodel.js`, `src/docx.js` — documents
- `src/ui/*.jsx` — React pages; `build.js` bundles everything into `index.html`
- `test/` — regression, annexure, import, day/evidence and v5 suites
- `docs/CLAUDE-PROJECT.md` — instructions and commands for the Claude "CAS Promotion" project

```
npm install
npm test
npm run build
```

## Credits

Created by **Ritwik Balo**.
