---
title: Getting started
weight: 1
---

BranchBooks is a double-entry accounting app with envelope budgeting and target budgeting, installed on
your own device. Each book is a plain-text ledger in a git repository.

> [!WARNING]
> BranchBooks is early software. Keep your own copy of anything you put in it.

## What it runs on

Windows, 64-bit. An Android app is planned.

## Your first book

1. [Install BranchBooks](install.md).
2. Choose **New book** and pick how it starts:
   - **Empty**, in the currency you budget in.
   - **The sample ledger**, to look around with made-up figures.
   - **A clone** of a book already on a git host, over HTTPS with a token.
   - **A GnuCash file**, with its accounts and full history. See [Importing from GnuCash](gnucash.md).
3. On **Accounts**, choose **Add an account or category** for each bank account and card, with today's balance. See
   [Accounts](accounts.md).
4. Start assigning money on **Budget**.

## How it fits together

- [Accounts](accounts.md) covers adding accounts and categories, and starting balances.
- [Budgeting](budgeting.md) explains envelopes, Unassigned, overspending and credit cards.
- [Targets](targets.md) covers monthly amounts and savings goals.
- [Loans](loans.md) tracks mortgages and other loans: payments split into interest and principal, and payoff.
- [Scenarios](scenarios.md) are what-if copies of your book, on git branches.
- [Sync](sync.md) keeps a book the same across devices through a git host.
- [The ledger format](ledger-format.md) shows what BranchBooks writes into your files.
