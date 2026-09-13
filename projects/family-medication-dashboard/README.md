# Family Medication Dashboard

[Open the live medication dashboard](https://crispynuggetd.github.io/nestbyte-codex/medication-dashboard/)

A zero-backend static dashboard. Medication data is encrypted locally with AES-256-GCM; the host receives only ciphertext.

> [!WARNING]
> This repository and its Git history are public because GitHub Pages requires public access for this setup. Never commit plaintext medication or health data, Apple Health exports or screenshots, the shared passphrase, credentials, or identifying sensitive information. Commit only the encrypted `data.enc.json` payload.

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

Never commit plaintext health exports or the passphrase. This is a family reference dashboard, not a clinical record or emergency system.

## Hosting

The included GitHub Pages workflow publishes this directory at the [live dashboard URL](https://crispynuggetd.github.io/nestbyte-codex/medication-dashboard/).

The repository's root Pages URL is a project index, allowing future projects to use their own subpaths. HTTPS is required for browser cryptography. In repository **Settings → Pages**, select **GitHub Actions** as the source once; subsequent merges update the site automatically.