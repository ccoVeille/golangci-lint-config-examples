# Changelog

<!-- markdownlint-configure-file {
  "blanks-around-headings": false,
  "blanks-around-lists": false,
  "no-duplicate-heading": {
    "siblings_only": true
  }
} -->

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2025-03-31
### Changed
- convert everything to golangci-lint v2 configuration format
- sort results

### Fixed
- add missing `unused` linter
- add missing `revive.exported` linter

### Added
- 03-safe: usetesting & exptostd

## [1.1.0] - 2024-12-06
### Added
- 80-reckless
- 90-daredevil

### Changed
- 03-safe: fatcontext & loggercheck

## [1.0.2] - 2024-12-06
### Fixed
- version in .golangci.yml files

## [1.0.1] - 2024-09-01
### Fixed
- context-as-argument default setting should allow \*testing.T

### Changed
- added default revive linters explicitly in 02-basic

## [1.0.0] - 2024-06-29
### Added
- initial version
- LICENSE
