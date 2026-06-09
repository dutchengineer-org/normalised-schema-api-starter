# Normalised Schema + API

Starter repository for the **Relational Data Systems** capstone on [DutchEngineer](https://dutchengineer.org).

## What you will build

A web service backed by a normalised relational schema — designed, migrated, indexed, and connected the way production systems are built.

The goal is not a toy API. The goal is a schema and service another engineer could run, inspect with query analysis tools, and extend without breaking existing queries. How you build each piece is yours to decide.

## Requirements

1. **Normalised schema** — at least three tables with foreign key relationships. No field that belongs to a different entity lives on the wrong table. Include a written explanation of which normalisation violations the schema avoids and why.
2. **Migration script** — a script that creates all tables and can tear them down, in the correct dependency order. Running the create step twice must not produce an error.
3. **Indexes supporting service queries** — at least two indexes that directly support the queries your service runs. Each index is documented with which query it supports and why it will be used rather than a sequential scan.
4. **Connection pool in the web service** — the service maintains a pool of database connections that is created on startup and closed on shutdown. Individual routes borrow from the pool rather than opening a new connection per request.
5. **Query plan evidence** — include query analyser output for at least one query in `docs/explain.txt`. The plan must show index usage on the indexed column, not a sequential scan. Include a written explanation of what the plan shows.

## Suggested domain

An order system with customers, products, and orders — plus one additional table of your choice. The domain is a suggestion, not a constraint. Any domain that meets the schema and query requirements qualifies.

## Getting started

1. **Fork this repository** — click **Fork** at the top of [this page](https://github.com/dutchengineer-org/normalised-schema-api-starter) to create your own copy.
2. Clone your fork:
   ```
   git clone https://github.com/<your-username>/normalised-schema-api-starter
   cd normalised-schema-api-starter
   ```
3. Install dependencies: `uv sync`
4. Build and run: `uv run pytest`

## Submitting

When your work is ready, paste your repository URL into the submission form on your [capstone page](https://dutchengineer.org/foundations/relational-data-systems/capstone-normalised-schema-api/).
