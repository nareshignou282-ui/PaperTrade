# PaperTrade v4 — Dhan-inspired paper trading mobile app

This Android prototype follows the mobile information architecture and light visual density shown in the user's Dhan reference screenshots while using original PaperTrade branding.

## Included
- Dhan-inspired Home / Watchlist / Portfolio / Orders / Funds navigation
- Positions | Orders | Super | Flash workflow
- NIFTY full-chain style option-chain UI with 50-point strikes around ATM
- Paper Buy/Sell order sheet, MIS/NRML/CNC/MTF, Market/Limit/SL/SL-M/Super fields
- Virtual wallet, margin utilization, realized/unrealized P&L
- Positions with Add / Exit / Reverse actions
- Trader's Diary and Trader Controls / Kill Switch
- Official TradingView ticker tape and Advanced Chart embeds
- GitHub Actions APK builder

## Market-data boundary
TradingView widgets are used only for their official embedded visual experience. TradingView does not expose widget prices as a public raw quote API for a custom order engine. Therefore the raw option-chain/execution layer is implemented behind the PaperTrade provider adapter and must be connected to an authorized live market-data provider for exchange-grade real-time NIFTY option-chain fills.

The included raw quote/option values are a demo provider so the complete paper-trading workflow can be tested without real money. Do not represent them as guaranteed exchange real-time prices.

## Build
Push this folder to GitHub. `.github/workflows/build-apk.yml` builds `PaperTrade.apk` as an Actions artifact.
