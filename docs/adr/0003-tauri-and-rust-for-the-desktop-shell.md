# 0003. Tauri and Rust for the desktop shell

- **Status:** Accepted
- **Date:** 2026-09-04

## Context

A local-first desktop app (see [ADR 0002](0002-local-first-desktop-architecture.md)) needs to ship a native application on macOS first, then Windows, with direct access to the local filesystem and document-processing libraries, while keeping install size and resource use reasonable.

## Decision

The desktop shell will be built with **Tauri**, with the application core in **Rust**. The UI runs in Tauri's system web view (see [ADR 0004](0004-react-and-typescript-for-the-ui.md)), while filesystem access, document processing, and persistence live in the Rust layer.

## Trade-offs

**What we gain**

- Small binaries and a low memory footprint compared with bundling a full browser runtime (e.g. Electron).
- A strong, safe foundation in Rust for the performance- and correctness-sensitive core: file watching, hashing, duplicate detection, parsing, extraction.
- Cross-platform packaging for macOS now and Windows later, via Tauri's tooling.

**What it costs**

- A Rust learning curve on the core — a smaller pool of contributors can comfortably work there.
- An extra seam to design and maintain: the boundary between the web UI and the Rust layer.
