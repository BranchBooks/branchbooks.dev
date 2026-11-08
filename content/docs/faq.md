---
title: FAQ
weight: 9
---

## Does BranchBooks see my data?

No. There is no BranchBooks server. Your books stay on your device, and on the git host you choose if you
sync. The app's only other network request is the update check, on `branchbooks.dev` and GitLab.

## Can I edit my books by hand?

Yes. They are plain text. BranchBooks refuses to save over a file you've edited but not committed, so
commit your edits with git first.

## Which git hosts work?

Any host that serves git over HTTPS with a token, such as GitHub, GitLab or your own server. SSH isn't
supported.

## Does it connect to my bank?

Not yet. Bank connections are planned.

## Does it handle more than one currency?

A book budgets in one currency. Accounts in other currencies are kept off budget.

## Is there a phone app?

An Android app is planned.

## How do I report a problem?

Open an issue on [GitLab](https://gitlab.com/branchbooks/branchbooks/-/issues). Report security problems
privately, as [SECURITY.md](https://gitlab.com/branchbooks/branchbooks/-/blob/main/SECURITY.md) describes.
