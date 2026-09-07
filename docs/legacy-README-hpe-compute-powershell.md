# hpe-compute-powershell

PowerShell automation for HPE ProLiant iLO infrastructure.

## Contents

| File | Purpose |
|------|---------|
| `get-ilo-server-health.ps1` | Read-only health report: system overview, CPUs, memory, storage, fans, power supplies, and firmware inventory |

## Prerequisites

```powershell
# Install HPEiLOCmdlets from PowerShell Gallery
Install-Module HPEiLOCmdlets -Scope CurrentUser
```

Requires PowerShell 5.1 or 7.x. iLO 5 (Gen10) or iLO 6 (Gen11) must be reachable over HTTPS (port 443).

## CI/CD

All PRs validated by PSScriptAnalyzer, secret scan, and header compliance.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Owner

humbledgeeks-allen | [HumbledGeeks.com](https://humbledgeeks.com)
