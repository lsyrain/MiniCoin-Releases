# MiniCoin for macOS

Free personal-use Beta downloads and feedback. MiniCoin is a native, local-first household bookkeeping app for **macOS 26 or later**. The application is proprietary; this repository contains release material only, not its source code.

**Status: the first Beta candidate is being validated. No public installer has been released yet.** Draft releases are visible only to authorized repository maintainers. A published prerelease will appear on the [Releases page](https://github.com/lsyrain/MiniCoin-Releases/releases) after its downloaded installer has passed acceptance.

## Start with local bookkeeping

MiniCoin includes manual cash accounts and transactions, categories and budgets, Overview totals, transaction review, CSV export, app authentication, and encrypted backup/restore. In the setup guide, choose **Finish later**, then **Accounts → Add cash**. You can use local bookkeeping without AI, a Plaid account, or an internet connection.

AI and personal bring-your-own-Plaid connections are optional, experimental integrations. You supply your own model/service and eligible Plaid developer access. No AI subscription or bank-connection service is included. Availability for a particular model or bank is not guaranteed.

## Installation

The first Beta uses ad-hoc signing and is **not notarized by Apple**. After downloading and moving MiniCoin.app into Applications, try opening it once. If macOS blocks it because the developer cannot be verified, use **System Settings → Privacy & Security → Open Anyway** for MiniCoin and confirm. Managed Macs may prevent this exception. See [Apple's instructions](https://support.apple.com/en-us/102445).

Read [installation, updates, and recovery](BETA_INSTALLATION.md) before testing. The download will include the exact version, architecture list, and a SHA-256 checksum.

## Data and recovery

The ledger stays in local SQLite. App authentication protects access to the app; it does not encrypt the live database. AI/Plaid credentials and backup keys use macOS Keychain. A remote AI provider receives the fields disclosed during setup.

Keep a verified encrypted backup and this Mac's Keychain before upgrading. A backup file alone is insufficient for recovery. Beta updates are manual, and database migrations can make a simple app downgrade unsafe.

## License and feedback

Official Beta binaries are free for personal and household use under [BETA_LICENSE.txt](BETA_LICENSE.txt). The source remains proprietary. Third-party software retains the licenses in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

Use [Issues](https://github.com/lsyrain/MiniCoin-Releases/issues) for non-sensitive bug reports. Include app/macOS versions and reproduction steps. Do not attach financial records, databases, backups, credentials, keys, or account numbers. For a security concern, request a private contact route without posting the vulnerability details.
