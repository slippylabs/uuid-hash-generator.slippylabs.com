# UUID & Hash Generator

Generate v4 and time-sortable v7 UUIDs in bulk, and compute SHA-1, SHA-256, SHA-384 and SHA-512 digests of text or a file, all locally.

**Live:** <https://uuid-hash-generator.slippylabs.com/>

## What it does

- Bulk-generate UUIDs — v4 (fully random) or v7 (time-sortable).
- SHA-1, SHA-256, SHA-384 and SHA-512 digests of any text or file.
- Output as hex or Base64, copy the lot in one click.

## How it works

v7 UUIDs are assembled by hand from a millisecond timestamp plus `crypto.getRandomValues()` entropy, with the version and variant bits set per RFC 9562, so a sorted list of them is in creation order. Hashing goes through WebCrypto `subtle.digest`, and files are read locally — nothing is uploaded.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/uuid-hash-generator.slippylabs.com.git
cd uuid-hash-generator.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
