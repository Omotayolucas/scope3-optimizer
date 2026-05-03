# 🌿 Scope 3 Emissions Optimizer
### Multi-Objective Supplier Routing · Cost vs. Emissions Trade-off



![Live Demo](https://img.shields.io/badge/Live%20Demo-View%20Tool-00e5a0?style=for-the-badge)




![GHG Protocol](https://img.shields.io/badge/GHG%20Protocol-Category%201-blue?style=for-the-badge)




![EU CSRD](https://img.shields.io/badge/EU%20CSRD-Art.29%20Aligned-green?style=for-the-badge)



## Live Tool
👉 https://omotayolucas.github.io/scope3-optimizer

## What This Is

A fully interactive, browser-based supply chain optimization 
tool that helps procurement and sustainability teams make 
data-driven supplier routing decisions by simultaneously 
minimizing annual procurement cost and Scope 3 carbon 
emissions (GHG Protocol Category 1 — Purchased Goods 
and Services).

No installation required. Runs entirely in the browser.

## Methodology

### 1. Multi-Objective Optimization (Pareto Frontier)

The core model uses weighted-sum scalarization to generate 
the Pareto-optimal frontier:

minimize: α · C(x) + (1-α) · E(x)
subject to: lead_time(x) ≤ L_max, |x| ≤ n_max

Where α ∈ [0,1] is the cost preference weight.
The frontier is swept across 40 alpha values and 
non-dominated solutions are filtered using Pareto 
dominance criteria.

### 2. Stochastic Demand Simulation (Monte Carlo)

1,000 independent demand scenarios using log-normal 
distribution:

D ~ LogNormal(μ, σ²) where μ = ln(D̄) - σ²/2

Outputs: Mean Cost, Standard Deviation, 95% VaR, 99% VaR.

### 3. Carbon Price Sensitivity Analysis

Total Cost = Procurement Cost + CO₂e × Carbon Price

Reveals the EU ETS price point where green routing 
becomes financially dominant.

### 4. ESG Alignment

| Framework | Coverage |
|-----------|----------|
| GHG Protocol | Scope 3, Category 1 |
| EU CSRD | Article 29 — supply chain emissions |
| EU ETS | Carbon price range $10–$150/tCO₂e |

## Features

- Pareto Frontier — 40-point cost vs emissions trade-off curve
- Monte Carlo Simulation — 1,000 log-normal demand trials with VaR
- Carbon Sensitivity — Total cost vs EU ETS price for 3 strategies
- Carbon Credit Valuation — Monetizes emissions savings
- CSV Export — Full structured report
- PDF Export — Print-ready professional report
- 5 Industry Sectors — FMCG, Pharma, Auto, Electronics, Agro

## Supplier Network

12 synthetic suppliers across 4 global regions:

| Region | Suppliers | Cost Range | CO₂e Range |
|--------|-----------|------------|------------|
| West Africa | 2 | $11.8–$12.4/unit | 0.8–1.1 kg/unit |
| Europe | 3 | $18.2–$22.4/unit | 0.2–0.5 kg/unit |
| Asia Pacific | 4 | $6.9–$10.2/unit | 1.9–5.2 kg/unit |
| Americas | 3 | $11.2–$16.8/unit | 0.6–1.4 kg/unit |

## How to Use

1. Open the live tool link above
2. Adjust α slider for cost vs emissions preference
3. Set annual demand, lead time, and carbon price
4. Click RUN OPTIMIZATION
5. Click RUN MONTE CARLO to stress-test under uncertainty
6. Check Carbon Sensitivity tab for EU ETS impact
7. Export results as CSV or PDF

## Skills Demonstrated

- Multi-Objective Optimization (Pareto frontier generation)
- Stochastic Modelling (Monte Carlo, Value-at-Risk)
- ESG Quantification (GHG Protocol, EU CSRD)
- Supply Chain Network Design (12-supplier global network)
- Data Visualization (Chart.js)
- Full-Stack Analytics Tool (HTML/CSS/JS, no backend)

## Author

Omotayo Agbabiaka
BSc Mathematics | LASUSTECH | Lagos, Nigeria
Supply Chain Analytics & Operations Research
GitHub: github.com/Omotayolucas
Live Tool: https://omotayolucas.github.io/scope3-optimizer
LinkedIn: https://www.linkedin.com/in/omotayo-agbabiaka-55b549164

## Disclaimer

All supplier data is synthetic and used for portfolio 
demonstration purposes only. Equal demand allocation 
assumed across selected suppliers. Capacity constraints 
not modelled in this prototype.
