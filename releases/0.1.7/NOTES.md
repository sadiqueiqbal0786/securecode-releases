> **Superseded by 0.1.8.** This build reports its own version as 0.1.6, so it announces an update to itself and keeps offering one. Everything else in it behaves as described below. Please install 0.1.8 instead.

SecureCode Auditor 0.1.7 for Apple Silicon Macs. **A clean branch is not a clean project — the app now says what is left to do.**

Three rules also stopped judging code by what it is called.

### After the push, the part no tool can do for you

Cleaning a branch on the server is the middle of the job, not the end. The app now says so in plain words, on the screen, as soon as the push has gone through:

- **Every existing copy has to be deleted and cloned again.** A pull does not fix one. It still holds the old commits, and pushing from it puts the malware back. The two commands are there to copy.
- **Which other branches or tags still carry something.** One clean-up covers one branch — the lease, the safety checks and the commit you approve are all about that one branch, and that is worth keeping. The next infected branch is now one tap, planned from the same audit. Decisions you made about the finished branch are cleared, because they were never made about this one.
- **Which pull requests still hold it,** and that only GitHub Support can clear those.
- **That tokens and keys the infected code could read have to be changed.**

### The purge message now names everything

The message for GitHub Support used to name the branch tip and nothing else. On a real incident Support cleared that one commit and kept serving the three infected ones behind it. A scoped clean-up knows exactly which commits it replaced, and every one of those ids is now in the message. Pull-request refs are asked for by name too, with the reason they cannot be rewritten locally.

### Fewer wrong calls on ordinary code

Measured on full-history audits of flask and vite — both clean, nothing malicious found in either, before or after:

- **A test reading back what it just sent is test code.** `testsuite/`, `__tests__/`, `*.spec.*` and `conftest.py` were not recognised as test locations, so 65 matches in a single flask test file were rated as a framework deserialising untrusted input.
- **A `createRequire` shim declared at the top of a file and used three hundred lines down is in use.** The check only looked within sight of the shim, which flagged 379 matches across four of vite's own source files. The two cases genuinely worth a look still stand: a shim passed into `new Function`, and one whose only use loads Node's module internals.
- **A remote script tag now says which weakness it found** — loaded over plain `http`, so it can be replaced in transit; or an unpinned path, so the CDN decides later what runs. Both stay serious: an unpinned path is a real technique, not noise. `polyfill.io` is deliberately not on the known-CDN list, because that is a host that was trusted until it was sold.

Every relaxation has an attack twin in the test corpus — malware in a test directory, a pinned library served over `http`, a leftover shim, a shim that loads `child_process` — and the guard that fails loudly if malware could ever be reclassified as harmless stays green. It refused a wider relaxation during this work, and was right to.

**Install:** download `SecureCode-Auditor-0.1.7-apple-silicon.dmg`, drag the app to Applications, and follow *How to open* (one-time "Open Anyway" in Privacy & Security — signed, not yet notarised).

**Needs:** Apple Silicon (M1 or later), macOS 13+, and Docker Desktop, OrbStack, Colima or Podman.

**SHA-256** `de8b7978ae854c87571b88827974862f15c5cda175311aa5e0958851c90532f8`
