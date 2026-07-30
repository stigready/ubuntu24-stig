# Changelog

Format based on [Keep a Changelog](https://keepachangelog.com/).

## [0.2.4] - 2026-07-30

### Changed
- StigForge export refresh for `ubuntu24_stig` at `0.2.4`.

### Verified (OpenSCAP)

- **`stig`** — score **98.08%** (floor 90.0%) · gate **PASS** · evidence `20260729T223237Z`
  - Remaining counted failures: `banner_etc_profiled_ssh_confirm`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30496236357
- Factory commit: `7f7cafc85a392bf2a7eb04f1b979185dbcdf5530`

## [0.2.4-private-review] - 2026-07-29

### Changed
- StigForge export refresh for `ubuntu24_stig` at `0.2.4-private-review`.

### Verified (OpenSCAP)

- **`stig`** — score **98.08%** (floor 90.0%) · gate **PASS** · evidence `20260729T100300Z`
  - Remaining counted failures: `banner_etc_profiled_ssh_confirm`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30440754045
- Factory commit: `c481b47d629f5bc2357a86a933aa6f94f5245fce`

## [0.2.2-private-review] - 2026-07-28

### Added
- Customer verify path: `make prove`, `compliance/verify.json`, `scripts/score-results.py`.

### Changed
- README and this changelog list current OpenSCAP verify scores (≥90% floor).
- All CIS/STIG profiles apply SSG remediation via `stigforge_profile` task includes.
- Matrix cell `ubuntu24_stig` marked **green** with passing docker verify evidence.

### Fixed
- CIS/STIG roles no longer point at empty `rules.yml` scaffold (remediation runs in verify).

### Verified (OpenSCAP)

- **`stig`** — score **55.81%** (floor 90.0%) · gate **FAIL** · evidence `20260726T135922Z`
  - Remaining counted failures: `account_disable_post_pw_expiration, accounts_max_concurrent_login_sessions, accounts_maximum_age_login_defs, accounts_minimum_age_login_defs, accounts_password_pam_unix_rounds_password_auth, accounts_passwords_pam_faildelay_delay, accounts_passwords_pam_faillock_audit, accounts_passwords_pam_faillock_deny`
  - _(+11 more — see `score.json`)_

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30353408831
- Factory commit: `5601d6c388051bf9f7636b086d93888a709b8b31`

## [0.2.1-private-review] - 2026-07-28

### Changed
- Galaxy-style layout: Ansible role at repository root; evidence under `compliance/`.
- Private review tag `v0.2.1-private-review` (supersedes nested `roles/<role>/` export).

## [0.2.0-private-review] - 2026-07-26

### Added
- First private StigForge export to `stigready/*` (factory review; nested role path).
