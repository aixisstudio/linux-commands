# Linux Commands

**English** | [Français](README.fr.md) | [Español](README.es.md) | [中文](README.zh-CN.md) | [日本語](README.ja.md) | [Русский](README.ru.md)

The Linux/Unix command reference you actually use

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

---
Maintained by [aixisstudio](https://github.com/aixisstudio) — author of [Snitch](https://github.com/aixisstudio/Snitch), the open-source application firewall.

## License

MIT
