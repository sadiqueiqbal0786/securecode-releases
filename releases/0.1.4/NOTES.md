SecureCode Auditor 0.1.4 for Apple Silicon Macs. Four small things that make it quicker to start, and quicker to get unstuck.

- **Drag a project onto the window.** A folder becomes a folder audit, a ZIP becomes a ZIP audit, and anything else says so instead of doing nothing. Only the path is taken; the audit still reads everything inside the sealed container.
- **Audit something again in one tap.** The last few projects you audited are offered above the choices, named the way you would say them.
- **Errors that offer the fix.** A container app that is not running gets a **Start it** button; a scanner that has not been built gets **Set up the scanner**; a refused or oversized folder gets **Choose a folder**; a private repository points at the token. The scanner's own message is still shown underneath.
- **A clean result reads like one** — what was actually read (files, past versions, branches, pull requests), and a plain line that nothing matching was found, which is not the same as the code being proven safe.

**Install:** download `SecureCode-Auditor-0.1.4-apple-silicon.dmg`, drag the app to Applications, and follow *How to open* (one-time "Open Anyway" in Privacy & Security — the app is signed but not yet notarised).

**Needs:** Apple Silicon (M1 or later), macOS 13+, and Docker Desktop, OrbStack, Colima or Podman.

**SHA-256** `53d4f549c04944b003fdce2b6ca6ed5b400a8c97691c9c4077362af8f4193e59`
