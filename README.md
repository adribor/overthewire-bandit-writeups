# OverTheWire Bandit Writeups (Levels 0–33)

[![OverTheWire](https://img.shields.io/badge/OverTheWire-Bandit-red?style=flat-square)](https://overthewire.org/wargames/bandit/)
[![Status](https://img.shields.io/badge/status-completed-brightgreen?style=flat-square)](#)
[![Focus](https://img.shields.io/badge/focus-Linux%20security-blue?style=flat-square)](#)

Personal solutions and learning notes for the [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) wargame. This repository covers the transitions from level 0 to level 33 (0 → 1 through 32 → 33).

> **Spoiler warning:** These notes contain hints and solutions for all levels. Try each challenge yourself before opening its writeup.

## What I Practiced

- Linux shell navigation, hidden files, unusual filenames, permissions, ownership, and redirection
- Searching and processing data with `find`, `grep`, `sort`, `uniq`, `awk`, and `sed`
- Identifying file formats and working with Base64, hexadecimal dumps, compression, and archives
- Connecting to services and exploring network basics with `nc`, `telnet`, `nmap`, and `openssl`
- SSH keys, restricted commands, and secure remote access fundamentals
- Inspecting SUID programs, scheduled tasks, and environment behavior in the challenge environment
- Bash scripting and command-line automation
- Git history, branches, tags, and hooks

## Writeups

Each file documents one transition. Open only the level you are currently working on if you want to avoid spoilers.

| Transition | Writeup |
|---|---|
| 0 → 1 | [Bandit 0 → 1](<Bandit 0 -> 1.txt>) |
| 1 → 2 | [Bandit 1 → 2](<Bandit 1 -> 2.txt>) |
| 2 → 3 | [Bandit 2 → 3](<Bandit 2 -> 3.txt>) |
| 3 → 4 | [Bandit 3 → 4](<Bandit 3 -> 4.txt>) |
| 4 → 5 | [Bandit 4 → 5](<Bandit 4 -> 5.txt>) |
| 5 → 6 | [Bandit 5 → 6](<Bandit 5 -> 6.txt>) |
| 6 → 7 | [Bandit 6 → 7](<Bandit 6 -> 7.txt>) |
| 7 → 8 | [Bandit 7 → 8](<Bandit 7 -> 8.txt>) |
| 8 → 9 | [Bandit 8 → 9](<Bandit 8 -> 9.txt>) |
| 9 → 10 | [Bandit 9 → 10](<Bandit 9 -> 10.txt>) |
| 10 → 11 | [Bandit 10 → 11](<Bandit 10 -> 11.txt>) |
| 11 → 12 | [Bandit 11 → 12](<Bandit 11 -> 12.txt>) |
| 12 → 13 | [Bandit 12 → 13](<Bandit 12 -> 13.txt>) |
| 13 → 14 | [Bandit 13 → 14](<Bandit 13 -> 14.txt>) |
| 14 → 15 | [Bandit 14 → 15](<Bandit 14 -> 15.txt>) |
| 15 → 16 | [Bandit 15 → 16](<Bandit 15 -> 16.txt>) |
| 16 → 17 | [Bandit 16 → 17](<Bandit 16 -> 17.txt>) |
| 17 → 18 | [Bandit 17 → 18](<Bandit 17 -> 18.txt>) |
| 18 → 19 | [Bandit 18 → 19](<Bandit 18 -> 19.txt>) |
| 19 → 20 | [Bandit 19 → 20](<Bandit 19 -> 20.txt>) |
| 20 → 21 | [Bandit 20 → 21](<Bandit 20 -> 21.txt>) |
| 21 → 22 | [Bandit 21 → 22](<Bandit 21 -> 22.txt>) |
| 22 → 23 | [Bandit 22 → 23](<Bandit 22 -> 23.txt>) |
| 23 → 24 | [Bandit 23 → 24](<Bandit 23 -> 24.txt>) |
| 24 → 25 | [Bandit 24 → 25](<Bandit 24 -> 25.txt>) |
| 25 → 26 | [Bandit 25 → 26](<Bandit 25 -> 26.txt>) |
| 26 → 27 | [Bandit 26 → 27](<Bandit 26 -> 27.txt>) |
| 27 → 28 | [Bandit 27 → 28](<Bandit 27 -> 28.txt>) |
| 28 → 29 | [Bandit 28 → 29](<Bandit 28 -> 29.txt>) |
| 29 → 30 | [Bandit 29 → 30](<Bandit 29 -> 30.txt>) |
| 30 → 31 | [Bandit 30 → 31](<Bandit 30 -> 31.txt>) |
| 31 → 32 | [Bandit 31 → 32](<Bandit 31 -> 32.txt>) |
| 32 → 33 | [Bandit 32 → 33](<Bandit 32 -> 33.txt>) |

## Useful Commands

| Command | Purpose |
|---|---|
| `find / -user <user> -size 33c 2>/dev/null` | Search for files matching owner and size criteria while suppressing permission errors |
| `strings <file> \| grep "<pattern>"` | Find readable strings in a binary file |
| `sort <file> \| uniq -u` | Find lines that occur only once |
| `tr 'A-Za-z' 'N-ZA-Mn-za-m'` | Apply ROT13 to input |
| `xxd -r <hexfile> <binaryfile>` | Convert a hex dump back to binary |
| `nmap -p 31000-32000 -sV localhost` | Inspect services in the specified local port range in the challenge environment |
| `openssl s_client -connect <host>:<port>` | Connect to a TLS service for inspection |

## Passwords and Sensitive Data

Challenge passwords and private keys are intentionally omitted or redacted. Do not copy credentials, private keys, or other sensitive values into public writeups.

## Disclaimer

This repository is for learning and documentation. Use these techniques only within OverTheWire or other environments where you have explicit authorization. Follow the platform's rules.

## Resources

- [OverTheWire Bandit](https://overthewire.org/wargames/bandit/)
