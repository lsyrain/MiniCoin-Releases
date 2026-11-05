# MiniCoin Beta: installation and recovery

MiniCoin is a free proprietary Beta for personal household bookkeeping on macOS 26 or later. The source code is private. The download includes the Beta binary license and third-party notices. AI and bank connections are optional; no AI subscription or Plaid access is included.

## Install the direct-download Beta

1. Download the official Beta archive and open it. Keep the included license, notices, and release notes. The release manifest identifies the version and supported architectures.
2. Quit any older MiniCoin app. Move **MiniCoin.app** to **Applications**, then open it there.
3. This initial Beta is locally signed and **not notarized by Apple**. macOS may prevent the first launch because it cannot verify the developer. After attempting to open MiniCoin once, open **System Settings → Privacy & Security**, find the blocked MiniCoin app in the Security section, choose **Open Anyway**, and confirm the system prompt for this app.
4. If **Open Anyway** is unavailable on an organization-managed Mac, contact its administrator. MiniCoin cannot override management policy. Do not disable macOS security protections globally. If macOS reports malware or a damaged download, stop and obtain a verified copy rather than treating that as the expected developer-verification prompt.
5. Unlock MiniCoin using the native system dialog. Touch ID is available on supported setups; the Mac login password is the fallback. MiniCoin never asks you to enter that password into its own interface.

## Start without AI or a bank connection

1. In the first-run guide, choose **Finish later**.
2. Open **Accounts → Add cash** and create a manually maintained account.
3. Add a transaction, choose its type/category, then review the totals in Overview or Categories.

A fresh ledger contains default categories, no sample accounts, and no sample transactions. Local edits persist on this Mac and bookkeeping works offline. The postponed guide returns at the next launch; you can choose **Finish later** again. Its full setup path currently finishes only after a personal Production Plaid account has synchronized successfully.

AI can be configured later in Settings. Local LM Studio or another compatible service requires your own model and setup; a remote service receives the transaction fields described before connection. Plaid is a personal bring-your-own-account integration: you supply credentials for your own Plaid team and its eligible access. Ordinary local bookkeeping requires neither integration.

## Updates and recovery

Beta updates are manual; there is no automatic updater.

1. Before installing a new version, unlock the current app and choose **File → Create Encrypted Backup**. Keep the backup and the previous app version. Verify recovery using a separate disposable ledger with the matching Keychain key; restoring into your working ledger replaces its contents.
2. Preserve this Mac's Keychain. The encrypted backup file does not include its decryption key, so the file alone cannot restore your data on another Mac or after losing the Keychain. Plaid credentials/tokens and AI credentials are separate from the ledger backup and may require reconfiguration.
3. Quit MiniCoin, replace only **MiniCoin.app** in Applications, then launch the new version. Do not delete Application Support data or Keychain entries as part of an update.
4. If macOS asks for Keychain access after the app changes, confirm that the request belongs to the official MiniCoin app you installed. Keep the existing entries. If access fails, retain the backup and previous app before attempting recovery.
5. Check that existing accounts, transactions, tags, categories, and budgets remain present. Verify a backup created by the previous build can still be decrypted with the retained key, and test any configured optional integrations.

The live ledger is stored at `~/Library/Application Support/MiniCoin/minicoin-native.sqlite`. App authentication does not encrypt that live SQLite database.

If MiniCoin cannot read the saved backup key, or the stored key is invalid, it stops the backup operation and retains the key. Restoring with a missing key also stops; it does not create a substitute. Preserve the backup and Keychain, resolve the system access problem, then retry. A failed key-creation attempt must not replace an existing key.

An older app may not support a database migrated by a newer version. **Replacing the app with an older binary is not a safe database rollback.** Roll back only to an app and pre-upgrade backup known to work together, with the required Keychain key retained. Keep the newer ledger intact until recovery is verified. If the release notes do not establish compatibility, request recovery guidance before opening that ledger in the older app.

## Report a problem

Official downloads and release notes are published at [MiniCoin-Releases](https://github.com/lsyrain/MiniCoin-Releases/releases). Use that repository's [Issues](https://github.com/lsyrain/MiniCoin-Releases/issues) for non-sensitive feedback. Include the MiniCoin version, macOS version, steps, and what you expected. Exclude credentials, tokens, keys, account numbers, financial records, databases, and backups. For a security concern, open only a non-sensitive request for a private contact route; do not publish vulnerability details or private data.
