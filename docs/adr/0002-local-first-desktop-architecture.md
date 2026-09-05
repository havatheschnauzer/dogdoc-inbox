# 0002. Local-first desktop architecture

- **Status:** Accepted
- **Date:** 2026-09-04

## Context

The product handles veterinary records, which owners consider private and personal. A common alternative would be a cloud service that ingests documents and stores them centrally, but that requires owners to upload their entire archive and trust a third party with it. The project's core promise is that records stay under the owner's control.

## Decision

DogDoc Inbox will be a **local-first desktop application**. Core work — importing, organizing, extracting, searching — happens on the user's own machine. No cloud account or silent document upload is required for core functionality. Original files are preserved in place rather than replaced by generated summaries.

## Trade-offs

**What we gain**

- Owners keep control of their documents; privacy becomes a structural property, not a policy promise.
- No server to run, secure, or pay for, and the app keeps working offline.

**What it costs**

- More work on the client: parsing, OCR, storage, and search all run locally instead of on a server.
- We give up free cross-device sync and collaboration — they would need deliberate, opt-in design later.
- Every future cloud feature must stay additive and optional, and be discussed before it touches core functionality.
