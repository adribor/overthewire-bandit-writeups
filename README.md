# 🛡️ OverTheWire: Bandit Wargame Writeups (Levels 0 – 33)

![Wargame](https://shields.io)
![Status](https://shields.io)
![Focus](https://shields.io)

Personal walkthroughs, command explanations, and notes for levels 0 through 33 of the **OverTheWire Bandit** wargame. This repository documents the methodology and Linux tools used to solve each challenge.

> **⚠️ Spoiler Policy:** In accordance with OverTheWire's guidelines, all actual level passwords and private SSH keys have been redacted (`[REDACTED]`). The goal of these writeups is to demonstrate the problem-solving process rather than provide shortcuts.

---

## 🎯 Skills & Concepts Covered

Throughout the wargame, the following core Linux and cybersecurity concepts were practiced:

* **File System & Navigation:** Handling hidden files, dashed/spaced filenames, file permissions, ownership (`find`, `file`, `du`), and redirection (`2>/dev/null`).
* **Text Processing & Data Manipulation:** Filtering, sorting, and extracting data using `grep`, `sort`, `uniq`, `strings`, `tr`, `awk`, and `sed`.
* **Encoding & Compression:** Decoding Base64 and hexadecimal dumps (`xxd`), and handling multi-layered archives (`gzip`, `bzip2`, `tar`).
* **Networking & Cryptography:** Interacting with local ports and network services (`nc`, `telnet`, `nmap`), establishing SSL/TLS connections (`openssl`), and SSH key authentication.
* **Privilege Escalation & Automation:** Exploiting SUID binaries, analyzing scheduled `cron` jobs, writing Bash scripts, and escaping restricted shells (`vim`, `more`).
* **Version Control (Git):** Inspecting commit history, branches, tags, and hooks in Git repositories.

---

## 📁 Repository Structure

Each level transition is documented in its own text file in the root directory:

```text
overthewire-bandit-writeups/
├── README.md
├── Bandit 0 -> 1.txt
├── Bandit 1 -> 2.txt
├── Bandit 2 -> 3.txt
├── ...
└── Bandit 32 -> 33.txt
```

---

## 🛠️ Key Commands Cheatsheet

| Command | Purpose |
| :--- | :--- |
| `find / -user X -size Y 2>/dev/null` | Search files by owner and size while hiding permission errors |
| `strings file \| grep "==="` | Extract human-readable text from binary data |
| `sort file \| uniq -u` | Find unique lines that appear only once |
| `tr 'A-Za-z' 'N-ZA-Mn-za-m'` | Decode ROT13 cipher text |
| `xxd -r hexfile > binfile` | Revert a hexdump back into a binary file |
| `nmap -p 31000-32000 -sV localhost` | Scan a port range and detect running service protocols |
| `openssl s_client -connect host:port` | Connect to a service over SSL/TLS |

---

## 🔗 Resources

* [OverTheWire: Bandit Official Page](https://overthewire.org)
