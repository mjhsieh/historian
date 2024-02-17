# historian changelog

## 0.0.4


* General Improvements
  - Tests are ported from travis to github action
  - Alleviates awk issue on the macOS
  - Fixes ZSH compatibility issues
  - Alleviates issues with simultaneous hist imports
  - locale improvement

* New Features
  - support of zsh history import with timestamp
  - support of export/zshexport so it can be appended to the history file

## 0.0.3

* General Improvements
  - Simplify subcommand invocation
  - Remove unused variables
  - Revamp zsh and bash import
  - shellcheck-proof test scripts
  - Print long messages with heredocs
  - Invoke bash with `#!/usr/bin/env`

* SQLite Improvements
  - Abstract sqlite invocations to `historian_sqlite()`
  - Normalize sqlite invocation options

* New Features
  - Add multiple search argument support for `cmd_search`
  - Add bi-temporal time support with import metadata
  - Add .historianrc for configurable metadata
  - Format hist search results in a nicer way
  - Tag sqlite timestamps as timestamps
  - Import from bash and zsh history simultaneously

* Bug Fixes
  - Fail in hist import if no input files were found

## 0.0.2

* Renames global variables to `HISTORIAN_SRC`, `HISTORIAN_DB`,
  `HISTORIAN_SQLITE3` and makes them overridable from outside the
  script

* Fixes import delimiter bug to allow for backtick (but disallow 0x01)

## 0.0.1

* Initial implementation
