# YEVRA — Zero-Token Slash Command Reference

YEVRA features a built-in keyboard command bar located at the top of the **Dashboard**, **Financials**, and **Ledger** screens.

Unlike AI chat prompts, slash commands execute **deterministically and instantly in the browser/database** — consuming **zero AI reasoning tokens** and requiring **zero wait time**.

---

## Command Quick Table

| Command | Syntax | Description | Example |
|---|---|---|---|
| **`/salaries pay`** | `/salaries pay [amount] [staff_name]` | Logs a salary disbursement in the ledger | `/salaries pay 45000 Aarav Patel` |
| **`/bills add`** | `/bills add [type] [amount] [due_day]` | Adds recurring monthly liability (Rent/Bill) | `/bills add Rent 65000 5` |
| **`/bills pay`** | `/bills pay [type]` | Marks a pending recurring bill as paid | `/bills pay Rent` |
| **`/expense add`** | `/expense add [category] [amount] [note]` | Logs general business or operational expense | `/expense add Marketing 12000 Google Ads` |
| **`/sku add`** | `/sku add [name] [cost] [price] [qty]` | Adds new item with automatic unit margins | `/sku add Classic_Hoodie 35 75 150` |
| **`/sku clear`** | `/sku clear` | Clears all SKU records from inventory | `/sku clear` |
| **`/sale log`** | `/sale log [sku_name] [qty]` | Deducts stock quantity and records revenue | `/sale log Classic_Hoodie 4` |
| **`/stock restock`** | `/stock restock [sku_name] [qty]` | Adds incoming replenishment units to stock | `/stock restock Classic_Hoodie 50` |
| **`/stock low`** | `/stock low` | Filters inventory for items with stock < 10 | `/stock low` |
| **`/profit`** | `/profit` | Computes live net profit and margin breakdown | `/profit` |
| **`/audit`** | `/audit` | Runs a complete multi-metric business audit | `/audit` |
| **`/poster`** | `/poster [id] "[headline]" "[subtext]"` | Opens Asset Studio with pre-filled banner text | `/poster 1 "DIWALI SALE" "Flat 40% Off"` |
| **`/help`** | `/help` | Opens full interactive command guide modal | `/help` |

---

## Detailed Command Walkthrough

### 1. Staff & Payroll Commands

#### `/salaries pay [amount] [staff_name]`
Logs a paid salary expense directly to the financial ledger and updates your monthly cash-out telemetry.
```bash
/salaries pay 50000 Sarah Jenkins
/salaries pay 32000 Dev Team Lead
```

---

### 2. Bills & Rent Management

#### `/bills add [type] [amount] [due_day]`
Registers a recurring monthly expense with a designated calendar due day. It shows up in your **Pending Rent & Bills** card until cleared.
- `type`: `Rent`, `Electricity`, `Cloud`, `SaaS`, or any label.
- `due_day`: Day of month (e.g. `1` to `31`).
```bash
/bills add Office_Rent 80000 1
/bills add AWS_Cloud 15400 15
```

#### `/bills pay [type]`
Finds the pending bill matching the name and transitions its state to `paid`, deducting from your net cash flow.
```bash
/bills pay Office_Rent
```

---

### 3. SKU & Inventory Operations

#### `/sku add [name] [cost] [price] [qty]`
Creates a new SKU entry. Unit profit margin and margin percentage are calculated automatically.
*(Tip: Use underscores for multi-word item names without quotes)*
```bash
/sku add Oversized_Tee 250 899 120
/sku add Canvas_Tote_Bag 150 499 75
```

#### `/sku clear`
Safely purges the full inventory list. Useful when re-uploading a revised master spreadsheet to avoid duplicated records.
```bash
/sku clear
```

#### `/sale log [sku_name] [qty]`
Logs a customer order. Automatically:
1. Deducts `[qty]` from your SKU stock count.
2. Multiplies `[qty] * selling_price` and deposits the income to the ledger.
3. Calculates gross profit and net margin.
```bash
/sale log Oversized_Tee 3
```

#### `/stock restock [sku_name] [qty]`
Increments the on-hand unit count for an existing item after receiving a supplier delivery.
```bash
/stock restock Oversized_Tee 200
```

#### `/stock low`
Instantly isolates high-priority inventory bottlenecks by highlighting every product with fewer than 10 units remaining.
```bash
/stock low
```

---

### 4. Telemetry & Financial Auditing

#### `/profit`
Returns a breakdown of:
- Total Gross Revenue
- Total Cost of Goods Sold (COGS)
- Total Disbursed Salaries
- Pending Bills & Liabilities
- True Net Margin percentage

#### `/audit`
Generates a comprehensive snapshot summarizing inventory valuation, top-selling lines, outstanding dues, and cash runway.

---

### 5. Creative Studio Shortcut

#### `/poster [id] "[headline]" "[subtext]"`
Instantly opens **Asset Studio** with the designated template number loaded and the copy pre-filled into the layout canvas.
```bash
/poster 1 "SUMMER DROP" "Available this Friday 6PM"
/poster 5 "LIMITED EDITION" "Only 50 units crafted"
```
