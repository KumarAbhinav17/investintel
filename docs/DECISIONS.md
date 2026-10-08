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

