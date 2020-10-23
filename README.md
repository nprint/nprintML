# nprintML

nprintML is built to bridge the gap from nPrint, which generates standard fingerprints for packets, and autoML, which allows for optimized model training and traffic analysis. nprintML enables users with traffic and labels to perform optimized packet-level traffic analysis **without writing any code**.


## Getting It

### Dependencies

Python versions 3.6 through 3.8 are supported.

You might check what versions of Python are installed on your system _e.g._:

    ls -1 /usr/bin/python*

As needed, consult your package manager or [python.org](https://python.org/).

Depending on your situation, consider [pyenv](https://github.com/pyenv/pyenv) for easy installation and management of arbitrary versions of Python.

### Installation

nprintML itself is available for download from the [Python Package Index (PyPI)](https://pypi.org/) and via `pip`:

    python -m pip install nprintml

This downloads, builds and installs the `nprintml` console command. If you're happy to manage your Python (virtual) environment, you're all set with the above.

That said, installation of this command via a tool such as [pipx](https://pipxproject.github.io/pipx/) is strongly encouraged. pipx will ensure that nprintML is installed into its own virtual environment, such that its third-party libraries do not conflict with any others installed on your system.

(Note that nprint and nprintML are unrelated to the PyPI distribution named "nprint.")


## Using It

nprintML supplies the top-level shell command `nprintml`.

In case of command path ambiguity and in support of debugging, the `nprintml` command is identically available through its Python module (no different from `pip` above):

    python -m nprintml ...

---

THIS IS HOW YOU USE IT!


## Development

Development requirements may be installed via the `dev` extra (below assuming a source checkout):

    pip install --editable .[dev]

(Note: the installation flag `--editable` is also used above to instruct `pip` to place the source checkout directory itself onto the Python path, to ensure that any changes to the source are reflected in Python imports.)

Development tasks are then managed via [`argcmdr`](https://github.com/dssg/argcmdr) sub-commands of `manage …`, (as defined by the repository module `manage.py`), _e.g._:

    manage version patch -m "initial release of nprintml" \
           --build                                        \
           --release
