# Changelog

Format based on [Keep a Changelog](https://keepachangelog.com/).

## [0.2.1-private-review] - export review

### Added
- Initial StigForge export of matrix role `ubuntu24_stig`.
- OpenSCAP verify evidence bundles per profile under `compliance/releases/`.

### Verified (CI)

- **`stig`** — score **55.81%** (floor 90.0%) · gate **FAIL** · evidence `20260726T135922Z`
  - OpenSCAP failures still counted: `account_disable_post_pw_expiration, accounts_max_concurrent_login_sessions, accounts_maximum_age_login_defs, accounts_minimum_age_login_defs, accounts_password_pam_unix_rounds_password_auth, accounts_passwords_pam_faildelay_delay, accounts_passwords_pam_faillock_audit, accounts_passwords_pam_faillock_deny`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30277229616
- Factory commit: `f0323b6e2f0f36a0418447b9859a0576278541b8`

