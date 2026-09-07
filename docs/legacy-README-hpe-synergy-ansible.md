# hpe-synergy-ansible

Ansible automation for HPE Synergy OneView infrastructure.

## Contents

| File | Purpose |
|------|---------|
| `synergy-gather-enclosure-info.yml` | Read-only inventory: enclosure health, compute module status, and server profile compliance from HPE OneView |

## Prerequisites

```bash
# Install hpe.oneview collection
ansible-galaxy collection install hpe.oneview

# Install Python SDK
pip install hpeOneView requests --break-system-packages
```

Requires Ansible 2.14+ and Python 3.9+. HPE OneView / Synergy Composer must be reachable over HTTPS (port 443).

## CI/CD

All PRs validated by ansible-lint, secret scan, and header compliance.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Owner

humbledgeeks-allen | [HumbledGeeks.com](https://humbledgeeks.com)
