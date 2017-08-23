# rsc.io/goversion

Goversion scans a directory tree and, for every executable it finds, prints
the Go version used to build that executable.

Usage:

    goversion [-crypto] [-v] path...

The list of paths can be individual files or directories; if the latter,
goversion scans all files in the directory tree, not following symlinks.

Goversion scans inside of tar or gzipped tar archives that it finds (named
`*.tar`, `*.tar.gz`, or `*.tgz`), but not recursively.

The `-crypto` flag causes goversion to print additional information about the
crypto libraries linked into each executable.

The `-v` flag causes goversion to print information about every file it
considers.
