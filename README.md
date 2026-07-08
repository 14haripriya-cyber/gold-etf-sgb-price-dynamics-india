# Interlinkages and Price Dynamics among Gold ETFs, Sovereign Bonds, and Physical Gold in India

## 📌 Why This Study

Gold plays a unique cultural and economic role in India — the country accounts 
for roughly 25% of global gold demand, met almost entirely through imports, which 
widens the current account deficit and pressures the currency. Sovereign Gold 
Bonds (SGBs) and Gold ETFs were introduced as financial alternatives to physical 
gold. This paper compares how these three instruments — SGBs, Gold ETFs, and 
physical gold — behave relative to one another.

## 🎯 Research Objectives

- Compare returns and volatility of SGBs, Gold ETFs, and Physical Gold
- Evaluate liquidity and investor suitability of each instrument
- Identify which instrument offers the best risk-adjusted performance for 
  different investor types
- Draw out policy implications of promoting financial gold over physical holdings

## 🗂️ Data

- **Period**: January 2015 – October 2025 (10-year window covering crises and 
  recovery)
- **SGBs**: daily prices from BSE
- **Gold ETFs**: daily trading prices from NSE
- **Physical Gold**: daily gold futures prices (USD), converted to INR using 
  Yahoo Finance exchange-rate data

## 🔬 Methodology

1. **Data cleaning** — daily returns and price-index series derived, aligned 
   by trading date
2. **Correlation & Regression** — baseline relationships between instruments
3. **ADF test** — check stationarity of return series
4. **ARCH test** — detect volatility clustering
5. **Granger causality** — test whether gold price movements predict SGB/ETF 
   returns
6. **Johansen cointegration test** — test for a stable long-run equilibrium 
   relationship among the three instruments

## 📊 Key Results

**Correlation:**
- SGB–Gold correlation: **0.71** → SGBs closely track gold's general trend but 
  with smoother movement (fixed interest income + lower trading frequency)
- ETF–Gold correlation: **–0.13** → ETFs react quickly and diverge from gold's 
  broader trend day-to-day

**Regression:**
| Model | Equation | R² | Interpretation |
|---|---|---|---|
| SGB on Gold | R_SGB = 0.43 + 0.77·R_Gold | 0.51 | Gold explains ~half of SGB movement |
| ETF on Gold | R_ETF = 0.07 + 0.88·R_Gold | 0.74 | ETFs move almost one-to-one with gold |

**ADF Test:** All return series stationary (p < 0.01) — suitable for regression 
and causality analysis

**ARCH Test:** No significant volatility clustering in any series 
(SGB p=0.33, ETF p=0.19, Gold p=0.87) — return spikes are isolated, not persistent

**Granger Causality:**
- Gold → SGB: significant at 1-period lag (p = 0.031) — SGB prices adjust to 
  gold with a slight delay
- Gold → ETF: **not** significant (p > 0.75) — ETFs react near-instantly due to 
  high liquidity, so lagged gold movements add no predictive power

**Johansen Cointegration:** At least one cointegrating relationship found among 
SGB, ETF, and Gold — despite short-run divergence, prices converge to a common 
long-run trend, reflecting the growing **financialization of gold** in India

## 🖼️ Figures

![Correlation Heatmap](https://github.com/14haripriya-cyber/gold-etf-sgb-price-dynamics-india/blob/main/figures/Correlation%20Heatmap.png)
![Regression Results](https://github.com/14haripriya-cyber/gold-etf-sgb-price-dynamics-india/blob/main/figures/Regression%20Results%20%5BETF%20on%20Gold%5D.png)

## 🧭 Conclusion

- All three instruments are linked long-run, but behave differently short-run
- **ETFs**: strongest, fastest reaction to gold price changes — suits active 
  traders
- **SGBs**: smoother returns due to fixed interest + lower trading frequency — 
  suits long-term, risk-averse savers
- Together, SGBs and ETFs modernize gold savings in India and can help reduce 
  reliance on physical gold imports

## 🛠️ Tools Used

Python (data cleaning, regression, ARCH/ADF tests, Granger causality, Johansen 
cointegration, visualization)

## 📄 Full Deck

See [`Gold_ETF_SGB_price_dynamics.pdf`](https://github.com/14haripriya-cyber/gold-etf-sgb-price-dynamics-india/blob/main/Gold%20ETF%20SGB%20price%20dynamics.pdf) or 
[`Gold_ETF_SGB_price_dynamics.pptx`](https://github.com/14haripriya-cyber/gold-etf-sgb-price-dynamics-india/blob/main/Gold%20ETF%20SGB%20price%20dynamics.pptx) for the complete presentation.
