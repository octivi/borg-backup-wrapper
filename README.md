# BorgBackup Wrapper

[![license](https://img.shields.io/github/license/octivi/borg-backup-wrapper)](https://choosealicense.com/licenses/mit/)

`borg-backup-wrapper` is a wrapper for the  deduplicating archiver [BorgBackup](https://www.borgbackup.org/), designed to simplify everyday tasks across multiple repositories.

BorgBackup is an excellent archiver offering deduplication, compression, and encryption.

## Install

1. This wrapper requires [Octivi Bash Boilerplate (OBB)](https://github.com/octivi/bash-boilerplate). Fetch raw
   [`octivi-bash-boilerplate`](https://github.com/octivi/bash-boilerplate/blob/main/octivi-bash-boilerplate) and save it
   as `/usr/local/share/octivi-bash-boilerplate`:

   ```bash
   curl -L https://raw.githubusercontent.com/octivi/bash-boilerplate/main/octivi-bash-boilerplate | sudo tee /usr/local/share/octivi-bash-boilerplate > /dev/null
   ```

2. Fetch raw [`borg-backup`](https://github.com/octivi/borg-backup-wrapper/blob/main/borg-backup) script, save it as
   `/usr/local/bin/borg-backup` and grant execution (x) permissions:

   ```bash
   curl -L https://raw.githubusercontent.com/octivi/borg-backup-wrapper/main/borg-backup | sudo tee /usr/local/bin/borg-backup > /dev/null
   sudo chmod +x /usr/local/bin/borg-backup
   ```

## Alternatives

- [Borgmatic](https://github.com/borgmatic-collective/borgmatic)

## License

All content is licensed under the terms of [The MIT License](LICENSE).
