SecureCode Auditor 0.1.1 for Apple Silicon Macs. It replaces 0.1.0, which has been withdrawn — if you installed 0.1.0, please install this version over it.

**What changed**
- The scanner engine now ships as compiled native code, and the sealed scanner's copy is built into its container image. Audit results are identical to 0.1.0.
- If an update brings a new scanner, the app replaces the sealed scanner image by itself, offline.

**What it does**
- Audits a folder, a ZIP or a repository online — every branch, tag, pull request and past version.
- Reads code only inside a sealed container: no network, read-only, no permissions. Nothing runs on your Mac.
- Plain-language verdict with what to do; the technical detail is one click away.
- Clean-up built in: removes leftovers from a local copy (backing up your own work first) and can rebuild a repository's history as one clean commit, with GitHub checks and the message for GitHub Support.
- Signed known-malware fingerprint updates, checked daily; offline first-run setup.

**Install:** download `SecureCode-Auditor-0.1.1-apple-silicon.dmg`, drag the app to Applications, and follow *How to open* (one-time "Open Anyway" in Privacy & Security — the app is signed but not yet notarised).

**Needs:** Apple Silicon (M1 or later), macOS 13+, and Docker Desktop, OrbStack, Colima or Podman.

**SHA-256** `176e6ae3f2872f625a918c8c84fd299ea4f85fdfb655a9fa6c6f8805bf408d1d`
