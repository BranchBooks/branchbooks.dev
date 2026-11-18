---
title: The ledger format
weight: 7
---

Books are plain text in BranchBooks' own format, `.branchbooks`: blocks of named fields that explain themselves,
in any text editor. The full description is
[FORMAT.md](https://gitlab.com/branchbooks/branchbooks/-/blob/main/docs/FORMAT.md) in the repository.

## Files

A book is a folder, and a git repository:

- `book.branchbooks` holds the `book` block (the book's currency) and one `account` block per account.
- One file per year, such as `2026.branchbooks`, holds that year's transactions, budget entries and loan terms.

## Accounts and budget settings

```
account Assets:Checking
  opened: 2026-10-01
  currencies: USD
  budget: on

account Expenses:Tax:Federal
  opened: 2026-10-01
  budget: excluded

account Expenses:Food
  opened: 2026-10-01
  budget: placeholder
```

`budget` is `on` or `off` for accounts, `excluded` for categories that never use an envelope, and `placeholder` for
a parent that only groups its sub-accounts. A category with no setting is budgeted. Names may hold spaces, such as
`Liabilities:Chase Visa`.

## Transactions

```
txn 7Q2M4K9XHD
  date: 2026-01-15
  payee: Employer
  note: Paycheck
  post -2000.00 USD Income:Salary
  post  2000.00 USD Assets:Checking
```

Every dated entry has a random id after its keyword, so two devices adding entries on the same day rarely touch the
same lines, and a sync can merge them entry by entry.

## Budget entries

Assignments, moves, targets and loan terms are entries of their own:

```
assign 5D1R7TXK2M
  date: 2026-10-01
  envelope: Expenses:Food:Groceries
  amount: 600.00 USD

target 8WQ4C6T1PB
  date: 2026-01-01
  category: Expenses:Savings:CarFund
  amount: 6000.00 USD
  due: 2026-06-01
```

See [Loans](loans.md) for the `loan` block.

## Every change is a commit

Each change you make is one small edit to the text and one git commit, so a book's history shows what changed and
when. Nothing outside the edited entries changes.

## Format versions

The `book` block names the format version. A book that holds loan terms is version 2; others stay at 1. An app too
old for a book's version opens it read-only and says which version of BranchBooks it needs, instead of misreading
it.

## Coming from Beancount

Beancount files come in through an import (**Files**, or a [GnuCash](gnucash.md) file), which writes them in this
format. Some Beancount syntax isn't read yet, such as `pad`, costs and prices on postings, and `pushtag`; the
import reports it as an error and never miscounts.
