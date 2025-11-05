Grocery List (Offline) 
A single file, offline grocery list web app. Add items with quantity and unit, mark purchased, search/filter, print, and export/import your list. No backend or build step — just open index.html in a browser.
Features
Add items with quantity and unit (no prices)
Inline edit item names; +/- buttons or direct typing for quantity
Mark purchased; quick filters (All | Needed | Purchased)
Search box to find items fast
Export to Excel friendly CSV; Import from CSV or JSON
Print friendly view for taking the list to the store
Saves automatically in your browser (localStorage)
Responsive layout; quantity controls centered; Delete aligned right
Quick start
Download or copy index.html.
Open index.html in any modern browser (Chrome, Edge, Firefox, Safari).
It works offline — all data stays in your browser.
Tip: Add to bookmarks or pin to your home screen for quick access.
How to use
Add: Enter Item, Quantity, choose Unit, then click “Add item”.
Edit name: Click the name to edit; press Enter or click elsewhere to save.
Adjust quantity: Use +/− or click the number to type a value.
Mark purchased: Tick the checkbox on the left.
Filter: Use All / Needed / Purchased.
Search: Type in the search box to filter by name.
Delete: Click the Delete button on the right of a row.
Clear: “Clear purchased” removes all checked items; “Clear all” empties the list.
Export: Click “Export CSV” to download grocery-list.csv.
Import: Click “Import” and select a .csv or .json file.
Note: Import replaces the current list.
Print: Click “Print” for a clean print view.
File formats
CSV (recommended for Excel)
Recommended header: Name, Quantity, Unit, Purchased
Delimiter: comma by default (import also accepts semicolon or tab)
Purchased values accepted: Yes/No, True/False, 1/0, Bought/Done/Purchased
Example CSV:
text
Name,Quantity,Unit,Purchased
Rice,2,kg,No
Eggs,12,pcs,Yes
Milk,1,L,No
JSON (backward compatible)
Array of items with keys: name, qty, unit, purchased (optional id is accepted)
Example JSON:
JSON
[
  { "name": "Rice", "qty": 2, "unit": "kg", "purchased": false },
  { "name": "Eggs", "qty": 12, "unit": "pcs", "purchased": true }
]
Data & privacy
Your list is stored locally in the browser under the key groceryList_v1.
Clearing browser data or using a different device/browser will reset the list.
Use Export to back up; Import to restore.
Customization
Units: Edit the <select> options in the “Add item” form.
Layout: The quantity pill is centered; actions are right aligned and stack on small screens.
Styling: Colors and spacing are defined in the <style> section (CSS variables at the top).
Troubleshooting
Import fails: Ensure your CSV has at least the Name and Quantity columns. For JSON, make sure it’s an array.
Excel shows one column: The CSV includes a UTF 8 BOM and commas. If your Excel locale expects semicolons, you can change the export delimiter in code, or open via Data → From Text/CSV and specify delimiter.
Numbers cut off in the quantity box: The CSS uses a width based on ch units; increase width or min-width in the .qty-input rule if needed.

Tech
HTML, CSS, and vanilla JavaScript
No dependencies or build tools
