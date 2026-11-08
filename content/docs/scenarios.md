---
title: Scenarios
weight: 4
---

A scenario is a what-if copy of your book. Try a bigger rent target, a new savings goal or a different
way of paying off a card, and see what it does to every month, without touching your real budget.

## Working with scenarios

- **Start** a scenario from your book. It begins as an exact copy.
- **Open** it and change anything: assignments, targets, transactions.
- **Compare** it with your book. The comparison shows which targets differ, and for each category and
  month how assignments, Available and shortfalls change, plus Unassigned.
- **Merge** it into your book when you like the result, or **set it aside**. Set-aside and merged
  scenarios keep their history.

A merge is refused if both your book and the scenario changed the same lines, or if it would add a ledger
error.

## Under the hood

Each scenario is a git branch named `scenarios/<name>` in the book's repository, so scenarios sync to
your other devices along with the book.
