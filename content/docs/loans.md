---
title: Loans
weight: 4
---

The **Loans** page tracks mortgages, car and student loans, and 0% promotional financing: what each owes, its
next payment, when it's paid off, and how much interest it will cost.

A loan is a **Loan or mortgage** account on [Accounts](accounts): off budget, with what it owes today as its
starting balance. Every such account is listed on Loans.

## Setting up the terms

Choose a loan, then **Terms**:

- **Rate %**, the annual rate, and **Interest**: **monthly** (a twelfth of the rate each period, as most
  mortgages charge) or **daily** (the rate ÷ 365 on each day's balance, as many car and student loans do).
- **Payment** and **Due day**: the scheduled payment, principal and interest, and the day of the month it's due.
- **Interest goes to**: an expense account set to **excluded** in its budget setting, such as
  `Expenses:Housing:Mortgage Interest`. Interest shows in your reports but never takes money from an envelope.
- **Payments come out of**: the budget category that pays the loan, such as `Expenses:Housing:Mortgage`.
- **Escrow** (optional): the amount added to each payment for taxes and insurance, and the off-budget account
  that holds it.
- **0% promo ends** and **Deferred rate %** (optional), for promotional financing that charges back interest if
  the balance isn't cleared in time.

Terms apply from their date until newer terms. A rate change, a new escrow amount or a refinance is new terms
from the day it starts, and earlier months don't change.

## Recording a payment

**Record a payment** shows the split before you save: the interest since the last one, then how much of the
payment goes to interest, principal and escrow. If your statement's interest differs, type it in. The interest
and the payment are saved together.

The whole payment, escrow included, comes out of the loan's category, so one envelope pays it. Interest is a
separate entry from the excluded interest account to the loan, so it never touches an envelope, and the loan's
balance matches the lender's.

**Post interest** records interest on its own, such as on a statement date between payments.

## Schedule and payoff

**Schedule** lists the payments left, with each one's interest, principal and what's owed after, the payoff date
and the total interest. Type an amount in **Extra principal each payment** to see how many payments and how much
interest it saves.

**Budget … a month** sets a monthly target on the loan's category for the payment and escrow, so the
[targets](targets) fund it.

If the scheduled payment would leave a balance when a 0% promo ends, the loan warns you, says what a month clears
it in time, and estimates the deferred interest it would cost.

## Refinancing and moving a balance

**Move to another loan** records a refinance, a consolidation or a balance transfer. It posts the old loan's
interest through the day, then moves what it owes, so a payoff leaves it at exactly zero. No money moves
through your accounts, so the budget doesn't change. When a loan is paid off, **Close the account** closes it.
