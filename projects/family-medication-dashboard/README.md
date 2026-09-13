# Family Medication Dashboard

A zero-backend static dashboard. Medication data is encrypted locally with AES-256-GCM; the host receives only ciphertext.

## Updating with another chat

Paste this project directory's GitHub URL into a capable ChatGPT or Codex chat, attach an Apple Health medication screenshot or export, and say:

> Follow this project's AGENTS.md and prepare my encrypted dashboard update.

Review the assistant's interpretation before it encrypts anything. See [UPDATE_GUIDE.md](UPDATE_GUIDE.md) for the complete handoff and upload path.

## Updating manually from an iPhone

1. Open `updater.html` through the deployed site.
2. Edit the JSON and enter the shared passphrase.
3. Download `data.enc.json`.
4. Replace this directory's `data.enc.json` in GitHub and merge the change.
5. Reload the dashboard.

The initial encrypted record contains no medication events. Never commit plaintext health exports or the passphrase. This is a family reference dashboard, not a clinical record or emergency system.

## Hosting

The included GitHub Pages workflow publishes this directory at:

`https://crispynuggetd.github.io/nestbyte-codex/`

HTTPS is required for browser cryptography. In repository **Settings → Pages**, select **GitHub Actions** as the source once; subsequent merges update the site automatically.