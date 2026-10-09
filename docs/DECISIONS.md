\# Architecture Decisions



\## ADR-001: Data Layer Naming Convention



\### Decision



InvestIntel will use the following naming convention:



\- PostgreSQL schemas: `bronze`, `silver`, `gold`

\- dbt models: `stg\_`, `int\_`, `fct\_`, `dim\_`



\### Reason



This gives the project a consistent data-layer vocabulary from the beginning and keeps the eventual transition to a more complete data engineering architecture straightforward.



\### Alternatives Considered



\- Using `raw`, `staging`, and `marts`

\- Using only one PostgreSQL schema

\- Mixing different naming conventions



\### Trade-offs



The full bronze/silver/gold architecture will not be implemented during the MVP. The naming convention is being established now so that the project can evolve without renaming its data layers later.


## ADR-002: NSE EOD Data Excluded from MVP

NSE End-of-Day and Historical market data is currently treated as a paid data product. Therefore, it will not be used as the primary stock-price source for the ?0 MVP. Legitimate alternative sources are being evaluated before ingestion development begins.


## ADR-002: NSE EOD Data Excluded from MVP

NSE End-of-Day and Historical market data is currently treated as a paid data product. Therefore, it will not be used as the primary stock-price source for the ?0 MVP. Legitimate alternative sources are being evaluated before ingestion development begins.

## ADR-003: Synthetic Data for Public Demo

**Status:** Accepted

**Context:** Public-display permissions for real financial market data have not been confirmed. The project must not depend on receiving permission or on an unverified third-party data provider.

**Decision:**
- The public demo will use synthetic financial data and clearly label it as simulated.
- Synthetic prices will only be associated with fictional instruments.
- Real-data imports will be supported in local mode for files the user is permitted to use.
- Public deployment will not accept real-data uploads in the MVP.
- Data-source integrations will be modular so an approved provider can be added later.
- No production feature will depend on an unverified data source.

**Consequences:** Development, testing, demonstration, and deployment can continue without external data permissions. Real-market-data functionality may be added later after the relevant rights and terms are verified.

**Revisit condition:** Written permission and applicable licensing terms are verified for a specific source.

