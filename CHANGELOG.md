# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),  
and this project adheres to [Semantic Versioning](https://semver.org/).

---

## [v0.1.0] - 2025-04-11

### Added
- Initial implementation of `gh-unpushed` GitHub CLI extension
- `gh unpushed` shows unpushed commits on the current Git branch
- `--remote` / `-r` flag for specifying a remote on demand
- `--set-remote` / `-sr` for setting a default remote
- `--help` / `-h` displays usage, options, and examples
- `--version` / `-v` flag added, reads from `VERSION` file
- Improved error messaging when remote branch does not exist
