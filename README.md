# Expense Tracker

A simple browser-based expense tracker that lets you record and manage your income and expenses. All data is stored locally in the browser using localStorage, so no backend or server is required.

## Features

- Set an opening balance
- Add income entries with amount, date, description, and category (Savings, Gift, Salary)
- Add expense entries with amount, date, description, and category (Food, Transport, Shopping)
- View current balance, total income, and total expenses at a glance
- Filter income and expense lists by category
- Delete individual transactions
- Responsive layout that works on mobile and desktop

## Getting Started

No installation or build step is needed. Simply open `index.html` in any modern web browser.

```
open index.html
```

Or serve it locally with any static file server, for example:

```
npx serve .
```

## Project Structure

```
.
├── index.html   # Application markup and JavaScript logic
└── style.css    # Styles and responsive layout
```

## How It Works

- **Opening balance** - Set via a prompt dialog and persisted in localStorage.
- **Transactions** - Each transaction is stored as a JSON object with a unique ID, type (income or expense), amount, date, description, and category. The full list is serialized to localStorage on every change.
- **Balance calculation** - Current balance is computed as `opening balance + total income - total expenses`.

## Browser Compatibility

Works in any modern browser that supports `localStorage` and `crypto.randomUUID()` (Chrome, Firefox, Edge, Safari).
