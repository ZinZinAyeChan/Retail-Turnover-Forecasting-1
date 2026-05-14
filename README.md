# 📈 Australian Department Store Turnover Forecasting — Winter's Exponential Smoothing

A business forecasting report developed for BUSA3015 Business Forecasting at Macquarie University. Acting as a consultant for the Business Council of Australia, this project forecasts monthly turnover for Australian department stores using exponential smoothing models applied to ABS retail trade data.

---

## 📋 Project Overview

Using 8 years of monthly ABS retail turnover data (July 2015 – June 2023), this project applies and evaluates exponential smoothing models to forecast department store turnover for the 12-month out-of-sample period (July 2023 – June 2024). Forecasts are validated against actual 2023–2024 data and analysed for business insights.

---

## 🔍 Analysis Summary

**Data**
- Series: Total State Department Stores Turnover (Original-adjusted, Series ID: A3348618X)
- Sample period: July 2015 – June 2023 (96 monthly observations)
- Avg. monthly turnover: ~$1,620M · December peak: ~$3,000M · February trough: ~$1,100M

**Models Applied**

| Exercise | Data Series | Model | Purpose |
|---|---|---|---|
| Exercise 1 | Seasonally-adjusted | Simple / Holt Exponential Smoothing | Trend forecasting |
| Exercise 2 | Original (unadjusted) | Winter's Exponential Smoothing (WES) | Seasonal forecasting |

**Key Findings**
- Additive seasonal pattern identified — consistent December spikes and February troughs
- WES model with Solver-optimised parameters (α, β, γ) minimises MSE for best accuracy
- Within-sample forecasts closely align with actual data; January and April 2024 forecasts show minimal error (<$20M)
- Largest errors in August–September 2023, exceeding $150M
- Residual analysis (scatter plot + correlogram) confirms mostly random errors, with one ACF value at Lag 17 slightly exceeding the confidence interval

---

## 🛠️ Built With

- Microsoft Excel — WES model implementation, Solver optimisation, error metrics (MSE, MAPE, MAE)
- Minitab — Correlogram / ACF analysis

---

## 📁 Project Structure

```
Answers_Report_1.pdf         # Written report (Exercise 3) — attribution, scope, application,
                             # analysis, articulation of issues, critique, position
Report_1.xlsx        # Excel workbook — all three exercises with models and forecasts
```

---

## 📂 Data Source

- ABS Retail Trade, Australia (Cat. 8501.0) — Table 1: Retail Turnover, By Industry Group
- Series ID: A3348618X (Original) · A3348621L (Seasonally-adjusted)
- Source: https://www.abs.gov.au/statistics/industry/retail-and-wholesale-trade/retail-trade-australia

---

## 🧠 Concepts Demonstrated

- Time series analysis and seasonal pattern identification
- Simple, Holt's, and Winter's Exponential Smoothing
- Parameter optimisation via Solver (MSE minimisation)
- Within-sample and out-of-sample forecasting
- Residual diagnostics — scatter plot and autocorrelation function (ACF)
- Error metrics — MSE, MAPE, MAE
- Business-facing forecasting interpretation and critique
