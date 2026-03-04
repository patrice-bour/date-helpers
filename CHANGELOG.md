# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2025-11-11

First stable release of Date Helpers - a comprehensive date toolkit for Obsidian with keyboard-first interaction, natural language parsing, and full internationalization support.

### Added

#### Core Features
- **Exclusive Modes**: Choose between Text formatting or Daily Notes wikilinks
  - Text mode: Insert formatted dates as plain text (e.g., "2025-11-11")
  - Daily Notes mode: Insert wikilinks to Daily Notes (e.g., `[[01_Journal/2025-11-11|November 11, 2025]]`)
  - Mode-aware commands and behavior
  - Seamless migration from Phase 5 dual-mode system

#### Natural Language Parsing (NLP)
- Parse date expressions in natural language:
  - Relative: "today", "tomorrow", "yesterday", "3 days ago", "in 2 weeks"
  - Weekdays: "next Monday", "last Friday", "this Wednesday"
  - Time expressions: "tomorrow at 2pm", "next Monday at 14:30"
- **6 languages supported**:
  - 🇬🇧 English (fully tested)
  - 🇫🇷 French (fully tested)
  - 🇩🇪 German (basic support)
  - 🇯🇵 Japanese (basic support)
  - 🇵🇹 Portuguese (basic support)
  - 🇳🇱 Dutch (basic support)
- **Auto-detect language**: Automatically detect language from input text
- **Parsing modes**: Casual (permissive) or Strict (conservative)
- **Fallback behaviors**: Configurable handling of unparseable text

#### Interactive Date Picker
- Calendar modal with month/year navigation
- **Keyboard shortcuts**:
  - Arrow keys: Navigate days
  - `Cmd/Ctrl + ←/→`: Navigate months
  - `Cmd/Ctrl + ↑/↓`: Navigate years
  - `Enter`: Select date
  - `Esc`: Cancel
- Locale-aware display (month names, day names, week start)
- Format selector (in Text mode)
- `@@` trigger character for inline insertion

#### Daily Notes Integration
- Generate wikilinks to Daily Notes with customizable aliases
- Support for custom Daily Notes folder and format
- Auto-create Daily Note if missing (optional)
- Alias format presets:
  - ISO 8601 (2025-11-11)
  - Locale Long (November 11, 2025)
  - Locale Short (11/11/2025)
  - And more...

#### Format Presets
- **11 built-in presets** across 3 categories:
  - **Date**: ISO 8601, Locale Short, Locale Long, Verbose, Short Month
  - **Time**: 24-hour, 12-hour, 24-hour with seconds
  - **DateTime**: ISO DateTime, Readable, Standard
- Custom preset support (planned for future release)
- Preset commands accessible in both modes

#### Internationalization (i18n)
- **Full locale support** for date formatting via Luxon
- Auto-detect locale from Obsidian settings
- Manual locale override in plugin settings
- Customizable week start day (Sunday, Monday, Saturday)
- Locale-aware format presets

### Technical Improvements
- **344 automated tests** (89.65% code coverage)
- TypeScript strict mode for type safety
- Comprehensive settings validation with safe fallbacks
- Automatic settings migration from Phase 5
- Desktop + Mobile support
- Build system: esbuild (dev) + Rollup (production)
- Code quality: ESLint + Prettier
- Bundle size: ~898 KB (includes Luxon + chrono-node)

### Documentation
- Comprehensive architecture documentation
- Phase-by-phase implementation guides
- Manual testing plans and checklists
- Contributing guidelines
- Technical decision records

## [0.1.0] - 2025-11-04

### Added
- Initial development release (Phases 0-5)
- Foundation: TypeScript setup, Jest testing, build pipeline
- Core date operations with Luxon
- Basic NLP parsing with chrono-node
- Date picker modal
- Daily Notes integration (dual-mode system)

### Changed
- N/A (initial release)

### Deprecated
- N/A

### Removed
- N/A

### Fixed
- N/A

### Security
- N/A

---

## Development Phases

This plugin was developed in structured phases:

- **Phase 0** (Foundation): Project setup, TypeScript, Jest, build system
- **Phase 1** (Core Operations): DateService, FormatterService, format presets, settings UI
- **Phase 2** (Date Picker): Interactive calendar modal with keyboard shortcuts
- **Phase 2.1** (Improvements): macOS-friendly shortcuts, year navigation
- **Phase 3** (NLP Basic): Natural language parsing with chrono-node
- **Phase 4** (NLP Advanced): Auto-detect language, parsing modes, datetime support
- **Phase 5** (Daily Notes): Wikilink generation, alias formatting, auto-create
- **Phase 6** (Exclusive Modes): Simplified UX with Text XOR Daily Notes modes
- **Phase 7** (Release v1.0): Community submission and documentation

---

## [Unreleased]

Features planned for future releases:

- Custom format presets (user-defined)
- Date range insertion
- Relative date adjustment commands ("shift date forward 3 days")
- Template variable support
- Additional NLP refiners and customization
- Performance optimizations

---

## Links

- [GitHub Repository](https://github.com/patrice-bour/obsidian-date-helpers)
- [Issue Tracker](https://github.com/patrice-bour/obsidian-date-helpers/issues)
- [Obsidian Community Plugins](https://obsidian.md/plugins?id=date-helpers)
