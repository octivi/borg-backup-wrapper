# Changelog

## [Unreleased]

### Changed

- Expand documentation with a complete quick start, runtime requirements, and
  manual SHA256 verification guidance
  ([`4de1440`](https://github.com/octivi/borg-backup-wrapper/commit/4de1440),
  [`0d3c053`](https://github.com/octivi/borg-backup-wrapper/commit/0d3c053),
  [`4157aa9`](https://github.com/octivi/borg-backup-wrapper/commit/4157aa9),
  [`8db4ca8`](https://github.com/octivi/borg-backup-wrapper/commit/8db4ca8))
- Improve README clarity and project metadata (badges, syntax highlighting,
  links, and examples)
  ([`6419813`](https://github.com/octivi/borg-backup-wrapper/commit/6419813),
  [`779e177`](https://github.com/octivi/borg-backup-wrapper/commit/779e177),
  [`d3cc7c5`](https://github.com/octivi/borg-backup-wrapper/commit/d3cc7c5),
  [`f5cf2de`](https://github.com/octivi/borg-backup-wrapper/commit/f5cf2de),
  [`1fd1492`](https://github.com/octivi/borg-backup-wrapper/commit/1fd1492),
  [`534ad7a`](https://github.com/octivi/borg-backup-wrapper/commit/534ad7a))
- Improve repository automation for release, dependency, and yearly header
  maintenance workflows
  ([`0c67388`](https://github.com/octivi/borg-backup-wrapper/commit/0c67388),
  [`cd2d856`](https://github.com/octivi/borg-backup-wrapper/commit/cd2d856),
  [`7d081a3`](https://github.com/octivi/borg-backup-wrapper/commit/7d081a3),
  [`eeaec58`](https://github.com/octivi/borg-backup-wrapper/commit/eeaec58))

### Added

- Add support for overriding the OBB library path via `OBB_LIB_PATH`
  ([`08606ff`](https://github.com/octivi/borg-backup-wrapper/commit/08606ff))
- Add a dedicated security policy file
  ([`ee4403f`](https://github.com/octivi/borg-backup-wrapper/commit/ee4403f))
- Add installation instructions for Bash and Ansible
  ([`441d30f`](https://github.com/octivi/borg-backup-wrapper/commit/441d30f))

### Removed

- No user-facing removals.

### Fixed

- Handle strict-mode failures without skipping exit reporting
  ([`94a161d`](https://github.com/octivi/borg-backup-wrapper/commit/94a161d))
- Fix path and issue-link problems in documentation examples
  ([`7bdd1bc`](https://github.com/octivi/borg-backup-wrapper/commit/7bdd1bc),
  [`5f8b251`](https://github.com/octivi/borg-backup-wrapper/commit/5f8b251))
- Fix multiple CI workflow issues (quoting, regex matching, and workflow
  triggering)
  ([`a9182d6`](https://github.com/octivi/borg-backup-wrapper/commit/a9182d6),
  [`33b6686`](https://github.com/octivi/borg-backup-wrapper/commit/33b6686),
  [`5f4e3bb`](https://github.com/octivi/borg-backup-wrapper/commit/5f4e3bb),
  [`171f024`](https://github.com/octivi/borg-backup-wrapper/commit/171f024),
  [`d786fd0`](https://github.com/octivi/borg-backup-wrapper/commit/d786fd0))

## [1.0.0] - 2025-12-16

### Changed

- Improve overall README wording and clarity
  ([`b23ac63`](https://github.com/octivi/borg-backup-wrapper/commit/b23ac63),
  [`a8d5c2b`](https://github.com/octivi/borg-backup-wrapper/commit/a8d5c2b))
- Improve CI quality checks and testing workflow defaults
  ([`09c9e4e`](https://github.com/octivi/borg-backup-wrapper/commit/09c9e4e),
  [`55dcda1`](https://github.com/octivi/borg-backup-wrapper/commit/55dcda1),
  [`f27b99e`](https://github.com/octivi/borg-backup-wrapper/commit/f27b99e))

### Added

- Publish the first stable release of `borg-backup-wrapper`
  ([`b78d8cb`](https://github.com/octivi/borg-backup-wrapper/commit/b78d8cb),
  [`527d44d`](https://github.com/octivi/borg-backup-wrapper/commit/527d44d),
  [`f355b1b`](https://github.com/octivi/borg-backup-wrapper/commit/f355b1b))

### Removed

- No user-facing removals.

### Fixed

- Fix `recreate` so it does not require additional arguments and correctly
  reuses `create` options
  ([`0d93e76`](https://github.com/octivi/borg-backup-wrapper/commit/0d93e76),
  [`f39c6b9`](https://github.com/octivi/borg-backup-wrapper/commit/f39c6b9))
- Allow selecting the compression algorithm for the `recreate` command
  ([`0ee9f17`](https://github.com/octivi/borg-backup-wrapper/commit/0ee9f17))

<!-- Reference links (recommended) -->

[Unreleased]: https://github.com/octivi/borg-backup-wrapper/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/octivi/borg-backup-wrapper/releases/tag/v1.0.0
