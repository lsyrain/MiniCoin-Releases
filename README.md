# MiniCoin

MiniCoin **1.0.0 Beta 3** is a free, proprietary, local-first bookkeeping app for personal and household use on **macOS 26 or later**. The application source stays private; this repository hosts release material and feedback.

**[Download Beta 3](https://github.com/lsyrain/MiniCoin-Releases/releases/download/v1.0.0-beta.3/MiniCoin-1.0.0-beta.3-universal-ad-hoc.zip)** · [Release notes and validation scope](https://github.com/lsyrain/MiniCoin-Releases/releases/tag/v1.0.0-beta.3) · [SHA-256 checksum](https://github.com/lsyrain/MiniCoin-Releases/releases/download/v1.0.0-beta.3/SHA256SUMS)

## Install and start

1. Download and unzip the archive. Quit any older MiniCoin app, then move **MiniCoin.app** to **Applications** and open it there.
2. This Beta is ad-hoc signed and **not notarized by Apple**. If macOS blocks the first launch because it cannot verify the developer, attempt to open the app once, then choose **System Settings → Privacy & Security → Open Anyway** for MiniCoin and confirm the system prompt. Managed Macs may restrict this option; do not disable security protections globally.
3. Unlock through the native Mac authentication dialog. In the setup guide, choose **Finish later**, then open **Accounts → Add cash** to start manual bookkeeping without AI or a bank connection.

The download includes Apple silicon and Intel binaries. See the release notes for the tested configurations and current limitations.

AI and personal BYO-Plaid bank connections are optional, experimental integrations. Configure your own model/service or eligible Plaid developer account if you choose to use them; no subscription or Plaid access is included.

## Updates and recovery

Updates are installed manually. Before upgrading, create and verify an encrypted backup and retain the matching Keychain key. A backup file alone is insufficient for recovery on another Mac. An older app may not support a migrated database, so replacing the app alone is not a safe rollback.

Read the [installation and recovery guide](BETA_INSTALLATION.md), [free personal-use Beta license](BETA_LICENSE.txt), and [third-party notices](THIRD_PARTY_NOTICES.md).

## Feedback

Report non-sensitive problems through [Issues](https://github.com/lsyrain/MiniCoin-Releases/issues), including your app/macOS version and steps to reproduce. Keep financial records, credentials, tokens, keys, databases, and backups out of public reports.
