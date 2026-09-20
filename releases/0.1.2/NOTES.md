SecureCode Auditor 0.1.2 for Apple Silicon Macs. This one is about making the app easier to use.

**New**
- **Try a sample project** — one button on the start screen audits a small demonstration project, for real, in the sealed scanner. No repository of your own needed to see what an audit looks like. It is clearly marked as a demonstration, and contains no real malware.
- **The verdict now tells you what to do** — "Clean this up", "Save a report" and "Audit again" sit right under it, instead of behind Technical details.
- **Findings in plain words** — every finding is titled in ordinary English ("A file has hidden code pushed far off-screen"), with the rule name kept beside it for searching.
- **Stop** — a long audit can be stopped. The sealed container is ended, and nothing is left running.
- **Recent audits** — the last 20 results are kept on your Mac, so closing the window no longer loses them. Each can be reopened or deleted, all can be deleted at once, and Settings can switch the keeping off entirely (which deletes the saved ones too). They never leave your computer.
- A notification when a long audit finishes while the app is in the background. It carries the verdict only — no repository, path, file name or finding.

**Unchanged:** what the scanner finds, and how it reads code — only inside a sealed container, with nothing from your project ever run on your Mac.

**Install:** download `SecureCode-Auditor-0.1.2-apple-silicon.dmg`, drag the app to Applications, and follow *How to open* (one-time "Open Anyway" in Privacy & Security — the app is signed but not yet notarised).

**Needs:** Apple Silicon (M1 or later), macOS 13+, and Docker Desktop, OrbStack, Colima or Podman.

**SHA-256** `d491a5c0a690d5ef32dbe284b50b6af2d1eb074111b68af1cbedb30b2f0ef893`
