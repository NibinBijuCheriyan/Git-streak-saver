Gitty: n8n Streak Saver
This repository contains the logic for an automated GitHub activity maintainer. The workflow, built in n8n, monitors Discord messages and triggers a file update in this repository to ensure your contribution graph remains active.

How It Works
Schedule Trigger: The workflow polls a specific Discord channel every minute.

Discord Check: It retrieves the latest message from the "the-guy" channel in the "GItty" server.

Conditional Logic: If the message content is exactly !savestreak:

GitHub Edit: It updates streak.txt with the current timestamp.

Cleanup: It deletes the trigger message from Discord to keep the channel clean.

Confirmation: It sends a success message back to Discord.
 
Caution & Ethical Use
This tool is intended for personal productivity tracking and as a proof-of-concept for n8n integrations.

Please note:

Do not misuse this automation to spoof meaningful work. A GitHub streak is most valuable when it represents actual progress and learning.

API Limits: Frequent polling (every minute) can consume n8n resources and Discord/GitHub API quotas. Adjust the Schedule Trigger as needed.

Security: Ensure your n8n credentials for Discord and GitHub are stored securely and never shared.
