# CAS API Tracker

A free, single-page web app that helps college teachers in **West Bengal Government-aided colleges** work out their **API (Academic Performance Indicator) score** for **CAS promotion**, keep every claim tied to its evidence, and print the dossier — without spreadsheets, logins or installation.

**▶ Use it now: https://ourbee.github.io/cas-api-tracker/**

Built to **G.O. 1373-Edn(CS) dated 07.12.2017** and the **UGC Regulations 2016 (4th Amendment)**, with the DPI office's working conventions (JDPI, T.K. Ghara) for turning duties into hours.

A screen-by-screen walkthrough is in **[USER-GUIDE.md](USER-GUIDE.md)**.

---

## What it does

- **Annexures are the record.** Everything you did goes into an annexure — class log, exam duties (question setting, invigilation, evaluation, scrutiny, marks upload, OIC/JOIC work), presentations and videos, meetings, committee and college work, student events, seminars, research, leave, and time on campus. Each row has a date, its details, an evidence reference and a verification status.
- **Hours from the rules.** Evaluation 0.3/0.5 h per script (UG) and 0.5/0.75 (PG), question setting 5–8 h, moderation 3–4 h, scrutiny 5 min per script, marks upload 30 s per script, meetings 2 h when no time is recorded, presentations 5 h, a full day 8 h — every number editable. Recorded times ("10AM–1PM") win over defaults.
- **Sessions made for you.** From your date of joining, the app builds the assessment period and its academic sessions (the first and last clipped to the period), sorts every dated row into its session, and scores Category I per session, Category II and III cumulatively, with "floor · short by" readings on every head.
- **Upload instead of typing.**
  - **The whole Yellow Book** (your day-by-day register workbook) is read into all annexures at once, with the cell each row came from. The app explains where the sheet's own TOTAL row is wrong (SUM ranges that start late, blank formula cells) and reads class lengths that change mid-year (45-minute classes, then 1-hour online classes).
  - **An individual annexure** — SP's Word formats, an evaluation list, or the app's own Excel templates — overrides the Yellow Book for that annexure, or its whole category, in the sessions it covers. Nothing is deleted; undo brings the Yellow Book rows back. A table shows which source each annexure is counted from.
- **Days.** Each day's recorded work is set against your time on campus. A meeting with no recorded duration is given the rest of the day; days with unaccounted time, or more work than time on campus, are flagged; online teaching periods (COVID) are exempt.
- **Evidence.** WhatsApp messages, e-mails, minutes, notices and flyers become an *evidence ledger* — prepared by a Claude project from a brief the app writes, or read in the app by Gemini — and every item is checked against your rows: recorded · recorded, not fully · more than the source shows · on another date? · not recorded. The app also lists work you recorded in one year but not (or more briefly) in another.
- **Counted once.** Remedial classes, mentoring, and talks that could sit under two heads are counted in one place only; lump sums typed before the annexures existed are set aside when annexure rows cover the same head.
- **Documents.** Every annexure in the session-grouped format, the Annexure-B proforma, the summary of API scores, or the complete file — printed (Save as PDF) or downloaded as Word.

## Why you might want it

- **Nothing to install.** Runs in any current browser. You can also save `index.html` and open it offline.
- **Your data stays with you.** Everything is stored in your own browser. Files you upload are read on your computer and never sent anywhere. The only optional exception is Gemini, which you switch on with your own key.
- **Backup and restore.** Download one small backup file after each sitting; restore it on any computer. Backups from every earlier version still import.

## Quick start

1. Open **https://ourbee.github.io/cas-api-tracker/** on a laptop or desktop.
2. **Dashboard** — fill in your profile, the promotion sought and your date of joining. Sessions appear.
3. **Upload** — upload the Yellow Book (Option 1). Review, then accept.
4. **Upload** again for any category where you have a better record (Option 2 · individual annexure).
5. **Dashboard** — confirm the class length for each session.
6. **Sessions** and **Days** — see where each session stands and which days need a look.
7. **Evidence** — download the brief, prepare the ledger in Claude, import it, act on the verdicts.
8. **Download backup**. When ready, print the annexures, proforma and summary.

## Backup and restore

Browser data can be lost by clearing browsing data, private windows, or a change of browser or computer. Click **Download backup** on the Dashboard after each sitting and keep the `.json` file safe; **Restore from backup** loads it back.

## The scoring rules

For **Stage 1→2** the maths is fixed: direct teaching hours ÷ 7.5 (cap 70); examination duties ÷ 10 (cap 20); innovative teaching ÷ 10 (cap 10); Category II sub-heads ÷ 10 (cap 15 each); Category III on the points table with impact-factor augmentation before the authorship split and the cap on lectures. Category I must reach 80 in every session (or, as an alternative reading, on average — you choose). Treat the totals as a working estimate: the Screening-cum-Evaluation Committee certifies the official score.

## Privacy

No account, no login, no tracking. Data lives in your browser. It leaves your computer only if you share a backup, print or download documents, or use the optional Gemini features with your own key.

## Frequently asked

**Is this an official tool?** No. It is an independent helper that follows the published rules and the DPI office's conventions.

**The numbers differ from my Yellow Book's TOTAL row.** The app counts each day's own value. Open the session — it explains which rows the TOTAL formula leaves out.

**I uploaded an annexure file and my Yellow Book rows disappeared.** They are set aside, not deleted: the file overrides them for that annexure in those sessions. Remove the upload (Upload tab → *Your uploads* → **Remove upload**) to bring them back, or untick a session when uploading.

## For development

The deliverable is the single `index.html`. Source lives in the development folder:

- `src/engine.js` — scoring engine, sessions and period, schema and migration (the Stage 1→2 maths must never change; `npm test` checks it against the original app)
- `src/annex.js` — annexure definitions, hour rules, time-slot parser, class-length changes
- `src/model.js` — rows → engine entries, precedence (annexure files over the Yellow Book, annexure rows over direct entries), flags
- `src/importer.js` — Yellow Book, list and annexure-file (.xlsx / .csv / .docx) reading
- `src/days.js` — the day view; `src/evidence.js` — ledger, verdicts, patterns, the brief
- `src/ai.js` — optional Gemini; `src/docmodel.js`, `src/docx.js` — documents
- `src/ui/*.jsx` — React pages; `build.js` bundles everything into `index.html`
- `test/` — regression, annexure, import and day/evidence suites
- `docs/CLAUDE-PROJECT.md` — instructions and commands for the Claude "CAS Promotion" project

```
npm install
npm test
npm run build
```

## Credits

Created by **Ritwik Balo**.
