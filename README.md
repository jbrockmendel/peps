# peps
Brainstorming Python features

1) `from foo.bar import **`

Import the _entire_ `foo.bar` namespace, not just the specifically exposed
names.

When debugging, manually running a failing test, or otherwise trying to step
through code, it is often necessary to have non-public names available
in an interactive session.  These can be imported one at a time as needed,
(`from foo.bar import _baz`), but it would be convenient to get them all at
once.   `from foo.bar import **` seems like a natural extension to the
existing syntax to do that.
