SecureCode Auditor 0.1.8 for Apple Silicon Macs.

**If you installed 0.1.7, please replace it with this.** That build reported its own version as 0.1.6, so it announces an update to itself and never stops offering one. Nothing else about it is wrong — the audit, the clean-up and the isolation all behave as described — but the version it tells you is not the version you have. The packaging script now refuses to build when the version in the code and the version in the project file disagree, which is how that got out.

### After a clean-up, you can tell what is actually left

The day after cleaning a branch, the same serious finding comes back — from a commit behind the new tip — and nothing said so. It read as "the clean-up failed". It had not.

- A finding whose content is in no branch, tag or pull request's **current files** is now marked **ONLY IN HISTORY** on its own row, without opening it.
- Those rows sort below anything still live at the same severity, so what you can fix today is at the top.
- The list says the split plainly: *"9 of 12 serious findings are only in the project's history, not in the current files."*
- A filter shows only what is still in the current code — the question you actually have after a clean-up.

None of it is hidden by default, and none of it is called safe: the host keeps serving those objects, and every old copy still holds them, until the history is rebuilt and purged. Severity still comes first, because malware left in history is still malware.

### A large folder is no longer refused

A 4.4 GB checkout used to be turned away: code is only ever read inside a sealed container, and that container's input lives in memory, which caps one pass at 1.8 GB.

Such a folder is now read in **several sealed containers, one after another**, and the results are added up. The isolation is unchanged — same filter, same arguments, same checks, no network, nothing read on your computer. The progress card says *"part 2 of 3"* so a long audit does not look stuck, and the coverage panel reports how many containers were used.

Checked against an audit of the same folder in one pass: the same files, the same findings, the same verdict. A single file too large to seal even on its own is reported as not inspected rather than quietly skipped.

**Install:** download `SecureCode-Auditor-0.1.8-apple-silicon.dmg`, drag the app to Applications, and follow *How to open* (one-time "Open Anyway" in Privacy & Security — signed, not yet notarised).

**Needs:** Apple Silicon (M1 or later), macOS 13+, and Docker Desktop, OrbStack, Colima or Podman.

**SHA-256** `2e991e97938f41faeaaf48b91f14af02ea9f9ac7624e4daef1ee74f851cf9e65`
