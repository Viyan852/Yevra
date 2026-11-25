# YEVRA — The Operating System for Brand Infrastructure

[![Live Platform](https://img.shields.io/badge/Platform-Live%20on%20Web-E86339?style=for-the-badge)](https://yevra-studio.web.app)
[![License](https://img.shields.io/badge/License-Proprietary-neutral?style=for-the-badge)](#)
[![Stack](https://img.shields.io/badge/Stack-Next.js%2016%20•%20Turbopack%20•%20Supabase-5865F2?style=for-the-badge)](#)

> **Live Web App:** [https://yevra-studio.web.app](https://yevra-studio.web.app)  
> **Designed & Built by:** Viyan

---

## What is YEVRA?

**YEVRA** is an all-in-one brand and financial operating system engineered for indie founders, startups, and e-commerce creators. It replaces scattered spreadsheets, disconnected design software, and manual bookkeeping by unifying:

1. **Autonomous Financial & Profit Telemetry** — Real-time margin computation, unit economics, rent & recurring bills, staff payroll, and profit analysis.
2. **SKU & Inventory Engine** — Live inventory management with instant Excel format importing, single-click `/sku clear`, and automatic cost-margin tracking.
3. **Asset Studio (75 Vector SVG Layout Engines)** — Client-side vector graphic creation with typography controls, live logo overlays, color palettes, and high-resolution 20x PNG/SVG vector export for social media, launch days, and festivals.
4. **AI Copilot & Market Trends** — Multi-tiered AI reasoning (Groq LPU, Gemini Hydrogen unlocked at 3-day streaks, OpenRouter) and real-time social intent queries.
5. **Staff Directory & Payroll Management** — Track team members, roles, ages, departments, and instantly disburse and record salaries.
6. **Zero-Token Slash Commands** — Ultra-fast, zero-token CLI built directly into the UI for keyboard-first founders to log transactions, adjust inventory, and audit finances in milliseconds without consuming AI credits.

---

## Key Modules & Features

```
┌────────────────────────────────────────────────────────────────────────┐
│                                YEVRA                                   │
├───────────────┬────────────────┬───────────────────┬───────────────────┤
│   Financial   │  SKU & Stocks  │   Asset Studio    │    AI & Trends    │
│  Bookkeeping  │ Excel Importer │ 75 SVG Templates  │  Groq / Gemini /  │
│ Recurring Due │ Unit Margins   │ 7 Custom Avatars  │   YouTube Trends  │
│ Staff Payroll │ Instant Clear  │ High-Res Exports  │  Zero-Token Slash │
└───────────────┴────────────────┴───────────────────┴───────────────────┘
```

### 1. Zero-Token Command Bar
Execute rapid operational tasks without spending AI credits.
- Instant autocomplete helper
- Instant updates to inventory, bills, and ledger
- Zero LLM latency

👉 **[See the Complete Slash Command Reference](COMMANDS.md)**

---

### 2. Excel Inventory Import Specification
YEVRA accepts structured Excel (`.xlsx` or `.xls`) files or provides an **Official Downloadable Template** directly in the dashboard.
- Automatic column matching: `Item Name`, `Unit Cost`, `Selling Price`, `Stock Quantity`, `Category`
- Instant margin and profit per unit calculation upon ingestion
- Full table reset command: `/sku clear`

👉 **[See the Excel Import & Data Format Guide](EXCEL_FORMAT.md)**

---

### 3. Studio & SVG Template Engines
- **75 Curated Templates**: Category tabs for Festivals, Sales, Billboards, Product Launches, and Social Media promos.
- **Dynamic Typography**: Google fonts, Display serif/sans pairings, live editable headlines, and promo banners.
- **Brand Identity Controls**: Color swatch presets, custom SVG logo upload with cooldown tracking.
- **Export Options**: Pure Vector SVG and up to 20x scaled high-resolution PNGs.
- **7 Executive Archetype Avatars**: First avatar selection free for founders; subsequent switching powered by AI credits.

---

### 4. Staff Directory & Financial Ledger
- Comprehensive team tracking: Name, Role, Department, Age, Monthly Base Salary.
- One-command salary dispatch via `/salaries pay [amount] [name]`.
- Recurring bill tracker with automatic due-date alerts for office rent, SaaS, and utilities.

---

### 5. Multi-Tier AI Reasoning System
- **Groq LPU (Ultra-Fast)**: Default high-speed intelligence for queries and parsing.
- **Gemini Hydrogen**: Unlocked automatically after maintaining a 3-Day user streak.
- **YouTube Market Trends**: Configured via YouTube Data API v3 to identify viral product hooks and competitor moves.
- **Admin Tier**: Unlimited reasoning quota with zero daily limit restriction.

---

## Documentation Index

- 📖 **[README.md](README.md)** — Core platform overview and feature architecture.
- ⚡ **[COMMANDS.md](COMMANDS.md)** — Comprehensive dictionary of all slash commands with syntax and examples.
- 📊 **[EXCEL_FORMAT.md](EXCEL_FORMAT.md)** — Schema and template rules for importing product inventory sheets.
- 🚀 **[GETTING_STARTED.md](GETTING_STARTED.md)** — User onboarding walkthrough, auth options, and dashboard setup.

---

## Technology Stack

- **Framework**: Next.js 16 (App Router & Turbopack)
- **Styling**: Tailwind CSS & Custom Frosted-Glass Glassmorphism
- **Database & Auth**: Supabase PostgreSQL + Auth (Session persistence)
- **Deployment**: Firebase Hosting (Global CDN Edge)
- **Visual Engine**: Browser-native Vector SVG & Canvas 2D
