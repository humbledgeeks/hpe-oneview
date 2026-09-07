# hpe-synergy-powershell

PowerShell automation for HPE Synergy OneView infrastructure.

## Contents

| File | Purpose |
|------|---------|
| `get-synergy-enclosure-health.ps1` | Read-only health report: enclosure status, compute module inventory, profile compliance, and active alerts |

## Prerequisites

```powershell
# Install HPEOneView module — match version to your appliance
Install-Module HPEOneView.800 -Scope CurrentUser
# Or for OneView 9.x:
Install-Module HPEOneView.900 -Scope CurrentUser
```

Requires PowerShell 5.1 or 7.x. HPE OneView / Synergy Composer must be reachable over HTTPS (port 443).

## CI/CD

All PRs validated by PSScriptAnalyzer, secret scan, and header compliance.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Owner

humbledgeeks-allen | [HumbledGeeks.com](https://humbledgeeks.com)
