# Medication Dashboard Agent Instructions

When the user supplies this project URL plus an Apple Health medication screenshot or export, help prepare an encrypted dashboard update.

## Required workflow

1. Read `README.md`, `UPDATE_GUIDE.md`, `index.html`, and `updater.html`.
2. Extract medication names, schedules, dose events, statuses, and timestamps from the supplied material.
3. Show the proposed structured record to the user and ask them to confirm ambiguous or safety-relevant details before encryption.
4. Never interpret an absent event as a missed dose. Use `missed` only when the source or user explicitly says it was missed.
5. Set `updatedAt` to the actual update time.
6. Encrypt the confirmed JSON using the format already used by `data.enc.json`: PBKDF2-HMAC-SHA256, 250,000 iterations, a random 16-byte salt, AES-256-GCM, and a random 12-byte IV. Append the 16-byte GCM authentication tag to the ciphertext before Base64 encoding.
7. Verify that the produced payload decrypts and parses correctly.
8. Return only the replacement `data.enc.json` as the persistent health-data artifact, plus concise upload instructions for `projects/family-medication-dashboard/data.enc.json`.

Do not commit or upload plaintext health data, screenshots, exports, passphrases, temporary files, tokens or or command output containing the passphrase. Do not silently change the cryptographic format. This dashboard is a family reference, not a clinical record or emergency alert system.