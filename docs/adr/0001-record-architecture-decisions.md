# 0001. Record architecture decisions

- **Status:** Accepted
- **Date:** 2026-09-04

## Context

DogDoc Inbox is in early development, and several foundational decisions — how it runs, what it is built with, how it is licensed — are being made now. As more people look at or contribute to the project, the reasoning behind these decisions needs to be discoverable, rather than living only in one person's head or scattered across issues and chat.

## Decision

We will record significant architecture and project decisions as Architecture Decision Records (ADRs) in `docs/adr/`.

- Each ADR is a numbered Markdown file (`NNNN-title.md`).
- Each ADR captures **Context**, the **Decision**, and its **Trade-offs**, plus a **Status** and **Date**.
- ADRs are immutable once Accepted. A decision is changed by adding a new ADR that supersedes the earlier one, which is then marked **Superseded**.

This follows the lightweight ADR approach popularized by Michael Nygard.

## Trade-offs

**What we gain**

- Contributors understand *why* the project is the way it is, not just *what* — every decision carries its reasoning.
- New decisions get an obvious, low-friction home instead of scattering across chat, issues, or one person's memory.

**What it costs**

- A small, ongoing discipline: writing the record as each significant decision is made.
- The log is only trustworthy if it's kept honest — a decision reversed in practice but never recorded becomes a documentation bug.
