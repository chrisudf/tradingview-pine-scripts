# TradingView Pine Scripts

Collection of Pine Script v5 indicators and strategies for TradingView.

## Scripts

| File | Description |
|------|-------------|
| [vol_regime_dashboard.pine](vol_regime_dashboard.pine) | Volatility regime dashboard combining VRP (VIX/RV), SKEW, and VVIX/VIX ratio into a single signal panel. Identifies sell-vol sweet spots, tail hedge opportunities, panic bottoms, and complacency zones. |
| [VIX_VIX3M.pine](VIX_VIX3M.pine) | VIX/VIX3M term-structure monitor (v2). Ratio bands 0.9 / 1.0 / 1.1 / 1.2 / 1.3, inversion and contango streaks, episode peak, 5-day / 15-day persistence alerts, relief signal after a ≥1.1 episode, 2-year percentile, optional full-curve check (VIX > VIX3M > VIX6M > VIX1Y) and a five-tier position guide. Use on a daily chart. |

## Usage

1. Open TradingView, load the relevant chart (SPX / SPY for most vol scripts)
2. Open **Pine Editor** at the bottom
3. Paste the script contents, click **Add to Chart**

Requires access to CBOE indices (VIX, VVIX, SKEW) — free TradingView accounts see 15-minute delayed data, which is fine for daily signals.
