# DogDoc Inbox: Architecture

> **Purpose:** a shared visual of how the pieces fit: the **tool layers** and the **journey of a document** from import to display.
> Complements the architecture **ADRs** ([docs/adr](adr/)), which record *why* each choice was made.

## The layers

The app is a single local-first desktop process: a web UI on top of a native shell, talking to on-device storage. Nothing leaves the machine.

```mermaid
flowchart TB
    subgraph UI["UI: React + TypeScript (Vite)"]
        A1[App shell + dog selector]
        A2["Import: picker · folder · drag-drop"]
        A3[Document viewer]
        A4["Timeline · weight chart · export (later)"]
    end
    subgraph SHELL["Desktop shell: Tauri (Rust)"]
        B1["dialog plugin: file picker"]
        B2["fs plugin: read / copy files"]
        B3["sql plugin: SQLite access"]
    end
    subgraph DATA["Local storage: on device"]
        C1[("SQLite\ndogs · source_documents · health_events*")]
        C2[[Original files on disk]]
    end
    UI --> SHELL --> DATA

    classDef ui fill:#E3F2FD,stroke:#1E88E5,color:#0D47A1;
    classDef shell fill:#E0F2F1,stroke:#00897B,color:#004D40;
    classDef data fill:#FFF3E0,stroke:#EF6C00,color:#E65100;
    class A1,A2,A3,A4 ui
    class B1,B2,B3 shell
    class C1,C2 data
    style UI fill:#F5FAFF,stroke:#90CAF9,color:#0D47A1
    style SHELL fill:#F1FBFA,stroke:#80CBC4,color:#004D40
    style DATA fill:#FFF9F0,stroke:#FFCC80,color:#E65100
```

\* `health_events` and related fact tables arrive with the extraction phase.

## The journey of a document

Solid path = the walking skeleton (import → store → view). Dotted path = the extraction phase (extraction, review, history, export).

```mermaid
flowchart LR
    A[Pick / drag a PDF or image] --> B[Hash + read metadata]
    B --> C[Copy original to app-data dir]
    C --> D[(Insert row in source_documents)]
    D --> V[View original in the app]

    D -. "later" .-> E["Extract text · OCR fallback"]
    E --> F[Classify + extract fields]
    F --> G[Review & approve facts]
    G --> H[(health_events + provenance)]
    H --> I[Timeline + weight chart]
    H --> J[Export summary with citations]

    classDef now fill:#E8F5E9,stroke:#43A047,color:#1B5E20;
    classDef later fill:#F5F5F5,stroke:#BDBDBD,color:#616161;
    class A,B,C,D,V now
    class E,F,G,H,I,J later
```

## Notes

- **Local-first:** the SQLite database and the original files both live on the user's device; there is no server.
- **Pragmatic thin Rust:** SQLite is reached from TypeScript via `@tauri-apps/plugin-sql`; native Rust is kept to plugin registration for now.
- **Provenance:** every extracted fact links back to its source document and page. The dotted path always carries the `source_documents` id forward.

## Related

- [Architecture Decision Records](adr/): the *why* behind these choices.
