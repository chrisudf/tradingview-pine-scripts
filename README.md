# TradingView Pine Scripts

Collection of Pine Script v5 / v6 indicators and strategies for TradingView.

## Scripts

| File | Description |
|------|-------------|
| [vol_regime_dashboard.pine](vol_regime_dashboard.pine) | Volatility regime dashboard combining VRP (VIX/RV), SKEW, and VVIX/VIX ratio into a single signal panel. Identifies sell-vol sweet spots, tail hedge opportunities, panic bottoms, and complacency zones. |
| [VIX_VIX3M.pine](VIX_VIX3M.pine) | VIX/VIX3M term-structure monitor (v2). Ratio bands 0.9 / 1.0 / 1.1 / 1.2 / 1.3, inversion and contango streaks, episode peak, 5-day / 15-day persistence alerts, relief signal after a ≥1.1 episode, 2-year percentile, optional full-curve check (VIX > VIX3M > VIX6M > VIX1Y) and a five-tier position guide. Use on a daily chart. |
| [rsi_oversold_v3.pine](rsi_oversold_v3.pine) | RSI oversold rebound (v6). Fires on the first close that crosses under the oversold line — no "wait for confirmation" filters, which backtested to zero edge. Grade A above the 200-day SMA, grade B below; exit when the close goes back above the 5-day SMA or after 10 bars. Presets: RSI14 / 30 (strongest per trade) and RSI6 / 20 (about 2.8 signals a year on QQQ). Panel shows the chart's own history of A/B trades; one `alert()` covers entries and exits. Backtested on daily bars only — on any other timeframe it shows a red warning and greys out the markers. |
| [kdj_moomoo.pine](kdj_moomoo.pine) | KDJ (v6) using the same formula as the moomoo / 通达信 default KDJ(9,3,3): RSV over 9 bars, K = (RSV + 2·K[1]) / 3, D = (K + 2·D[1]) / 3 (both seeded at 50), J = 3K − 2D. TradingView has no built-in KDJ and community versions use different smoothing. Checked against moomoo on QQQ, NVDA and GLD daily (2026-10-07 close): K / D / J identical to 3 decimals. |

## Usage

1. Open TradingView, load the relevant chart (SPX / SPY for most vol scripts)
2. Open **Pine Editor** at the bottom
3. Paste the script contents, click **Add to Chart**

Requires access to CBOE indices (VIX, VVIX, SKEW) — free TradingView accounts see 15-minute delayed data, which is fine for daily signals.
