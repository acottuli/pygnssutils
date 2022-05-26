# pygnssutils How to contribute

**pygnssutils** is a volunteer project and we appreciate any contribution, from fixing a grammar mistake in a comment to extending device test coverage or implementing new functionality. Please read this section if you are contributing your work.

Being one of our contributors, you agree and confirm that:

* The work is all your own.
* Your work will be distributed under a BSD 3-Clause License once your pull request is merged.
* You submitted work fulfils or mostly fulfils our coding conventions, styles and standards.

Please help us keep our issue list small by adding fixes: #{$ISSUE_NO} to the commit message of pull requests that resolve open issues. GitHub will use this tag to auto close the issue when the PR is merged.

If you're adding or amending UBX payload definitions or configuration database keys, it would be helpful to quote/hyperlink the documentation source (e.g. specific u-blox Interface Specification).

## Coding conventions

* This is open source software. Code should be as simple and transparent as possible. Favour clarity over brevity.
* The code should be compatible with Python >=3.7.
* The core code should be as generic and reusable as possible. We endeavour to limit the amount of processing dedicated to specific UBX message types, though this is sometimes unavoidable.
* Avoid external library dependencies unless there's a compelling reason not to.
* Code should be documented in accordance with [Sphinx](https://www.sphinx-doc.org/en/master/) docstring conventions.
* Code should formatted using [black](https://pypi.org/project/black/) (>= 20.8).
* We use and recommend Visual Studio Code with the Python extension for development and testing.
* We use and recommend [pylint](https://pypi.org/project/pylint/) (>=2.6.0) for code analysis.

## Testing

While we endeavour to test on as wide a variety of GNSS devices as possible, as a volunteer project we only have a limited number of devices available.

We use python's native unittest framework for local unit testing, complemented by the GitHub Actions automated build and testing workflow. We endeavour to have 100% code coverage.

Please write unittest examples for new code you create and add them to the `/tests` folder following the naming convention `test_*.py`.

We test on the following platforms using u-blox [NEO-6](https://www.u-blox.com/en/product/neo-6-series), [NEO-7](https://www.u-blox.com/en/product/neo-7-series), [NEO-8](https://www.u-blox.com/en/product/neo-m8-series) and [NEO-9](https://www.u-blox.com/en/product/neo-m9n-module) devices:
* Windows 11
* MacOS (Monterey)
* Linux (Ubuntu Jammy Jellyfish)
* Raspberry Pi OS (Bullseye)

## Submitting changes

Please send a [GitHub Pull Request to pygnssutils](https://github.com/semuconsulting/pygnssutils/pulls) with a clear list of what you've done (read more about [pull requests](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-pull-requests)). Please follow our coding conventions (above) and make sure all of your commits are atomic (one feature per commit).

Always write a clear log message for your commits. One-line messages are fine for small changes, but bigger changes should look like this:

    $ git commit -m "A brief summary of the commit
    > 
    > A paragraph describing what changed and its impact."



Thanks,

semuadmin