# YEVRA — Getting Started & User Guide

Welcome to **YEVRA**, the unified operating system for brand and financial infrastructure. This guide covers how to set up your workspace and start using all features.

---

## 1. Accessing the Platform

- **Live URL**: [https://yevra-studio.web.app](https://yevra-studio.web.app)
- **Sign In Methods**:
  - **Discord OAuth**: Instant 1-click verification with your Discord account.
  - **Email Magic Link**: Enter your email address to receive an instant, password-free login link.
  - **Email & Password**: Standard password authentication.

---

## 2. Navigating the Workspace

Once authenticated, the left sidebar provides instant access to all core modules:

- 📊 **Financials**: Top status KPI cards (Net Profit, Total Revenue, Paid Staff Salaries, Pending Rent & Bills) and transactional stream.
- 📦 **SKU Inventory**: Your live warehouse item matrix, unit cost vs. selling price comparison, margin percentages, and bulk stock indicators.
- 🎨 **Asset Studio**: 75 SVG vector design engines for posters, festival drops, billboard mockups, and social carousels.
- 📈 **AI Trends**: Real-time social intent signals, market opportunities, and AI-assisted brand recommendations.
- 👥 **Staff Directory**: Active team members, compensation schedules, ages, and roles.
- 📑 **Ledger & Bills**: Upcoming liabilities, office rent dues, and operational expense logs.
- ⚙️ **Settings**: Brand name, niche selection, logo uploads, and preferences.

---

## 3. Recommended First-Time Workflow

### Step 1: Import Your Inventory
1. Click **Import Your First Excel Sheet** on the homepage or open **SKU Inventory** in the dashboard.
2. Upload your existing inventory spreadsheet or download our [Excel Template](EXCEL_FORMAT.md).
3. The dashboard automatically calculates your profit per unit and total inventory valuation.

### Step 2: Set Up Recurring Bills
Keep your financial telemetry accurate by recording fixed overhead:
```bash
/bills add Office_Rent 50000 1
/bills add Internet_Bill 2500 10
```

### Step 3: Add Staff & Log Payroll
Add your team members in the **Staff Directory** page, and disburse compensation when due:
```bash
/salaries pay 40000 Sarah
```

### Step 4: Design Your First Campaign in Asset Studio
1. Navigate to **Asset Studio**.
2. Select a category tab (**Festivals**, **Sales**, **Billboards**, **Launches**, **Social Media**).
3. Choose a template preset, customize the typography, upload your brand logo, and click **Download High-Res PNG** or **Download Vector SVG**.

### Step 5: Select Your Executive Avatar
Click your user profile pill in the sidebar to browse **7 Custom SVG Avatars** (Founder, Creative, Tech Lead, Operator, etc.). First-time selection is free for all founders!

---

## 4. Daily Streaks & AI Tiers

- **Daily Limit**: 15 AI reasoning requests/day on the free tier.
- **Streak Bonus**: Log in daily to build your streak. Maintaining a **3-Day Streak** unlocks the **Gemini Hydrogen** tier for deeper market analysis and richer copy generation.
