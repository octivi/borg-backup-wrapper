# BorgBackup Wrapper

[![license](https://img.shields.io/github/license/octivi/borg-backup-wrapper)](https://choosealicense.com/licenses/mit/)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org/)
[![semver](https://img.shields.io/badge/SemVer-2.0.0-blue)](https://semver.org/spec/v2.0.0.html)


`borg-backup-wrapper` is a wrapper around the deduplicating archiver [BorgBackup](https://www.borgbackup.org/)
that streamlines everyday tasks across multiple repositories

BorgBackup is an excellent archiver offering deduplication, compression, and encryption.

## Installation

### Manual

Just download [Octivi Bash Boilerplate (OBB)](https://github.com/octivi/bash-boilerplate)
and `borg-backup-wrapper` and grant execution (x) permission to `borg-backup`

```
# or https://github.com/octivi/bash-boilerplate/releases/latest/download/octivi-bash-boilerplate if you want always latest release
sudo curl -fsSLo /usr/local/share/octivi-bash-boilerplate https://github.com/octivi/bash-boilerplate/releases/download/v1.0.0/octivi-bash-boilerplate

# or https://github.com/octivi/borg-backup-wrapper/releases/latest/download/borg-backup
sudo curl -fsSLo /usr/local/bin/borg-backup-wrapper https://github.com/octivi/borg-backup-wrapper/releases/download/v1.0.0/borg-backup
sudo chmod +x /usr/local/bin/borg-backup
```

### Ansible

Two simple tasks to install `borg-backup-wrapper`

```
- name: 'Install Octivi Bash Boilerplate (OBB)'
  ansible.builtin.get_url:
    # or https://github.com/octivi/bash-boilerplate/releases/latest/download/octivi-bash-boilerplate if you want always latest release
    url: 'https://github.com/octivi/bash-boilerplate/releases/download/v1.0.0/octivi-bash-boilerplate'
    dest: '/usr/local/share/bash-boilerplate'
    owner: 'root'
    group: 'root'
    mode: '0644'
    # or https://github.com/octivi/bash-boilerplate/releases/latest/download/octivi-bash-boilerplate.sha256 if you want always latest release
    checksum: 'sha256:https://github.com/octivi/bash-boilerplate/releases/download/v1.0.0/octivi-bash-boilerplate.sha256'
  register: '__bash_boilerplate_download'
  until: __bash_boilerplate_download is succeeded
  retries: 5
  delay: 2

- name: 'Install Borg Backup Wrapper'
  ansible.builtin.get_url:
    # or https://github.com/octivi/borg-backup-wrapper/releases/latest/download/borg-backup if you want always latest release
    url: 'https://github.com/octivi/borg-backup-wrapper/releases/download/v1.0.0/borg-backup'
    dest: '/usr/local/bin/borg-backup'
    owner: 'root'
    group: 'root'
    mode: '0755'
    # or https://github.com/octivi/borg-backup-wrapper/releases/latest/download/borg-backup.sha256 if you want always latest release
    checksum: 'sha256:https://github.com/octivi/borg-backup-wrapper/releases/download/v1.0.0/borg-backup.sha256'
  register: '__borg_backup_wrapper_download'
  until: __borg_backup_wrapper_download is succeeded
  retries: 5
  delay: 2
```

## Alternatives

- [Borgmatic](https://github.com/borgmatic-collective/borgmatic)

## License

All content is provided under the terms of [The MIT License](LICENSE).
