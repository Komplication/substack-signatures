# Substack Article Signatures

This repository contains cryptographically signed copies of my Substack articles.

Each article is clear-signed using GPG and committed to a public, append-only Git history. The associated public key and fingerprint are published to allow independent verification of authorship, integrity, and approximate publication time.

Articles are never edited in place. Corrections are issued as new signed artifacts, preserving a transparent editorial history.


## Repository Structure
```
substack-signatures/
  README.md
  pubkey/
    michael_pubkey.asc
  articles/
    YYYY-MM-DD-title.md.asc
```

## Public Key

The public key used to sign all articles is located at:

pubkey/michael_pubkey.asc

Key identity:
Name: Michael J. Miller
Email: michael.miller.ee.com

Fingerprint:
```
0094 F7F4 B8A9 7859 B001  6035 D37A 8544 EC1E 765B
```

## Verification Instructions

1. Import the public key

Command:
gpg --import michael_j_miller_pubkey.asc


2. Verify an article signature

Command:
```
gpg --verify YYYY-MM-DD-title.md.asc
```

Expected output:
Good signature from "Michael <michael.miller.ee@gmail.com>"


## Revisions and Corrections

Published articles are never modified or removed.

If a correction or clarification is required, a new signed version is added with an incremented revision suffix. All prior versions remain available for comparison.


## Notes

- A GPG signature proves control of the signing key, not originality of ideas.
- Integrity is anchored by both the signature and the Git commit history.
- Clear-signed files are used to preserve human readability.
- This repository is independent of Substack and resilient to platform changes.


## License

Copyright retained by the author.
Redistribution permitted only with attribution and without modification of signed content.
