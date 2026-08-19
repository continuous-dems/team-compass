# Contributor Guide

Thank you for considering contributing to the Continuous DEMs Ecosystem! We welcome contributions from the community to help make geospatial data acquisition and processing easier for everyone.

Whether you're fixing a bug, adding a new data module, improving documentation, or participating in community governance, this guide will help you get started.

Specific [projects](/projects.md) may have information on contributing or other information about getting started.

## Connections
First off, get yourself connected with the Continuous-DEMs community online. There are a few places where we have conversations and discussion.

* The [Continuous-DEMs Zulip Chat Space](https://cudem.zulipchat.com). The Continuous-DEMs team uses this for most conversations.
* The `issues` section of the specific repositories Github page.

As a reminder, we expect all members of the Continuous-DEMs community to adhere to the Continuous-DEMs [Code of Conduct](/policies/code-of-conduct) in these conversations.

## Development Setup

1.  **Fork the Repository:** Click the "Fork" button on the top right of the repositories GitHub page.
2.  **Clone your Fork:**
    ```bash
    git clone https://github.com/<YOUR_USERNAME>/<PROJECT_NAME>.git
    cd fetchez
    ```
3.  **Create a Virtual Environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
4.  **Install the repository in Editable Mode:**
    ```bash
    pip install -e .
    ```

## Reporting Bugs

If you find a bug, please create a new issue on the repositories GitHub page. Include:
* The exact command you ran or api function you called.
* The error message / traceback if applicable.
* Your operating system and Python version.

With this information we should be able to recreate the bug and work to get it fixed!

## Improving Documentation

Great documentation is just as important as code! We want the Continuous-DEMs ecosystem to be accessible and understandable to everyone.

**How you can help:**
* **Fix Typos & Clarity:** Found a confusing sentence in the README or a typo in a docstring? Please fix it! Small changes make a big difference.
* **Add Examples:** Have a cool workflow using one of our projects? Please share it!
    * Create a Jupyter Notebook, a Markdown tutorial, or a simple shell script.
    * Submit it to the [Continuous-DEMs repository](https://github.com/continuous-dems.github.io) in it's `examples/` or `tutorials/` directory via a Pull Request.
* **Find Out More:** For more information on contributing documentation, refer to our [Documentation](/contributing/documentation) guidelines.

## Pull Request Guidelines

1.  **Branching:** Create a new branch for your changes (`git checkout -b feature/add-mydata`).
2.  **Coding Style:** Refer to our Community Compass policy on [Software Quality](/policies/software-quality/).
    * Follow PEP 8 guidelines.
    * Use type hints where possible.
    * Use existing geospatial utility functions from when possible.
    * Use `logging` instead of `print`.
3.  **Documentation:** Update the docstrings in your code. If you added a new module, ensure it has a class-level docstring describing it's purpose and usage.
4.  **Commit Messages:** Write clear, concise commit messages (e.g., "Add support for MyData API").
5.  **Pull Request:** Make a pull request to merge your branch into main.

## Contributions to a specific repository
Continuous-DEMs develops and maintains a number of open-source repositories and specific contributions may depend on the repoository you're working with.

To get oriented with a specific repository’s needs and process around making new contributions, look for a repository-specific contributing guide. This often comes in the form of a CONTRIBUTING.md file, or a contributing section of the documentation.

For example, here is the [contributing section](https://fetchez.readthedocs.io/en/latest/contribute/index.html) for the Fetchez project. Note that it covers some of the tools specific needs you’ll need for testing and developing code for Fetchez, which are not necessarily needed for other repositories.

Are the contributing docs unclear or misleading? Then please let us know! We try to make this documentation as helpful as possible, but we often don’t have the perspective of a new member to the community. Your input is extremely valuable in making it easy for others to join the Continuous-DEMs community!

— Based in part on contributing guidelines from the [JupyterHub](https://compass.hub.jupyter.org/contribute/guide/) project.
