# 0004. React and TypeScript for the UI

- **Status:** Accepted
- **Date:** 2026-09-04

## Context

DogDoc Inbox has a document-centric, review-heavy interface: health timelines, document viewers, extraction-review workflows, and generated reports. It needs an accessible, maintainable UI layer that runs inside the Tauri web view (see [ADR 0003](0003-tauri-and-rust-for-the-desktop-shell.md)) and is familiar to a wide pool of contributors.

## Decision

The user interface will be built with **React** and **TypeScript**.

## Consequences

- A large, familiar ecosystem lowers the barrier for UI contributors.
- TypeScript's type checking helps keep the UI honest as the data model — extracted facts, their sources, and confidence — grows.
- Requires a clearly defined, typed boundary between the React UI and the Rust core.
- Accessibility remains an explicit responsibility rather than something the framework guarantees on its own.
