# Linux Commands

[English](README.md) | [Français](README.fr.md) | **Español** | [中文](README.zh-CN.md) | [日本語](README.ja.md) | [Русский](README.ru.md)

La referencia de comandos Linux que realmente usas

Archivos de navegación

Silencio .
|---|---|
Silencio `ls -lah` Silencio Lista con tamaños &amp; archivos ocultos Silencio
Silencio `find . -name "*.log" -mtime +30` Silencio Archivos por nombre &gt; edad Silencio
Silencio `fd pattern`
Silencio `du -sh */ | sort -rh`
Silencio `rsync -avh --progress src/ dst/`
confidencialidad `ln -s target link`

## 📝 Text Processing

Silencio .
|---|---|
Silencio `grep -rn "pattern" .`
Silencio `rg "pattern"` Silencio ondulante — instantáneo, respetos .gitignore TEN
Silencio `sed -i 's/old/new/g' file`
confidencialidad `awk '{print $2}'`
Silencio `cut -d: -f1 /etc/passwd`
Silencio `sort | uniq -c | sort -rn`
Silencio `jq '.key'`
Silencio `xargs -P8 -n1 cmd` Silencio Comando paralelo por línea

## 🌐 Network

Silencio .
|---|---|
Silencio `ss -tulpn` Silencio Escuchando puertos + procesos
Silencio `curl -sI url`
Silencio `curl -w '%{time_total}\n' -o /dev/null -s url` Silencio
Silencio `scp file user@host:/path`
Silencio `ssh -L 8080:localhost:80 host` Silencio Puerto local adelante
Silencio `tcpdump -i any -n host x`
Silencio `mtr host`

Procesos

Silencio .
|---|---|
Silencio `ps aux | grep proc` Silencio Encontrar un proceso
Silencio `htop` / `btop`
Silencio `kill -9 PID`
Silencio `lsof -p PID` Silencio Archivos un proceso mantiene abierto Silencio
Silencio `nohup cmd &`
Silencio `systemctl status svc`

## 💾 Disk &amp; System

Silencio .
|---|---|
Silencio `df -h`
confidencialidad `free -h`
Silencio `uname -a`
Silencio `dmesg | tail`
Silencio `lsblk` Silencio dispositivos Block
Silencio `mount | column -t` Silencio Sistemas de archivos montados Silencio

Permisos

Silencio .
|---|---|
Silencio para el propietario, rx para los demás
Silencio `chown user:group file`
Silencio `sudo !!`
Silencio `visudo`

Archivos

Silencio .
|---|---|
Silencio `tar -xzf f.tar.gz`
Silencio `tar -czf out.tar.gz dir/`
confidencialidad `zip -r out.zip dir/`
confidencialidad `7z x f.7z`

♪ ♪ ♪ ♪♪ Productivity

Silencio .
|---|---|
Silencio `Ctrl-R`
Silencio `!!`
Silencio `!$` Silencio Último argumento
Silencio `alias ll='ls -lah'` Silencio Aliases viven en ~/.bashrc
Silencio `tldr cmd`
Silencio `bat file` Silencioso gato con alas
Silencio `watch -n2 cmd`

## 🧰 Disk &gt; Archivos (extras)

← Mando Silencioso
|---|---|
Silencio `ncdu` Silencio Navegador interactivo de uso de disco
Silencio `tree -L 2`
Silencio `fdupes -r dir` Silencio Buscar duplicados
Silencio `stat file` Silencio Metadatos completos

## Permisos &quot; Propiedad (extras)

← Mando Silencioso
|---|---|
Silencio `chmod g+s dir`
Silencio `getfacl file`
Silencio `chattr +i file` Silencio Hacer inmutable (root incluso no puede editar)
Silencio `umask 022`

## 🐛 Debugging &amp; Observability

← Mando Silencioso
|---|---|
Silencio `strace -c cmd` Silencio Resumen de Syscall — donde el tiempo pasa
Silencio `ltrace cmd` Silencio Biblioteca-call trace
Silencio `perf top`
Silencio `journalctl -fu svc` Silencio Seguir los registros de servicios
Silencio `dmesg -w` Silencio Vea los mensajes del kernel

## 📦 Packages

Silencio
|---|---|
TEN Debian/Ubuntu ANTE `apt search`, `apt show`, `dpkg -L pkg`
← Fedora ← `dnf list installed`, `dnf provides file`
← Arco Silencio `pacman -Ss`, `pacman -Ql pkg`
TENIDO macOS TENIDO `brew info`, `brew services list`

## ¦

← Mando Silencioso
|---|---|
Silencio `crontab -e`
Silencio `at now +1 hour` Silencio Una misión retrasada
Silencio `systemd-run --on-calendar="Mon 09:00"`
Silencio `sleep 300 && cmd &`

Paralelismo

← Mando Silencioso
|---|---|
Silencio `cmd1 & cmd2 & wait`
Silencio `xargs -P8 -n100 cmd`
Silencio `parallel -j+0 'cmd {}' ::: a b c`

---
## Contribuir

Los pull requests son bienvenidos: abre una PR y será revisada y fusionada. Mantenido por [aixisstudio](https://github.com/aixisstudio), autor de [Snitch](https://github.com/aixisstudio/Snitch), firewall de aplicaciones open source.

## Licencia: MIT
