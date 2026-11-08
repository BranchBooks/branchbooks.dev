---
title: The ledger format
weight: 7
---

Books are [Beancount](https://beancount.github.io/) text files, so they stay readable in any text editor
and open in Beancount and Fava. Every fixture in BranchBooks' tests is checked against real Beancount.

## Files

`main.beancount` holds the options and the account opens and closes. Transactions go in one file per
year, such as `2026.beancount`, included from `main.beancount`.

## Budget flags

Whether an account is on budget is metadata on its `open`:

```beancount
2026-10-01 open Assets:Checking USD
  budget: "on"            ; or "off" (assets and liabilities)
2026-10-01 open Expenses:Tax:Federal USD
  budget: "excluded"      ; categories with no flag are budgeted
2026-10-01 open Expenses:Food
  budget: "placeholder"   ; only groups its sub-accounts
```

## Envelope entries and targets

Assignments, moves and targets are Beancount `custom` entries:

```beancount
2026-10-01 custom "envelope-assign" Expenses:Food:Groceries 600.00 USD
2026-10-10 custom "envelope-move" Expenses:Housing:Rent Expenses:Food:Groceries 20.00 USD
2026-01-01 custom "target" Expenses:Housing:Rent 1400.00 USD
  recurrence: "monthly"
2026-01-01 custom "target" Expenses:Savings:CarFund 6000.00 USD
  due: 2026-06-01
```

## Every change is a commit

Each change you make is one small edit to the text and one git commit, so a book's history shows what
changed and when. Nothing outside the edited lines changes.

## Not supported yet

Some Beancount features are reported as errors, never miscounted: `pad`, costs and prices on postings,
`pushtag` and `pushmeta`. Plugins are not run. Foreign currency budgeting and bank connections are not
built yet.
