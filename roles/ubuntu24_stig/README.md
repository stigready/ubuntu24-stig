# `ubuntu24_stig`

StigForge-owned remediation role imported from ComplianceAsCode playbooks, with cloud-breaker tasks stripped.

- Profiles: stig
- SSG datastream: `ssg-ubuntu2404-ds.xml`
- Generation summary: see `GENERATED.json`

## Attribution

Task bodies originate from [ComplianceAsCode/content](https://github.com/ComplianceAsCode/content) (BSD-3-Clause).
StigForge owns the packaging, cloud policy filter, and verify gate.

Do not cut over stigready until docker verify clears the ≥90% floor.
