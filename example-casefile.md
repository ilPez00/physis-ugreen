# Example casefile — manually written illustration

**Status: hand-written by the entrant against fixture Case A
(`fixtures.md`). This is NOT a device run, NOT model output, and NOT evidence
of execution. It illustrates the report shape defined in
`skill/physis-casefiles/references/report-format.md` and the evidence rules
the skill enforces. Actual runtime results on a UGREEN device may differ and
will be recorded separately in Round 2.**

Fixture Case A inputs: question *"What changed between estimate and final
invoice?"*; folder containing `A1-estimate.txt`, `A2-approval.txt`,
`A3-invoice.txt`.

---

## 1. Question and scope

Question (user's words): what changed between estimate and final invoice?
Scope: the selected folder only; all three files in it; no date range applied.
Nothing outside the folder was read.

## 2. Chronology

- 2026-03-03 (date as written in the document): `A1-estimate.txt` records an
  estimate of EUR 18,000, inclusive of tax, for the work.
- 2026-04-12 (date as written in the document): `A2-approval.txt` records
  both parties signing a change order for plumbing, EUR 2,700, tax-inclusive.
- 2026-05-07 (date as written in the document): `A3-invoice.txt` records the
  final invoice, EUR 20,700 tax-inclusive, stated as comprising the original
  EUR 18,000 and plumbing EUR 2,700.

All three dates are document-internal dates. That a document bears a date is
not proof the events it describes happened on that date.

## 3. Supported findings

- An estimate of EUR 18,000 tax-inclusive exists — supported by
  `A1-estimate.txt` ("estimated EUR 18,000 inclusive of tax").
- A plumbing change order of EUR 2,700 tax-inclusive, recorded as signed by
  both parties, exists — supported by `A2-approval.txt`.
- A final invoice of EUR 20,700 tax-inclusive exists, itemized in the
  document as EUR 18,000 plus EUR 2,700 plumbing — supported by
  `A3-invoice.txt`.
- Arithmetic shown: EUR 18,000 + EUR 2,700 = EUR 20,700. Operand currency and
  tax treatment match (tax-inclusive), so the comparison is valid.

No finding is offered that payment occurred or that the work was completed:
no document in scope records either.

## 4. Conflicts and possible discrepancies

None found. The invoice's stated composition matches the estimate plus the
signed change order. On these documents alone there is no unsupported charge.

## 5. Unresolved questions

- Whether the EUR 18,000 estimate and the invoice's EUR 18,000 component
  cover exactly the same scope (the documents in scope do not itemize the
  base work) — not established.
- Whether any other change orders existed but were not placed in this folder
  — not established; absence here is not proof of absence.

## 6. Source list

- `A1-estimate.txt` — text, used for the estimate finding.
- `A2-approval.txt` — text, used for the change-order finding.
- `A3-invoice.txt` — text, used for the invoice finding and the arithmetic.
No discovered file was left unused; no locator convention beyond the file
itself was returned by the fixture.

## 7. Coverage and limitations

All three files in the selected folder were read in full; the result set was
complete for this fixture. This example asserts nothing about files outside
the folder, about signatures' validity, or about events after 2026-05-07.

## 8. Suggested next investigations

- Obtain the itemized breakdown of the EUR 18,000 base work to confirm scope
  identity between estimate and invoice.
- If payment is in question, look for payment records — none are in scope.
