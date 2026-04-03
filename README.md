# 🐧 Linux Mastery — College-Level Course

> A comprehensive, self-contained interactive Linux course built as a single HTML file. Designed for macOS users running Ubuntu in VMware Fusion, covering everything from VM setup to bash scripting automation.

---

## 📖 Overview

**Linux Mastery** is a college-level, browser-based Linux course with 16 modules across 7 units. It requires no server, no dependencies, and no internet connection after the initial load — just open the HTML file and start learning.

The course follows a progressive curriculum: you build a working VM environment in Module 1 and end by writing automation scripts and sitting a 20-question final exam.

---

## ✨ Features

- **16 deep-content modules** with theory, diagrams, terminal examples, and real-world context
- **Hands-on labs** at the end of every module with step-by-step exercises
- **Interactive quizzes** embedded throughout each unit
- **20-question final exam** with auto-scoring (80% to pass)
- **Progress tracking** — sidebar updates as you complete each module
- **Zero dependencies** — single `.html` file, works fully offline
- **Parchment light theme** — easy on the eyes for long study sessions
- **Syntax-highlighted terminal blocks** with color-coded commands, flags, output, and comments

---

## 🗂️ Course Structure

### Unit 1 — Foundations
| Module | Title | Topics |
|--------|-------|--------|
| 01 | VM Environment Setup | VMware Fusion, Ubuntu ISO, snapshots, open-vm-tools |
| 02 | Linux Architecture | Kernel/userspace, syscalls, distros, boot process, modules |
| 03 | The Shell & Bash | Variables, I/O redirection, pipes, expansions, `.bashrc` |

### Unit 2 — Filesystem & Files
| Module | Title | Topics |
|--------|-------|--------|
| 04 | Filesystem Hierarchy (FHS) | `/proc`, `/sys`, filesystem types, mounting, inodes, links |
| 05 | File Operations & Text Editors | cp/mv/rm, cat/less/tail, nano, vim modal editing, tar/gzip |
| 06 | Search & Text Processing | grep, find, sed, awk, cut, sort, uniq |

### Unit 3 — Users & Security
| Module | Title | Topics |
|--------|-------|--------|
| 07 | Users, Groups & sudo | `/etc/passwd`, UIDs, useradd/usermod, sudoers, `/etc/shadow` |
| 08 | Permissions, ACLs & Special Bits | chmod (numeric/symbolic), SUID/SGID/sticky, umask, setfacl/getfacl |

### Unit 4 — System Management
| Module | Title | Topics |
|--------|-------|--------|
| 09 | Package Management | apt, dpkg, sources.list, PPAs, snap, flatpak |
| 10 | Processes & systemd | ps/top/htop, signals, job control, systemctl, journalctl, unit files |
| 11 | Storage, Disks & LVM | lsblk, parted, mkfs, fstab, LVM (pvcreate/vgcreate/lvcreate), swap |

### Unit 5 — Networking
| Module | Title | Topics |
|--------|-------|--------|
| 12 | Networking Deep Dive | ip command, Netplan, DNS (dig), ss, tcpdump, UFW firewall |
| 13 | SSH & Remote Access | Key generation, `ssh-copy-id`, `~/.ssh/config`, sshd hardening, tunneling |

### Unit 6 — Automation
| Module | Title | Topics |
|--------|-------|--------|
| 14 | Bash Scripting | `set -euo pipefail`, conditionals, loops, functions, real health-check script |
| 15 | Cron & Scheduling | Crontab syntax, system cron dirs, systemd timers, `OnCalendar` |

### Unit 7 — Assessment
| Module | Title | Topics |
|--------|-------|--------|
| 16 | Final Exam | 20 questions covering all units, auto-scored, 80% pass threshold |

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- For hands-on labs: [VMware Fusion](https://support.broadcom.com) (free for personal use) + Ubuntu 24.04 LTS

### Running the Course
```bash
# Clone or download
git clone https://github.com/your-username/linux-mastery-course.git
cd linux-mastery-course

# Open in browser (macOS)
open linux-college-course.html

# Or serve locally
python3 -m http.server 8080
# Then visit http://localhost:8080/linux-college-course.html
```

No build step. No npm install. No framework. Just open the file.

---

## 🖥️ VM Setup (Recommended)

The course is designed for hands-on practice in a safe virtual machine. All terminal examples were tested on **Ubuntu 24.04 LTS**.

**Quick setup:**
1. Download [VMware Fusion](https://support.broadcom.com) (free, requires Broadcom account)
2. Download [Ubuntu 24.04 LTS](https://ubuntu.com/download/desktop) ISO
3. Create a VM: 2 CPU cores, 4GB RAM, 25GB disk, NAT networking
4. Install Ubuntu, then run:
   ```bash
   sudo apt update && sudo apt install -y open-vm-tools-desktop
   sudo reboot
   ```
5. **Take a snapshot** before starting labs — you can always revert

> **Apple Silicon note:** Download the ARM64 Ubuntu Server ISO, not the AMD64 desktop ISO. Install desktop after: `sudo apt install ubuntu-desktop`

---

## 📋 What You'll Learn

By the end of this course you'll be able to:

- [ ] Navigate the Linux filesystem and understand every major directory's purpose
- [ ] Manage files, directories, links, and archives from the command line
- [ ] Process and transform text with grep, sed, awk, and pipes
- [ ] Create and manage user accounts, groups, and sudo policies
- [ ] Set file permissions, special bits, and access control lists (ACLs)
- [ ] Install, update, and audit packages with apt and dpkg
- [ ] Monitor processes, send signals, and manage services with systemd
- [ ] Partition disks, format filesystems, configure LVM logical volumes
- [ ] Configure network interfaces, diagnose connectivity, and manage firewall rules
- [ ] Set up SSH key authentication and secure sshd configuration
- [ ] Write production-quality bash scripts with error handling and functions
- [ ] Schedule automated jobs with cron and systemd timers

---

## 🏗️ Technical Details

### Built With
- Pure HTML5, CSS3, and vanilla JavaScript — no frameworks or libraries
- [Google Fonts](https://fonts.google.com): Syne (headings), DM Sans (body), Fira Code (terminal)
- Self-contained: all styles and scripts are inline in a single file

### File Size
| File | Size |
|------|------|
| `linux-college-course.html` | ~200 KB |
| `linux-crash-course.html` (original) | ~47 KB |

### Design System
```
Colors:
  Background:  #f5f2eb  (warm parchment)
  Accent red:  #c0392b  (headings, borders)
  Accent blue: #2563eb  (info callouts)
  Accent green:#16a34a  (success/tips)
  Terminal bg: #1e1b16  (dark code blocks)

Typography:
  Syne 800     → module titles, h2 headings
  DM Sans 400  → body text, UI elements
  Fira Code    → terminal blocks, code, paths
```

---

## 📚 Companion Course

This is the **expanded college-level edition**. The original **Linux Crash Course** (8-module condensed version) covers the same fundamentals in a faster format.

| Course | Modules | Depth | Best For |
|--------|---------|-------|----------|
| Crash Course | 8 | Surface-level | Quick reference, review |
| **College Course** (this) | **16** | **Deep dive** | **Learning from scratch** |

---

## 🤝 Contributing

Contributions welcome! Areas for improvement:

- Additional lab exercises or challenge problems
- Module 17+: Docker, git, firewall deep-dive, monitoring
- Accessibility improvements (ARIA labels, keyboard navigation)
- Mobile layout optimizations
- Dark mode toggle

```bash
# Fork the repo, make changes, then submit a PR
git checkout -b feature/module-docker
# edit linux-college-course.html
git commit -m "Add Module 17: Docker & Containers"
git push origin feature/module-docker
```

---

## 📄 License

MIT License — free to use, modify, and distribute. If you teach a class with this, a shoutout is appreciated but not required.

---

## 🙏 Acknowledgments

- Course design inspired by real sysadmin onboarding curricula
- Terminal color scheme adapted from base16-tomorrow-night
- Built as a single-file interactive document to maximize portability and accessibility

---

<div align="center">

**Happy learning. Break things in your VM. That's what snapshots are for.**

`$ sudo rm -rf /fear` 🐧

</div>
