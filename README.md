# Financial Report Analyzer

A modern, client-side financial report analysis tool built with React + TypeScript + Vite. Upload CSV or XLSX financial reports and instantly get a professional dashboard with key metrics, charts, and AI-generated insights — no backend, no API keys, no database required.

![Financial Report Analyzer](https://img.shields.io/badge/Status-Production%20Ready-green) ![Tech Stack](https://img.shields.io/badge/Stack-React%20%2B%20TypeScript%20%2B%20Vite-blue)

---

## Features

- **Upload CSV or XLSX** financial reports with drag-and-drop
- **Demo Data mode** — instantly see a complete dashboard without uploading a file
- **Financial Dashboard** with:
  - Revenue, Expenses, Net Income, Profit Margin
  - Total Assets, Liabilities, Shareholders' Equity
  - Revenue vs. Expenses area chart
  - Net Income bar chart (by period)
  - Balance Sheet pie chart
- **Automated Insights** — profit margin analysis, debt ratios, ROE, and more
- **Responsive** — works on desktop and mobile
- **Client-side only** — all parsing and analysis runs in the browser; no data ever leaves your device

---

## Expected CSV Format

Your CSV file should have a header row. Supported column names (case-insensitive):

| Column | Aliases |
|--------|---------|
| `Period` | `Quarter`, `Date`, `Month`, `Year` |
| `Revenue` | `Total Revenue`, `Sales`, `Total Sales` |
| `Expenses` | `Total Expenses`, `Costs`, `Operating Expenses` |
| `Net Income` | `Net Profit`, `Profit`, `Earnings` |
| `Assets` | `Total Assets` |
| `Liabilities` | `Total Liabilities` |
| `Equity` | `Total Equity`, `Shareholders Equity` |

**Example:**
```csv
Period,Revenue,Expenses,Net Income,Assets,Liabilities,Equity
Q1 2024,2950000,2100000,850000,26000000,10500000,15500000
Q2 2024,3200000,2280000,920000,27000000,10800000,16200000
Q3 2024,3050000,2310000,740000,27800000,11000000,16800000
Q4 2024,3250000,2490000,760000,28600000,11200000,17400000
```

---

## Quick Start

### Prerequisites
- Node.js 18+ and npm

### Local Development

```bash
# Clone the repository
git clone https://github.com/gouthamnaik13/financial-report-analyzer.git
cd financial-report-analyzer

# Install dependencies
npm install

# Start development server
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Production Build

```bash
npm run build
npm run preview
```

---

## Deployment on Render

1. Push this repository to GitHub.
2. Go to [Render.com](https://render.com) → New → **Static Site**.
3. Connect your GitHub repository.
4. Configure:
   - **Build Command:** `npm install && npm run build`
   - **Publish Directory:** `dist`
5. Click **Create Static Site**.

Render will automatically deploy on every push to `main`.

---

## Tech Stack

| Technology | Purpose |
|-----------|---------|
| React 19 | UI framework |
| TypeScript | Type safety |
| Vite | Build tool & dev server |
| Recharts | Charts and visualizations |
| Papa Parse | CSV parsing |
| SheetJS (xlsx) | Excel file parsing |
| Lucide React | Icons |

---

## Project Structure

```
src/
├── components/
│   ├── Navbar.tsx          # Top navigation bar
│   ├── UploadScreen.tsx    # File upload + form
│   ├── LoadingScreen.tsx   # Loading state
│   ├── Dashboard.tsx       # Results dashboard with charts
│   └── ErrorScreen.tsx     # Error state
├── types.ts                # TypeScript interfaces
├── utils.ts                # Data parsing & calculations
├── App.tsx                 # Root component & state machine
├── main.tsx                # Entry point
└── index.css               # Global styles
```

---

## License

MIT © 2024 Financial Report Analyzer
