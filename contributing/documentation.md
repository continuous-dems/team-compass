# Documentation

All of the team’s repositories are documented using the [Sphinx](https://sphinx-doc.org/) documentation engine with [MyST Markdown](https://myst-parser.readthedocs.io/). This page contains resources to help you understand [Sphinx](https://sphinx-doc.org/) and [MyST Markdown](https://myst-parser.readthedocs.io/) and the configurations we commonly use in our repositories.

## Building with `sphinx-build`
You can build the documentation locally with the `shpinx-build` CLI tool.

```bash
sphinx-build -E -b html docs/source/ docs/build/html
```
