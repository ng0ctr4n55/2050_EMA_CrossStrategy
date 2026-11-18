# 2050 EMA CrossStrategy Collection

Pine Script v6 trading strategies and indicators for TradingView, built around EMA crossovers, Bollinger Bands, and intraday range setups.

## Files

| File | Type | Description |
|------|------|-------------|
| `2050EMA.pine` | Strategy | Weekly EMA 20/50 cross with Bollinger Bands and long/short/both direction filter |
| `2050EMA-indicator.pine` | Indicator | Weekly EMA 20/50 cross overlay with Bollinger Bands and crossover alerts |
| `50-200SMA-MACD.pine` | Indicator | 50/200 SMA trend filter with MACD histogram confirmation |
| `DayTrades/5M-4Hscalping.pine` | Indicator | 5M/4H scalping overlay: first 4-hour range of the NY day, failed-breakout trap signals |

## Quick Start (TradingView)

1. Log in to [tradingview.com](https://tradingview.com)
2. Open the **Pine Editor** (bottom panel)
3. Copy the content of any `.pine` file into the editor
4. Save and apply to your chart
5. For **strategies**, open **Strategy Tester** to view backtest results

## Strategies

### 2050EMA — Weekly EMA Cross
- **Timeframe**: Weekly
- **Entry**: EMA 20 crosses above EMA 50
- **Exit**: Opposite cross
- **Filter**: Bollinger Bands; choose Long, Short, or Both in settings

## Indicators

### 2050EMA-indicator
- Weekly chart overlay
- Plots EMA 20 and EMA 50
- Bullish/bearish crossover shapes and alerts
- Bollinger Bands background coloring

### 50-200SMA-MACD
- Plots the **50 SMA** and **200 SMA** with trend-based bar coloring
- **Long signal**: `close > 50 SMA`, `close > 200 SMA`, `50 SMA > 200 SMA` by **0.15%**, and **MACD histogram > 0**
- **Short signal**: the exact opposite conditions
- Real-time info table shows `Close vs 50`, `Close vs 200`, `MACD Hist`, and `50 vs 200` differentials
- Long/short signal arrows and alert conditions included

### DayTrades/5M-4Hscalping
- Same 5M/4H failed-breakout logic as above
- Added configurable **50 SMA** and **200 SMA** overlays for trend reference
- Toggle each SMA on/off and adjust length in the "SMAs" input group

## Recent Changes

- Refactored `50-200SMA-MACD.pine` to a pure 50/200 SMA + MACD histogram strategy:
  - Removed the 20 SMA and all related inputs/plots/bar-color logic
  - Long entry requires `close > 50 SMA`, `close > 200 SMA`, `50 SMA > 200 SMA` by 0.15%, and `MACD hist > 0`
  - Short entry uses the inverse conditions
  - Info table now displays `Close vs 50`, `Close vs 200`, `MACD Hist`, and `50 vs 200`
  - Removed dead code (`sma_diff`, duplicated `macd_diff`) and fixed alert messages
- Added 50 SMA and 200 SMA plots to `DayTrades/5M-4Hscalping.pine`
- Removed legacy `20-50SMA-MACD.pine` and `qullamaggie_breakout_setup1.pine`

## Video Walkthrough
- [2050EMA Strategy Explanation](https://youtu.be/cGd2FPyhacI)

---

Disclaimer:
The content shared on this channel reflects personal opinions and interpretations intended for educational and informational purposes only. It is not professional advice, nor should it be relied upon as such.

Viewers are encouraged to consult qualified professionals before making decisions based on the material presented. While every effort is made to ensure accuracy, the creator makes no guarantees regarding completeness, reliability, or applicability to individual circumstances.
