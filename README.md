# Nasar Analytics

Event-driven hedging engine: turns KAP disclosures into BIST 30 portfolio shock estimates and recommends a futures hedge.

![status](https://img.shields.io/badge/status-in%20development-red)
![python](https://img.shields.io/badge/python-3.11+-blue)
![license](https://img.shields.io/badge/license-MIT-green)

Nasar is an engine for Borsa İstanbul. When a company in the BIST 30 publishes a KAP disclosure, Nasar estimates how the news shocks the price and volatility of a portfolio, then recommends how to adjust the BIST 30 futures hedge.

## The problem

A risk manager at an asset management firm holds a portfolio of BIST 30 stocks and hedges it with VİOP futures. When a KAP disclosure arrives, two questions follow:

1. How much does this news move the portfolio, and how much does it raise risk?
2. How should the hedge change right now?

## What Nasar does
Takes the KAP disclosure, extract the event and classifies it. Then it estimates the shock (price movement, volatility change) and shows the portfolio impact of it. The output is the hedge recommendation (hedge ratio, contract count, residual risk) for the portfolio.

The AI layer extracts and labels events. The product is the hedge.

## Why it is different

| Existing tools | Nasar |
|---|---|
| Summarize and score KAP news | Turns the news into a portfolio-level risk number |
| Stop at the stock | Goes to the portfolio and the futures hedge |
| Output a sentiment score | Outputs a hedge ratio and contract count |

## Status

| Component | Status |
|---|---|
| KAP ingestion | Planned |
| Labeled event dataset (BIST 30, 2018 to 2026) | Planned |
| Event study | Planned |
| Event-adjusted volatility model | Planned |
| Hedge engine | Planned |
| Backtest vs static hedge | Planned |
| Dashboard | Planned |

MVP target: end of February 2027.

## Results

Coming back to `Results` after the backtest. This section will show the event-conditional hedge against a static hedge: hedging error, drawdown, and cost.

## Scope

- **Now:** BIST 30 stocks and BIST 30 futures.
- **Later:** BIST 100, single-stock futures, other event sources (TCMB), options, other markets.

## Team

- **Omer Faruk Ruzgar:** Event study, volatility model, hedge engine, backtest
- **Melih Eserler:** KAP ingestion, LLM extraction.

Built as a graduation project in Computer Engineering.

## Disclaimer

This is a research project. It is not investment advice.

## Licanse

MIT


