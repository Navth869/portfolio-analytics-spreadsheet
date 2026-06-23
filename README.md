# 🎯 Project Overview
A privacy-first portfolio analytics engine built for retail ETF investors. This project addresses the common "visibility gap" in personal finance: the inability to easily visualize aggregate look-through sector and country weightings or cleanly separate actual invested capital from structural cash flow.

## 💡 The Problem
Standard brokerage interfaces and retail investing apps frequently obfuscate the underlying composition of a portfolio. For multi-ETF investors, this introduces two major friction points:
* **Lack of Multi-Asset Granularity:** Existing tools fail to provide a true "look-through" analysis of aggregate sector and geographical exposure across overlapping funds (e.g., owning both an all-world ETF and a tech-tilted ETF).
* **Privacy & Security Trade-offs:** Most automated portfolio trackers demand direct brokerage API access or open-banking credentials (Plaid, etc.), exposing sensitive financial data to third-party monetization.

## 🚀 The Solution
This project implements a **Privacy-First Data Pipeline** that keeps all sensitive financial records localized and entirely under the user's control.

* **Ingestion:** Streamlined manual entry via a secure, self-hosted Google Form to maintain zero-trust data integrity.
* **Core Architecture Engine:** A modular, multi-currency Google Sheets framework handling real-time FX conversions (USD/HKD), granular transactional cost-basis auditing, and localized performance metrics via native `GOOGLEFINANCE` integration.
* **Look-Through Analytics:** Automated allocation matrices using weighted `SUMPRODUCT` array logic to deconstruct individual ETF tickers into a unified, cross-portfolio exposure dashboard.

## ⚡ Current Features & Architecture
* **Multi-Currency Cash Flow Ledger:** Separates capital injections/withdrawals from active market performance, maintaining a true HKD/USD cost basis.
* **Dynamic Transaction Auditor:** Live market valuation using `GOOGLEFINANCE` data streams tied to categorical bucketing (Core ETF, Growth ETF, Cash).
* **Aggregate Exposure Engine:** Custom mathematical matrices calculating the exact weighted average of sector and country exposure across all combined holdings, preventing accidental over-concentration.

## ⚠️ Scope & Limitations
In alignment with data integrity principles and platform Terms of Service (ToS), this framework purposefully relies on a structured user-input model rather than brittle web-scraping scripts.
* **ToS Compliance:** Respects data provider boundaries by utilizing only sanctioned native Google environment metrics.
* **Data Sovereignty:** Zero outbound API dependencies. Your net worth data never leaves your personal ecosystem.

## 🗺️ Future Roadmap

### 📊 1. Multi-Platform Strategy: TradingView Technical Integration
Rather than overloading the portfolio dashboard with heavy, retrofitted technical screener logic, the next phase focuses on deploying lightweight, external execution triggers.
* Develop custom **Pine Script v5** indicators in TradingView to monitor 50-day and 200-day Simple/Exponential Moving Averages (SMA/EMA) for core tickers (`VWRA`, etc.).
* Set up dynamic TradingView alerts linked to webhooks (or mobile notifications) to signal structural portfolio rebalancing windows based on macro technical trends.

### 📉 2. Cash Drag & Automated Rebalancing Matrix
* Design a predictive "Dry Powder" calculator that models the drag effect of uninvested cash against historical portfolio returns.
* Build a target-vs-actual variance matrix that auto-calculates the exact fiat amount required to rebalance the portfolio back to target weights using fresh capital infusions, minimizing taxable selling events.

### 🛡️ 3. Portfolio Drawdown & Stress-Testing Simulator
* Implement historical maximum drawdown (MDD) modeling based on historical asset variance data.
* Build a static macro stress-test component allowing users to simulate how their current sector/regional concentrations would perform under historical market shocks (e.g., 2000 Dot-com crash, 2008 Financial Crisis, 2020 Liquidity Crunch).

### 📝 4. Automated Ledger Backup & Export Pipeline
* Write a lightweight Google Apps Script to automatically compress, encrypt, and export daily or weekly portfolio snapshots to a localized CSV format or personal Git repository, ensuring permanent version control over net worth history.
