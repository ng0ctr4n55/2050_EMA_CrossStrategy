# 2050 EMA CrossStrategy Collection

A set of Pine Script v6 trading strategies and indicators for TradingView, focused on EMA crossovers with momentum and trend confirmations.

## Files

| File | Type | Description |
|------|------|-------------|
| `2050EMA.pine` | Strategy | EMA 20/50 cross with Bollinger Bands, designed for weekly charts |
| `LT01_Strategy.pine` | Strategy | Triple Confirm — SuperTrend + Trendilo + EMA + Volume Index |
| `SuperTrend_EMA.pine` | Indicator | SuperTrend with KDE-based relative volume probability and EMA cross |
| `BB_20EMA_150EMA.pine` | Indicator | Bollinger Bands with standalone EMA overlay |
| `Trendilo_lt.pine` | Indicator | Trendilo + 9 EMA / 200 EMA momentum indicator |
| `qullamaggie_breakout_setup1.pine` | Indicator | Qullamaggie breakout setup |

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

### LT01 — Triple Confirmation
Requires four conditions to align:
- SuperTrend direction
- EMA 20 vs EMA 50 alignment
- Price vs EMA 9
- Trendilo oscillator crossing RMS band

## Indicators

### Trendilo_lt — Trendilo + 9/200 EMA
Uses three confirmations for signal arrows:
1. **9 EMA vs 200 EMA** — trend direction
2. **Price vs 9 EMA** — short-term momentum
3. **Trendilo** — ALMA-smoothed momentum crossing RMS bands

- **Long**: 9 EMA > 200 EMA, Price > 9 EMA, Trendilo crosses up through RMS band
- **Short**: 9 EMA < 200 EMA, Price < 9 EMA, Trendilo crosses down through RMS band
- **No-Go Zone**: Label appears when Trendilo touches zero

## Video Walkthrough
- [2050EMA Strategy Explanation](https://youtu.be/cGd2FPyhacI)

---

Disclaimer:
The content shared on this channel reflects personal opinions and interpretations intended for educational and informational purposes only. It is not professional advice, nor should it be relied upon as such.

Viewers are encouraged to consult qualified professionals before making decisions based on the material presented. While every effort is made to ensure accuracy, the creator makes no guarantees regarding completeness, reliability, or applicability to individual circumstances.
