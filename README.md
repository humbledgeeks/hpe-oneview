# hpe-oneview

Reusable **HPE** health-reporting automation: Synergy enclosures via **OneView** and ProLiant
servers via **iLO** (Redfish / HPEiLOCmdlets). All scripts are read-only reports.

## Contents

| Path | Language | What it does | Effect |
|---|---|---|---|
| `ansible/synergy-gather-enclosure-info.yml` | Ansible (`hpe.oneview` collection) | Enclosure health, compute module status, server-profile compliance | read-only |
| `ansible/ilo-gather-server-health.yml` | Ansible (built-in `uri`, Redfish) | System, CPU, memory, thermal, power supply and iLO firmware summary | read-only |
| `powershell/get-synergy-enclosure-health.ps1` | PowerShell (`HPEOneView.800`/`.900`) | Enclosure status, compute inventory, profile compliance, active alerts | read-only |
| `powershell/get-ilo-server-health.ps1` | PowerShell (`HPEiLOCmdlets`) | iLO health, hardware inventory, firmware versions | read-only |
| `docs/legacy-README-*.md` | — | Original per-repository READMEs | — |

## Prerequisites

- Ansible 2.14+ / Python 3.9+; `ansible-galaxy collection install hpe.oneview` for the Synergy playbook (the iLO playbook needs no extra collection).
- PowerShell 5.1/7 with `Install-Module HPEOneView.<version matching the appliance>` and `HPEiLOCmdlets`.
- HTTPS (443) reachability to OneView / Synergy Composer and to iLO.

## Environment-specific configuration

Appliance addresses and credentials are supplied at run time. Nothing environment-specific is
stored here. There is no firmware-update or configuration-change automation in this repository.

## Credentials and safety

No credentials are stored in this repository. PowerShell scripts prompt (`Get-Credential`) or read
environment variables; Ansible playbooks expect an Ansible Vault (`--ask-vault-pass`) providing the
`vault_*` variables named in `group_vars`. Never commit vault files, Clixml exports or `.env` files
(see `.gitignore`). Run output (reports, CSV, logs) is generated content and is git-ignored; keep it
outside the repository.

## Provenance

Consolidated from previous local automation repositories during the 2026 LabOps repository
cleanup. This repository starts with a fresh history; earlier history is retained locally only.
