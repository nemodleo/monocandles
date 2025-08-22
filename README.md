# Monocandles

**Monocandles** is a minimalist, black-and-white candlestick charting service — starting with **Ethereum (ETH)**.  
It removes the distracting red/blue visuals of conventional crypto charts and redefines market analysis as a calm, dignified experience.

> *“Less noise, more clarity. A graceful way to read the markets.”*


## 📖 Overview

- **Product name**: Monocandles  
- **Definition**: A monochrome candlestick charting tool for Ethereum  
- **Goal**: Provide a refined, composed user experience by eliminating the emotional triggers of typical red/blue UIs.  


## ❗ Problem Definition

- Conventional crypto charts use **red/blue aggressive visuals** that overstimulate users’ emotions.  
- In public spaces (café, office, classroom), opening such charts feels **stigmatized** as “gambling” or “speculative.”  
- There is a lack of charting services that offer **aesthetic, restrained, and dignified market analysis.**


## 🧑‍💻 Target Users

- **MZ generation**: Users familiar with minimal, aesthetic digital products.  
- **Casual investors**: People who want to check charts in public without drawing negative attention.  
- **Long-term investors**: Those preferring calm, neutral interfaces over emotional cues.  


## ✨ Core Value Proposition

1. **Monochrome UI** — No red/blue, just black & white candlesticks.  
2. **Anywhere-friendly** — Looks like a design tool/artwork rather than a casino dashboard.  
3. **Professional indicators** — Minimal does not mean limited. Essential analysis tools included.  
4. **Calm alerts** — Neutral, non-alarming notifications (“range break” instead of “-10% drop!”).  


## 📊 MVP Scope

### Supported Asset
- Ethereum (ETH) only

### Supported Timeframes
- **Seconds candles**: 1s (Upbit API, recent 3 months, missing if no trade)  
- **Minutes candles**: 1m, 5m, 10m  
- **Hours candles**: 1h, 4h  
- **Days candles**: 1d  

### Indicators
- **Bollinger Bands (BB)**  
- **Moving Averages (MA: 7, 15, 50, 200)**  
- **VWMA (Volume Weighted Moving Average)**  
- **VPVR (Volume Profile Visible Range)** – based on trade data binning  
- **DMF (Demand Flow, volume-based)** — explicit formula to be defined  

### Additional
- Volume bars (black & white)  
- Neutral alerts  
- Light/Dark mode  


## 🎨 Design Principles

- **Monochrome First**  
  - Background: `#FAF9F6` (Ivory White), `#1A1A1A` (Ink Black)  
  - Candles: White = Bullish, Black = Bearish  

- **Supporting Colors**  
  - `#9A9A9A` (Ash Gray)  
  - `#D6C7B0` (Antique Beige)  

- **Typography**  
  - Modern Sans-serif: *Inter*, *Neue Haas Grotesk*  

- **Philosophy**  
  - Restraint, balance, dignity  
  - Inspired by art galleries, design books, and monochrome photography  


## 🖼️ Differentiation

### Conventional Charts
- Red/blue aggressive visuals  
- Emotional triggers (fear/greed)  
- Social stigma in public use  

### Monocandles
- Black & white minimal UI  
- Calm, dignified viewing experience  
- Feels like a **design object**, usable anywhere without stigma  


## 🛠️ Tech Stack

- **Framework**: Next.js 14 (App Router) + TypeScript  
- **Charting**: [TradingView Lightweight Charts™](https://github.com/tradingview/lightweight-charts)  
  - Custom series styling (white bullish, black bearish)  
  - Lightweight, high-performance canvas rendering  
- **Indicators**: [`technicalindicators`](https://www.npmjs.com/package/technicalindicators) + custom implementations (VWMA, VPVR, DMF)  
- **Data Source**:  
  - Upbit REST API → OHLCV candles (seconds, minutes, hours, days)  
  - Upbit WebSocket API → real-time ticks & trades  
- **State Management**: TanStack Query + Zustand  
- **Deployment**: Vercel (Edge-ready, env-managed)  


## 🗺️ Roadmap

**Phase 1 (MVP, 1–2 months)**  
- Ethereum-only monochrome candlestick chart  
- 7 timeframes (1s → 1d)  
- Core indicators (BB, MA, VWMA, VPVR, DMF)  

**Phase 2 (3–4 months)**  
- Light/Dark mode toggle  
- Neutral alert system  
- Screenshot & share feature  

**Phase 3 (6 months~)**  
- User-defined indicator sets  
- Extended monochrome themes (Ivory, Graphite, Olive, Burgundy)  
- Performance optimization for large datasets  


## 🚀 Getting Started (Development)

### Requirements
- Node.js >= 20  
- npm >= 9  
- Framework: Next.js 14 + TypeScript  

### Clone the repository
```bash
git clone https://github.com/<your-username>/monocandles.git
cd monocandles

Install dependencies

npm install

Run development server

npm run dev

Then open http://localhost:3000 in your browser.
```

## 📜 License

This project is licensed under the Apache 2.0 License.
See the LICENSE file for details.

## 🙏 Acknowledgments
	•	Crypto data powered by Upbit API (initial MVP)
	•	Chart rendering with TradingView Lightweight Charts™
	•	Inspired by minimalist design, monochrome art, and classic financial charting
