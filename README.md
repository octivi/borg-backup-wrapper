# BorgBackup Wrapper

[![GitHub Releases](https://img.shields.io/github/v/release/octivi/borg-backup-wrapper?sort=semver)](https://github.com/octivi/borg-backup-wrapper/releases)
[![License: MIT](https://img.shields.io/github/license/octivi/borg-backup-wrapper)](https://choosealicense.com/licenses/mit/)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org/)
[![Semantic Versioning](https://img.shields.io/badge/SemVer-2.0.0-blue)](https://semver.org/spec/v2.0.0.html)

`borg-backup-wrapper` is a wrapper around the deduplicating archiver [BorgBackup](https://www.borgbackup.org/)
that streamlines everyday tasks across multiple repositories.

BorgBackup is an excellent archiver offering deduplication, compression, and encryption.

## Requirements

- Bash 4.4 or newer.
- `borg` installed and available in `PATH`.
- [Octivi Bash Boilerplate (OBB)](https://github.com/octivi/bash-boilerplate) is embedded in the `borg-backup` script, so no separate OBB installation is required.

## Install

### Manual

Just download

```bash
# or https://github.com/octivi/borg-backup-wrapper/releases/latest/download/borg-backup if you always want the latest release
curl -fsSLO https://github.com/octivi/borg-backup-wrapper/releases/download/v1.1.0/borg-backup \
  && curl -fsSL https://github.com/octivi/borg-backup-wrapper/releases/download/v1.1.0/borg-backup.sha256 \
  | sha256sum -c - \
  && sudo install -m 0755 borg-backup /usr/local/bin/borg-backup \
  || { echo "Checksum verification failed; aborting installation." >&2; exit 1; }
```

### Ansible

One simple task to install `borg-backup`

```yaml
- name: "Install Borg Backup Wrapper"
  ansible.builtin.get_url:
    # or https://github.com/octivi/borg-backup-wrapper/releases/latest/download/borg-backup if you always want the latest release
    url: "https://github.com/octivi/borg-backup-wrapper/releases/download/v1.1.0/borg-backup"
    dest: "/usr/local/bin/borg-backup"
    owner: "root"
    group: "root"
    mode: "0755"
    # or https://github.com/octivi/borg-backup-wrapper/releases/latest/download/borg-backup.sha256 if you always want the latest release
    checksum: "sha256:https://github.com/octivi/borg-backup-wrapper/releases/download/v1.1.0/borg-backup.sha256"
  register: "__borg_backup_wrapper_download"
  until: __borg_backup_wrapper_download is succeeded
  retries: 5
  delay: 2
```

## Quick start

Example `borg-backup` configuration file:

```bash
# /etc/borg-backup.conf
BORG_REPO="ssh://backup@example.com:22/./repo-hostname"
BORG_PASSPHRASE="replace-with-a-strong-passphrase"

BORG_BASE_DIR="/var/lib/borg-backup"
BORG_ARCHIVE_NAME="{hostname}-{now:%Y-%m-%dT%H:%M:%S}"
BORG_COMPRESSION="zstd,6"

BORG_KEEP_YEARLY=5
BORG_KEEP_MONTHLY=24
BORG_KEEP_WEEKLY=52
BORG_KEEP_DAILY=30
BORG_KEEP_HOURLY=168

BORG_PATHS=(
  "/etc"
  "/home"
  "/var/www"
)

BORG_OPTIONS_CREATE=(
  "--one-file-system"
  "--exclude=/proc"
  "--exclude=/sys"
  "--exclude=/dev"
  "--exclude=/run"
  "--exclude=/tmp"
)
```

Initialize a repository, then run a normal backup cycle:

```bash
sudo borg-backup -c /etc/borg-backup.conf init
sudo borg-backup -c /etc/borg-backup.conf create+prune+check
```

## Alternatives

- [Borgmatic](https://github.com/borgmatic-collective/borgmatic)

## License

All content is provided under the terms of [The MIT License](LICENSE).
