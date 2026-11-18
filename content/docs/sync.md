---
title: Sync
weight: 5
---

A book can stay on one device, or sync with a git repository on a host you choose. The host's own access
control decides who can read it. There is no BranchBooks server or account.

## Setting up

In [Settings](settings.md), under **This book**, give the remote's HTTPS address and an access token from
your git host. The
token is kept in Windows Credential Manager, never in a file, and is only ever sent to that remote's
host over HTTPS.

To use a book on a second device, choose **New book**, then clone it from the same address.

## When it runs

When a book opens, after each change you save, and when you press **Sync**.

## What it does

- Only this device changed: your changes are pushed.
- Only the remote changed: your copy catches up.
- Both changed: the changes are merged in one commit, checked like any other change, then pushed.

Scenarios and closed months sync too.

## When it stops

When both sides changed the same file, the changes are merged entry by entry: entries added on both
devices are all kept, and an entry changed on only one side takes that change.

Sync stops without pushing anything, and keeps your local changes, when:

- both sides changed the same entry differently,
- the merge would add ledger errors, or
- the book's files have changes made outside BranchBooks that aren't saved yet.

## Choosing between changes

When both devices changed the same entry, BranchBooks shows each one, this device's version beside the
remote's. Choose which to keep for each (this device's is chosen to start), or keep all of one side's, then
**Merge and sync**. Nothing is chosen for you: **Not now** leaves both as they are.

## Replacing the remote

If a book's history has split from the remote's, **Replace the remote with this book** makes this book
the remote's. The remote's old book stays in its history.
