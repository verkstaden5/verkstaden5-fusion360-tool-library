# Changelog

All notable changes to this tool library are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2026-07-21

### Fixed
- Library failed to import in Autodesk Fusion after the July 2026 release
  ("Failed to import 1 out of 1 tool libraries"). The rewritten tool-library
  loader rejects any tool whose feeds-and-speeds preset list is empty. Six PCB
  end mills (E6, E7, E8, E9, E10, E11) shipped with an empty preset list, which
  caused the entire file to be rejected on import.

### Added
- An "FR4 / PCB" starting preset for each of the six PCB end mills, tuned for
  24 000 rpm. Chip loads scale with diameter (0.010–0.035 mm/tooth); the
  DLC-coated variants run ~20 % higher feed. These are conservative starting
  values intended to be verified against a test cut and adjusted.

### Notes
- Tool geometry is unchanged; no tools were added, removed or renamed.
- The internal Fusion schema version in the file (`"version": 35`) is unchanged —
  it is Fusion's own format version, separate from this library's release version.

### Known issues
- Two tools share the name `V-D6.0-TD0.2-30°-F4` (tool numbers 110 and 111) with
  differing feeds. They import fine but are indistinguishable by name in Fusion.
  To be resolved in a future release (rename, merge, or remove one).

## [1.0.0] - 2026-04-28

### Added
- Initial published tool library for Verkstaden 5: 111 carbide tools
  (flat, ball, tapered and chamfer mills) for CNC milling, with feeds and
  speeds presets for wood, plastic, composite and aluminium.

[1.1.0]: https://github.com/USER/REPO/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/USER/REPO/releases/tag/v1.0.0
