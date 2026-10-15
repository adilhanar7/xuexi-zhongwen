# HSK — Vocabulary & Mock Tests (汉语)

One web page that combines a **vocabulary trainer for HSK 1–5** with a **mock-test and lesson app**, plus **CSCA Chinese exam prep**. The interface is available in **English, Russian and Chinese**.

Live page: https://claude.ai/artifact/3BoK29LMLrZAvfToAyZfyF

---

## What's inside

The top bar switches between the two parts and holds the **EN / RU / 中文** language buttons.

### 📖 Vocabulary (HSK 1–5)
- **Search** – by hanzi, pinyin, Russian or English.
- **Daily plan** – each level is split into days of 7 words, with a phrase of the day, a "test yourself" mode that hides translations, and a "mark as learned" button.
- **Dictionary** – every entry in pinyin order, filterable by words / phrases.
- **My list** – tap ☆ on any card to collect words.
- Four character styles (print sans, print serif, brush, cursive) and a 🔊 button on every card (browser voice).

### 🧪 Mock tests (汉语水平模拟测试)
- **Exam mode** (submit once) and **Practice mode** (instant feedback).
- Five sections: listening, reading, writing, translation, grammar.
- **Test words** selector: *My list*, *HSK lists* or *Both*, with HSK 1–5 buttons (multi-select).
- **Listening transcripts**: every recording has a "Show transcript" button; after submitting, the text and translation are always shown.
- **Review of mistakes** after every test: your answer, the correct answer, notes, transcripts, and a jump to the question.
- **Test history** with a review of every saved test.
- **Daily lessons**, **vocabulary & flashcards**, and an **add-a-word** form: type a word and the pinyin, meaning, example sentence and useful expressions are filled in automatically.
- **Resources**: paste Chinese text, add a link, or upload a photo, and a lesson (vocabulary, grammar, expressions) is created from it.

### 🎓 CSCA prep
- Two tracks built from the exam papers provided: **Humanities (文科中文)** and **Technical (理科中文)**, the latter with math and physics terms and a glossary.
- A new random set of questions is generated every time the app opens, and "New set" makes another one.
- Every finished CSCA test is saved on the **CSCA 记录** page, where you can review your mistakes.

---

## Word data

| Level | Content |
|---|---|
| HSK 1–2 | Original lists with Russian translations |
| HSK 3 | Only about 35 words (too few for a test of its own; it falls back to your list) |
| HSK 4 | About 1,000 words (new HSK 3.0 list) |
| HSK 5 | About 1,600 words (new HSK 3.0 list) |

The HSK 4 and 5 lists come from the MandarinBean PDFs. Those entries have **English translations only**.

---

## Using the AI features

Lessons from text/photos/links and the automatic word fill use Claude. The page is published with the `sample` capability: the viewer asks for permission on first use. Without it:
- Lessons from links or pasted text fall back to a basic dictionary-based lesson.
- Photos need AI (or you can type the text).
- Automatic word fill is unavailable; fill the fields by hand.

The explanation language for lessons follows the language switcher.

---

## Your data

Everything is stored in **your browser** (localStorage and IndexedDB): progress, favourites, added words, test history, CSCA records, resources and lessons. Nothing is sent to a server except the text or photo you ask Claude to turn into a lesson. Clearing the browser data, or using another browser or device, starts you from scratch.

---

## How it is built

- A single self-contained HTML file.
- The two parts run side by side in **Shadow DOM** so their styles and scripts do not clash; a small bridge lets the test app read the HSK word lists.
- Interface translation works from a dictionary that rewrites text on screen; it is applied to the interface strings listed in the file.
- To change something, edit the HTML and republish; small edits can be sent as find-and-replace pairs.

---

## Known limitations

- **Interface translation is partial.** The main screens are translated, but the daily lessons, history, vocabulary/flashcard pages and long sentences with numbers are not fully covered. Daily-plan topic titles stay in Russian.
- **HSK systems are mixed.** Levels 1–3 follow the older lists; levels 4–5 follow the new HSK 3.0 lists.
- **CSCA answers are not official.** The source papers have no answer keys, so the answers were worked out by hand and questions with an unclear intended answer were left out. Check important ones against an official key.
- **Listening depends on your browser's Chinese voice.** Chrome, Edge or Safari work best; the transcript button helps when no voice is installed.
- **Mixed-level tests are uneven.** HSK 5 has far more words than HSK 1, so a test mixing them draws mostly from HSK 5.

---

## Sources

- HSK 4 and HSK 5 vocabulary: MandarinBean (New HSK Vocabulary, levels 4 and 5).
- CSCA practice questions: the exam papers supplied by the owner of this app.
