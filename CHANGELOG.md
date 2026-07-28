# Changelog

Format based on [Keep a Changelog](https://keepachangelog.com/).

## [0.2.2-private-review] - export review

### Added
- Initial StigForge export of matrix role `ubuntu24_stig`.
- OpenSCAP verify evidence bundles per profile under `compliance/releases/`.

### Verified (CI)

- **`stig`** — score **98.08%** (floor 90.0%) · gate **PASS** · evidence `20260728T093156Z`
  - OpenSCAP failures still counted: `banner_etc_profiled_ssh_confirm`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30348467615
- Factory commit: `49f1c019fbf7ba7f8edc345d79321ed45f9534de`

