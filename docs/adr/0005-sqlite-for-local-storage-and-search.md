# 0005. SQLite for local storage and search

- **Status:** Accepted
- **Date:** 2026-09-04

## Context

The application needs durable local storage for extracted facts, document metadata, health events, and the links back to source documents, plus fast search across records — all without a server (see [ADR 0002](0002-local-first-desktop-architecture.md)).

## Decision

Local data will be stored in **SQLite**, using its full-text search capability for search across records and extracted information.

## Consequences

- A single embedded, well-understood, file-based database with no separate service to run.
- Full-text search is available locally without additional infrastructure.
- Original documents remain the source of truth; the database holds the extracted and organizational data that links back to them.
- Schema migrations must be handled deliberately as the data model evolves.
