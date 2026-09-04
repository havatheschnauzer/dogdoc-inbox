# Security Policy

DogDoc Inbox is intended to handle local veterinary records, so privacy and file-handling issues are treated as security concerns.

## Reporting a vulnerability

Please do not publish an exploitable security issue, sensitive test document, or privacy-impacting vulnerability in a public issue.

Once the GitHub repository is live, use the repository's **GitHub Private Vulnerability Reporting / Security Advisory** feature when available.

Examples of issues that should be reported privately include:

- A path traversal or arbitrary file-write vulnerability
- A document that causes code execution or unsafe command invocation
- Leakage of local document contents
- Unexpected network transmission of record data
- Exposure of local database contents
- Insecure handling of temporary files
- A bypass of user review that could cause unapproved extracted facts to be treated as authoritative

General bugs that do not expose sensitive information can be reported through normal GitHub issues.
