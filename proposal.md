# PHYSIS CASEFILES: From file investigator to an emerging cognitive system

Round 1 proposal answers, mapped to the ten official Devpost questions.

## 1. What does your Skill do? (one sentence)

PHYSIS Casefiles investigates one question across a folder you select and
returns a source-cited casefile: dated chronology, supported findings,
conflicts quoted both sides, unresolved questions, source list.

## 2. Who is your target user, and what is their problem?

Homeowners and small offices whose NAS holds contracts, estimates, change
orders and invoices. When a project goes wrong the truth is in the folder,
but nobody re-reads forty documents, so disputes are settled by the loudest
memory.

## 3. What is your solution?

A Uliya Skill that reconstructs what happened from the folder's own
documents. Every finding carries one of three states — supported, conflicting,
not established — cited to the named file. Gaps are reported as missing
evidence, never filled with a story.

## 4. What is the main user flow?

You name the folder and ask one question. The skill discovers documents,
extracts dates, amounts, parties and commitments, reconciles agreements
against invoices, optionally transcribes recordings or reads photographed
documents, and returns the casefile in conversation. Saving happens only on
your request and confirmed destination.

## 5. How is your idea different from existing tools or common AI solutions?

Search finds documents; chat assistants complete the story confidently.
Casefiles refuses: no arithmetic unless currency and tax treatment match, no
inference of fraud, payment or causation, copies never counted as
corroboration, an empty search reported as a finding. Absence, correctly
reported, is the product.

## 6. Which UGREEN AI NAS features does your Skill use, and at which step?

Discovery: `ug-filesystem find`/`ls` via file-agent. Extraction and
comparison: `ug-document extract`, `metadata`, native `reconcile` via
document-agent. Optional enrichment: `ug-knowledge audio-transcription`
(approval), `ug-photo vision-ocr`/`search-picture` via photo-agent. Saving:
`ug-knowledge save-text` (approval). All through UGOS's registered agents.

## 7. What is your technical approach?

A Markdown-only Skill: no scripts, binaries or network calls. Each stage
delegates to one registered expert with an instruction built from the user's
actual inputs and real upstream results; nothing is invented between stages.
Mappings follow UGREEN's catalog v2.2.0. Approval-classified operations run
only after explicit confirmation. Documents are untrusted evidence: embedded
instructions are ignored. Passes the official static checker, zero
diagnostics.

## 8. What have you built so far? What is not built yet? What still needs
testing on a NAS?

Built: the complete Skill, three fixture cases with a manual oracle
(complete evidence, a two-source conflict, a missing approval), an adversarial
prompt-injection document, a worked example report, a clean static check.
Not built: nothing runs on a device yet — a static pass does not establish
agent reasoning, approvals or returned locators. All of that needs testing
on a NAS.

## 9. How will you test your Skill if you become a Finalist?

Core 1 (complete evidence): estimate EUR 18,000 plus a signed EUR 2,700
change order must reconcile to the EUR 20,700 invoice, every step cited.
Core 2 (conflict): a EUR 2,700 approval against a EUR 4,100 invoice must be
reported as a EUR 1,400 discrepancy, both sources cited, never as fraud.
Edge: a missing approval plus a document with an embedded prompt-injection
instruction — the Skill must report "not established", refuse the injection,
not invent knowledge of the inaccessible file.

## 10. What are the known limits, risks, or outside dependencies?

Static checks only so far. OCR and transcription quality on scanned or
noisy files is unverified on device; illegible scans must be reported
unreadable, not guessed. Depends on UGREEN's registered experts, their
approval flow, and actual device behavior — catalog examples are placeholders,
device responses authoritative. No privacy or deployment claims without
verification. AI assistance disclosed per rules.
