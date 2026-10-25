# P&G Media Spend Optimizer

AI solution 01 of 14 · Marketing · built for **Procter & Gamble**

Prepared by **K Bhargav Raju**.

## Problem statement

A company is spending heavily across multiple marketing channels, but management cannot determine which campaigns generate profitable customers. Develop an AI-driven system that analyzes campaign, customer, conversion and revenue data to identify inefficient spending, estimate campaign effectiveness, and recommend how the marketing budget could be reallocated.

## Why Procter & Gamble

P&G spends billions a year across TV, digital, retail media and influencers, and it has publicly cut digital spend that was not driving sales. This tool finds which channels pay back and moves money to them.

## Algorithm

1. **Collect and align data**: Weekly spend, revenue, conversions and customer value per channel
2. **Adstock transform**: Grid search the carry-over decay for each channel
3. **Marketing Mix Model**: Regression of revenue on transformed spend, with seasonality
4. **Saturation curves**: Hill curve per channel to find diminishing returns
5. **ROI and marginal ROI**: Revenue per $ now, and for the next $
6. **Profitability check**: Weight ROI by the lifetime value of customers each channel brings
7. **Budget optimizer**: Greedy reallocation in 1% steps toward the highest marginal profit
8. **LLM memo**: AI analyst explains the plan below

## Data

104 weeks of spend, revenue, conversions and customer value across 6 channels for one P&G category (sample data). All figures are illustrative and are not Procter & Gamble's actual numbers.

## How to use

Open `index.html` in any web browser. No installation is needed; the whole tool is one self-contained file.

The controls panel lets you change total budget change, max shift per channel, and the analysis reruns instantly. "New sample data" generates a fresh dataset.

## AI analyst panel

The "Ask the AI analyst" panel answers questions about the results in plain English through Claude. It works when the page is opened as a Claude artifact on claude.ai. Opened from GitHub, GitHub Pages or a local folder, all the models, charts and controls still run, and the panel shows that it is unavailable.
