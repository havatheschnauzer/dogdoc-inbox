# 0003. Tauri and Rust for the desktop shell

- **Status:** Accepted
- **Date:** 2026-09-04

## Context

A local-first desktop app (see [ADR 0002](0002-local-first-desktop-architecture.md)) needs to ship a native application on macOS first, then Windows, with direct access to the local filesystem and document-processing libraries, while keeping install size and resource use reasonable.

## Decision

The desktop shell will be built with **Tauri**, with the application core in **Rust**. The UI runs in Tauri's system web view (see [ADR 0004](0004-react-and-typescript-for-the-ui.md)), while filesystem access, document processing, and persistence live in the Rust layer.

## Consequences

- Small binaries and low memory footprint compared with bundling a full browser runtime.
- Rust provides a strong foundation for the performance- and correctness-sensitive parts: file watching, hashing, duplicate detection, parsing, and extraction.
- Cross-platform packaging (macOS, later Windows) is supported by Tauri's tooling.
- The project needs Rust proficiency for core work, and the web/Rust boundary must be designed deliberately.
