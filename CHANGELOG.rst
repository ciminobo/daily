===========
 Changelog
===========
All notable changes to daily will be documented in this file.

The format is based on `Keep a Changelog <https://keepachangelog.com/en/1.0.0/>`_,
and this project adheres to `Semantic Versioning <https://semver.org/spec/v2.0.0.html>`_.

[0.2.0] - 2022-02-18
====================
This release adds the ability to perform batch additions / editing of entries,
fixes a couple of bugs, and changes the versioning of the project to use
single-source versioning. package.bash and setup.py will now determine the
version of daily from git-describe. Daily can now print its own version via
the ``--version`` option.

Added
-----
- Batch editing of entries.
- ``--version`` option to print the version of daily.
- Filter options to the "add" subcommand.
- Entries now display with an ID. This ID may not be searched on.

Changed
-------
- Version update methodology. Simply update the CHANGELOG with the new version
  when cutting a new release and then push a git tag named after that version.

Fixed
-----
- `daily show` not processing the `-d, --date` option.
- Bug in Journal.entry_filter function where providing only args.date
  would return all entries.
- Improper handling of `-d, --date` options in parsergroups.
- Package description in DEBIAN/control.

[0.1.0-alpha] - 2021-07-08
==========================
First release of "daily". There are a couple of known bugs and the features are
bare, but this release constitutes a minimal viable product as I envisioned
the program when I started. Each command has a functional "happy path", so
the program is operational.

Added
-----
- Installation and packaging logic for pywheel, deb, rpm, and gz.
- README for development instructions.
- General structure for manpages.
- General structure for unittests.
- Tab completion for all of daily (bash only).
- Basic configuration file and logic to fill in missing command-line args
  with those from the configuration file.
- Structure for argument parsing logic.
- pycodestyle configuration.
- Wrote man pages.
- Implemented the "add", "show", "refresh", and "upcoming" commands.
- Licensed under GPLv2.
