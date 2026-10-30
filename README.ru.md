# Linux Commands

[English](README.md) | [Français](README.fr.md) | [Español](README.es.md) | [中文](README.zh-CN.md) | [日本語](README.ja.md) | **Русский**

Справочник команд Linux/Unix, которыми реально пользуются

##  ️ Файлы и навигация

Командование, использование
|---|---|
`ls -lah` Список с размерами и скрытыми файлами
| `find . -name "*.log" -mtime +30` | Файлы по имени и возрасту |
`fd pattern` - современный быстрый `find`
| `du -sh */ | sort -rh` | Самые большие каталоги
| `rsync -avh --progress src/ dst/` | Верная копия с прогрессом |
`ln -s target link` | Symlink |

##  Text Текстовая обработка

Командование, использование
|---|---|
`grep -rn "pattern" .` - Рекурсивный поиск
| `rg "pattern"` | ripgrep — моментально, уважает .gitignore |
| `sed -i 's/old/new/g' file` | Вместо |
| `awk '{print $2}'` | Экстракция колонки |
| `cut -d: -f1 /etc/passwd` | Разделение поля
| `sort | uniq -c | sort -rn` | Частотный счет |
`jq '.key'` - запрос JSON
| `xargs -P8 -n1 cmd` | Параллельная команда на строку

###Сеть

Командование, использование
|---|---|
| `ss -tulpn` | Прослушивающие порты + процессы |
| `curl -sI url` | Только заголовки
| `curl -w '%{time_total}\n' -o /dev/null -s url` | Время запроса |
`scp file user@host:/path` Копировать SSH
| `ssh -L 8080:localhost:80 host` | Локальный порт вперед
| `tcpdump -i any -n host x` | Захват пакетов
`mtr host` - Live traceroute

##  ️ Процессы

Командование, использование
|---|---|
`ps aux | grep proc` - Найти процесс
| `htop` / `btop` | Интерактивный монитор
`kill -9 PID` - Force Kill
| `lsof -p PID` | Файлы процесс держит открытым |
| `nohup cmd &` | Выживание
| `systemctl status svc` | Состояние обслуживания

##Диск и система

Командование, использование
|---|---|
| `df -h` | Использование файловой системы
`free -h` — память
| `uname -a` | Информация о ядре
| `dmesg | tail` | Сообщения ядра
| `lsblk` | Блок-устройства |
| `mount | column -t` | Установленные файловые системы |

##   Разрешения

Командование, использование
|---|---|
| `chmod 755 file` | rwx для владельца, rx для других |
`chown user:group file` — собственность
| `sudo !!` | Перезапустить последнюю команду как root |
`visudo` - Безопасные убийцы

## s Архивы

Командование, использование
|---|---|
| `tar -xzf f.tar.gz` | Экстракт
`tar -czf out.tar.gz dir/` Создать
`zip -r out.zip dir/` | Zip
| `7z x f.7z` | 7-Zip экстракт |

##Производительность

Командование, использование
|---|---|
| `Ctrl-R` | Нечеткая история поиска
| `!!` | Повторить последнюю команду
`!$` - последний аргумент
| `alias ll='ls -lah'` | Алиасы живут в ~/.bashrc |
| `tldr cmd` | Практические страницы человека
Кот с крыльями / Cat with Wings
`watch -n2 cmd` - Запуск каждые 2

## ) Диск и файлы (дополнительные)

Командир, что такое
|---|---|
| `ncdu` | Браузер интерактивного использования дисков |
| `tree -L 2` | Дерево директорий |
`fdupes -r dir` Найти дубликаты
`stat file` - полные метаданные

## ) Разрешения и право собственности (дополнительные)

Командир, что такое
|---|---|
`chmod g+s dir` — наследование группы Sticky
| `getfacl file` | Тонкие зернистые ACLs |
| `chattr +i file` | Сделайте неизменяемым (корень даже не может редактировать) |
| `umask 022` | Маска разрешения по умолчанию

##Отладка и наблюдаемость

Командир, что такое
|---|---|
| `strace -c cmd` | Syscall summary — Where Time Goes |
| `ltrace cmd` | След библиотечного звонка |
| `perf top` | CPU hot spots live |
| `journalctl -fu svc` | Следите за журналами обслуживания |
| `dmesg -w` | Сообщения ядра

## s Пакеты

Дистрибутивы / Command
|---|---|
Debian/Ubuntu | `apt search`, `apt show`, `dpkg -L pkg`
Федора, `dnf list installed`, `dnf provides file`
Обсуждение `pacman -Ss`, `pacman -Ql pkg`
macOS | `brew info`, `brew services list`

## ed Расписание

Командир, что такое
|---|---|
| `crontab -e` | Edit cron jobs |
| `at now +1 hour` | Задержка с одним выстрелом |
`systemd-run --on-calendar="Mon 09:00"` - системный таймер
[Перенаправлено с The Poor-man's scheduler]

##Параллелизм

Командир, что такое
|---|---|
| `cmd1 & cmd2 & wait` | Справочная информация + ожидание
| `xargs -P8 -n100 cmd` | Параллельная партия |
`parallel -j+0 'cmd {}' ::: a b c` - параллель GNU

---
## Участие

Pull request'ы приветствуются — открой PR, он будет проверен и принят. Ведёт [aixisstudio](https://github.com/aixisstudio), автор [Snitch](https://github.com/aixisstudio/Snitch) — open-source application firewall.

## Лицензия: MIT
