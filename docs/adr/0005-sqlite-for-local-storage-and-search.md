# 0005. SQLite for local storage and search

- **Status:** Accepted
- **Date:** 2026-09-04

## Context

The application needs durable local storage for extracted facts, document metadata, health events, and the links back to source documents, plus fast search across records — all without a server (see [ADR 0002](0002-local-first-desktop-architecture.md)).

## Decision

Local data will be stored in **SQLite**, using its full-text search capability for search across records and extracted information.

## Trade-offs

**What we gain**

- A single embedded, well-understood, file-based database with no separate service to run or secure.
- Local full-text search with no additional infrastructure.
- The database stays a derived index over untouched original documents, so it can be rebuilt from source if needed.

**What it costs**

- We own schema migrations and versioning as the data model evolves.
- SQLite fits local, single-user access; a future networked or multi-user need would mean revisiting the storage choice.
