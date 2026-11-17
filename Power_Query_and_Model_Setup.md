# Power Query and Data Model Setup

## Import
In Power BI Desktop choose Home > Get data > Excel workbook. Select:
- Transactions
- Budget
- Calendar

## Power Query checks
For `Transactions`:
- `TransactionID`, `Type`, `Category`, `Department`, `Description`, `Counterparty`, `PaymentMethod`, `Status`: Text
- `Date`: Date
- `Amount_INR`: Decimal Number or Fixed Decimal Number

For `Budget`:
- `BudgetMonth`: Date
- `Type`, `Category`, `Department`: Text
- `BudgetAmount_INR`: Decimal Number or Fixed Decimal Number

For `Calendar`:
- `Date`: Date
- `Year`, `MonthNumber`, `WeekNumber`, `Day`: Whole Number
- `MonthName`, `MonthShort`, `YearMonth`, `Quarter`, `DayName`: Text
- `IsWeekend`: True/False

Use Transform data to apply the types, then Close & Apply.

## Relationships
Create these active relationships:
1. `Calendar[Date]` (one) -> `Transactions[Date]` (many)
2. `Calendar[Date]` (one) -> `Budget[BudgetMonth]` (many)

Set cross-filter direction to Single. Calendar should be on the one side.
Because BudgetMonth is stored as the first day of each month, month-level filtering works when visuals use fields from Calendar. Avoid using a month name alone without Year.

## Date table
Select Calendar in the Fields pane, then Table tools > Mark as date table > Date.

## Important actuals rule
The sample Transactions table contains Posted and Pending records. The supplied DAX measures explicitly include only `Status = "Posted"` for actual amounts and transaction counts.

## Currency
Format amount measures as Currency / Indian Rupee (₹). Suggested custom format:
`₹#,##0;[Red](₹#,##0);-`

Format percentage measures as Percentage with 1 or 2 decimal places.
