# SecureCode Auditor — downloads

Installers for **SecureCode Auditor**, a Mac app that finds malware hidden in code — in every
file, every past version, and every branch and pull request of a Git repository — and helps
you remove it. Code is only ever read inside a sealed container; nothing from a project runs
on your Mac, and nothing you audit leaves it.

Learn more: **https://comp-sci-tech.web.app/securecode-auditor.html**

This repository holds release files only. The source code is not published.

## Download

Get the latest `.dmg` from **[Releases](https://github.com/sadiqueiqbal0786/securecode-releases/releases/latest)**.

**Needs:** a Mac with Apple Silicon (M1 or later) running macOS 13 or later, and a container
app — Docker Desktop, OrbStack, Colima or Podman. The app's first-run guide helps with that.

## Opening it the first time

The app is signed but not yet notarised by Apple, so macOS asks once:

1. Drag **SecureCode Auditor** onto **Applications**, then open it. macOS says it cannot verify
   the app — click **Done**.
2. Open **System Settings → Privacy & Security**, find *"SecureCode Auditor was blocked"* and
   click **Open Anyway**, then confirm with your password.

After that it opens like any other app. (Terminal alternative:
`xattr -dr com.apple.quarantine "/Applications/SecureCode Auditor.app"`.)

## Check your download

Each release lists the file's SHA-256. Compare it with:

```bash
shasum -a 256 ~/Downloads/SecureCode-Auditor-*.dmg
```

## Support

Questions, problems or an incident you need help with: **sadiqueiqbal.si@gmail.com**.
In the app, *Settings → About & your data → Export diagnostics* creates a file you can attach —
you see everything in it first, and it never contains your code, file names or repository addresses.

© 2026 Comp-sci-tech · Sadique Iqbal. See the privacy policy and terms of use in the app.
