# InvestIntel — Project Scope

## Project Objective

InvestIntel is a personal investment analytics platform designed to demonstrate practical data engineering, financial analytics, backend development, and frontend development skills.

The MVP focuses on portfolio tracking, financial calculations, data ingestion, validation, and stock research using synthetic demo data.

## Target User

Individual investors who want to track transactions, understand portfolio performance, and explore financial analytics.

## MVP

The first version will include:

- User authentication with secure password hashing and account-level data isolation
- Portfolio management and transaction tracking
- Cost-basis calculations and realized profit/loss
- Portfolio valuation and unrealized profit/loss using available price data
- Stock research with OHLCV charts using synthetic data for fictional instruments
- CSV ingestion and data validation
- Duplicate detection and rejected-record handling
- PostgreSQL database
- FastAPI backend
- Next.js frontend
- Public deployment with clearly labelled synthetic demo data
- Local-only import of real financial data from files the user is permitted to use
- Documentation, tests, and reproducible setup instructions

## Data Policy

- Public demo data must be synthetic and clearly labelled as simulated.
- Synthetic prices must only be associated with fictional instruments.
- Real financial data must not be presented as verified unless its source and permitted use have been established.
- The public deployment will not accept real-data uploads in the MVP.
- Local imports may process files the user has permission to use.
- External data providers may be integrated later after their relevant licensing and usage terms have been verified.
- No feature may depend on receiving an external provider's response or approval.

## Deferred After MVP

- Mutual fund research using external data
- Live market data and real-time quotes
- Market-wide overview using external data
- Corporate events and FII/DII analytics
- Advanced IPO analytics
- Object storage and data lake
- dbt
- Airflow
- Docker
- Cloud data warehouse
- Advanced monitoring and CI/CD
- Personalized financial news
- AI, RAG, and Text-to-SQL
- Advanced alerts

## Out of Scope

InvestIntel will NOT:

- Execute trades
- Store broker credentials
- Provide direct buy/sell recommendations
- Predict stock prices
- Operate as a trading bot
- Replace a broker such as Zerodha or Groww
- Publish unverified real-market data as authoritative information

## Feature Cut Policy

If a required external data source cannot be obtained reliably, legitimately, and within the available time and budget, the dependent feature will be deferred rather than using fabricated real-world data or an unverified source.

The core portfolio, ingestion, analytics, API, and frontend work must remain independent of external data-source approvals.

## 30-Day Constraint

The MVP is targeted for completion within 30 days, with approximately four hours of development and learning per day.

The priority is a working, publicly demonstrable vertical slice rather than a large number of incomplete features.

## Success Criteria

The MVP is successful if:

- A user can securely register or log in.
- Each user's portfolio data is isolated from other accounts.
- A user can add, view, and manage portfolio transactions.
- Cost basis and realized profit/loss are calculated correctly.
- Portfolio valuation and unrealized profit/loss work with available price data.
- Fictional instruments and synthetic prices are clearly labelled in the public demo.
- CSV data is validated before entering the database.
- Invalid records are rejected with understandable reasons.
- Repeated ingestion does not create duplicate records.
- The backend and frontend communicate through an API.
- Automated tests cover important calculations and ingestion rules.
- The application can be publicly demonstrated without external data permissions.
- Documentation and setup instructions allow another developer to reproduce the project.