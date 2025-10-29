# Vaultwarden - Self-Hosted Password Manager

Bitwarden-compatible password manager for homelab.

## Access

URL: http://192.168.1.216

## First Time Setup

1. Create admin account
2. Disable signups (edit docker-compose.yml: `SIGNUPS_ALLOWED=false`)
3. Install Bitwarden browser extension
4. Point extension to: http://192.168.1.216

## Features

- Password storage
- Secure notes
- 2FA/TOTP
- Browser extensions
- Mobile apps
- Secure sharing

## Stack

- **Vaultwarden**: Lightweight Bitwarden server
- **Docker Compose**: Container orchestration
- **GitHub Actions**: Automated deployment via self-hosted runner

## Deployment

Automatically deployed via GitHub Actions when pushing to main branch.

Manual deployment trigger:
```bash
gh workflow run deploy.yml -R jake-garnier/vaultwardenApp
```

## Security Note

After creating your first account, remember to set `SIGNUPS_ALLOWED=false` in docker-compose.yml to prevent unauthorized registrations.
