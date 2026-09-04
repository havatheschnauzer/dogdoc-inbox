# Contributing to DogDoc Inbox

Thank you for your interest in DogDoc Inbox.

The project is in early development, so contributions can include code, architecture discussion, testing, documentation, accessibility feedback, and domain knowledge about how dog owners, breeders, and veterinary professionals actually use records.

## Before starting a large change

For anything substantial, please open an issue first. This helps avoid duplicate work and makes it possible to agree on scope before a large implementation is written.

Small bug fixes, documentation improvements, and focused tests can generally go directly to a pull request.

## Areas where help is especially useful

- Tauri and Rust desktop application development
- React and TypeScript UI work
- PDF parsing, rendering, and page-level navigation
- OCR and document extraction
- SQLite data modeling and full-text search
- File watching, hashing, and duplicate detection
- Extraction confidence and review workflows
- Report and export generation
- macOS and Windows packaging
- Automated testing and extraction regression tests
- Accessibility and interaction design

Domain contributors are welcome too. If you participate in the dog fancy, breeding, dog sports, health testing, or veterinary-record management, your experience can help identify workflows that software engineers might otherwise miss.

## Privacy rules for contributions

Veterinary documents may contain sensitive information. Please follow these rules when opening issues, pull requests, or adding fixtures:

1. Do not commit private veterinary records from real owners without explicit permission.
2. Do not include home addresses, phone numbers, email addresses, account numbers, microchip registration credentials, or other unnecessary identifying information.
3. Prefer synthetic fixtures created specifically for testing.
4. If a real document is essential for reproducing a parser issue, redact it before sharing and confirm that you have the right to provide it.
5. Never place private test records in the Git repository simply because the repository itself is currently small or lightly used.

## Product principles to preserve

Changes should generally reinforce these principles:

- Local-first processing
- Original documents remain unchanged
- Extracted facts remain traceable to their source
- Uncertainty is shown rather than hidden
- Users can review and correct extracted information
- Record organization is kept separate from diagnosis or treatment advice
- Charts and trends are used only when the underlying data supports them

If a proposed change intentionally alters one of these principles, discuss it in an issue before implementation.

## Pull requests

A good pull request should:

- Have a focused purpose.
- Explain the user or engineering problem being solved.
- Include tests when the change affects parsing, extraction, persistence, or reconciliation.
- Avoid unrelated formatting or refactoring changes.
- Note any macOS- or Windows-specific behavior.
- Avoid introducing cloud dependencies for core functionality without prior discussion.

## Testing document extraction

Document-processing changes should eventually be evaluated against a repeatable fixture set with expected structured outputs. When adding a new parser or extraction rule, please include an appropriate synthetic or distributable fixture whenever possible.

## Development setup

The development environment is still being established. Setup instructions will be added once the initial Tauri application scaffold and local processing pipeline are committed.

## License of contributions

By submitting a contribution to this repository, you agree that your contribution will be licensed under the same **Mozilla Public License 2.0** that applies to the project.
