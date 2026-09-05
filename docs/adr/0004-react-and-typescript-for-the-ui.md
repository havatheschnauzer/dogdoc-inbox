# 0004. React and TypeScript for the UI

- **Status:** Accepted
- **Date:** 2026-09-04

## Context

DogDoc Inbox has a document-centric, review-heavy interface: health timelines, document viewers, extraction-review workflows, and generated reports. It needs an accessible, maintainable UI layer that runs inside the Tauri web view (see [ADR 0003](0003-tauri-and-rust-for-the-desktop-shell.md)) and is familiar to a wide pool of contributors.

## Decision

The user interface will be built with **React** and **TypeScript**.

## Trade-offs

**What we gain**

- A large, familiar ecosystem that lowers the barrier for UI contributors.
- TypeScript's type checking keeps the UI honest as the data model — facts, their sources, confidence — grows.

**What it costs**

- A front-end build toolchain to set up and maintain, plus the upkeep of a typed boundary between the React UI and the Rust core.
- Accessibility stays our explicit responsibility — the framework does not guarantee it for us.
