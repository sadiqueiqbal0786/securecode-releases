SecureCode Auditor 0.1.6 for Apple Silicon Macs. **Cleaning a repository no longer costs you its history.**

Until now there was one way to clean an infected branch: replace it with a single clean commit. That removes the malware and everything else with it — every message, every author, every date, the whole record of how the project got there.

**The clean-up is now scoped by default.** Only the commits that actually carry the malware are rebuilt, with the infected file restored or removed. Every other commit keeps its author, its dates and its message exactly. Commits before the first infection keep their original ids; later ones change id only because an ancestor did, which Git cannot avoid.

It proves this rather than promising it. Before a push is offered, five checks run against the original branch:

- every commit is still there
- author, dates and message unchanged on every commit
- no malicious object is reachable from the rebuilt branch
- each rewritten commit changed only the files you decided about
- how much history was kept, stated plainly ("101 of 128 commits keep their id; 1 carried the malware and was rebuilt")

The old behaviour is still available as a deliberate choice — *Replace the branch with one clean commit* — for when the history itself cannot be trusted. The screen says what each option costs before you pick one, and changing your mind discards any plan built for the other.

**Still true of both:** ids change from the infection point onward, so everyone with a copy must re-clone, and pull-request refs can only be cleared by GitHub Support.

**Install:** download `SecureCode-Auditor-0.1.6-apple-silicon.dmg`, drag the app to Applications, and follow *How to open* (one-time "Open Anyway" in Privacy & Security — signed, not yet notarised).

**Needs:** Apple Silicon (M1 or later), macOS 13+, and Docker Desktop, OrbStack, Colima or Podman.

**SHA-256** `3e94a931402ed9495c91eec31ae195ea6b1b738fe958ffde101ad8f6a4f62d1a`
