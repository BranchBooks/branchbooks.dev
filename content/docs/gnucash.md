---
title: Importing from GnuCash
linkTitle: GnuCash
weight: 6
---

BranchBooks can start a book from a GnuCash file saved as compressed XML, GnuCash's default format.

## What comes over

- The account tree, with each account on or off budget by its type, and GnuCash's placeholder accounts.
- Every transaction, with its full history.
- Shares and amounts in other currencies, at their value in the transaction's currency. The quantity is
  kept as metadata.

Budget assignments start fresh. GnuCash budgets, scheduled transactions and prices are left out, and the
import's notes count what was skipped.

## Importing ledger files

You can also import Beancount files into an existing book. BranchBooks shows a preview first and adds
only the entries the book doesn't already have. A transaction matches on its date and amounts, not its
description, since a bank file and a hand-entered copy describe a payment differently.
