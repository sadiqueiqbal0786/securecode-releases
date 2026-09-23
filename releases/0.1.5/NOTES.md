SecureCode Auditor 0.1.5 for Apple Silicon Macs. One fix, and it matters.

**A repository that defends itself against this malware is no longer called infected.**

The loader-marker rule matched the marker `global['!']` wherever it appeared — including inside a GitHub Actions workflow whose whole job is to grep for that marker, and inside an incident report describing it. One line of a defensive workflow was enough to turn an entirely clean repository into "Malicious code confirmed".

The rule now requires the marker to be *used* — assigned to, called, indexed or read as a property — which is what the real loader does (`global['!']='9-5889-1';`). Naming it is not carrying it.

Detection is unchanged: the marker is still caught when it is assigned with any spacing or escaping, when it is called, and when it appears inside a workflow as code that actually runs. Six cases were added to the test corpus to keep both halves true.

If you audited a repository with 0.1.4 and were told malware was confirmed in a security workflow or a security document, audit it again with this version.

**Install:** download `SecureCode-Auditor-0.1.5-apple-silicon.dmg`, drag the app to Applications, and follow *How to open* (one-time "Open Anyway" in Privacy & Security — the app is signed but not yet notarised).

**Needs:** Apple Silicon (M1 or later), macOS 13+, and Docker Desktop, OrbStack, Colima or Podman.

**SHA-256** `edeca18d85dc068faac6b298761861298ff666ece0d49d8c637468f7c3d0186c`
