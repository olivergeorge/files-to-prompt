# Changelog

All notable changes to this project will be documented in this file.

## [0.6.2] - 2025-10-23

### Changed
- Non-existent paths are now skipped with a warning instead of causing an error
- XML wrapper (`<documents>`) is now written before processing paths, ensuring valid output even when some paths don't exist

### Fixed
- Tool now tolerates references to files that don't exist in the filesystem, useful when piping from commands like `find`

## [0.6.1] - 2025-10-23

### Fixed
- Added explicit package discovery configuration to prevent build errors when test directories exist in project root
- Configured setuptools to only include `files_to_prompt` package and exclude test directories

### Changed
- Added uv as alternative setup method in development documentation

## [0.6] - 2024

### Added
- Support for nested `.gitignore` files

### Changed
- `-m` is now a shortcut for `--markdown`

## [0.5] - 2024

### Added
- Support for reading paths from stdin
- `--null` / `-0` flag to use NUL character as separator when reading from stdin

### Changed
- `--ignore` patterns now include directory names unless `--ignore-files-only` is specified
- Documented fnmatch pattern syntax

### Fixed
- Dropped Python 3.8 testing, added Python 3.13

## [0.4] - 2024

### Added
- `-e` / `--extension` flag to filter files by extension
- `--line-numbers` / `-n` flag to add line numbers to output
- UTF-8 encoding to output file handling

### Fixed
- Formatting in `--help` output
- Short flag for Claude XML output in README

## [0.3] - 2024

### Added
- `-o` / `--output` option to write output to a file

### Changed
- Switched to more recent Claude XML format

## [0.2.1] - 2024

### Fixed
- Warn and continue on binary files instead of failing

## [0.2] - 2024

### Added
- `--cxml` flag for Claude XML format output
- `--ignore` flag (renamed from `--ignore-patterns`) to ignore file patterns
- Support for multiple files and paths as arguments

## [0.1] - 2024

### Added
- Initial release
- Basic file concatenation functionality
- Recursive directory traversal
- Hidden file handling with `--include-hidden`
