# Software quality

Software quality checks are important for a healthy community.
They make software easier to modify, and in the case of code formatters, can eliminate
unproductive debates.


## Docstrings and autodoc

We use docstrings on components of our software's public API and use "autodoc" tools to
generate API documentation from docstrings as the source of truth.


## Typechecking

We use type annotations and type checkers to:

* protect us from bugs as early in the  development cycle as possible.
* make our code more self-documenting
* stay in line with modern Pythonic conventions;
  [typechecking is strongly adopted by the Python community](https://pyrefly.org/blog/why-typed-python/).
* enable easier and safer refactoring of code.

We use [mypy](https://mypy-lang.org/) for typechecking and aim to enable
[strict mode](https://mypy.readthedocs.io/en/stable/config_file.html#confval-strict) for
all projects.


## Code linting

Linters help avoid common programming pitfalls and readability problems.

We use [Ruff](https://docs.astral.sh/ruff/) for linting and aim to enable as many rules as possible.


## Code formatting

Using a code formatter can eliminate
[bikeshedding](https://en.wikipedia.org/wiki/Law_of_triviality) about code style.

We use [Ruff](https://docs.astral.sh/ruff/) for code formatting.


## Unit tests

We use unit tests to exercise our code and ensure its behavior matches expectations.

We use [pytest](https://docs.pytest.org) for testing.

We use [pytest-cov](https://pypi.org/project/pytest-cov/) to measure test coverage and
aim for a reasonable standard of coverage.


## Spelling

To help identify common spelling errors, we use
[Codespell](https://github.com/codespell-project/codespell).


## Automations

We use [pre-commit](https://pre-commit.com) to automate running code quality tools.

We only set up fast tools like Ruff with pre-commit, otherwise the commit process
becomes annoying.

We use [pre-commit.ci](https://pre-commit.ci) to automate pre-commit checks in PRs.

We use GitHub Actions to automate all other quality checks.
