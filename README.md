# SSH Auth Monitor

A dependency-free, offline-first browser tool for reviewing SSH authentication logs from an authorized lab. Paste log text or open a `.log`/`.txt` file to see failed and accepted events, repeated failure sources, a filterable timeline, and response follow-up notes. Export parsed events as CSV.

## Run

Open `index.html` in a modern browser. There is no installation, build step, or network connection. Use **Load demo** to explore with synthetic example records.

## Supported lines

Common OpenSSH auth/journal lines containing failed password/public key/keyboard-interactive attempts, invalid users, `authentication failure`, and accepted password/public key/keyboard-interactive logins. Unrecognized lines are ignored. Source and timestamp are shown as written; this tool does not validate timestamps or contact IP addresses.

## Privacy and limits

All parsing occurs in the browser tab. No information is uploaded. Inputs larger than 2 MB are rejected. This is an educational helper, not an IDS; flagged counts are not a determination of malicious activity. It does not block accounts, change firewall rules, scan networks, or contact addresses.

See [PROJECT_PROMPT.md](PROJECT_PROMPT.md) for the self-written brief and acceptance criteria.

