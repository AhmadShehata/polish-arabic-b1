# polish-arabic-b1 — Polish Language Learning Skill for Arabic Speakers

A **GitHub Copilot Skill** that acts as a personalised Polish language coach for Arabic-speaking learners targeting the **TELC B1** proficiency exam. The skill is built around Arabic-first explanations and leverages the learner's native linguistic intuition to accelerate Polish acquisition.

---

## 📖 What This Project Does

`polish-arabic-b1` is an AI skill (a structured prompt + reference system) that enables a Copilot-powered assistant to:

- **Teach Polish grammar** using Arabic analogies (e.g. Polish cases ↔ Arabic إعراب)
- **Provide verb conjugations** for all B1-level verbs across 10 thematic groups, including aspect pairs
- **Explain pronunciation** of all Polish sounds with Arabic phonetic equivalents
- **Deliver topic-based vocabulary** covering 12 real-life themes aligned with the TELC B1 syllabus
- **Guide exam preparation** with writing templates, speaking frameworks, and a 4-week study sprint plan
- **Correct errors** by naming the violated grammar rule and offering a reinforcing example
- **Translate between Arabic and Polish** instantly for words, phrases, and sentences
- **Update a Notion workspace** (Ahmed's B1 hub) via the Notion MCP tool

The skill activates automatically whenever the user asks about any Polish language topic — grammar, vocabulary, pronunciation, cases, verbs, adjectives, aspects, tenses, or TELC B1 exam preparation.

---

## 🗂️ Repository Structure

```
polish-arabic-b1/
├── SKILL.md                  # Main skill definition — loaded by the AI at session start
└── references/
    ├── grammar-cases.md      # The 7 Polish cases with Arabic analogies, ending tables, preposition maps
    ├── verbs.md              # 10 verb groups (60+ verbs), aspect pairs, tense formation, conditional
    ├── pronunciation.md      # Full alphabet, Arabic-equivalent sounds, stress rules, practice drills
    ├── vocabulary.md         # 12 thematic sections (~300 words) with Arabic translations and examples
    └── exam-prep.md          # TELC B1 exam structure, writing templates, speaking frameworks, 4-week sprint
```

### File Roles

| File | Purpose | When Loaded |
|------|---------|-------------|
| `SKILL.md` | Core persona, teaching philosophy, quick-answer rules, Notion page IDs | Always — on every activation |
| `references/grammar-cases.md` | Deep-dive on all 7 cases, adjective agreement, comparison | When the user asks about cases, endings, prepositions |
| `references/verbs.md` | Full conjugation tables, aspect pairs, future/conditional tense | When the user asks to conjugate a verb or asks about aspect |
| `references/pronunciation.md` | Sound-by-sound breakdown with Arabic equivalents | When the user asks about sounds, letters, or reading aloud |
| `references/vocabulary.md` | Thematic word lists with Arabic translations | When the user asks for vocabulary by topic |
| `references/exam-prep.md` | TELC B1 exam strategies, letter templates, speaking structure | When the user asks about the exam or writing/speaking tasks |

---

## 🛠️ Technologies & Frameworks

| Component | Technology |
|-----------|-----------|
| **AI Runtime** | GitHub Copilot (Claude-based) — the skill runs as a Copilot Skill |
| **Skill Format** | Markdown-based prompt engineering (`SKILL.md` + `references/`) following the [GitHub Copilot Skills specification](https://docs.github.com/en/copilot) |
| **Notion Integration** | [Notion MCP tool](https://developers.notion.com/) — used to write back to Ahmed's B1 Notion workspace |
| **Target Language** | Polish (B1 CEFR level) |
| **Explanation Language** | Arabic (Modern Standard / Levantine) |
| **Exam Target** | [TELC Polski B1](https://www.telc.net/en/candidates/language-examinations/exams/detail/telc-polski-b1.html) |

---

## 🚀 How to Use / Run It

### Prerequisites
- Access to a GitHub Copilot-enabled environment (GitHub.com chat, VS Code Copilot Chat, etc.)
- The skill must be registered/available in the Copilot session

### Activating the Skill

The skill triggers automatically when the user mentions any of the following:

- Any Polish word, phrase, or grammar concept (*Mianownik*, *Dopełniacz*, etc.)
- Learning Polish, practising Polish, or reviewing Polish
- TELC B1 exam preparation, writing practice, speaking practice
- Translating between Arabic and Polish
- Questions like *"how do I say X in Polish"*, *"what case does Y take"*, *"conjugate Z"*
- Anything about Polish pronunciation, aspect pairs, or adjective agreement

### Example Interactions

```
User: "كيف أصرّف فعل 'jechać' في الماضي؟"
→ Skill returns full conjugation table with masc/fem endings and aspect pair

User: "What case does 'szukać' take?"
→ Skill answers: Dopełniacz — always. Gives example: Szuka pracy.

User: "Give me vocabulary for health topics"
→ Skill loads references/vocabulary.md Section 8 — Health

User: "Write me a formal letter for the TELC exam about a complaint"
→ Skill uses the formal letter template from references/exam-prep.md

User: "Remind me of all prepositions that take Narzędnik"
→ Skill answers directly from the Case → Preposition Quick Map in SKILL.md
```

### Notion Updates

When the user asks to save something to Notion, the skill uses the Notion MCP tool with these pre-configured page IDs:

| Page | Notion Page ID |
|------|---------------|
| Hub (Road to B1) | `33275b8b-badf-811c-af16-eceb3d206f4e` |
| Vocabulary System | `33275b8b-badf-8155-bfdf-f565e5c1157c` |
| Grammar System B1 | `33275b8b-badf-8147-b96e-c6c6e0e91a68` |
| Quick Reference | `33275b8b-badf-816a-b340-dcaa1af4bdfd` |
| Exam Prep (TELC B1) | `33375b8b-badf-81ee-878a-c7c90b0a0455` |
| Verb Reference | `33775b8b-badf-81d7-a0eb-e46118ca8697` |

---

## 🧠 Teaching Philosophy

The skill is built on four core principles:

1. **Arabic-first**: Every Polish pattern is introduced through an Arabic analogy
   - Polish 7 cases → Arabic إعراب (same logic, more cases)
   - Polish verbal aspect → Arabic فَعَل / يفعل (completed vs ongoing)
   - Polish gender → Arabic مذكر/مؤنث + neuter (one new category added)

2. **Pattern over memorisation**: Teach the rule, then derive many words from it

3. **B1 communicative focus**: Prioritise structures that unlock real conversation

4. **Error tolerance**: Errors are corrected constructively; Poles appreciate every attempt

---

## 📚 Content Coverage

| Area | Coverage |
|------|---------|
| Grammar cases | All 7 Polish cases with Arabic analogies, ending tables for all 3 genders, adjective agreement, comparison |
| Verbs | 60+ verbs across 10 groups (existence, motion, modal, communication, daily life, work, feeling, action, health, home), full aspect pairs list, future and conditional tense formation |
| Pronunciation | Full 32-letter alphabet, all digraphs (sz, cz, rz, ch, dz, dź, dż), nasal vowels (ą, ę), stress rules, Arabic equivalents for every sound |
| Vocabulary | ~300 words across 12 TELC B1 topics: survival, places, daily routine, family, numbers/time, food, transport, health, work, emotions, connectors, environment |
| Exam prep | Reading/listening/writing/speaking strategies, formal & informal letter templates, 5-step monologue structure, role-play scenarios, 4-week study sprint, grammar pre-exam checklist |