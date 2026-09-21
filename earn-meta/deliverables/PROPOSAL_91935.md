## Proposal

### What is the root cause of that problem?

The Spend report transaction table’s **own** default is Date/ASC (that pair also gates RBR pre-sort). Header clicks go through shared `SortableHeaderText`, which always starts an **inactive** column on DESC.

So: open report (Date/ASC) → click Total (Total/DESC) → click Date again → shared header emits Date/DESC because Date was inactive. The report view stores that value as-is, so it never returns to Date/ASC and RBR pre-sort stays off.

Search still wants DESC-on-first-click, so changing the shared header would break Search. The mismatch belongs only to this report table.

### What changes do you think we should make in order to solve the problem?

Keep `SortableHeaderText` unchanged. In the money-request report header path, when the user **switches to** Date from another column, force ASC before calling the parent `onSortPress`. Leave ASC↔DESC toggles while Date is already active alone. Leave every other column’s DESC first-click alone.

I would put that rule in a tiny pure helper (easy to unit-test) and wrap `onSortPress` in `MoneyRequestReportTableHeaderRow` so Search and other consumers stay untouched.

Covered cases: Date→Total→Date restores ASC; Date→Date still toggles; switching to Total still lands on DESC.

### What alternative solutions did you explore? (Optional)

- Flip shared `SortableHeaderText` to ASC on inactive columns — rejected; Search defaults to DESC and persists order in the URL.
- Fix only the grouped-layout alphabetical override — related UX, but it does not restore Date/ASC on the flat path the OP steps describe.

Note: draft PR https://github.com/Expensify/App/pull/101765 was auto-closed because I was not yet assigned. Happy to reopen the same approach once hired.
