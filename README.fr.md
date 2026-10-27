# Linux Commands

[English](README.md) | **Français** | [Español](README.es.md) | [中文](README.zh-CN.md) | [日本語](README.ja.md) | [Русский](README.ru.md)

La référence de commandes Linux/Unix que tu utilises vraiment

_Le contenu détaillé (listes, liens, descriptions) est en anglais pour rester maintenable — les sections ci-dessous te guident._

## 🗂️ Files & Navigation

| Command | Usage |
|---|---|
| `ls -lah` | List with sizes & hidden files |
| `find . -name "*.log" -mtime +30` | Files by name & age |
| `fd pattern` | Modern fast `find` |
| `du -sh */ | sort -rh` | Biggest directories first |
| `rsync -avh --progress src/ dst/` | Faithful copy with progress |
| `ln -s target link` | Symlink |

## 📝 Text Processing

| Command | Usage |
|---|---|
| `grep -rn "pattern" .` | Recursive search |
| `rg "pattern"` | ripgrep — instant, respects .gitignore |
| `sed -i 's/old/new/g' file` | In-place replace |
| `awk '{print $2}'` | Column extraction |
| `cut -d: -f1 /etc/passwd` | Field split |
| `sort | uniq -c | sort -rn` | Frequency count |
| `jq '.key'` | JSON query |
| `xargs -P8 -n1 cmd` | Parallel command per line |

## 🌐 Network

| Command | Usage |
|---|---|
| `ss -tulpn` | Listening ports + processes |
| `curl -sI url` | Headers only |
| `curl -w '%{time_total}\n' -o /dev/null -s url` | Request timing |
| `scp file user@host:/path` | Copy over SSH |
| `ssh -L 8080:localhost:80 host` | Local port forward |
| `tcpdump -i any -n host x` | Packet capture |
| `mtr host` | Live traceroute |

## ⚙️ Processes

| Command | Usage |
|---|---|
| `ps aux | grep proc` | Find a process |
| `htop` / `btop` | Interactive monitor |
| `kill -9 PID` | Force kill |
| `lsof -p PID` | Files a process holds open |
| `nohup cmd &` | Survive logout |
| `systemctl status svc` | Service state |

## 💾 Disk & System

| Command | Usage |
|---|---|
| `df -h` | Filesystem usage |
| `free -h` | Memory |
| `uname -a` | Kernel info |
| `dmesg | tail` | Kernel messages |
| `lsblk` | Block devices |
| `mount | column -t` | Mounted filesystems |

## 🔐 Permissions

| Command | Usage |
|---|---|
| `chmod 755 file` | rwx for owner, rx for others |
| `chown user:group file` | Ownership |
| `sudo !!` | Re-run last command as root |
| `visudo` | Safe sudoers editing |

## 📦 Archives

| Command | Usage |
|---|---|
| `tar -xzf f.tar.gz` | Extract |
| `tar -czf out.tar.gz dir/` | Create |
| `zip -r out.zip dir/` | Zip |
| `7z x f.7z` | 7-Zip extract |

## ⚡ Productivity

| Command | Usage |
|---|---|
| `Ctrl-R` | Fuzzy history search |
| `!!` | Repeat last command |
| `!$` | Last argument |
| `alias ll='ls -lah'` | Aliases live in ~/.bashrc |
| `tldr cmd` | Practical man pages |
| `bat file` | cat with wings |
| `watch -n2 cmd` | Run every 2s |

## 🧰 Disk & Files (extras)

| Command | What |
|---|---|
| `ncdu` | Interactive disk-usage browser |
| `tree -L 2` | Directory tree |
| `fdupes -r dir` | Find duplicates |
| `stat file` | Full metadata |

## 🔒 Permissions & Ownership (extras)

| Command | What |
|---|---|
| `chmod g+s dir` | Sticky group inheritance |
| `getfacl file` | Fine-grained ACLs |
| `chattr +i file` | Make immutable (root even can't edit) |
| `umask 022` | Default permission mask |

## 🐛 Debugging & Observability

| Command | What |
|---|---|
| `strace -c cmd` | Syscall summary — where time goes |
| `ltrace cmd` | Library-call trace |
| `perf top` | CPU hot spots live |
| `journalctl -fu svc` | Follow service logs |
| `dmesg -w` | Watch kernel messages |

## 📦 Packages

| Distro | Command |
|---|---|
| Debian/Ubuntu | `apt search`, `apt show`, `dpkg -L pkg` |
| Fedora | `dnf list installed`, `dnf provides file` |
| Arch | `pacman -Ss`, `pacman -Ql pkg` |
| macOS | `brew info`, `brew services list` |

## ⏰ Scheduling

| Command | What |
|---|---|
| `crontab -e` | Edit cron jobs |
| `at now +1 hour` | One-shot delayed task |
| `systemd-run --on-calendar="Mon 09:00"` | systemd timer |
| `sleep 300 && cmd &` | Poor-man's scheduler |

## 🧵 Parallelism

| Command | What |
|---|---|
| `cmd1 & cmd2 & wait` | Background + wait |
| `xargs -P8 -n100 cmd` | Parallel batching |
| `parallel -j+0 'cmd {}' ::: a b c` | GNU parallel |

---
## Contribuer

Les pull requests sont les bienvenues : ouvre une PR, elle sera relue et fusionnée. Maintenu par [aixisstudio](https://github.com/aixisstudio), auteur de [Snitch](https://github.com/aixisstudio/Snitch), pare-feu applicatif open source.

## Licence: MIT
