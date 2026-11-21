# Security policy

## Reporting a vulnerability

Please **do not** open a public issue for a security problem. Email
**digitsplash@outlook.com** with `SECURITY` in the subject line and include:

- the version you are running (shown in the app's About panel or the installer
  file name),
- your operating system (or browser and version, for the extension),
- the steps to reproduce,
- what you expected versus what happened.

We aim to acknowledge within 3 business days and to ship a fix or a mitigation
plan within 30 days for anything exploitable.

## In scope

- The published installers and the extension package.
- Launcher / auto-update behaviour, file permissions, local data storage.
- License and activation weaknesses: running the app without a valid key,
  reusing one key on several machines, or faking a device.

## Out of scope

- The published builds are **not code-signed**. Windows SmartScreen and macOS
  Gatekeeper warnings are expected and documented — they are not
  vulnerabilities.
- Issues that require an attacker to already have administrator rights or
  physical access to the machine.
- Vulnerabilities in third-party dependencies that are already fixed upstream
  (a heads-up is still welcome).

## Credits

With your permission we credit reporters in the release notes.
