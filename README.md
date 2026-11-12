# PHYSIS Casefiles

A Uliya Skill for the UGREEN Hackathon 2026 on AI NAS ("Bring Your Skills to
UGOS"). PHYSIS Casefiles investigates one question across one folder the user
explicitly selects on a UGREEN NAS — contracts, invoices, change orders,
notes, and on request recordings and photographed documents — and returns a
**casefile**: a dated chronology, supported findings, conflicts quoted from
both sides, unresolved questions, and a source list where every claim cites
its file and locator.

## The idea in one line

Distinguish what a document says from what happened in the world — and say
plainly what is missing instead of filling the gap with a plausible story.

## The three evidence states

Every finding carries exactly one state:

- **Supported** — a named source directly supports the assertion, cited by
  path and locator.
- **Conflicting** — two sources make incompatible claims; both are cited and
  quoted, no side is chosen.
- **Not established** — records are missing, inaccessible, ambiguous or
  insufficient. The absence of a found record is not proof the record never
  existed.

## How it works

The skill is Markdown only. It delegates to UGOS's registered experts —
`file-agent`, `document-agent`, `photo-agent`, `knowledge-agent` — using the
documented UGREEN capability catalog (v2.2.0). It uses native, read-only
operations wherever they exist (`ug-filesystem find`, `ug-document extract`
and `reconcile`, `ug-photo vision-ocr` and `search-picture`), and touches
approval-classified operations (`ug-knowledge audio-transcription`,
`save-text`) only with explicit user request and platform approval. No
scripts, no binaries, no Docker, no network calls.

## Repository contents

- `skill/physis-casefiles/` — the skill package (`SKILL.md` + references),
  also shipped as the Round 1 ZIP.
- `fixtures.md` — three synthetic evaluation cases with a manually written
  oracle (complete evidence / genuine conflict / missing approval), plus an
  adversarial document with an embedded prompt injection the skill must
  ignore. Fixtures establish expected outcomes, not execution results.
- `proposal.md` — draft Round 1 proposal answers (≤ 500 substantive words).
  The exact ten application questions live on the Devpost submission form;
  these drafts cover the known themes and must be transcribed onto the real
  questions before any PDF is generated.
- `check-result.json` — output of UGREEN's official static checker
  (`status: static-pass`, zero errors) for the current skill.

## Status and honesty

- Nothing has been registered or submitted yet.
- The skill has passed **static checks only**. It has not executed on a UGREEN
  device; agent reasoning, gateway approvals and output locators on the real
  platform are not established by a static pass.
- Developed during the competition with AI assistance (drafting, catalog
  review, static checks), disclosed per contest rules. No UGREEN kit files,
  catalogs or third-party code are bundled in this repository.
- The entrant is responsible for verifying eligibility, originality and
  disclosure completeness before submission.

## Links

- Contest: https://ugreenhackathon.devpost.com/
- Starter kit: https://ai.ugreen.com/pages/hackathon-starter-kit
