# 2050 EMA CrossStrategy Collection

Pine Script v6 trading strategies and indicators for TradingView, built around EMA crossovers, Bollinger Bands, and intraday range setups.

## Files

| File | Type | Description |
|------|------|-------------|
| `2050EMA.pine` | Strategy | Weekly EMA 20/50 cross with Bollinger Bands and long/short/both direction filter |
| `2050EMA-indicator.pine` | Indicator | Weekly EMA 20/50 cross overlay with Bollinger Bands and crossover alerts |
| `50-200SMA-MACD.pine` | Indicator | 5M/4H scalping overlay: first 4-hour range of the NY day, failed-breakout trap signals |
| `DayTrades/5M-4Hscalping.pine` | Indicator | Same 5M/4H scalping overlay, now with configurable 50 SMA and 200 SMA |

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

### 50-200SMA-MACD / 5M-4H Scalping
- **Timeframe**: 5-minute
- Uses the high/low of the first 4-hour candle of the NY session as the daily range
- Signals a short when price breaks above the range then closes back inside
- Signals a long when price breaks below the range then closes back inside
- Visual range zone and S/L plot shapes

### DayTrades/5M-4Hscalping
- Same 5M/4H failed-breakout logic as above
- Added configurable **50 SMA** and **200 SMA** overlays for trend reference
- Toggle each SMA on/off and adjust length in the "SMAs" input group

## Recent Changes

- Added 50 SMA and 200 SMA plots to `DayTrades/5M-4Hscalping.pine`
- Removed legacy `20-50SMA-MACD.pine` and `qullamaggie_breakout_setup1.pine`
- Added new standalone `50-200SMA-MACD.pine` 5M/4H scalping indicator

## Video Walkthrough
- [2050EMA Strategy Explanation](https://youtu.be/cGd2FPyhacI)

---

Disclaimer:
The content shared on this channel reflects personal opinions and interpretations intended for educational and informational purposes only. It is not professional advice, nor should it be relied upon as such.

Viewers are encouraged to consult qualified professionals before making decisions based on the material presented. While every effort is made to ensure accuracy, the creator makes no guarantees regarding completeness, reliability, or applicability to individual circumstances.
