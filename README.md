# SeedCrypt — Releases

Official binaries for **SeedCrypt**, an offline seed phrase manager.
AES-256-GCM, PBKDF2-SHA512 with 600,000 iterations, no account, no cloud.

**[→ Download the latest version](https://github.com/femto7/SeedCrypt-Releases/releases/latest)**
· [seedcrypt.app](https://seedcrypt.app)

---

## About the "Source code" archives

Every GitHub release automatically gets a `Source code (zip)` and
`Source code (tar.gz)` attachment. GitHub generates these and they cannot be
removed.

**They contain this README and nothing else.** This repository exists purely to
host release binaries — there is no application code in it.

SeedCrypt itself is closed source. If auditability matters to you, and it
should for anything holding a seed phrase, the part that actually matters *is*
open:

### [SeedCrypt Recover](https://github.com/femto7/seedcrypt-recover) — MIT licensed

A standalone BIP-39 recovery tool written in Rust. It reads SeedCrypt packets
without SeedCrypt, so **you are never dependent on this project, or on us, to
get your seed back**. Read it, audit it, build it yourself.

That is the guarantee worth having: not that you trust the encryption tool, but
that you can walk away from it and still recover your funds.

---

## Verifying what you downloaded

The binaries are **not code-signed**. Windows SmartScreen and macOS Gatekeeper
will warn you on first launch. That is expected, and it is exactly why every
release publishes SHA-256 checksums — a hash you can verify yourself is worth
more than a signature you have to take on faith.

Each release includes a `SHA256SUMS.txt`. Compare it against your download:

**Windows** (PowerShell)

```powershell
Get-FileHash .\SeedCrypt-Setup.exe -Algorithm SHA256
```

**macOS / Linux**

```bash
shasum -a 256 SeedCrypt-macos.dmg
```

If the hash does not match the one published in the release notes, do not run
the file.

---

## Stable download links

Release assets use stable filenames, so these URLs always resolve to the most
recent version and never break:

| Platform | Link |
|---|---|
| Windows | [`SeedCrypt-Setup.exe`](https://github.com/femto7/SeedCrypt-Releases/releases/latest/download/SeedCrypt-Setup.exe) |
| Android | [`seedcrypt.apk`](https://github.com/femto7/SeedCrypt-Releases/releases/latest/download/seedcrypt.apk) |
| macOS | [`SeedCrypt-macos.dmg`](https://github.com/femto7/SeedCrypt-Releases/releases/latest/download/SeedCrypt-macos.dmg) |
| Linux | [`SeedCrypt-linux-x64.tar.gz`](https://github.com/femto7/SeedCrypt-Releases/releases/latest/download/SeedCrypt-linux-x64.tar.gz) |

---

## Support

Bug reports and questions: **support@seedcrypt.app**
