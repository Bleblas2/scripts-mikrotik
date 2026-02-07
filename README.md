# MikroTik LTE SMS Script

This repository is a collection of MikroTik scripts I used a few years ago while working
with MikroTik devices. It includes practical utilities like an LTE SMS handler that reads
the inbox, matches message content to predefined actions, and triggers the appropriate
response.

## What it does
- Listens for SMS messages on a MikroTik LTE device.
- Detects known commands in SMS content.
- For the "network status" command, it sends an HTTP POST to a server that replies by SMS.
- Unknown messages can be forwarded by email and are removed from the inbox.

## Configuration notes
- Adjust the server URL in the script to point to your endpoint.
- If you want email forwarding, set `$EmailAddress` in the script and enable the email lines.
- Scheduler runs every 10 seconds by default; tune the interval to your needs.

## Limitations
- MikroTik scripting is minimal, so parsing is intentionally simple.
- SMS replies are handled server-side (the router sends a POST only).

## Files
- `read-sms-from-inbox-and-do-action.txt` - script content and scheduler instructions.
