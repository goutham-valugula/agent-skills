---
name: bank-reconciliation-reviewer
description: Compare user-provided bank transaction exports with bookkeeping or ledger exports, suggest evidence-backed matches, and list exceptions for human review. Use for small-business or bookkeeping reconciliation support; do not post or change accounting records.
---

# Bank reconciliation reviewer

Help a small-business owner or bookkeeper review bank statement lines against an accounting or ledger export. The result is a clear review worksheet—not an official reconciliation, accounting entry, tax conclusion, or replacement for accounting software or a qualified bookkeeper.

## Inputs and privacy

Ask for only what is needed:

- A bank transaction export and the corresponding ledger or bookkeeping export for the same account and period; CSV or spreadsheet files are preferred.
- The account currency, date format, statement start/end dates, and opening/closing balances when available.
- Any relevant notes about pending transactions, expected clearing delays, or known payee/reference aliases.

Do not request bank logins, passwords, one-time codes, full card numbers, or unrelated personal details. Encourage the user to remove full account numbers and redact unrelated transactions before sharing files. Work only with the supplied files; do not upload them to another service or connect to a bank unless the user explicitly selects an available, trusted integration.

## Review workflow

1. **Confirm the scope.** Identify the bank account, currency, period, and which file is the bank record versus the ledger. If the files cover different periods or accounts, stop and ask for the missing or corrected export.
2. **Check the data before matching.** Map date, description/payee, reference, debit, credit, and amount columns. Preserve each original row number or transaction ID. Report unreadable rows, duplicate IDs, mixed currencies, ambiguous date formats, missing amounts, and any sign convention that is unclear. Do not silently repair source values.
3. **Check available totals.** Where the data contains opening and closing balances, compare them with the transaction totals using the stated debit/credit convention. Show the arithmetic and any difference. Do not claim the books reconcile if required balances or transactions are missing.
4. **Propose only evidence-backed matches.** Prefer a unique match supported by amount plus reference/payee and a reasonable date relationship. Account for weekends or normal clearing delays only as a possible timing explanation. Treat amount-only or description-only similarity as weak evidence.
5. **Handle complex payments conservatively.** A batch deposit, one payment covering several invoices, a partial payment, a transfer between accounts, a refund, a fee, or a reversal may have multiple explanations. Show a grouped or split match only as a *candidate* when the rows and totals support it; never force it to zero or assume a transaction category.
6. **Label every bank and ledger row.** Use clear statuses such as `Unique likely match`, `Possible match — review`, `Unmatched bank item`, `Unmatched ledger item`, `Possible duplicate`, `Timing item to check`, or `Data issue`. Keep ambiguous items unresolved and state exactly what evidence is missing.
7. **Recheck coverage and arithmetic.** Ensure every source row is accounted for once in the review output, no transaction is matched twice, and any grouped totals equal their component rows. Compare row counts and totals with the source exports.

## Output

Lead with the account/period reviewed and the overall status. Then provide:

1. A short totals check, including any opening/closing balance difference and its calculation.
2. A match table with bank row ID, ledger row ID, dates, amounts, status, evidence, and reviewer question.
3. Separate lists for unmatched bank rows, unmatched ledger rows, possible duplicates, timing items, and data problems.
4. The smallest next action to resolve each exception, such as checking an invoice, payment advice, transfer, or source export.

Keep source references beside each proposed match so a person can verify it quickly. If the files are too large or the available tools cannot inspect them reliably, say so and narrow the review rather than implying full coverage.

## Boundaries

- Do not change, reconcile, categorize, delete, or post anything to an accounting system or source file.
- Do not invent a payee, account code, tax treatment, or reason for a difference. Do not create a journal entry or recommend tax treatment.
- A suggested match is not proof of payment, business purpose, or proper accounting treatment. The user or their bookkeeper must approve the final reconciliation and any adjustment.
- Do not report “reconciled” unless the complete statement period, required balances, row coverage, and arithmetic have all been checked—and even then describe it as a review result, not an official accounting approval.

## Example request

“Compare these bank CSV and bookkeeping exports for October. The account is in SGD and the dates are day/month/year. Flag exact matches, partial or batch payments, duplicates, and anything uncertain. Do not change the files or post entries.”
