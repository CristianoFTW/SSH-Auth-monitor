# Project brief: SSH Auth Monitor

## Prompt
Build a polished, dependency-free, offline-first browser tool for a cybersecurity student to analyze SSH authentication logs from an authorized lab. The tool should accept pasted text or a local log file, identify failed and successful SSH authentication events, group repeated failures by source IP, flag sources at a configurable threshold, show a chronological event timeline, and export the parsed events to CSV. Include synthetic demo data, input validation, readable empty/error states, and clear privacy language. Do not connect to any network or attempt to block, scan, or contact any IP address. Keep all processing in the browser.

## Selected project
Screenshot item 4: SSH Authentication-Failure Monitoring and Response.

## Scope and assumptions
This is a local educational log-review helper, not an intrusion detection system. It handles common OpenSSH journal/syslog lines containing `Failed password`, `Failed publickey`, `Invalid user`, `authentication failure`, `Accepted password`, or `Accepted publickey`. It reports source strings found in log text, without validating or contacting those addresses.

## Acceptance criteria
- Runs by opening `index.html`; no install or build step.
- Demo data produces both failed and successful events and highlights repeated sources.
- Users can paste text or select a local `.log`/`.txt` file.
- Threshold and text filtering update the event summary and tables.
- CSV export quotes cell values correctly.
- Malformed/unrecognized input gets a useful message and does not crash.
- No remote scripts, stylesheets, fonts, requests, or data upload.

