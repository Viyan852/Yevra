# YEVRA — Official Excel Sheet Import Specification

To prevent broken imports, inconsistent data, or incomplete telemetry, YEVRA uses an intelligent column-detection engine for Excel spreadsheets (`.xlsx` and `.xls`).

You can download the pre-formatted **Official Excel Template** directly from the YEVRA homepage or dashboard, or format your custom sheet according to the guidelines below.

---

## Accepted Columns & Formatting

| Column Name (Header) | Required? | Accepted Header Aliases | Example Value | Notes |
|---|---|---|---|---|
| **Item Name** | **YES** | `name`, `item`, `product`, `sku`, `title`, `description` | `Classic Heavyweight Hoodie` | Plain text title of product |
| **Unit Cost** | **YES** | `cost`, `unit_cost`, `buy_price`, `cogs`, `cost_price` | `450.00` | What it costs you to manufacture/buy |
| **Selling Price** | **YES** | `price`, `selling_price`, `retail`, `mrp`, `sale_price` | `1299.00` | Customer checkout price |
| **Stock Quantity** | **YES** | `quantity`, `stock`, `qty`, `units`, `inventory`, `count` | `85` | Integer unit count in warehouse |
| **Category** | Optional | `category`, `type`, `department`, `tag` | `Apparel` | Defaults to `General` if blank |

---

## Example Spreadsheet Layout

A standard file (e.g. `inventory.xlsx`) should look like this:

| Item Name | Unit Cost | Selling Price | Stock Quantity | Category |
|---|---|---|---|---|
| Classic Oversized Hoodie | 35.00 | 85.00 | 120 | Apparel |
| Nylon Minimalist Backpack | 28.00 | 70.00 | 45 | Accessories |
| Matte Ceramic Mug | 6.50 | 22.00 | 200 | Drinkware |
| Heavy Cotton Tee | 12.00 | 38.00 | 350 | Apparel |
| Canvas Utility Tote | 9.00 | 29.00 | 90 | Accessories |

---

## Best Practices & Validation Rules

1. **Header Row on Row 1**: Always keep your table column titles on the first row of sheet 1.
2. **Numeric Values Only**: Do not include currency symbols (`$`, `₹`, `€`) inside the numeric cells (e.g., enter `35.00`, not `$35.00`).
3. **No Merged Cells**: Avoid merged column headers as they can disrupt row indexing.
4. **Clean Import with `/sku clear`**: If you are replacing an entire season's stock list, run `/sku clear` in the command bar before uploading to prevent duplicate entries.
5. **Sheet Format**: Save files with `.xlsx` (Excel Workbook) or `.xls`. CSVs can be converted to `.xlsx` in Excel or Google Sheets.

---

## Download Official Template
You can download the ready-to-fill `.xlsx` template anytime from:
1. YEVRA Homepage &rarr; **"Download Official Excel Template"** button.
2. Dashboard &rarr; **"Import Excel"** modal &rarr; **"Download Template"**.
