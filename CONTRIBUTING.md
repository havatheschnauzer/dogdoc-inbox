# Contributing to DogDoc Inbox

DogDoc Inbox is in early development, and I'd genuinely like to hear from you.

The best first step is to **email Aaron Smith at [havatheschnauzer@gmail.com](mailto:havatheschnauzer@gmail.com)** — or open an issue if you prefer. Tell me what you're interested in — code, testing, design, domain knowledge about how dog owners and breeders actually manage records, or ideas for the [roadmap](ROADMAP.md) — and we'll figure out a good starting point together.

Dog experience is not required. If you *are* part of the dog fancy (shows, sports, breeding, health testing, multi-dog record keeping), that perspective is especially valuable.

## Technical areas we'd love help with

DogDoc Inbox is a local-first desktop app, so the work spans a few areas. **You don't need all of these — pick one that interests you, and there's room to learn the rest:**

- **TypeScript & React** — the application interface (most of the app)
- **Tauri desktop shell** — packaging the app for macOS and Windows (some Rust, but much of the surface is TypeScript)
- **SQLite** — local data storage and search
- **PDF processing & OCR** — pulling text out of documents and scans
- **Document extraction & review** — turning raw text into structured, source-linked facts
- **Local-first & desktop privacy** — keeping records on the owner's machine
- **Testing & document-processing quality** — making extraction trustworthy
- **Accessibility & clear interfaces** — health records people can actually read

Non-code contributions matter just as much: domain knowledge about veterinary records, design, documentation, and testing with real-world (redacted) documents.

## How we work: AI-assisted development

DogDoc Inbox is built with AI assistance — Claude is a working collaborator on the project. This is a big part of what makes it exciting: development that would traditionally take months or years can become a working prototype in a matter of weeks. Worth saying plainly, for two reasons:

- **Transparency** — it's how the project is actually developed.
- **So you don't feel you need to be an expert in everything.** You'll have a capable pair-programmer to help you ramp up on an unfamiliar part of the stack, explain what existing code does, and move faster. Strong in one area and rusty in another, or just curious and willing to learn? This project is set up for exactly that — bring your enthusiasm and the skills you have, and we'll lean on the tools for the rest.

## One rule that matters right now: privacy

Veterinary records can contain sensitive information. Please **do not** commit real records, home addresses, phone numbers, account numbers, microchip credentials, or other identifying details to this repository. Use synthetic or redacted fixtures for testing.

## License of contributions

By submitting a contribution, you agree that it will be licensed under the project's **Mozilla Public License 2.0 (MPL-2.0)**.
