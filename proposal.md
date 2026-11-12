# PHYSIS CASEFILES: From file investigator to an emerging cognitive system

Draft answers for the Round 1 proposal PDF (≤ 500 substantive words).
**The exact ten questions live on the Devpost submission form, which requires
registration; these drafts cover the known themes and must be transcribed
onto the real questions before any PDF is generated.** Nothing here has been
submitted or registered.

## 1. Project name

PHYSIS CASEFILES.

## 2. Inspiration

When a renovation goes wrong, the truth is already in the folder: the
estimate, the change order, the invoice that quietly grew. Nobody assembles
it, and reading forty documents carefully is what people avoid, so disputes
are settled by whoever remembers loudest. A NAS is where a household's
documents accumulate; it should reconstruct what happened from them.

## 3. What it does

PHYSIS Casefiles investigates one question across one folder the user
explicitly selects. It discovers contracts, estimates, invoices, change
orders, notes, and — on request — recordings and photographed documents. It
returns a casefile: a dated chronology, supported findings, conflicts quoted
from both sides, unresolved questions, and a source list where every claim
cites its file and locator. It distinguishes what a document says from what
happened in the world, and treats an empty search as a finding, not a failure.

## 4. How we built it

A Uliya Skill delegating only to UGOS's registered experts: file-agent for
discovery, document-agent for extraction and native reconciliation, photo-agent
for OCR of photographed records, knowledge-agent for transcription and saving.
No custom binaries, no Docker, no scripts — Markdown and the platform's own
capabilities. It passes UGREEN's official static checker.

## 5. Challenges

The hardest problem was honesty under completion pressure: a language model
wants to finish the story. We built abstention into every stage — three
evidence states only (supported, conflicting, not established), no arithmetic
unless currency and tax treatment are clear, no inference of fraud, payment
or causation, copies never counted as corroboration.

## 6. Accomplishments

Three synthetic fixture cases with a manually written oracle — complete
evidence, a two-source conflict, and a missing approval that must stay
unresolved — plus an adversarial document with an embedded prompt injection
the skill must ignore. Every honesty rule is exercised.

## 7. What we learned

Evidence discipline is a product feature. Users do not want a confident
story; they want to know which file says what, and to be told plainly what is
missing. Absence, correctly reported, builds more trust than a
complete-looking answer.

## 8. What's next

Round 2: run the fixtures on a real UGOS device, compare outputs against the
oracle, and record what passed and what did not. Beyond the hackathon: the
casefile method — observe, cite, abstain — is the seed of a household
cognitive system that remembers what its documents say, notices when records
contradict, and never fills a gap with imagination. The file investigator is
the first verifiable step toward that system.

## 9. A note on the system behind the skill

The skill's evidence method mirrors an open-source evidence engine the entrant
builds: append-only observations, claims checked against evidence, uncertainty
as first-class output. None of it ships in the skill; the skill stands on
UGOS's own registered experts.

## 10. Built with

UGOS Skill Creation Tool, UGREEN capability catalog v2.2.0, and AI assistance
(drafting, catalog review, static checks), disclosed per rules.
