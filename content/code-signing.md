---
title: Code signing policy
toc: true
sidebar:
  hide: true
---

Free code signing provided by [SignPath.io](https://about.signpath.io/), certificate by
[SignPath Foundation](https://signpath.org/).

BranchBooks for Windows is signed through SignPath Foundation's program for open-source projects. Until the
certificate is issued, releases are unsigned, and each release's files carry a
[Sigstore](https://www.sigstore.dev/) signature from the pipeline that built them.

## What is signed

Only files built from the [BranchBooks repository](https://gitlab.com/branchbooks/branchbooks) by its GitLab CI
pipeline, from a version tag on `main`: Setup (`BranchBooks-setup.exe`) and the BranchBooks program files inside
it. Nothing built on a developer's computer is signed, and no third-party program is signed under this
certificate.

## Team and roles

| Role | Who | What it means |
|---|---|---|
| Committers and reviewers | [Joshua Crump](https://gitlab.com/JoshuaCrump) | Can change the source. Changes from anyone else are reviewed by a team member before they're merged. |
| Approvers | [Joshua Crump](https://gitlab.com/JoshuaCrump) | Approves each release for signing, by hand. |

Every team member uses multi-factor authentication on GitLab and SignPath.

## Privacy

BranchBooks has no server and no account, and it collects nothing about you.

It connects to the network only for:

- **Sync**, with the git remote you give a book, sending that book to it. A book with no remote is never sent
  anywhere.
- **The update check**, to `branchbooks.dev` and GitLab, when the app starts and when you choose **Check for
  updates**. It asks for the latest version and downloads it; it sends nothing about you or your books.

It doesn't transfer any other information to other networked systems unless you ask it to.

## Contact

Write to [hello@branchbooks.dev](mailto:hello@branchbooks.dev). Report a security problem privately, as
[SECURITY.md](https://gitlab.com/branchbooks/branchbooks/-/blob/main/SECURITY.md) describes.
