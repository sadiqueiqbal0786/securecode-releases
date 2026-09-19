First public beta of SecureCode Auditor for Apple Silicon Macs.

**What it does**
- Audits a folder, a ZIP or a repository online — every branch, tag, pull request and past version.
- Reads code only inside a sealed container: no network, read-only, no permissions. Nothing runs on your Mac.
- Plain-language verdict with what to do; the technical detail is one click away.
- Clean-up built in: removes leftovers from a local copy (backing up your own work first) and can rebuild a repository's history as one clean commit, with GitHub checks and the message for GitHub Support.
- Signed known-malware fingerprint updates, checked daily; offline first-run setup.
- Optional second opinion from an AI you connect (a model on your Mac or your own key).

**Install:** download `SecureCode-Auditor-0.1.0-apple-silicon.dmg`, drag the app to Applications, and follow *How to open* (one-time "Open Anyway" in Privacy & Security — the app is signed but not yet notarised).

**Needs:** Apple Silicon (M1 or later), macOS 13+, and Docker Desktop, OrbStack, Colima or Podman.

**SHA-256** `f3aef69f76ce8d256204c7d86e98b9205453d766eedfdf9a65bfd161149b66a1`
