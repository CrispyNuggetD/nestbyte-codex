# Family Medication Dashboard

A zero-backend static dashboard. Medication data is encrypted locally with AES-256-GCM; the host receives only ciphertext.

## Updating from an iPhone

1. Open `updater.html` through the deployed site.
2. Edit the JSON and enter the shared passphrase.
3. Download `data.enc.json`.
4. Replace this directory's `data.enc.json` in GitHub and merge the change.
5. Reload the dashboard.

The initial encrypted record contains no medication events. Never commit plaintext health exports or the passphrase. This is a family reference dashboard, not a clinical record or emergency system.

## Hosting

Publish `projects/family-medication-dashboard` as a static directory with no build command. HTTPS is required for browser cryptography.