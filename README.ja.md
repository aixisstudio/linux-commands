# Linux Commands

[English](README.md) | [Français](README.fr.md) | [Español](README.es.md) | [中文](README.zh-CN.md) | **日本語** | [Русский](README.ru.md)

本当に使う Linux/Unix コマンドリファレンス

## ライブファイルとナビゲーション

| コマンド | 使い方 |
|---|---|
| `ls -lah` | サイズ・非表示ファイル一覧 |
| `find . -name "*.log" -mtime +30` | 商品名・年齢別 |
| `fd pattern` | モダンファースト `find` |
| `du -sh */ | sort -rh` | ビッグベスト・ディレクター |
| `rsync -avh --progress src/ dst/` | 進行中のコピー |
| `ln -s target link` | シンリンク |

## テキスト処理

| コマンド | 使い方 |
|---|---|
| `grep -rn "pattern" .` | 再帰検索 |
| `rg "pattern"` | ripgrep — 即刻、敬意 |
| `sed -i 's/old/new/g' file` | 交換場所 |
| `awk '{print $2}'` | コラム抽出 |
| `cut -d: -f1 /etc/passwd` | フィールドスプリット |
| `sort | uniq -c | sort -rn` | 周波数カウント |
| `jq '.key'` | JSON クエリ |
| `xargs -P8 -n1 cmd` | 並列操作 |

## バックアップネットワーク

| コマンド | 使い方 |
|---|---|
| `ss -tulpn` | リスニングポート + プロセス |
| `curl -sI url` | ヘッダーのみ |
| `curl -w '%{time_total}\n' -o /dev/null -s url` | リクエストのタイミング |
| `scp file user@host:/path` | SSHをコピー |
| `ssh -L 8080:localhost:80 host` | ローカルポート転送 |
| `tcpdump -i any -n host x` | パケットキャプチャ |
| `mtr host` | ライブトレースルート |

## ⚙️ プロセス

| コマンド | 使い方 |
|---|---|
| `ps aux | grep proc` | プロセスを探す |
| `htop` / `btop` | インタラクティブモニター |
| `kill -9 PID` | フォースキル |
| `lsof -p PID` | プロセスが開いているファイル |
| `nohup cmd &` | 総合ログアウト |
| `systemctl status svc` | サービス状態 |

## 💾ディスク&システム

| コマンド | 使い方 |
|---|---|
| `df -h` | ファイルシステム利用 |
| `free -h` | メモリー |
| `uname -a` | カーネル情報 |
| `dmesg | tail` | カーネルメッセージ |
| `lsblk` | ブロックデバイス |
| `mount | column -t` | マウントファイルシステム |

## 🔐 許可

| コマンド | 使い方 |
|---|---|
| `chmod 755 file` | rwx オーナー様・ rx 様向け | `chmod 755 file` | `chmod 755 file` | rwx オーナー様・ rx 様向け |
| `chown user:group file` | オーナーシップ |
| `sudo !!` | 最後のコマンドを root で再実行 |
| `visudo` | 安全疑惑編集 |

## 📦 アーカイブ

| コマンド | 使い方 |
|---|---|
| `tar -xzf f.tar.gz` | エキストラ |
| `tar -czf out.tar.gz dir/` | クリエイト | クリエイト |
| `zip -r out.zip dir/` | ジップ |
| `7z x f.7z` | 7-Zip エキスプレス |

## ⚡ 生産性

| コマンド | 使い方 |
|---|---|
| `Ctrl-R` | ファジー歴史検索 |
| `!!` | 最後のコマンドを繰り返す |
| `!$` | 最後の引数 |
| `alias ll='ls -lah'` | エイリアス ライブ |
| `tldr cmd` | 実用マンページ |
| `bat file` | 羽根付き猫 |
| `watch -n2 cmd` | 全て走る |

## ディスク & ファイル (extras)

| コマンド | 使い方 |
|---|---|
| `ncdu` | インタラクティブディスク使用ブラウザ |
| `tree -L 2` | ディレクトリツリー |
| `fdupes -r dir` | 重複の検索 |
| `stat file` | フルメタデータ |

## 投稿許可と所有権 (extras)

| コマンド | 使い方 |
|---|---|
| `chmod g+s dir` | スティッキーグループ継承 |
| `getfacl file` | ファイングラインド ACL |
| `chattr +i file` | 不変(rootも編集できません) |
| `umask 022` | 既定の許可マスク |

## 🐛 分解と防腐性

| コマンド | 使い方 |
|---|---|
| `strace -c cmd` | シコールサマリー | 所要時間 |
| `ltrace cmd` | ライブラリーコールトレース |
| `perf top` | CPUホットスポットライブ |
| `journalctl -fu svc` | サービスログのフォロー |
| `dmesg -w` | カーネルメッセージを見る |

## パッケージ

| コマンド |
|---|---|
| Debian/Ubuntu | `apt search`, `apt show`, `dpkg -L pkg` |
| フェドラ | `dnf list installed` | `dnf provides file` |
| アーカイブ | `pacman -Ss` | `pacman -Ql pkg` |
| macOS | `brew info`, `brew services list` | macOS | `brew info`, `brew services list` | macOS | `brew info`, `brew services list` | macOS | macOS | `brew info`, `brew services list`, `brew services list` | macOS | macOS | macOS | `brew info`, `brew services list` | macOS | macOS | macOS | macOS | `brew info`, `brew info`, `brew services list`, `brew services list` | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS | macOS |

## スケジューリング

| コマンド | 使い方 |
|---|---|
| `crontab -e` | cronジョブの編集 |
| `at now +1 hour` | ワンショット遅延タスク |
| `systemd-run --on-calendar="Mon 09:00"` | システムタイマー |
| `sleep 300 && cmd &` | ポアマンのスケジューラ |

## 🧵 パレルリズム

| コマンド | 使い方 |
|---|---|
| `cmd1 & cmd2 & wait` | 背景+お待ち |
| `xargs -P8 -n100 cmd` | 並列バッチ |
| `parallel -j+0 'cmd {}' ::: a b c` | GNU パラレル |

---
## 貢献

プルリクエストを歓迎します。レビューしてマージします。[aixisstudio](https://github.com/aixisstudio) による管理 — オープンソースのアプリケーションファイアウォール [Snitch](https://github.com/aixisstudio/Snitch) の作者です。

## ライセンス: MIT
