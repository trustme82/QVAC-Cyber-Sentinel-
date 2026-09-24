# QVAC Cyber Sentinel

A local, privacy-first cybersecurity threat detector and log analyzer powered by the [QVAC SDK](https://docs.qvac.tether.io/).

QVAC Cyber Sentinel analyzes command-line instructions, terminal logs, system scripts, and file hashes on-device to detect potential threats, destructive scripts (like `rm -rf /`), and unverified payload executions before they run — completely offline, without sending sensitive terminal activity or system logs to external cloud servers.

---

## Why local AI matters for local security analysis

Terminal commands and system execution logs contain critical operational context:
- Environment variables, API keys, and credentials
- Internal server IPs and private network architecture
- Proprietary directory structures and user activity

Sending terminal logs to cloud-based LLM APIs exposes sensitive infrastructure to third-party data leaks. By executing threat evaluation locally via `@qvac/sdk`, system instructions are audited entirely in-memory on your machine. Zero network requests, zero cloud latency, and 100% privacy guarantee.

---

## How it works

1. **On-Device Model Loading:** The application loads a lightweight local LLM into system memory using QVAC's `loadModel`.
2. **Interactive Analysis:** Paste system scripts, bash/PowerShell commands, or log snippets into the Cyber Sentinel web interface.
3. **Local LLM Completion:** The model processes the text using `completion()` to identify anomalies, evaluate risk levels, and explain potential threats.
4. **Offline Resilience:** Includes local fallback rules and signature verification to ensure instant feedback even without active network connectivity.

---

## What's inside

qvac-cyber-sentinel/
├── package.json
├── package-lock.json
├── .gitignore
├── README.md
├── server.js
└── public/
└── index.html
___
