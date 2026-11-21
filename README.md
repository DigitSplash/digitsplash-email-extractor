# Digitsplash Email Extractor

**DigitSplash** · [product.digitsplash.com](https://product.digitsplash.com) · [digitsplash@outlook.com](mailto:digitsplash@outlook.com)

Find business emails, phone numbers and social profiles from a list of domains - locally, on your own computer.

Import a list of domains or company websites; the app visits each site with a
hybrid HTTP + browser engine and extracts the contact details it can find
(public email addresses, phone numbers, social profiles). Results are stored in
a local database and exported to CSV / XLSX.

Everything runs on your machine. There is no telemetry, no cloud account for
your data, and the only outbound calls are the websites you asked it to visit
and the license check.

> This repository is the public home for the **download, installation, activation
> and troubleshooting** documentation of Digitsplash Email Extractor. The application itself is
> distributed as a ready-to-use package from **https://product.digitsplash.com**;
> its source code is not published.

---

## Download

Get the newest build from **https://product.digitsplash.com**. Every file's
SHA-256 is shown on the download page, so you can verify what you got.

| Platform | File | Notes |
| --- | --- | --- |
| Windows 10 / 11 (64-bit) | `email-extractor-setup-win.exe` | Installer, per-user, no admin rights needed |
| macOS 11+ (Intel or Apple Silicon) | `email-extractor-mac.dmg` | Universal build - the same file runs on both |
| Linux (64-bit, glibc) | `email-extractor-linux.AppImage` | No installation - make it executable and run |
| Debian / Ubuntu | `email-extractor-linux.deb` | Installs into the system menu |

---

## Install from the terminal

Prefer the command line? Install the newest build with one command.

**Windows (PowerShell):**

```powershell
irm https://product.digitsplash.com/install/digitsplash-email-extractor.ps1 | iex
```

**Linux / macOS:**

```sh
curl -fsSL https://product.digitsplash.com/install/digitsplash-email-extractor.sh | sh
```

The command downloads the newest official build from
**https://product.digitsplash.com** and installs it. When it finishes, open the
app and **activate it with your license key** - the app is not usable without a
valid key.

---

## Install (short version)

1. Download `email-extractor-setup-win.exe` from the store.
2. Double-click it. Windows may show **"Windows protected your PC"** (SmartScreen)
   because our installers are not code-signed yet.
3. Click **More info** -> **Run anyway**.
4. The installer is per-user, so it does not ask for an administrator password.
   It finishes by launching the app.

The full guide - macOS, Linux, activation, updates, uninstall and a
troubleshooting table - is in **[INSTALL.md](INSTALL.md)**.

---

## Activate

Digitsplash Email Extractor runs on a paid license key.

1. Start the app (or open the extension's side panel).
2. Sign in with your DigitSplash account, or press **Continue with Google** -
   the sign-in finishes in your browser and comes back to the app.
3. Paste the key from your purchase email (DGS-XXXX-XXXX-XXXX-XXXX) and press
   **Activate**.
4. The key is bound to that computer (or browser profile). Release it before
   moving the license to another machine.

---

## Requirements

- Windows 10/11 (64-bit), macOS 11 or newer, or a 64-bit Linux with glibc 2.28+.
- 4 GB RAM (8 GB recommended for large batches), 500 MB free disk space.
- An internet connection (for the sites being scanned and for activation).

---

## Support

- **Email:** digitsplash@outlook.com - include your operating system, the app
  version and the exact error text.
- **Bug reports:** open an issue in this repository. Please do not paste license
  keys, customer lists or other private data into a public issue.
- **Security problems:** see [SECURITY.md](SECURITY.md) - report them privately.

---

## License

Digitsplash Email Extractor is proprietary software. This repository's documentation may be read,
linked and shared as-is. Copying, redistributing, reselling or reverse-
engineering the application, or bypassing its activation, is not permitted. See
[LICENSE](LICENSE) for the full notice.

© 2026 DigitSplash. All rights reserved.
