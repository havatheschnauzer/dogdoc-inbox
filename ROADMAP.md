# DogDoc Inbox — Roadmap

This roadmap is early and will change as the project takes shape. It exists to make the priorities visible, not to promise dates. Ideas and feedback are welcome — [email me at havatheschnauzer@gmail.com](mailto:havatheschnauzer@gmail.com).

## The first priority

**Import a dog and aggregate all of its records into one health history.**

This is the thing that matters most to real owners: veterinary records live in too many places — portals, PDFs, lab reports, certificates, scans, photos, downloads — and no single view of a dog's history exists. The first job of DogDoc Inbox is to point it at a dog's records, pull them together, and make them usable, while keeping the original documents intact.

Everything else is secondary until this works well for a single dog.

## Now

- Point DogDoc Inbox at a folder (or folders) of one dog's records and import them.
- Aggregate mixed formats — PDFs, images/scans, portal exports, downloaded files — into one place per dog.
- Preserve the original files exactly as provided; never replace a record with a summary.
- Basic organization and search across the imported documents.

## Next

- Extract key health events and data (vaccinations, tests, weight) with the original document always linked as the source.
- Human review of extracted information before it becomes part of the health history.
- Longitudinal tracking where the data is genuinely meaningful (e.g. weight over time).

## Later

- Concise, source-linked reports for veterinarians, breeders, co-owners, and puppy owners.
- Managing records for multiple dogs.
- Windows support (first desktop build targets macOS).

## Principles that constrain the roadmap

Whatever gets built stays inside the product principles in the [README](README.md#product-principles): local-first, originals preserved, facts traceable to their source, uncertainty shown rather than hidden, and trends only when the data supports them.
