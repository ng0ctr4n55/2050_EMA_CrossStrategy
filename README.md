# 2050 EMA CrossStrategy Collection

A set of Pine Script v6 trading strategies and indicators for TradingView, focused on EMA crossovers with momentum and trend confirmations.

## Files

| File | Type | Description |
|------|------|-------------|
| `2050EMA.pine` | Strategy | EMA 20/50 cross with Bollinger Bands, designed for weekly charts |
| `20EMA-150EMA-supertrend-trendilo.pine` | Indicator | 20/150 EMA + SuperTrend + Trendilo — 4-condition confirmation with info table |
| `qullamaggie_breakout_setup1.pine` | Indicator | Qullamaggie breakout setup — prior move, consolidation, bull backdrop |

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
- **Filter**: Bollinger Bands

## Indicators

### 20EMA-150EMA-SuperTrend-Trendilo — 4-Condition Confirmation
Combines four conditions for entry signals:
1. **20 EMA vs 150 EMA** — trend direction
2. **Price vs 20 EMA** — short-term momentum
3. **SuperTrend** — trend-following filter
4. **Trendilo** — ALMA-smoothed momentum oscillator crossing RMS band

- **Long**: 20 EMA > 150 EMA, Price > 20 EMA, SuperTrend UP, Trendilo crosses up through zero
- **Short**: 20 EMA < 150 EMA, Price < 20 EMA, SuperTrend DOWN, Trendilo crosses down through zero
- Displays an info table (bottom-right) showing all 4 condition statuses
- Trend-aligned background colouring

### Qullamaggie Breakout Setup 1
Based on Kristjan Kullamägi's flag/continuation breakout setup:
- Prior big move detection
- ATR compression (consolidation)
- Higher lows in consolidation
- Bull backdrop (fast EMA > slow EMA)

## Video Walkthrough
- [2050EMA Strategy Explanation](https://youtu.be/cGd2FPyhacI)

---

Disclaimer:
The content shared on this channel reflects personal opinions and interpretations intended for educational and informational purposes only. It is not professional advice, nor should it be relied upon as such.

Viewers are encouraged to consult qualified professionals before making decisions based on the material presented. While every effort is made to ensure accuracy, the creator makes no guarantees regarding completeness, reliability, or applicability to individual circumstances.
