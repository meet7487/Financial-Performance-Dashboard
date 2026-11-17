# Dashboard Layout: BI Build Navy Blue Theme

Use the reference image as the design guide. Power BI's theme JSON applies colours and visual styling, but the dark navigation sidebar and custom filter panel must be created manually with shapes, text boxes, buttons, and slicers.

## Canvas and overall style
- Page size: 16:9 widescreen.
- Page background: very light blue-grey `#F4F7FB`.
- Main report area: white cards with subtle light-grey borders.
- Primary navy: `#0B1426` (left navigation), `#174A8B` (titles and key charts).
- Secondary blue: `#6EA6D7`.
- Positive variance: green `#2E8B57`.
- Negative variance: red `#D83A4B`.
- Font: Segoe UI.
- Keep consistent gaps and align visuals to a grid.

## Suggested page structure
1. Left navigation rail: about 16% of canvas width, dark navy rectangle.
   - Add a title/logo text at the top: `FINANCE BI`.
   - Add page navigation buttons: Performance Overview, Revenue Analysis, Expense Analysis, Transaction Listing.
   - Add slicers below: Department, Manager, Account Category, Account Name.
   - Use white text, blue selected-page button, and thin separators.
2. Header: title `Revenue Analysis` and a small subtitle/filter summary.
3. Month selector row: use a horizontal Month/Year slicer and a comparison-period button-style slicer.
4. KPI row: Actual Income, Budget Remaining, Projected Full Year.
5. Middle row: variance-to-budget column chart on the left and revenue-by-month matrix on the right.
6. Bottom row: clustered column chart for Actual vs Budget with a line for prior-year revenue if prior-year data exists.

## Important dataset note
The included practice dataset covers Jan-Dec 2025 only. It does not contain 2024 actuals, so do not label a measure as Last Year (LY) unless you add prior-year data. For this dataset, use Actual vs Budget and Month-over-Month comparisons instead.

## Suggested visuals and fields
- KPI cards: `[Total Income]`, `[Income Budget Remaining]`, `[Projected Full Year Income]`.
- Variance chart: Calendar[YearMonth] axis and `[Income Budget Variance]`.
- Monthly table: Calendar[YearMonth], `[Total Income]`, `[Income Budget]`, `[Income Budget Variance]`, `[Income Budget Variance %]`.
- Trend chart: Calendar[YearMonth], `[Total Income]`, `[Income Budget]`.
- Slicers: Calendar[YearMonth], Transactions[Department], Transactions[Category], Transactions[Type].
