# 📊 LifeSight Fund Analytics & Return Matrix Suite

[![GitHub Repo](https://img.shields.io/badge/GitHub-lakeuk%2Flifesight--unit--prices-blue?logo=github)](https://github.com/lakeuk/lifesight-unit-prices)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5 / JS](https://img.shields.io/badge/Tech-HTML5%20%7C%20Chart.js%20%7C%20SheetJS-brightgreen)](https://github.com/lakeuk/lifesight-unit-prices)

Welcome to the **LifeSight Fund Analytics Suite** — a powerful, client-side, zero-dependency interactive toolkit for visualizing, analyzing, and benchmarking pension fund historical unit price performance and return matrix dynamics.

This repository features two lightweight, standalone HTML/JavaScript applications designed to provide pension members, trustees, and financial analysts with institutional-grade insights into multi-year fund performance, risk metrics, and holding-period returns.

---

## 🚀 Interactive Applications Included

### 1. 📈 LifeSight Fund Analytics Dashboard (`lifesight_fundprices.html`)
An interactive historical performance dashboard that renders dynamic line charts (Unit Price or Total Return %), metrics tables (CAGR, Annualized Volatility, Max Drawdown, Sharpe Ratio), custom compound return benchmark overlays, and flexible date sliders.

![LifeSight Fund Analytics Dashboard](assets/dashboard_overview.png)

### 2. 📐 LifeSight Fund Return Matrix (`lifesight_fundprices_triangle.html`)
A dynamic triangular return matrix app that evaluates cumulative performance across every possible combination of purchase (buy) and evaluation (sell) months. Includes dual-axis range controls, synchronized window locking, hover tooltips with detailed holding metrics, and color-coded return heatmaps.

![LifeSight Fund Return Matrix](assets/triangle_matrix_overview.png)

---

## ✨ Key Features & Capabilities

* **🔒 100% Client-Side & Private:** Pure HTML/JS/CSS that runs completely in your web browser. No backend server, database, or API required.
* **📈 Dual Visualization Modes:** Switch between absolute unit price movement (£) and relative benchmarked percent change (%).
* **📊 Risk & Performance Analytics:** Automatically calculates:
  * **Total Return (%)** across selected time windows
  * **CAGR** (Compound Annual Growth Rate)
  * **Annualized Volatility (%)** (Daily return standard deviation × √252)
  * **Max Drawdown (%)** (Worst-case peak-to-trough drop)
  * **Sharpe Ratio** (Risk-adjusted return baseline $R_f = 2.0\%$)
* **🎯 Custom Benchmark Targets:** Overlay annual target compounding curves (+2.0% p.a. up to +13.0% p.a.) to measure fund performance against inflation or target growth objectives.
* **🔗 Dynamic Dual-Axis Date Sliders:** Drag sliders or select date inputs (1Y, 3Y, 5Y, MAX) with options to **Lock Window Span** or **Synchronize Horizontal & Vertical Axes**.
* **🌙 Dark Mode & Responsive Layout:** Fully adaptive UI with instant dark/light theme toggling.
* **📤 Multi-Format Exporting:** Export tailored datasets and formatted matrices directly to **CSV**, **Excel (.xlsx)**, or high-res **PNG Chart Images**.  

---

## 🛠️ How to Use

### Quick Start (No Installation Needed)
1. **Clone or Download** this repository:
   ```bash
   git clone [https://github.com/lakeuk/lifesight-unit-prices.git](https://github.com/lakeuk/lifesight-unit-prices.git)
   cd lifesight-unit-prices


# 📖 LifeSight Fund Analytics Suite — Comprehensive Operating Guide

This guide provides step-by-step instructions for operating the **LifeSight Fund Analytics Suite**, comprising the **Analytics Dashboard** (`lifesight_fundprices.html`) and the **Return Matrix Tool** (`lifesight_fundprices_triangle.html`).

---

## 📋 Table of Contents
1. [Overview & System Requirements](#-overview--system-requirements)
2. [Operating the Analytics Dashboard (`lifesight_fundprices.html`)](#-operating-the-analytics-dashboard)
   * [1. Loading Data](#1-loading-data)
   * [2. Switching Chart Modes](#2-switching-chart-modes)
   * [3. Filtering Funds & Administrators](#3-filtering-funds--administrators)
   * [4. Benchmarking Against Target Growth Rates](#4-benchmarking-against-target-growth-rates)
   * [5. Adjusting Timeframes & Date Sliders](#5-adjusting-timeframes--date-sliders)
   * [6. Interpreting Performance & Risk Metrics](#6-interpreting-performance--risk-metrics)
   * [7. Exporting Chart Data & Graphics](#7-exporting-chart-data--graphics)
3. [Operating the Return Matrix (`lifesight_fundprices_triangle.html`)](#-operating-the-return-matrix)
   * [1. Loading Data](#1-loading-triangle-data)
   * [2. Selecting Active Funds](#2-selecting-active-funds)
   * [3. Dual-Axis Date Controls](#3-dual-axis-date-controls)
   * [4. Window Locking & Axis Synchronization](#4-window-locking--axis-synchronization)
   * [5. Reading Cell Heatmaps & Tooltips](#5-reading-cell-heatmaps--tooltips)
   * [6. Exporting Matrices](#6-exporting-matrices)
4. [Custom CSV Data Specifications](#-custom-csv-data-specifications)

---

## 🌐 Overview & System Requirements

The LifeSight Fund Analytics Suite is 100% client-side and requires no web server, backend infrastructure, or software installation.

* **Supported Browsers:** Google Chrome, Microsoft Edge, Mozilla Firefox, Apple Safari, or Opera (any modern web browser).
* **Dependencies:** None (all chart engines and export libraries are bundled inline).
* **Data Privacy:** All calculations and data rendering occur entirely in your local browser memory. No data is transmitted or read externally.

---

## 📈 Operating the Analytics Dashboard (`lifesight_fundprices.html`)

The Analytics Dashboard visualizes historical unit price dynamics, tracks cumulative total returns, overlays target performance curves, and calculates standard institutional risk metrics.

### 1. Loading Data
* **Default Load:** The app automatically attempts to parse `lifesight_fundprices.csv` from the same folder.
* **Manual Load:** Drag and drop your CSV file into the designated top dropzone, or click **Browse File** to locate `lifesight_fundprices.csv` on your computer.

### 2. Switching Chart Modes
Use the toggle buttons at the top left of the dashboard control bar:
* **Unit Price Chart (£):** Displays raw unit price trajectories over time.
* **Percent Change Chart (%):** Re-bases all selected funds to 0% at the start of the active date window to evaluate comparative cumulative total return.

### 3. Filtering Funds & Administrators
* **Administrator Filter:** Use the dropdown menu to display funds managed by specific providers (e.g., *LifeSight*, *BlackRock*, or *All Administrators*).
* **Fund Search Box:** Type keywords into the search box to filter fund titles dynamically.
* **Fund Tile Grid:** Click any fund tile at the bottom to toggle its visibility on the active chart. Selected funds remain highlighted.

### 4. Benchmarking Against Target Growth Rates
* Locate the **Benchmark Target** dropdown in the top toolbar.
* Select an annual compounding rate target (e.g., *Target +3.0% p.a.* through *Target +10.0% p.a.*).
* A dotted compounding baseline curve will overlay on the Percent Change chart, allowing direct visual comparison against target inflation or growth thresholds.

### 5. Adjusting Timeframes & Date Sliders
* **Quick Presets:** Click **1Y**, **3Y**, **5Y**, or **MAX** to immediately frame the corresponding historical window ending on the latest available dataset date.
* **Dual Range Sliders:** Drag the left or right handles of the slider underneath the chart to adjust start and end dates.
* **🔒 Lock Span Checkbox:** Check **Lock Span** to preserve the active timeframe duration (e.g., 3 years) while dragging the window backward or forward through historical dates.

### 6. Interpreting Performance & Risk Metrics
The table beneath the chart automatically updates based on the selected timeframe:

| Metric | Calculation / Description |
| :--- | :--- |
| **Total Return (%)** | Cumulative return percentage over the selected period: $\frac{P_{\text{end}} - P_{\text{start}}}{P_{\text{start}}} \times 100$. |
| **CAGR (%)** | Compound Annual Growth Rate: $\left(\frac{P_{\text{end}}}{P_{\text{start}}}\right)^{\frac{1}{\text{Years}}} - 1$. |
| **Annualized Volatility (%)** | Standard deviation of daily log returns scaled to 252 annual trading days: $\sigma_{\text{daily}} \times \sqrt{252}$. |
| **Max Drawdown (%)** | The largest percentage peak-to-trough decline experienced within the active window. |
| **Sharpe Ratio** | Risk-adjusted excess return per unit of volatility relative to a 2.0% risk-free baseline ($R_f$): $\frac{\text{CAGR} - R_f}{\text{Annualized Volatility}}$. |

### 7. Exporting Chart Data & Graphics
Click **📤 Export Data** in the toolbar to choose an export format:
* **Export Filtered CSV:** Downloads raw unit price data for active funds within the selected date window.
* **Export Excel (.xlsx):** Generates a formatted Excel workbook with separate sheets for data and metrics.
* **Export PNG Image:** Captures a high-resolution snapshot image of the current chart layout.

---

## 📐 Operating the Return Matrix (`lifesight_fundprices_triangle.html`)

The Return Matrix tool generates a triangular holding-period heatmap, demonstrating total return outcomes for every possible pair of buy (purchase) and sell (evaluation) months.

### 1. Loading Triangle Data
* **Default Load:** The tool automatically loads `lifesight_fundprices_triangle.csv`.
* **Manual Load:** Drag and drop `lifesight_fundprices_triangle.csv` into the top file upload area.

### 2. Selecting Active Funds
* Click any fund tile in the fund selector bar at the bottom of the tool.
* The matrix instantly re-calculates and renders the performance matrix for the selected fund.

### 3. Dual-Axis Date Controls
The matrix features independent date range controls for each axis:
* **Horizontal Axis (Purchase Date Range):** Defines the range of entry (buy) months displayed along the top header.
* **Vertical Axis (Evaluation Date Range):** Defines the range of exit/evaluation (sell) months displayed down the left column.

### 4. Window Locking & Axis Synchronization
* **🔒 Lock Horizontal Span:** Freeze the length of the purchase range window while sliding through time.
* **🔒 Lock Vertical Span:** Freeze the length of the evaluation range window.
* **🔗 Synchronize Both Axes:** Checking this toggle forces purchase and evaluation date windows to move in tandem when adjusting range controls.

### 5. Reading Cell Heatmaps & Tooltips
* **Color Formatting:** Cells are dynamically shaded based on cumulative return performance:
  * **Green:** Positive returns 5% or greater.
  * **Shade between Red to Green:** Greater than 0%, less than 5%.
  * **Red:** 0% or negative returns.
* **Interactive Tooltip:** Hovering your mouse over any cell opens a popup box detailing:
  * Purchase Date & Initial Unit Price
  * Evaluation Date & Final Unit Price
  * Total Holding Duration (Months and Years)
  * Cumulative Return (%)

### 6. Exporting Matrix
Click **📤 Export Matrix** to save the active matrix view:
* **Export Grid as CSV:** Download the full triangular matrix in view as a CSV file.
* **Export Excel (.xlsx):** Generates a unformatted Excel workbook of the matrix in view.
* **Export Matrix Image (PNG):** Save a high-resolution graphic of the heatmap matrix for reports and presentations.

---

## 💡 Custom CSV Data Specifications

To use custom fund dataset files with these applications, construct your input CSV files according to these schema requirements:

### Daily Unit Price CSV (`lifesight_fundprices.csv`)
Required headers (case-sensitive): `Administrator`, `FundID`, `Fund`, `Date`, `UnitPrice`

```csv
Administrator,FundID,Fund,Date,UnitPrice
LifeSight,101,LifeSight Equity - LSEQ,2016-08-31,1.2534
LifeSight,101,LifeSight Equity - LSEQ,2016-09-01,1.2465