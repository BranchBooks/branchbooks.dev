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

1. [Install BranchBooks](install).
2. Choose **New book** and pick how it starts:
   - **Empty**, in the currency you budget in.
   - **The sample ledger**, to look around with made-up figures.
   - **A clone** of a book already on a git host, over HTTPS with a token.
   - **A GnuCash file**, with its accounts and full history. See [Importing from GnuCash](gnucash).
3. On **Accounts**, choose **Add account** for each bank account and card, with today's balance. See
   [Accounts](accounts).
4. Start assigning money on **Budget**.

## How it fits together

- [Accounts](accounts) covers adding accounts and categories, and starting balances.
- [Budgeting](budgeting) explains envelopes, Unassigned, overspending and credit cards.
- [Targets](targets) covers monthly amounts and savings goals.
- [Scenarios](scenarios) are what-if copies of your book, on git branches.
- [Sync](sync) keeps a book the same across devices through a git host.
- [The ledger format](ledger-format) shows what BranchBooks writes into your files.
