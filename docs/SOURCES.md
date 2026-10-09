# InvestIntel - Data Source Research

## 1. Stock End-of-Day (EOD) Prices

### Candidate A - NSE India
- Dataset: Equity EOD and historical market data
- Source type: Official primary source
- Access: Paid subscription
- Cost suitability: Not suitable for the INR 0 MVP
- Decision: Excluded as the MVP's primary price source

### Candidate B - Twelve Data
- Dataset: Indian equity prices and historical OHLCV
- Source type: Third-party API
- Access: NSE/BSE access requires a paid plan according to reviewed plan information.
- Decision: Not selected as the public production source.

### Candidate C - Yahoo Finance / yfinance
- Dataset: Historical Indian equity prices
- Source type: Third-party
- Access: Python library accessing Yahoo Finance data
- Technical suitability: Useful for prototyping and local experiments.
- Decision: Development use only where permitted by applicable terms.

## 2. Current Source Strategy
- Keep InvestIntel public-facing.
- Target INR 0 operating cost for the MVP.
- Do not assume freely accessible data is licensed for public redistribution.
- Keep source-specific ingestion code separate from canonical schemas and analytics.
- Preserve raw data and source metadata where permitted.
- Do not fabricate financial data or describe delayed/historical data as real-time.

## 3. Outstanding Research
- Identify a legitimate stock EOD source suitable for the public MVP.
- Verify corporate-action data access and usage terms.
- Research AMFI NAV data and applicable terms.
- Research NSE FII/FPI and DII data access, revision behavior, and terms.

## 4. Current Status
Stock-price source selection is unresolved. No production ingestion implementation should depend on an unverified provider.
