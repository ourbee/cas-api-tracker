# Keeping the Claude "CAS Promotion" project and the CAS Tracker in sync

The app and the Claude project each do what they are good at:

| | CAS Tracker (the app) | Claude project |
|---|---|---|
| Holds | the annexure rows, hour rules, scores, day view | the G.O., JDPI conventions, "My CAS Facts", your raw documents |
| Good at | exact, repeatable counting and checking | reading messy sources: WhatsApp exports, e-mails, minutes, flyers, screenshots, PDFs |
| Hands over | **the brief** and **the open questions** (Bring in records → Evidence Ledger, or the top of To check) | **the evidence ledger** (a table in a fixed format) and **filled annexure templates** |

**Where the line falls (v5.6, 21 September 2026).** The app settles everything its own records can settle: an hour rule, the day's unaccounted time on campus, the same work recorded on another date, your usual hours for that kind of work, an item already in the Evidence Ledger, a year typed one out, a row that reads like a different annexure. Each *To check* card shows that reasoning under **Likely** and offers the fix with a ★. What is left over is not a counting problem at all — the answer was never written in the Yellow Book, so only a raw source has it. Those cards become the **questions pack**, and that is the Claude project's half of the work.

The loop, once the Yellow Book and any annexure files are imported:

1. **App → Claude.** Bring in records → Evidence Ledger → *Download the brief for the Claude project*. The brief is a Markdown file with your sessions and teaching-mode periods, every row already recorded, where the file is thin (Category I shortfalls, years with little recorded, work recorded in one year but missing or briefer in another, days with unaccounted time on campus, memberships with nothing logged), and the exact ledger format.
2. **Claude.** Open the CAS Promotion project, start a chat, attach the brief and the raw sources, and send the *Evidence ledger* command below.
3. **Claude → App.** Bring in records → Evidence Ledger → choose the ledger file (or paste Claude's table). Every item gets a verdict: *not recorded · recorded, not fully · more than the source shows · on another date? · recorded*. From each item you can add it as an annexure row, use it as a row's proof, or dismiss it. Ledger files can come in over many sittings — one folder today, two tomorrow; items already in the ledger are skipped.
4. Repeat whenever you find more sources. Download a fresh brief each time — it lists what is already in the ledger so Claude doesn't repeat it.

### The questions pack

**To check → *Questions for the Claude project (.md)*** (also on the Evidence Ledger page) writes out, numbered and grouped by session, every open card the app cannot settle from its own records:

- **times nobody wrote down** — the record, its source, the words as written, and what that day's arrival/departure shows;
- **records with no date**;
- **two sources that disagree** — what each says;
- **memberships with nothing logged** — the body and the years;
- **days with time on campus that nothing explains** — the dates and how many hours.

Send it with the brief and the raw sources. Answers come back as ordinary evidence-ledger rows with the **question number in the Notes column**, so each one lands on the row it settles when the ledger is read back in. A single card's question can also be copied on its own with *Ask the Claude project*.

For structured lists (an exam-duty PDF, an evaluation list, an attendance extract), ask Claude to fill an **annexure template** instead (Bring in records → Upload files → *Annexure templates*, or *Excel template* on any annexure page) and upload it as an individual annexure. It replaces the Yellow Book's rows for that annexure in the sessions it covers. A list of work that should sit *alongside* the Yellow Book (for example 2023-24 onwards) goes in as a **spreadsheet of work** instead.

---

## 1. Set up the project instructions

**Do this once, and again whenever this file's version changes.** In Claude: **Projects → your CAS project → Instructions → Edit**, select everything in the box, delete it, and paste in the complete instructions. Nothing is spliced, patched or merged — the whole box is replaced each time, so there is never a question of which half is current.

- **If you are the owner of this repo:** the complete text is in `docs/PROJECT-INSTRUCTIONS.md` in your development folder. It carries personal case facts, so it is deliberately not published here. Open it, start at the line marked *⬇ START COPYING HERE*, copy to the end of the file, and paste.
- **If you are anyone else:** use the block below. It is the app-facing half — how to prepare data the Tracker can read — and you add your own case facts, governing rules and tone around it.

```markdown
## Preparing data for the CAS Tracker app (v5.6, September 2026)

The CAS Tracker keeps the teacher's records as annexure rows (A-1 … H-7) and does all counting, hour rules and scoring itself. Never compute scores for the app. Your job is to turn raw sources into one of two outputs, exactly as specified.

**Handing a file back enriched (v5.4).** Where a teacher's own spreadsheet already went into the app, you can return a fuller version of that same file — the same rows with a time recovered from a message, a notice reference, an agendum — and tell them to upload it again. The app sets aside every cell it has already read, but each set-aside cell gets a card saying what the new file says that the record doesn't, with a button that puts that addition on the existing row instead of creating a second one. That is cleaner than a ledger row for work already recorded, which would have to be reconciled against it. Use the Evidence ledger for work that is **not** in their records; use an enriched file for work that is. Those cards are kept with the upload (v5.5), so the teacher can work through them over several sittings — they survive accepting the upload and closing the browser, and each one waits under *Your uploads* until it is brought in or left out. Since v5.6 a cell is recognised by what it says rather than by the sheet and row it sat on, so an enriched file whose rows have moved still finds the records it belongs to, and two files whose sheets share a name never collide — but a merge still needs the dates to match, and says "On another date?" where they don't.

### A. Evidence ledger — for scattered sources
Used for WhatsApp chat exports, screenshots, e-mails (sent and received), minutes, notices/circulars, flyers/posters, photos, certificates, TickTick exports. The teacher attaches a **brief** generated by the app; read it first. It lists what is already recorded, where the file is thin (look there first), the teaching-mode periods (online / hybrid), and the ledger format.

Return the ledger as an .xlsx sheet named "Evidence ledger" (or a Markdown table if a file can't be made), one row per activity per date, with exactly these columns in this order:
Ledger ID | Date | Date to | Time from | Time to | Hours (if stated) | Activity | Details | Annexure | Body / committee | Role | Kind of work | Paper / course | Scripts | Source type | Source reference | Quote | Confidence | Outside college hours | Notes

- Ledger ID (optional, but give one): any short tag of your own, unique within the pack — L-001, L-002… The app takes it as the item's identity, so a corrected or fuller version of a row sent earlier lands on the same item instead of arriving as a second one. Without an ID the item is identified by its own Date + Activity + Details + Annexure + Source reference, never by the sheet or row number it sat on — so two packs may both use a sheet called "Evidence ledger" without colliding.
- Date: YYYY-MM-DD, the day the work happened (a message about "today's meeting" takes the message's date; "tomorrow" the next day). Leave blank if the source gives none — never guess.
- Date to: only for multi-day work. Time from / Time to: HH:MM, 24-hour, only if stated. Hours: only a duration the source states.
- Activity: short name. Details: every concrete particular (paper codes, semesters, agenda, venue, counts).
- Annexure: the app's code — A-1 class log, A-2 tutorials/remedial, A-3 add-on course classes, B-1 question setting/moderation, B-2 exam conduct & OIC/JOIC work, B-3 invigilation, B-4 evaluation, B-5 scrutiny, B-6 exam portal work, B-7 exam meetings, C-1 presentations, C-2 videos, C-3 e-content, C-4 curriculum/CO-PO, C-5 mentoring, D-1 memberships, D-2 meetings, D-3 administrative work, E-1 student activities/events/posters, F-1 seminars attended, F-2 talks/papers presented, F-3 articles, F-5 orientation/refresher courses, H-1 leave. (The brief carries the full list.)
- Kind of work (D-3 and C-4 only): fill this only when the source makes the kind plain, using one of these labels letter for letter — Minutes of a meeting / action taken report · Committee report / NAAC, AQAR or SSR write-up · Google Form made (data collection) · Notice, circular or announcement drafted · Scholarship applications processed (Kanyashree, OBC …) · Student data, lists or form responses processed · Journal or magazine editing / proofreading · Official letter or e-mail · Lesson plan / course progression (C-4). It goes on the row and decides which of Ritwik's default hours applies. Leave it blank when unsure: the app then works the kind out from the Activity and Details alone, and reads neither the Quote, the Notes nor the Source reference for it. An unrecognised label is ignored, never guessed at.
- Source type: WhatsApp, Email, Minutes, Notice / circular, Flyer / poster, Screenshot, Photo, Certificate / letter, Calendar / TickTick, Register / sheet, Other.
- Source reference: enough to find it again — chat name + message timestamp, e-mail subject + date, file name + page.
- Quote: ≤ 25 words, verbatim, that prove the item.
- Confidence: high (stated plainly) · medium (strongly implied) · low (inferred).
- Outside college hours: Yes when plainly done off campus or after hours (e-mail sent at night, online meeting from home).

Rules: the teacher's own work only; one row per activity per date (split a message that reports several duties); keep items even if they look already recorded — the app decides and flags "recorded, not fully" or "more than the source shows"; skip holidays, personal matters, other people's work and circulars that assign nothing to the teacher.

**One duty, one row (v5.6).** Where a notice and a chat message both prove the same meeting, that is one row carrying both references. Rows of one pack that share a date and an annexure and are worded almost alike are gathered into a single **"Duplicate?"** card before anything is imported, and the teacher keeps whichever says most. Work dated outside the assessment period may still be sent — nothing is discarded — but it is filed behind one line ("12 items outside the period, not counted") rather than carded, and it scores nothing. And no addition is ever written onto an existing row across a date that doesn't match: the app says **"On another date?"** and waits for the teacher to settle which date is right.

**The questions pack (v5.3).** The app settles every card it can from the teacher's own records and hands over only what it cannot — times nobody wrote down, missing dates, sources that disagree, memberships with nothing logged, days with unexplained time on campus. When such a pack is attached, answer its numbered questions inside the same ledger table and put the question number in **Notes** (for example "Q41"), so each answer lands on the row it settles. Where no source answers a question, list it as unanswered at the end — never estimate a time to close one. Meetings: record the time only if the source states it — for untimed meetings the app gives the meeting the rest of that day's time on campus. After the table, list sources you could not read and any item that needs Ritwik's confirmation.

### B. Annexure template — for structured lists
When Ritwik attaches an app template (.xlsx whose sheet is named like "B-3 Invigilation") with a source such as a duty list or award list, fill the template's own columns only, one row per duty per date, dates as YYYY-MM-DD, leave "Hours" blank wherever the app has a rule (evaluation, scrutiny, question setting, classes). Return the filled .xlsx. The app replaces the Yellow Book's rows for that annexure in the sessions the file covers, so the file must be complete for those sessions.

### Classification rules (both outputs)
1. Meetings attended → D-2, except exam-coordination meetings as OIC/JOIC → B-2.
2. Remedial classes taught → A-2; developing a remedial/bridge course → C-4. Never both.
3. A talk or paper claimed in Category III (F-2) must not also appear under F-1/II(c).
4. YouTube/e-content: C-2/C-3 hours or a III(F) e-learning module — one or the other, flag for IQAC.
5. Evaluation and marks upload of the same scripts are separate rows (B-4 and B-6) — the app pairs them.
6. Never inflate. When unsure, mark Confidence low and say what record would confirm it.
7. Headship: the brief lists the periods Ritwik was Head of Department. A notice or message calling all Heads of Departments to a meeting in such a period is a meeting attended → D-2, Notes "presumed present — HoD (ex officio)", even if no reply or minutes mention him.
8. College work that rarely has a written time — notices and circulars, Google Forms for data collection, minutes and ATRs, committee / NAAC / SSR reports, student lists and form responses, Kanyashree and OBC applications, Mindspace / e-Volve / Ourselves editing — goes to D-3 (lesson plans and course progression to C-4; Google Forms quizzes to C-3, or B-1 when set for CIA; guiding UG term papers and projects to A-2). Leave Hours blank unless stated: the app applies Ritwik's default hours for each kind.
9. Roles: the brief lists the cells and committees Ritwik belongs to (Roles held). Work for these bodies is his; name the body in "Body / committee". Intertext Research and the anthology project are not college work — leave them out.
```

## 2. Commands to use in the project

**Evidence ledger** (attach the brief + sources):

> Prepare the evidence ledger from the attached sources, following the brief. Look first for what the brief lists under "Where the file is thin". Return the "Evidence ledger" .xlsx, then list anything you couldn't read or that needs my confirmation.

**Answer the open questions** (attach the brief + the questions pack + sources):

> Answer the numbered questions in the attached questions pack from these sources. Return one Evidence ledger row per answer, with the question number in the Notes column and a verbatim quote. Where a source gives no time or date, say so for that number rather than estimating — list those separately at the end.

**Focus on one gap** (attach the brief + sources):

> Using the brief, look only for evidence of *[e.g. B-2 · compiling and posting TU topics]* in *[2022-23]*. Return the evidence ledger for what you find.

**Fill an annexure template** (attach the template + source):

> Fill this CAS Tracker template from the attached *[duty list / award list]*. Use only the template's columns, one row per duty per date, dates as YYYY-MM-DD, Hours blank where the app has a rule.

**Before submission** (attach the brief):

> Read the brief as the Screening-cum-Evaluation Committee would. Which recorded items look weakest on evidence, and which "thin" areas would a scrutineer question first?

## 2b. Calendar records — what the *college* did (v5.8)

A source that says what the college did rather than what the teacher did — a holiday list, an academic calendar, a closure notice, an order moving classes online, an examination programme, a routine change — goes in a **separate .xlsx** with one sheet named `Calendar records`:

`Date | Date to | Kind | Classes affected | Details | Source reference | Quote | Confidence`

**Kind** must be one of nine, letter for letter: *Holiday · College closed · Classes suspended · Online teaching · Exam period · Routine changed · Session start · Session end · Other*. Dates are YYYY-MM-DD; use *Date to* only where the source states an end — where a closure notice gives none, leave it blank and say so in Details rather than inventing one.

These come in under Bring in records → Evidence Ledger → *Calendar records* and become Annexure **H-2** records. **They carry no points.** Their use is the clash: the Tracker then cards every class, duty or meeting recorded on a day the college was *closed* or classes were *suspended*, showing both records and their sources, so the teacher can answer it before a scrutineer asks. Nothing of the teacher's is changed or deleted. A *Holiday* is deliberately not a closure.

## 3. A handful of items: the hand-over

The app reads nothing itself and calls no outside service (the in-app Gemini reader was removed in v5.7). For a handful of items at a time — one screenshot, one flyer, a few pasted messages — the Evidence Ledger offers **Hand a few messages, screenshots or flyers over for reading**: attach them or paste the text, and it downloads them together with a short note saying who the teacher is, which record they belong to, and the exact ledger format to send back. Whole WhatsApp exports, a year of e-mail, or long minutes go to the Claude project with the brief, which reads large files and knows the case facts.
