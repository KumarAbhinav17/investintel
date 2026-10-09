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

### Technical Sample Test — NSE CM-UDiFF Bhavcopy

**Sample file:** `BhavCopy_NSE_CM_0_0_0_20261009_F_0000.csv`

- Records inspected: 3,687
- Columns: 34
- EQ-series records: 2,675
- Relevant fields include symbol, trading date, open, high, low, close, previous close, traded volume, traded value, and number of transactions.
- TCS is present in the sample.
- The file also contains other instrument types, so ingestion must validate and filter records appropriately.

**Assessment**
- Technical feasibility: Promising for bulk daily stock-price ingestion.
- Data quality: Requires further validation and instrument filtering.
- Public-display permission: Not yet confirmed.
- Production status: Not approved pending verification of data-use and redistribution rights.

**Decision:** Retain NSE CM-UDiFF Bhavcopy as a candidate source. Do not use it for public production display until the applicable permissions are verified.

## 5. Permission Requests and Fallback Plan

| Organisation | Request | Status |
|---|---|---|
| NSE | Public display rights and licensing for Bhavcopy data | Email sent; awaiting response |
| Indian API | Upstream data provenance, licensing, and free-plan limits | Inquiry submitted; awaiting response |
| AMFI | Terms for public display of NAV data | Inquiry submitted; awaiting response |

### Fallback if No Replies Arrive

- The public MVP will use clearly labelled synthetic financial data.
- Synthetic prices will only be associated with fictional instruments.
- Local imports may process real-data files only where the user has permission to use them.
- The public deployment will not accept real-data uploads in the MVP.
- Source-specific ingestion will remain separate from canonical schemas and analytics.
- No external source will be used for public production display until its applicable usage and licensing terms are verified.

**Review point:** Day 14 of development. No response does not constitute permission.