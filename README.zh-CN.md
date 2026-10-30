# Linux Commands

[English](README.md) | [Français](README.fr.md) | [Español](README.es.md) | **中文** | [日本語](README.ja.md) | [Русский](README.ru.md)

你真正会用到的 Linux/Unix 命令参考

# # # # # 文件与导航

命令使用量
|---|---|
`ls -lah` 包含大小和隐藏文件的列表 QQ
`find . -name "*.log" -mtime +30` 按名称和年龄划分的文件
`fd pattern` 现代快速 `find`
`du -sh */ | sort -rh` 最大目录第一
`rsync -avh --progress src/ dst/` 有进展的忠实副本
`ln -s target link` ========================================================================================== (============================== (======================================================

# # # # 文本处理

命令使用量
|---|---|
`grep -rn "pattern" .` 递归搜索
(掌声) `rg "pattern"` QQ rigrep——即时,尊重.gitignore QQ
`sed -i 's/old/new/g' file` 现场替换
`awk '{print $2}'` 列提取
`cut -d: -f1 /etc/passwd` 现场拆分
`sort | uniq -c | sort -rn` 频率计
`jq '.key'` JSON查询
`xargs -P8 -n1 cmd` 每行并行命令 QQ

###QQ网络

命令使用量
|---|---|
`ss -tulpn` 监听端口+进程
`curl -sI url` 只有标题
`curl -w '%{time_total}\n' -o /dev/null -s url` 请求时间
`scp file user@host:/path` 复制到SSH上
`ssh -L 8080:localhost:80 host` 本地端口前进
`tcpdump -i any -n host x` 包装捕获 QQ
`mtr host` 现场追踪路线

□ □ 过程

命令使用量
|---|---|
`ps aux | grep proc` 找到一个进程 QQ
`htop` / `btop` 互动显示器 QQ
`kill -9 PID` 强杀 强杀
`lsof -p PID` 文件一个进程将打开 QQ
`nohup cmd &` 生存登记
`systemctl status svc` 服务状态

^ QQ 磁盘系统( S)

命令使用量
|---|---|
`df -h` 文件系统使用量
`free -h` 记忆
`uname -a` 核心资讯 QQ
`dmesg | tail` 核心消息 {}
`lsblk` 区块设备
`mount | column -t` 已挂载的文件系统

# # # # 权限

命令使用量
|---|---|
`chmod 755 file` rwx 给所有者,rx 给其他人。
`chown user:group file` 所有权
QQ `sudo !!` 将最后一个命令作为 root QQ 重运行
============================================================================================================================================================================================================================

□□□□□□□ 档案

命令使用量
|---|---|
`tar -xzf f.tar.gz` 摘录
`tar -czf out.tar.gz dir/` 创建 QQ
`zip -r out.zip dir/` 齐普
`7z x f.7z` 7-Zip 节选

□ 生产率

命令使用量
|---|---|
`Ctrl-R` 模糊的历史搜索 QQ
`!!` 重复最后的命令 {}
`!$` 最后一个参数 {}
* * `alias ll='ls -lah'` * * 异物生活在 ~/.bashrc * * *
`tldr cmd` 实用男版
`bat file` 有翅膀的猫
`watch -n2 cmd` 每2s运行一次

□ QQ 磁盘文件( extras)

{\fn方正准圆简体\fs12\1cHC9ECC4}什么?
|---|---|
`ncdu` 互动磁盘用户浏览器
`tree -L 2` 目录树
`fdupes -r dir` 查找复制件 QQ
`stat file` 完整元数据

^ QQ 权限和所有权( extras)

{\fn方正准圆简体\fs12\1cHC9ECC4}什么?
|---|---|
`chmod g+s dir` 粘性组的继承
`getfacl file` 精细ACLs ===
* * `chattr +i file` * * 使不可改变(根本无法编辑) * * * *
`umask 022` 默认权限掩码

^ QQ 调试可观察性( O)

{\fn方正准圆简体\fs12\1cHC9ECC4}什么?
|---|---|
`strace -c cmd` Syscall摘要——时间在哪里?
`ltrace cmd` 图书馆呼叫追踪
`perf top` CPU热点直播 腾讯网.
`journalctl -fu svc` 跟踪服务日志
`dmesg -w` 监视内核消息 QQ

# # # # 软件包

{\fn黑体\fs22\bord1\shad0\3aHBE\4aH00\fscx67\fscy66\2cHFFFFFF\3cH808080}你说什么?
|---|---|
^ Debian/Ubuntu ^ `apt search`, `apt show`, `dpkg -L pkg` ^
`dnf list installed`, `dnf provides file` 请检查date=中的日期值 (帮助)
`pacman -Ss`号拱门 `pacman -Ql pkg`号拱门
`brew info` `brew services list` 互联网档案馆的存檔,存档日期2013-09-02.

□ □ 时间安排

{\fn方正准圆简体\fs12\1cHC9ECC4}什么?
|---|---|
`crontab -e` 编辑 cron 任务 {}
`at now +1 hour` 一发延迟任务
`systemd-run --on-calendar="Mon 09:00"` 系统计时器
`sleep 300 && cmd &` 穷人的排程器

□ 平行主义

{\fn方正准圆简体\fs12\1cHC9ECC4}什么?
|---|---|
`cmd1 & cmd2 & wait` 背景 + 等待 + 等待
`xargs -P8 -n100 cmd` 平行批量 QQ
`parallel -j+0 'cmd {}' ::: a b c` GNU 平行 QQ

---
## 贡献

欢迎提交 Pull Request，我们会审查并合并。由 [aixisstudio](https://github.com/aixisstudio) 维护，他也是开源应用防火墙 [Snitch](https://github.com/aixisstudio/Snitch) 的作者。

## 许可证: MIT
