# tg

`tg` is the agent of [tiefgang.sh](https://tiefgang.sh): it turns a
machine you own into a runner for your CI jobs. This repository is its
**release log**: every release of `tg` is published here, with its
tarballs, checksums and signature bundles. It holds no source — the
source lives in a private repository — and nobody commits to it; a
release workflow writes it.

## Releases

- A release marked **pre-release** is an **alpha**: cut automatically
  and often. A release without the mark is **stable**: the same build,
  promoted after it has proven itself.
- Releases are immutable: assets and tags are locked at publication.
  A version number is never reused.
- Every asset is signed with the release key. Verify a download with
  [cosign](https://github.com/sigstore/cosign) against the published
  public key:

      cosign verify-blob --key tg-release.pub --bundle <file>.bundle <file>

## Installing

How to install `tg` — the one-line installer, the Homebrew tap and the
service it runs as — is documented at <https://tiefgang.sh>.
