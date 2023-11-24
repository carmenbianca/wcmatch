[![Donate via PayPal][donate-image]][donate-link]
[![Discord][discord-image]][discord-link]
[![Build][github-ci-image]][github-ci-link]
[![Coverage Status][codecov-image]][codecov-link]
[![PyPI Version][pypi-image]][pypi-link]
[![PyPI Downloads][pypi-down]][pypi-link]
[![PyPI - Python Version][python-image]][pypi-link]
![License][license-image-mit]
# Wildcard Match

## Overview

Wildcard Match provides an enhanced `fnmatch`, `glob`, and `pathlib` library in order to provide file matching and
globbing that more closely follows the features found in Bash. In some ways these libraries are similar to Python's
builtin libraries as they provide a similar interface to match, filter, and glob the file system. But they also include
a number of features found in Bash's globbing such as backslash escaping, brace expansion, extended glob pattern groups,
etc. They also add a number of new useful functions as well, such as `globmatch` which functions like `fnmatch`, but for
paths.

Wildcard Match also adds a file search utility called `wcmatch` that is built on top of `fnmatch` and `globmatch`. It
was originally written for [Rummage](https://github.com/facelessuser/Rummage), but split out into this project to be
used by other projects that may find its approach useful.

Bash is used as a guide when making decisions on behavior for `fnmatch` and `glob`. Behavior may differ from Bash
version to Bash version, but an attempt is made to keep Wildcard Match up with the latest relevant changes. With all of
this said, there may be a few corner cases in which we've intentionally chosen to not *exactly* mirror Bash. If an issue
is found where Wildcard Match seems to deviate in an illogical way, we'd love to hear about it in the
[issue tracker](https://github.com/facelessuser/wcmatch/issues).

## Features

A quick overview of Wildcard Match's Features:

- Provides an interface comparable to Python's builtin in `fnmatch`, `glob`, and `pathlib`.
- Allows for a much more configurable experience when matching or globbing with many more features.
- Adds support for `**` in glob.
- Adds support for escaping characters with `\`.
- Add support for POSIX style character classes inside sequences: `[[:alnum:]]`, etc. The `C` locale is used.
- Adds support for brace expansion: `a{b,{c,d}}` --> `ab ac ad`.
- Adds support for expanding `~` or `~username` to the appropriate user path.
- Adds support for extended match patterns: `@(...)`, `+(...)`, `*(...)`, `?(...)`, and `!(...)`.
- Adds ability to match path names via the path centric `globmatch`.
- Provides a `pathlib` variant that uses Wildcard Match's `glob` library instead of Python's default.
- Provides an alternative file crawler called `wcmatch`.
- And more...

## Installation

Installation is easy with pip:

```
pip install wcmatch
```

## Documentation

https://facelessuser.github.io/wcmatch/

## License

MIT


[github-ci-image]: https://github.com/facelessuser/wcmatch/workflows/build/badge.svg?branch=main&event=push
[github-ci-link]: https://github.com/facelessuser/wcmatch/actions?query=workflow%3Abuild+branch%3Amain
[codecov-image]: https://img.shields.io/codecov/c/github/facelessuser/wcmatch/main.svg?logo=codecov&logoColor=aaaaaa&labelColor=333333
[codecov-link]: https://codecov.io/github/facelessuser/wcmatch
[pypi-image]: https://img.shields.io/pypi/v/wcmatch.svg?logo=pypi&logoColor=aaaaaa&labelColor=333333
[pypi-down]: https://img.shields.io/pypi/dm/wcmatch.svg?logo=pypi&logoColor=aaaaaa&labelColor=333333
[pypi-link]: https://pypi.python.org/pypi/wcmatch
[python-image]: https://img.shields.io/pypi/pyversions/wcmatch?logo=python&logoColor=aaaaaa&labelColor=333333
[license-image-mit]: https://img.shields.io/badge/license-MIT-blue.svg?labelColor=333333
[donate-image]: https://img.shields.io/badge/Donate-PayPal-3fabd1?logo=paypal
[donate-link]: https://www.paypal.me/facelessuser
