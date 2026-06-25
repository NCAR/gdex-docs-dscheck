Read the Docs documentation for dscheck
=======================================

Read the tutorial here:

https://docs.readthedocs.io/en/stable/tutorial/

This user guide repo is for

https://github.com/NCAR/rda-python-dscheck

The latest documentation for this repo can be viewed at

https://gdex-docs-dscheck.readthedocs.io

Publishing a new version
------------------------

When ``dscheck.usg`` is changed in https://github.com/NCAR/rda-python-dscheck, a
GitHub Actions workflow automatically converts it into the ``section*.rst`` files
and opens a pull request from the ``automated-update-branch`` branch against the
``main`` branch of this repository. The same workflow also syncs the version
number from ``rda-python-dscheck`` into ``pyproject.toml`` (from which
``docs/source/conf.py`` reads it).

To publish the documentation as the latest version, review and merge that
automatically generated pull request into ``main``. Read the Docs then rebuilds
and serves the merged content as the ``latest`` version.

To publish the documentation as the ``stable`` version on Read the Docs, create a
GitHub release. Tagging and releasing the merged ``main`` branch produces a
tagged, versioned build, and Read the Docs serves the latest release as the
``stable`` version (in addition to ``latest``).
