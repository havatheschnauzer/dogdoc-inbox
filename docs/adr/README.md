# Architecture Decision Records

This directory records significant architecture and project decisions for DogDoc Inbox, following the lightweight format described in [ADR 0001](0001-record-architecture-decisions.md).

Each record is immutable once **Accepted**: to change a decision, add a new ADR that supersedes the old one (and mark the old one **Superseded**) rather than rewriting history.

## Index

| ADR | Title | Status |
|-----|-------|--------|
| [0001](0001-record-architecture-decisions.md) | Record architecture decisions | Accepted |
| [0002](0002-local-first-desktop-architecture.md) | Local-first desktop architecture | Accepted |
| [0003](0003-tauri-and-rust-for-the-desktop-shell.md) | Tauri and Rust for the desktop shell | Accepted |
| [0004](0004-react-and-typescript-for-the-ui.md) | React and TypeScript for the UI | Accepted |
| [0005](0005-sqlite-for-local-storage-and-search.md) | SQLite for local storage and search | Accepted |
| [0006](0006-mpl-2.0-license.md) | MPL-2.0 license | Accepted |

## Adding a new ADR

1. Copy the structure of an existing record.
2. Give it the next number and a short, descriptive title (`NNNN-title.md`).
3. Fill in Context, Decision, and Trade-offs; set Status and Date.
4. Add a row to the index above.
