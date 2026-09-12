# 💰 Personal Expense Tracker

A command-line application for tracking daily expenses, categorizing them, and viewing spending summaries by category or month. Data is stored locally in a CSV file.

## Features

- Add expenses with amount, category, and description (date is stamped automatically)
- View all recorded expenses
- View total expenses across all time
- View totals grouped by category
- View totals filtered by month
- Data persists between sessions in `expenses.csv`

## Demo

```
=== Expense Tracker ===
1. Add expense
2. View all expenses
3. View total expenses
4. View total by category
5. View total by month
6. Exit
Enter your choice (1-6): 1
Amount: 12.50
Category: Food
Description: Lunch
Expense added.

Enter your choice (1-6): 3
Total expenses: 12.50
```

## Requirements

- Python 3.7+ (standard library only — no external dependencies)

## Installation

```bash
git clone https://github.com/your-username/expense-tracker.git
cd expense-tracker
```

## Usage

Run the app from the command line:

```bash
python main.py
```

Follow the on-screen menu to add expenses and view summaries.

## Data Format

Expenses are stored in `expenses.csv` with one row per entry:

```csv
2026-08-04,12.50,Food,Lunch
2026-08-04,5.00,Transport,Bus ticket
2026-08-05,45.00,Shopping,T-shirt
```

Columns: `date, amount, category, description`

## Project Structure

```
expense-tracker/
├── main.py          # Main application logic
├── expenses.csv      # Saved expenses (auto-created/updated on run)
└── README.md
```

## How It Works

1. Expenses are appended to `expenses.csv` as they're added, with today's date filled in automatically
2. Viewing options read the CSV and aggregate totals on the fly (overall, by category, or by month)
3. If `expenses.csv` doesn't exist yet, the app reports there's no data instead of crashing

## License

This project is open source and available under the [MIT License](LICENSE).
