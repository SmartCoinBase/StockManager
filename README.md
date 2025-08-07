# StockManager

> Be Rich or Avoid Bankruptcy

**StockManager** is a self-hosted Progressive Web App (PWA) designed to help individuals manage their stock portfolios.

Smartly, privately, and without reliance on cloud-based services or third-party APIs.

## Project Overview

A lightweight, local-first application to

- **track**
- **analyze**
- **support decision-making**

For stock portfolios.

Using **simple interpretable machine learning** techniques.

Built to run entirely on your own machine.  

No data sent to the cloud, and no bloatware dependencies.

## What Makes Stockmanager Smart?

A smart portfolio tracker does more than display charts — it:

- Analyzes your historical and current holdings

- Detects risk patterns and price movement trends

- Applies **lightweight ML models** (like decision trees) to propose actions

- Offers **offline-first** predictive capability

- Respects user control instead the them own decision

We do not use **OpenAI**, **Claude**, **Gemini** or other API-heavy "AI" solutions.

Instead, we focus on **transparent**, **CPU-only**, and **locally executed** intelligence.

## Intelligence Without Hype

### Methods We Use

- **Decision Tree** for rule-based actions (e.g. BUY/SELL/HOLD)
- **Simple Predictive Models** (linear regression, volatility scoring)
- **Portfolio Health Check** (diversification ratio, exposure limits)

### Methods We Avoid

- Black-box neural networks
- GPU-hungry models
- API-based cloud inference engines

## Planned Features

### Integrations

- [ ] Stock Discovery module

- [ ] Support for non-stock-based investments

- [ ] Connect to banks via **OpenFinance** API

- [ ] Connect to brokers via their **Web APIs**

- [ ] Manual import via **CSV** / **JSON**

### Automatic Decision Exceution

The core of StockManager is **automated portfolio management** through **explicit rules defined by the user**.

#### Support Strategies

- **Stop Loss** — sell when price drops below a defined threshold
- **Take Profit (Stop Gain)** — sell when price reaches a desired target
- **Trailing Stop** — dynamically sell when price drops X% from peak
- **Date-based Rules** — sell if no appreciation by a specific date
- **Conditional Buy/Hold/Sell** — based on model predictions or thresholds

#### Rule Behavior

- Rules are **defined and prioritized by the user**
- Actions may be **automatically executed** by the system, according to configuration
- All automated logic is **explainable and deterministic**
- The system logs and justifies all actions for auditability

### User Control First

- Automatic actions are only performed if rules are enabled and configured
- Each rule must be explicitly authorized by the user
- The system is non-opinionated: it does not assume — it executes what you've defined

### Example Scenario

#### System found a promising stock (with automatic execution)

> The StockManager **Discover module** identifies a stock matching your criteria:
>
> **Stock**: [AAPL34](https://statusinvest.com.br/bdrs/aapl34)
> **P/E Ratio**: 10.5
> **Dividend Yield**: 4.5%
> **Current Price**: R$38.00
>
> 50-day Moving Average: R$36.50
>
> The system evaluates your current cash balance and portfolio exposure:
>
> Available cash: R$5,000
>
> Maximum allocation per stock (user-defined): 20% of portfolio
>
> Current exposure to AAPL34: 0%
>
> Because the conditions meet your rules and there is sufficient cash, the system proceeds to:
>
> Automatically place a BUY order for AAPL34 at the target entry price of R$37.00
>
> Create associated Stop Loss (5%) and Take Profit (15%) rules
>
> Log the purchase and rule creation with timestamps and decision metadata
>
> The system notifies you:
>
> "Order placed: BUY 135 shares of AAPL34 at R$37.00
> Stop Loss set at R$35.15, Take Profit at R$42.55.
> This action was performed automatically based on your configured rules and available balance."

#### User bought a Stock

> You bought [PETR4](https://statusinvest.com.br/acoes/petr4) at R$32.50
> Current market price is R$30.75
>
> You configured the following rules:
>
> Stop Loss at R$30.00
>
> Take Profit at R$36.00
>
> Trailing Stop at 5%
>
> The system:
>
> Monitors the asset in real-time (offline/local)
>
> Detects that price is nearing Stop Loss
>
> Triggers a SELL action automatically (or notifies you, depending on your rule priority)
>
> Logs the reason and logic used (e.g. "Trailing Stop triggered: price dropped 5.1% from peak")
>
> ✅ All decisions are traceable, local, and under your control

## Privacy & Ownership

- 100% self-hosted — no external servers
- Local-only processing — no telemetry or background sync
- No vendor dependency — everything runs on your machine
- Your rules, your data, your decisions
