# Linux Commands

[English](README.md) | **Français** | [Español](README.es.md) | [中文](README.zh-CN.md) | [日本語](README.ja.md) | [Русский](README.ru.md)

La référence de commandes Linux/Unix que tu utilises vraiment

Fichiers & Navigation

Commande Utilisation
|---|---|
Liste avec tailles et fichiers cachés
Fichiers par nom et âge
`fd pattern`: Un `find` rapide moderne
D'abord, les plus gros répertoires
`rsync -avh --progress src/ dst/`: Copie fidèle avec progrès
Symlien

Traitement de texte

Commande Utilisation
|---|---|
Recherche récursive
`rg "pattern"`. — instant, respecte .gitignore.
`sed -i 's/old/new/g' file`
`awk '{print $2}'`
`cut -d: -f1 /etc/passwd`
Nombre de fréquences
Demande JSON
Commande parallèle par ligne

Réseau

Commande Utilisation
|---|---|
`ss -tulpn`: Ports d'écoute + processus
En-têtes seulement
`curl -w '%{time_total}\n' -o /dev/null -s url`=Délais de demande
Copier sur SSH
`ssh -L 8080:localhost:80 host`
`tcpdump -i any -n host x`= Capture de paquets
`mtr host`=Live traceroute=

Processus

Commande Utilisation
|---|---|
Rechercher un processus
`htop` / `btop`
`kill -9 PID`
`lsof -p PID`. Fichiers un processus tient ouvert.
`nohup cmd &`?Logout de survie
État du service

Système & disque

Commande Utilisation
|---|---|
Utilisation du système de fichiers
Mémoire
`uname -a`
Messages du noyau
Dispositifs de bloc
Systèmes de fichiers montés

Autorisations

Commande Utilisation
|---|---|
`chmod 755 file`=Rwx pour le propriétaire, rx pour les autres
Propriété
Ré-exécuter la dernière commande comme root
`visudo`

Archives

Commande Utilisation
|---|---|
Extrait de `tar -xzf f.tar.gz`
Créer
`zip -r out.zip dir/`
Extrait de 7-Zip

Productivité

Commande Utilisation
|---|---|
Recherche d'historique flou
Répète la dernière commande
Dernier argument
Les Aliases vivent dans ~/.bashrc
`tldr cmd`) Pages d'homme pratiques
`bat file`: chat avec ailes
Exécuter tous les 2s

Disque et fichiers (extras)

Qu'est-ce qui se passe ?
|---|---|
`ncdu`= Navigateur interactif d'utilisation du disque
`tree -L 2`= Arbre de répertoire
Rechercher des duplicatas
`stat file`=Métadonnées complètes

Droits et propriété (extras)

Qu'est-ce qui se passe ?
|---|---|
`chmod g+s dir`: L'héritage du groupe collant
`getfacl file`=LAC à grains fins
`chattr +i file` : rendre immuable (root ne peut même pas éditer)
`umask 022`: Masque de permission par défaut

Débogue et observabilité

Qu'est-ce qui se passe ?
|---|---|
Récapitulatif Syscall — où va le temps
`ltrace cmd`=Ligne d'appel de la bibliothèque
CUP points chauds live
`journalctl -fu svc`.Suivez les journaux de service.
Voir les messages du noyau

Les paquets

Commandement Distro
|---|---|
Debian/Ubuntu: `apt search`, `apt show`, `dpkg -L pkg`
Fedora, `dnf list installed`, `dnf provides file`
`pacman -Ss`, `pacman -Ql pkg`
CdPH0X, CdPH1X

Calendrier

Qu'est-ce qui se passe ?
|---|---|
Éditer les emplois de cron
Une seule prise de vue a retardé la tâche.
`systemd-run --on-calendar="Mon 09:00"`
`sleep 300 && cmd &`: L'horaire des pauvres

Parallélisme

Qu'est-ce qui se passe ?
|---|---|
Contexte + attente
`xargs -P8 -n100 cmd`
GNU parallèle

---
## Contribuer

Les pull requests sont les bienvenues : ouvre une PR, elle sera relue et fusionnée. Maintenu par [aixisstudio](https://github.com/aixisstudio), auteur de [Snitch](https://github.com/aixisstudio/Snitch), pare-feu applicatif open source.

## Licence: MIT
