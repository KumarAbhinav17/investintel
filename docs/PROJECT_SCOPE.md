\# InvestIntel — Project Scope



\## Project Objective



InvestIntel is a personal investment intelligence and financial analytics platform that brings portfolio analytics, stock research, mutual fund research, market intelligence, and corporate events into one place.



The goal is to build a data-driven application that demonstrates practical data engineering, financial analytics, backend development, and frontend development skills.



\## Target User



Individual investors who want to understand and analyze their investments and financial markets from one platform.



\## MVP



The first version will include:



\- User authentication

\- Portfolio management

\- Stock research

\- Mutual fund research

\- Market overview

\- Basic corporate events

\- Financial analytics

\- Data ingestion and validation

\- PostgreSQL database

\- FastAPI backend

\- Next.js frontend



\## Deferred After MVP



\- Object storage / data lake

\- dbt

\- Airflow

\- Docker

\- Cloud data warehouse

\- Advanced monitoring

\- Advanced CI/CD

\- Personalized financial news

\- Advanced IPO analytics

\- AI / RAG / Text-to-SQL

\- Advanced alerts



\## Out of Scope



InvestIntel will NOT:



\- Execute trades

\- Store broker credentials

\- Provide direct buy/sell recommendations

\- Predict stock prices

\- Operate as a trading bot

\- Replace a broker such as Zerodha or Groww



\## Feature Cut Policy



If a required external data source cannot be obtained reliably, legitimately, and within the available time and budget, the dependent feature will be deferred rather than using fabricated or unverified data.



Feature cut order:



1\. FII/DII

2\. Corporate events

3\. Mutual funds

4\. Portfolio / stock research only as a last resort



\## 30-Day Constraint



The MVP is targeted for completion within 30 days with approximately 4 hours of development and learning time per day.



The priority is a working, publicly demonstrable vertical slice rather than a large number of incomplete features.



\## Success Criteria



The MVP is successful if:



\- A user can securely log in.

\- A user can add and view portfolio transactions.

\- Portfolio value and basic P\&L can be calculated.

\- Users can research stocks and mutual funds.

\- Market information can be displayed from legitimate external sources.

\- Data is validated before entering the database.

\- Duplicate ingestion does not create duplicate records.

\- The backend and frontend communicate through an API.

\- The application can be publicly demonstrated.

\- The project has clear documentation and reproducible setup instructions.

