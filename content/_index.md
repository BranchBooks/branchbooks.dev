---
title: BranchBooks
layout: hextra-home
toc: false
---

{{< hextra/hero-badge link="https://gitlab.com/branchbooks/branchbooks" >}}
  <span>Free and open source, GPL-3.0</span>
  {{< icon name="arrow-circle-right" attributes="height=14" >}}
{{< /hextra/hero-badge >}}

<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-headline >}}
  Double-entry books&nbsp;<br class="hx:sm:block hx:hidden" />with envelope budgets
{{< /hextra/hero-headline >}}
</div>

<div class="hx:mb-12">
{{< hextra/hero-subtitle >}}
  An accounting app for your own device. Your books are plain-text ledgers in git:&nbsp;<br class="hx:sm:block hx:hidden" />keep them local, or sync them to any git host you choose.
{{< /hextra/hero-subtitle >}}
</div>

<div class="hx:mb-6 hero-actions">
{{< hextra/hero-button text="Download for Windows" link="https://gitlab.com/branchbooks/branchbooks/-/releases/permalink/latest" >}}
{{< hextra/hero-button text="Read the docs" link="docs" style="background: transparent; color: inherit; box-shadow: inset 0 0 0 1px currentColor;" >}}
</div>

<div class="hx:mt-6"></div>

{{< hextra/feature-grid >}}
  {{< hextra/feature-card
    title="Real double entry"
    icon="scale"
    subtitle="Accounts, transactions that balance, reconciling against statements and balance assertions. Every amount is an exact decimal."
  >}}
  {{< hextra/feature-card
    title="Envelope budgeting"
    icon="inbox"
    subtitle="Give every dollar a job. Overspending, credit card payments and moving money between envelopes are handled for you."
  >}}
  {{< hextra/feature-card
    title="Targets"
    icon="flag"
    subtitle="Set a monthly amount or a goal with a due date, and BranchBooks works out what each month needs."
  >}}
  {{< hextra/feature-card
    title="Scenarios on branches"
    icon="share"
    subtitle="Try a budget change on its own branch, compare it with your book, then merge it or set it aside."
  >}}
  {{< hextra/feature-card
    title="Plain text you own"
    icon="document-text"
    subtitle="Books are Beancount-compatible text files, so they open in Beancount and Fava and in any text editor."
  >}}
  {{< hextra/feature-card
    title="No account, no server"
    icon="lock-closed"
    subtitle="Nothing to sign up for. Sync over HTTPS to a git host you choose, whose access control decides who can read your books."
  >}}
{{< /hextra/feature-grid >}}
