# Casefile report format

The report is returned in conversation by default. Saving happens only after
the user requests it and confirms the destination. Every section below is
required; if a section has nothing to report, say so explicitly rather than
omitting it.

## 1. Question and scope

The user's question in their words; the folder investigated; the date range
applied, if any; what was excluded and why.

## 2. Chronology

Events ordered by documented dates. Each entry states: the date, which kind
of date it is (document date, stated event date, or inferred order), what the
source says, and the source path with its locator. Entries with no reliable
date go last, marked undated.

## 3. Supported findings

Each finding: the assertion, its evidence state (supported), the source path
and locator, and the quoted span. If two findings rest on copies of one
record, say so.

## 4. Conflicts and possible discrepancies

Each conflict: the two sources, what each says, quoted, and where they
disagree. No cause is invented and no side is chosen. A charge without a
matching approval is reported here as a discrepancy, without speculation
about intent.

## 5. Unresolved questions

What could not be established: missing records, inaccessible files, ambiguous
documents, comparisons that could not be made (with the reason). Absence of a
found record is reported as missing evidence, not as proof of absence.

## 6. Source list

Every file actually used: path, type, and the locator convention returned.
Files discovered but not used are listed with the reason.

## 7. Coverage and limitations

What was searched, what was readable, what was truncated or failed, and
whether the result set was reported complete. An explicit empty result is
reported as no matching files in the searched scope.

## 8. Suggested next investigations

Bounded, concrete next steps the user could take (for example: locate the
missing approval, request the itemized invoice). No step asserts anything
about what the missing evidence would show.
