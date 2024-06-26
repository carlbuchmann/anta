<!--
  ~ Copyright (c) 2023-2024 Arista Networks, Inc.
  ~ Use of this source code is governed by the Apache License 2.0
  ~ that can be found in the LICENSE file.
  -->

# Arista Network Test Automation (ANTA) Framework

| **Code**       | [![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff) [![Numpy](https://img.shields.io/badge/Docstring_format-numpy-blue)](https://numpydoc.readthedocs.io/en/latest/format.html) |
| :------------: | :-------|
| **License**    | [![License](https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg)](https://github.com/arista-netdevops-community/anta/blob/main/LICENSE) |
| **GitHub**     | [![CI](https://github.com/arista-netdevops-community/anta/actions/workflows/code-testing.yml/badge.svg)](https://github.com/arista-netdevops-community/anta/actions/workflows/code-testing.yml) ![Coverage](https://raw.githubusercontent.com/arista-netdevops-community/anta/coverage-badge/latest-release-coverage.svg) ![Commit](https://img.shields.io/github/last-commit/arista-netdevops-community/anta) ![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/m/arista-netdevops-community/anta) [![Github release](https://img.shields.io/github/release/arista-netdevops-community/anta.svg)](https://github.com/arista-netdevops-community/anta/releases/) [![Contributors](https://img.shields.io/github/contributors/arista-netdevops-community/anta)](https://github.com/arista-netdevops-community/anta/graphs/contributors) |
| **PyPi**       | ![PyPi Version](https://img.shields.io/pypi/v/anta) ![Python Versions](https://img.shields.io/pypi/pyversions/anta) ![Python format](https://img.shields.io/pypi/format/anta) ![PyPI - Downloads](https://img.shields.io/pypi/dm/anta) |

ANTA is Python framework that automates tests for Arista devices.

- ANTA provides a [set of tests](api/tests.md) to validate the state of your network
- ANTA can be used to:
    - Automate NRFU (Network Ready For Use) test on a preproduction network
    - Automate tests on a live network (periodically or on demand)
- ANTA can be used with:
    - As a [Python library](advanced_usages/as-python-lib.md) in your own application
    - The [ANTA CLI](cli/overview.md)

![anta nrfu](https://raw.githubusercontent.com/arista-netdevops-community/anta/main/docs/imgs/anta-nrfu.svg)

## Install ANTA library

The library will **NOT** install the necessary dependencies for the CLI.

```bash
# Install ANTA as a library
pip install anta
```

## Install ANTA CLI

If you plan to use ANTA only as a CLI tool you can use `pipx` to install it.
[`pipx`](https://pipx.pypa.io/stable/)  is a tool to install and run python applications in isolated environments. Refer to `pipx` instructions to install on your system.
`pipx` installs ANTA in an isolated python environment and makes it available globally.

**This is not recommended if you plan to contribute to ANTA**

```bash
# Install ANTA CLI with pipx
$ pipx install anta[cli]

# Run ANTA CLI
$ anta --help
Usage: anta [OPTIONS] COMMAND [ARGS]...

  Arista Network Test Automation (ANTA) CLI

Options:
  --version                       Show the version and exit.
  --log-file FILE                 Send the logs to a file. If logging level is
                                  DEBUG, only INFO or higher will be sent to
                                  stdout.  [env var: ANTA_LOG_FILE]
  -l, --log-level [CRITICAL|ERROR|WARNING|INFO|DEBUG]
                                  ANTA logging level  [env var:
                                  ANTA_LOG_LEVEL; default: INFO]
  --help                          Show this message and exit.

Commands:
  check  Commands to validate configuration files
  debug  Commands to execute EOS commands on remote devices
  exec   Commands to execute various scripts on EOS devices
  get    Commands to get information from or generate inventories
  nrfu   Run ANTA tests on devices
```

You can also still choose to install it with directly with `pip`:

```bash
$ pip install anta[cli]
```

## Documentation

The documentation is published on [ANTA package website](https://www.anta.ninja). Also, a [demo repository](https://github.com/titom73/atd-anta-demo) is available to facilitate your journey with ANTA.

## Contribution guide

Contributions are welcome. Please refer to the [contribution guide](contribution.md)

## Credits

Thank you to [Angélique Phillipps](https://github.com/aphillipps), [Colin MacGiollaEáin](https://github.com/colinmacgiolla), [Khelil Sator](https://github.com/ksator), [Matthieu Tache](https://github.com/mtache), [Onur Gashi](https://github.com/onurgashi), [Paul Lavelle](https://github.com/paullavelle), [Guillaume Mulocher](https://github.com/gmuloc) and [Thomas Grimonet](https://github.com/titom73) for their contributions and guidances.
