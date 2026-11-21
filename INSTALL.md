# Installing Digitsplash Email Extractor

**DigitSplash** · [product.digitsplash.com](https://product.digitsplash.com) · [digitsplash@outlook.com](mailto:digitsplash@outlook.com)

Last reviewed: 2026-11-21

---

## 1. What you need

- Windows 10/11 (64-bit), macOS 11 or newer, or a 64-bit Linux with glibc 2.28+.
- 4 GB RAM (8 GB recommended for large batches), 500 MB free disk space.
- An internet connection (for the sites being scanned and for activation).

---

## 2. Download

1. Open **https://product.digitsplash.com** and sign in (or create an account).
2. Buy a license key if you do not have one yet - it arrives by email.
3. Download the file for your operating system:

| Platform | File |
| --- | --- |
| Windows 10 / 11 (64-bit) | `email-extractor-setup-win.exe` |
| macOS 11+ (Intel or Apple Silicon) | `email-extractor-mac.dmg` |
| Linux (64-bit, glibc) | `email-extractor-linux.AppImage` |
| Debian / Ubuntu | `email-extractor-linux.deb` |


4. Optional but recommended: on the same page download SHA256SUMS.txt and
   check the file you downloaded.

**Windows (PowerShell):**

```powershell
Get-FileHash .\email-extractor-setup-win.exe -Algorithm SHA256
```

**macOS / Linux:**

```bash
shasum -a 256 <file-name>
```

The printed hash must match the line for that file in SHA256SUMS.txt.

**Or install with one command** (downloads from product.digitsplash.com):

Windows (PowerShell):

```powershell
irm https://product.digitsplash.com/install/digitsplash-email-extractor.ps1 | iex
```

Linux / macOS:

```sh
curl -fsSL https://product.digitsplash.com/install/digitsplash-email-extractor.sh | sh
```

Then open the app and activate it with your license key.

---

## 3. Install

### Windows 10 / 11 (64-bit)

1. Download `email-extractor-setup-win.exe` from the store.
2. Double-click it. Windows may show **"Windows protected your PC"** (SmartScreen)
   because our installers are not code-signed yet.
3. Click **More info** -> **Run anyway**.
4. The installer is per-user, so it does not ask for an administrator password.
   It finishes by launching the app.

### macOS 11+ (Intel and Apple Silicon)

1. Download `email-extractor-mac.dmg` and open it.
2. Drag **Digitsplash Email Extractor** into the **Applications** folder.
3. Open **Applications**, then **right-click (or Control-click) the app -> Open**,
   and confirm **Open** in the dialog.
   (Double-clicking the first time is blocked by macOS because the build is not
   notarized; right-click -> Open is the allowed way through.)
4. From then on the app opens normally.

### Linux (64-bit)

**AppImage**

```bash
chmod +x email-extractor-linux.AppImage
./email-extractor-linux.AppImage
```

If it refuses to start with a FUSE error, either install `libfuse2`
(`sudo apt install libfuse2`) or run it with
`./email-extractor-linux.AppImage --appimage-extract-and-run`.

**Debian / Ubuntu**

```bash
sudo apt install ./email-extractor-linux.deb
```

Then start it from the application menu (or run `digitsplash-email-extractor`).

---

## 4. First run and activation

1. Launch the app (or open the extension's side panel).
2. The license screen appears. Either
   - sign in with your DigitSplash account email and password, or
   - press **Continue with Google** - your normal browser opens, you finish the
     sign-in there, and the app receives the result automatically.
3. Paste the key from your purchase email in the form
   DGS-XXXX-XXXX-XXXX-XXXX and press **Activate**.
4. You are done - the key stays bound to this computer (or browser profile).

**Moving the license to another machine:** open the app's license screen, press
**Release this computer**, then activate the same key on the new machine. If the
old machine is gone, release the key from your account page on the website.

---

## 5. Updating

- Install the newer file from the download page over the old one; your data and
  your activation are kept.
- **macOS:** quit the app, drag the new copy into **Applications**, choose
  **Replace**.
- **Linux:** replace the AppImage file, or sudo apt install ./<new>.deb.
- **Extension:** unzip the new package into the *same* folder you loaded
  originally, then press the reload arrow on chrome://extensions. Do not delete
  the folder - the browser loads the extension from it.

---

## 6. Uninstalling

| Platform | Steps |
| --- | --- |
| Windows | **Settings -> Apps -> Installed apps -> Digitsplash Email Extractor -> Uninstall**. |
| macOS | Quit the app, drag it from **Applications** to the Trash, then empty the Trash. |
| Linux (AppImage) | Delete the AppImage file. |
| Linux (deb) | sudo apt remove <package-name> |
| Extension | chrome://extensions -> **Remove**. |

Your local data lives in the OS user-data folder (Windows:
%APPDATA%, macOS: ~/Library/Application Support, Linux: ~/.config).
Uninstalling usually keeps it; delete the app's folder there if you want a clean
slate. **Release the license first** if you plan to use the key elsewhere.

---

## 7. Troubleshooting

| Symptom | Fix |
| --- | --- |
| "Windows protected your PC" / SmartScreen | Expected: the installer is not code-signed. Click **More info -> Run anyway**. If the button is missing, right-click the .exe -> **Properties** -> tick **Unblock** -> OK. |
| macOS says the app "is damaged" or "cannot be opened" | Right-click the app -> **Open** -> **Open** (do not double-click). If macOS still blocks it, open **System Settings -> Privacy & Security** and click **Open Anyway**. |
| Linux: "AppImage requires FUSE" | Install `libfuse2`, or run the AppImage with `--appimage-extract-and-run`. |
| Antivirus quarantines the installer | Unsigned installers from small vendors often trigger heuristics. Restore the file and add an exclusion for the installer folder. The SHA-256 of every file is published in `SHA256SUMS.txt` on the download page, so you can confirm the file was not altered. |
| The app starts but says it cannot reach the license server | Check your firewall/proxy. The app needs HTTPS to `product.digitsplash.com/api`. Corporate proxies that break TLS interception will also break activation. |

---

## 8. সংক্ষেপে (বাংলা)

1. **https://product.digitsplash.com** থেকে নিজের OS-এর ফাইলটা নামান
   (Windows: `setup-win.exe`, Mac: `.dmg`, Linux: `.AppImage` বা `.deb`)।
2. **Windows:** ফাইলে ডাবল-ক্লিক → "Windows protected your PC" এলে **More info →
   Run anyway**। **Mac:** `.dmg` খুলে অ্যাপটা **Applications**-এ ড্র্যাগ করুন, তারপর প্রথমবার অ্যাপে **right-click → Open**।
3. অ্যাপ খুললে **Continue with Google** চাপুন বা ইমেইল-পাসওয়ার্ড দিয়ে সাইন ইন করুন।
4. কেনা ইমেইলে পাওয়া কী (DGS-XXXX-XXXX-XXXX-XXXX) পেস্ট করে **Activate** চাপুন।
5. অন্য কম্পিউটারে নিতে চাইলে আগের কম্পিউটার থেকে **Release this computer** করুন।
6. সমস্যা হলে: digitsplash@outlook.com — OS, ভার্সন আর এরর মেসেজ লিখে পাঠান।

---

## 9. Getting help

- **Email:** digitsplash@outlook.com
- **Issues:** open an issue in this repository (no license keys, no private data).
- **Security:** [SECURITY.md](SECURITY.md)

© 2026 DigitSplash. All rights reserved. See [LICENSE](LICENSE).
