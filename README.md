# ubuntu24_stig — Ansible role (ubuntu24-stig)

**Ansible hardening role** for **Ubuntu 24.04 LTS** (DISA STIG). Suitable for playbooks, Packer/Ansible provisioners, and golden-image pipelines. Search keywords: `ansible`, `ansible-role`, `compliance`, `devsecops`, `disa`, `disa-stig`, `hardening`, `infrastructure`, `noble`, `openscap`, `security`, `stig`, `stigforge`, `ubuntu`.

StigForge-exported Ansible role **`ubuntu24_stig`** · release **`0.3.49`**.
Matrix cell status: **`green`**.

## Install

This repository root **is** the Ansible role (Galaxy-style layout). OpenSCAP evidence
lives under `compliance/` and is not loaded when the role runs.

From **GitHub** (public):

```yaml
# requirements.yml
roles:
  - src: https://github.com/stigready/ubuntu24-stig
    scm: git
    version: v0.3.49   # or an immutable commit SHA
    name: ubuntu24_stig
```

```bash
ansible-galaxy role install -r requirements.yml -p ./roles
ansible-playbook -i inventory site.yml   # role: ubuntu24_stig
```

## Verification status (this release)

This release carries no per-role OpenSCAP score. A container cannot evaluate most STIG rules, so the
role is scored where it runs: the StigReady AMI build scores each image against the unmodified SSG
profile. `compliance/releases/0.3.49/manifest.json` records this.

## Exceptions (excluded from the score gate)

These rules are excluded from the OpenSCAP score gate. Most depend on the network or organisation the AMI is deployed into, so the role leaves them to the AMI owner; where the role does enforce a control and only the scanner cannot confirm it, the table says so. Each is tracked in the StigForge policy for this role and listed in the image's POA&M. The shared cloud policy strips a further documented set (for example the bootloader password and smartcard rules).

| Rule | Requirement | What this role does | What the AMI owner does |
|---|---|---|---|
| `chronyd_specify_remote_server` | UBTU-24-600160 | Configures the Amazon Time Sync Service (`server 169.254.169.123 prefer iburst minpoll 4 maxpoll 4`) as the chrony server and removes the public pool lines, so the `server` directive and `maxpoll` rules of the same finding pass. | Add your organisation's approved time server(s) as `server` lines under /etc/chrony/conf.d/, or replace the Amazon Time Sync line in /etc/chrony/chrony.conf. |

## Reports & review

- **[reports/index.html](reports/index.html)** — HTML report index
- **[CHANGELOG.md](CHANGELOG.md)** — release notes and verify summary

## Verify the score (customer)

Re-run OpenSCAP in Docker and compare to this release's evidence:

```bash
make prove RELEASE=0.3.49
```

Or score your own `results.xml`: see **[compliance/README.md](compliance/README.md)**.

## License

- **[LICENSE](LICENSE)** (MIT) — StigForge export packaging
- **[NOTICE](NOTICE)** — ComplianceAsCode / BSD-3-Clause task body attribution

## Catalog

- [https://stigready.com/#stigforge](https://stigready.com/#stigforge)

