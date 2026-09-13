# Updating with ChatGPT or Codex

In a new capable chat, provide:

1. The URL of this project directory.
2. An Apple Health medication screenshot or export.
3. The instruction: “Follow this project's AGENTS.md and prepare my encrypted dashboard update.”
4. The shared passphrase only when you are ready to create the encrypted file.

The assistant should first show you the interpreted medication record. Check medication names, doses, timestamps, time zone, and whether each event was explicitly recorded as taken or missed.

After confirmation, the assistant should return one file named `data.enc.json`. Upload it to:

`projects/family-medication-dashboard/data.enc.json`

Do not upload the original screenshot/export or any plaintext JSON to GitHub. After the website redeploys, open it on your father's phone, enter the shared passphrase, and check the displayed “Last updated” time and medication events.

If a chat cannot access the repository or create files, open the deployed `updater.html`, paste the confirmed JSON, and download `data.enc.json` directly on the iPhone.