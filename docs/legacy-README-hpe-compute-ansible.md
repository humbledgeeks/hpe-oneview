# hpe-compute-ansible

Ansible automation for HPE ProLiant iLO infrastructure.

## Contents

| File | Purpose |
|------|---------|
| `ilo-gather-server-health.yml` | Read-only health report via Redfish: system overview, processors, memory, thermal, power supplies, and iLO firmware version |

## Prerequisites

```bash
# Ansible 2.14+ and Python 3.9+ required
pip install ansible --break-system-packages

# No extra collection needed — uses built-in uri module against iLO Redfish API
```

iLO 5 (Gen10) or iLO 6 (Gen11) must be reachable over HTTPS (port 443).

## CI/CD

All PRs validated by ansible-lint, secret scan, and header compliance.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Owner

humbledgeeks-allen | [HumbledGeeks.com](https://humbledgeeks.com)
