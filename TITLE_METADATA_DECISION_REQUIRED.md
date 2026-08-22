# TITLE_METADATA_DECISION_REQUIRED

**Status: UNRESOLVED — requires an author/editorial decision.** No title was changed, restored, or normalized in
this task. The manuscript, cover letter, Response Letter, and submission metadata were **not** edited. This file
only reports where the two titles currently differ.

There are **two distinct titles** in play. The working manuscript (and the accompanying letters) now carry the
**revised** title; the **iSys submission system** was registered with the **original** title. This mismatch must be
reconciled by a human, because reverting vs. keeping has opposite implications for the reviewer-driven scope
change.

## 1. Title originally registered in the submission system
> **"Generative AI for Open Government Data Access and Public Transparency: A Systematic Literature Review"**

(Per this task's statement of the submission-system record. It is **not** independently verifiable from the repo;
the repo only contains the working files, not the iSys system metadata.)

## 2. Title currently present in the revised manuscript
> **"Generative AI for Public-Sector Information Access and Public Transparency: A Systematic Literature Review"**
> — short/running form: **"Generative AI for Public-Sector Information: An SLR"**

Introduced during the Major Revision in response to the reviewers' scope criticism (OGD too narrow for the corpus).

## 3. Where each title currently appears in the project

### Revised title ("Public-Sector Information Access …") — RENDERED / authoritative
| File | Line | Field / role |
|---|---|---|
| `isys_rsl.tex` | 87–88 | `\title{…}` — **rendered manuscript title** (full) |
| `isys_rsl.tex` | 87 | `\title[…]` — **short/running header**: "…Public-Sector Information: An SLR" |
| `isys_rsl.tex` | 65 | `pdftitle` — **PDF metadata** |
| `isys_rsl.tex` | 5 | internal source comment (non-rendered) |
| `cover_letter.md` | 10 | cover-letter body (rendered) |
| `response_letter.md` | 3 | "**Manuscript:**" header (rendered) |
| `response_letter.md` | 231 | title-change "Changes" note |

### Revised title — internal support/audit docs (non-submission)
`FINAL_VALIDATION_REPORT.md:36`, `07_visual_pdf_audit.md:31`, `revision_audit.md:105`,
`COVER_LETTER_FINAL_AUDIT.md:9`, `AI_DISCLOSURE_FINAL_AUDIT.md:36,62`.

### Original title ("Open Government Data Access …") — still present
| File | Line | Role |
|---|---|---|
| `revision_audit.md` | 3 | "**Manuscript:**" header (stale — still original) |
| `HANDOFF_iSys.md` | 39, 79 | handoff notes referencing the original title |
| `COVER_LETTER_FINAL_AUDIT.md` | 8, 77, 93 | audit text describing the *old* title (historical) |
| `AI_DISCLOSURE_FINAL_AUDIT.md` | 36, 64 | audit text describing the corrected source comment (historical) |

**Net:** every *rendered submission artifact* (manuscript title/short-title/PDF-metadata, cover letter, Response
Letter header) is on the **revised** title. The **original** title survives only in the submission-system record
(external) and in internal audit/handoff notes (`revision_audit.md:3` header, `HANDOFF_iSys.md`).

## 4. Does the Response Letter explicitly explain the title change?
**Yes.** `response_letter.md` (§"Title and scope (Reviewers A & C — scope clarification)", ~lines 222–232) states
that the reviewers found the corpus broader than OGD *stricto sensu*, that OGD remains a **paradigmatic** case, and
that the title was updated to "Public-Sector Information Access…" to describe the scope already covered — explicitly
noting **the corpus was not expanded, only the terminology**. So the change is documented and justified there.

## 5. Does the cover letter use the original or the revised title?
**Revised** — `cover_letter.md:10` uses "Generative AI for Public-Sector Information Access and Public
Transparency: A Systematic Literature Review".

## 6. Files that would need synchronization under each option

### Option A — KEEP the revised title ("Public-Sector Information Access")
- **External (human):** update the **iSys submission-system** title field to the revised title so system metadata
  matches the manuscript. *(Cannot be done from the repo.)*
- **Repo (rendered): none** — `\title`, short title, `pdftitle`, cover letter, and Response Letter header are
  already revised.
- **Repo (optional tidy, internal only):** `revision_audit.md:3` header and `HANDOFF_iSys.md:39,79` still show the
  original title; update for internal consistency if desired (not submission-facing).
- **Coherence note:** this option is consistent with the reviewer-driven scope broadening already reflected in the
  abstract, introduction, method (CI1), results and conclusion (all use "public-sector information").

### Option B — REVERT to the original title ("Open Government Data Access")
- **Repo (rendered):** `isys_rsl.tex:87–88` (`\title` full), `isys_rsl.tex:87` (short/running title — currently
  "Public-Sector Information: An SLR"), `isys_rsl.tex:65` (`pdftitle`); `cover_letter.md:10`; `response_letter.md:3`
  header.
- **Response Letter:** the §"Title and scope" item (~222–232) would have to be **rewritten**, since it currently
  argues *for* the broadened title in response to the reviewers.
- **Manuscript body cascade (significant):** the scope was broadened to "informação do setor público" throughout —
  Abstract/Resumo, Introduction objective, Background (`subsec:bg_ogd`), Method CI1, Related Work differentiator,
  Discussion and Conclusion, plus the keyword "Public-Sector Information". A narrower OGD title would reintroduce
  the **construct-validity tension** the revision resolved and contradict the reviewers' request; these passages
  would need reconciliation, not just the title string.
- **Internal:** `revision_audit.md`, `HANDOFF_iSys.md` already carry the original title.
- **External (human):** submission-system metadata already holds the original title (no change needed there).

### Option C — Hybrid (keep revised title, but confirm with the editor first)
- No file change now; a short note to the handling editor requesting permission to update the registered title to
  the revised one (attaching the Response Letter's "Title and scope" justification). If approved → Option A.

## Recommendation posture
**Not resolved here, by instruction.** For the authors/editor: Option A (keep revised, update system metadata) is
the lower-risk path because the entire manuscript body, keywords, and Response Letter are already aligned to the
broadened scope, and the change is reviewer-requested and documented; Option B triggers a broad body-text cascade
and re-opens the construct-validity tension. Confirm the title with the handling editor before finalizing the
system metadata.
