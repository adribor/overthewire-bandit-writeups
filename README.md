# OverTheWire Bandit Writeups (Levels 0–33)

[![OverTheWire](https://img.shields.io/badge/OverTheWire-Bandit-red?style=flat-square)](https://overthewire.org/wargames/bandit/)
[![Status](https://img.shields.io/badge/status-completed-brightgreen?style=flat-square)](#)
[![Focus](https://img.shields.io/badge/focus-Linux_security-blue?style=flat-square)](#)

Personal solutions and notes for the [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) wargame, covering levels 0 through 33.

Each level has a separate text file containing the commands, explanations, and methodology used to reach the next level. To avoid sharing challenge passwords and private SSH keys, sensitive values are replaced with `[REDACTED]`.

> **Spoiler warning:** This repository contains solutions and hints for every level. Try solving each level yourself before reading the corresponding writeup.

## Skills and Concepts Covered

- File navigation, hidden files, filenames with spaces or dashes, permissions, ownership, and redirection
- Searching and filtering data with `find`, `grep`, `sort`, `uniq`, `awk`, and `sed`
- Working with encoded data, Base64, hex dumps, compression, and archives
- Connecting to network services with `nc`, `telnet`, `nmap`, and `openssl`
- Using SSH keys and restricted SSH commands
- Exploiting SUID binaries and understanding scheduled `cron` jobs
- Automating tasks with Bash scripts
- Escaping restricted shells and limited utilities
- Inspecting Git commits, branches, tags, and hooks

## Repository Structure

```text
overthewire-bandit-writeups/
├── README.md
├── Bandit 0 -> 1.txt
├── Bandit 1 -> 2.txt
├── Bandit 2 -> 3.txt
├── ...
└── Bandit 32 -> 33.txt
```

Level files are named according to the starting and destination levels.

## Useful Commands

| Command | Purpose |
|---|---|
| `find / -user user -size 33c 2>/dev/null` | Search files by owner and size while hiding permission errors |
| `strings file  grep "=== "` | Extract readable text from binary data |
| `sort file  uniq -u` | Find lines that appear only once |
| `tr 'A-Za-z' 'N-ZA-Mn-za-m'` | Decode ROT13 text |
| `xxd -r hexfile > binfile` | Convert a hex dump back to binary |
| `nmap -p 31000-32000 -sV localhost` | Scan a port range and identify running services |
| `openssl s_client -connect host:port` | Connect to an SSL/TLS service |

## Disclaimer

These notes are provided for educational purposes. Follow the rules of the OverTheWire platform and use the techniques only in authorized environments.

## Resources

- [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/)
