---
title: Accounts
weight: 2
---

The **Accounts** page lists every account and category with its balance, and is where you add new ones.

## Adding an account

Choose **Add account**, then:

1. **Pick what kind it is.** The kind decides where it goes in your books and how the budget treats it:

   | Kind | Budget |
   |---|---|
   | Checking or cash | On budget: its money is yours to assign |
   | Credit card | On budget: purchases set money aside for the payment |
   | Savings or investments | Off budget: tracked, not budgeted |
   | Loan or mortgage | Off budget: tracked, not budgeted |
   | Spending category | A budget category |
   | Income | Money that arrives is yours to assign |

   **More…** lets you choose the type and budget setting yourself, for example to add a placeholder or
   an excluded category.
2. **Type a name in plain words**, such as "Chase Visa". The form shows what it will be saved as:
   `Liabilities:Chase-Visa`. Names are written without spaces in the file, and shown with them.
3. **Inside** (optional) puts it under an existing parent, such as Food for a "Dining" category. It
   suggests the parents you already have.
4. **Opened** is the date it starts.
5. For an account, **Balance today** (or **Owed today** for a card or loan) starts it with that
   balance.

### Starting balances

A starting balance is written as one transaction against `Equity:Opening-Balances`, which BranchBooks
opens the first time it needs it.

- Money in a checking or cash account arrives as money to assign.
- What a credit card owes shows on the card's payment envelope as owed and not yet covered. Assign money
  to the card to set aside for paying it down.

Each step is saved separately, so if the balance is refused, the account is still added and the message
says why.

## The list

On a wide window, accounts sit on the left and expense categories on the right. Click a type's heading
to fold it; Equity starts folded. Parents fold their sub-accounts with ▾.

Badges mark the less usual budget settings: **off budget**, **excluded** and **placeholder**.

Click an account's name to see its transactions. Its **⋯** menu, which shows when you point at or tab
to the row, has the rest:

- **Edit**: rename it everywhere, or change its date, currencies or budget setting.
- **Reconcile**: enter a statement's date and balance, tick the pending transactions it shows, and
  BranchBooks records that the balance matched.
- **Close** on a date, or **Reopen**.
- **Delete**: refused while transactions or budget entries use it. Close it instead to keep its history.
- **Make placeholder**, for a parent that only groups its sub-accounts.
