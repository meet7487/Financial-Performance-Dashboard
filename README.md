# Financial Performance Dashboard - Power BI Project Pack

## What's included
- `PowerBI_Financial_Performance_Dataset_INR.xlsx`: sample 2025 transactions, budgets, calendar, and setup guide.
- `DAX_Measures.dax`: measures to create in Power BI.
- `BI_Build_Navy_Blue_Theme.json`: importable corporate theme.
- `Power_Query_and_Model_Setup.md`: data types, relationships, and modeling steps.
- `Dashboard_Layout_and_Insights.md`: report page design.

## Can this bundle open as a PBIX?
This bundle is a ready-to-build project pack, not a native `.pbix` file. A PBIX file must be authored and saved by Power BI Desktop. This environment cannot reliably generate a valid native PBIX directly. Follow the setup guide to assemble the report in Power BI Desktop.

## Quick start
1. Extract this ZIP to a folder.
2. Open Power BI Desktop.
3. Get Data > Excel workbook > select the included XLSX.
4. Load Transactions, Budget, and Calendar.
5. Configure the relationships in `Power_Query_and_Model_Setup.md`.
6. Mark Calendar as the date table.
7. Import the theme: View > Themes > Browse for themes > select `BI_Build_Navy_Blue_Theme.json`.
8. Create each measure from `DAX_Measures.dax` using Modeling > New measure. Add one measure at a time.
9. Build visuals using the layout guide.
10. Save as `Financial_Performance_Dashboard.pbix`.

## Suggested report slicers
- Calendar[YearMonth]
- Transactions[Department]
- Transactions[Type]
- Transactions[Category]

Tip: If you use Transaction Category or Department to filter Budget visuals, the category/department fields should come from shared dimensions in a more advanced model. In this starter model, month/date filters are modeled directly; transaction-side category/department filters do not automatically filter Budget.


## Reference-inspired styling
The updated theme uses navy titles, blue chart colours, white visual cards, light blue-grey page background, green positive values, and red negative values. Build the left navy navigation panel manually using Power BI shapes, text boxes, buttons, and slicers; theme JSON cannot create the page layout by itself.
