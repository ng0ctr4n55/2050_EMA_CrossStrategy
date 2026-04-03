# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a collection of Pine Script v6 trading strategies and indicators for TradingView. The strategies focus on EMA crossovers combined with various confirmation indicators (SuperTrend, Trendilo, Volume Index, Bollinger Bands).

## Files

| File | Type | Description |
|------|------|-------------|
| `2050EMA.pine` | Strategy | EMA 20/50 cross strategy with Bollinger Bands, designed for weekly charts |
| `LT01_Strategy.pine` | Strategy | Triple Confirm Strategy - SuperTrend + Trendilo + EMA + Volume Index |
| `SuperTrend_EMA.pine` | Indicator | SuperTrend with KDE-based relative volume probability and EMA cross |
| `BB_20EMA_150EMA.pine` | Indicator | Bollinger Bands with standalone EMA overlay |
| `Trendilo_lt.pine` | Indicator | Trendilo oscillator with ALMA smoothing |

## Pine Script Conventions

- **Version**: All scripts use `//@version=6`
- **License**: Mozilla Public License 2.0 header required
- **Structure**: Inputs → Calculations → Signal Conditions → Plots → Alerts

## Usage

To use these scripts in TradingView:
1. Open TradingView.com and sign in
2. Open PINE Editor (bottom panel)
3. Copy the `.pine` file content into the editor
4. Save and apply to chart
5. For strategies, use Strategy Tester to view results

## Strategy Patterns

### EMA Cross Strategy (`2050EMA.pine`)
- Uses `strategy()` with `calc_on_every_tick=true`
- Enforces weekly timeframe with runtime error check
- Entry on EMA crossover, exit on opposite cross

### Triple Confirmation Pattern (`LT01_Strategy.pine`, `SuperTrend_EMA.pine`)
- Requires multiple conditions to align before entry:
  - SuperTrend direction alignment
  - EMA relationship (fast above/below slow)
  - Volume Index above EMA (volume confirmation)
  - Trendilo oscillator signal (crossover/crossunder)

### Volume Index
- Ratio of current volume to its EMA
- `vi_ratio >= 1.0` indicates volume above average (confirming momentum)
- Displayed as aqua background when confirmed

### Trendilo Oscillator
- ALMA-smoothed percent change with RMS bands
- `cdir > rms` = bullish (green), `cdir < -rms` = bearish (red)
- Zero line is "no-go zone" - avoid entries when oscillator is near zero

## Key Indicators

- **SuperTrend**: `ta.supertrend(factor, atr_length)` - trend direction
- **EMA**: `ta.ema(source, length)` - exponential moving average
- **ATR**: `ta.atr(length)` - average true range for stop-loss distances
- **ALMA**: `ta.alma(source, length, offset, sigma)` - Arnaud Legoux moving average

## Alert Conditions

Alerts use `alertcondition()` for signal notifications:
```pine
alertcondition(long_cond, 'LONG Signal', 'message')
alertcondition(short_cond, 'SHORT Signal', 'message')
```