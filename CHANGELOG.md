# Changelog

## [Unreleased] - 2026-02-18

### Changed

- Embed Octivi Bash Boilerplate directly in the wrapper to simplify distribution and keep runtime helpers available without external sourcing ([`1c91fe7`](https://github.com/octivi/borg-backup-wrapper/commit/1c91fe7)) (Marcin Engelmann)

### Added

- Add support for overriding the OBB library path via `OBB_LIB_PATH` ([`08606ff`](https://github.com/octivi/borg-backup-wrapper/commit/08606ff)) (Marcin Engelmann)

### Fixed

- Handle strict-mode failures without skipping exit reporting ([`94a161d`](https://github.com/octivi/borg-backup-wrapper/commit/94a161d)) (Marcin Engelmann)
- Show `usage()` output even when `borg` is not available in the environment ([`d525868`](https://github.com/octivi/borg-backup-wrapper/commit/d525868)) (Marcin Engelmann)

## [v1.0.0] - 2025-12-16

### Added

- Add the initial `borg-backup-wrapper` release ([`b78d8cb`](https://github.com/octivi/borg-backup-wrapper/commit/b78d8cb)) (Marcin Engelmann)

### Fixed

- Fix `recreate` behavior so it supports compression selection, does not require extra positional arguments, and reuses `create` command options correctly ([`0ee9f17`](https://github.com/octivi/borg-backup-wrapper/commit/0ee9f17), [`0d93e76`](https://github.com/octivi/borg-backup-wrapper/commit/0d93e76), [`f39c6b9`](https://github.com/octivi/borg-backup-wrapper/commit/f39c6b9)) (Marcin Engelmann)

[Unreleased]: https://github.com/octivi/borg-backup-wrapper/compare/v1.0.0...HEAD
[v1.0.0]: https://github.com/octivi/borg-backup-wrapper/releases/tag/v1.0.0
