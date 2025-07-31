# Automated Python Linter with Ruff ⚙️

![Workflow Status](https://github.com/varunventra/Push-Ruff-Action/actions/workflows/linter.yml/badge.svg)

A simple GitHub Action workflow that automatically lints and formats Python code using Ruff on every push to the `main` branch. This is a learning project to understand repository automation and CI/CD basics for code quality.

## How to Use This Workflow

To use this automated workflow in your own project, follow these steps:

1.  In your repository, create a directory named `.github/workflows/`.
2.  Copy the `linter.yml` file from this project into that directory.
3.  Commit and push the new file.

That's it. The action will now run automatically on every push to your `main` branch, checking your code with Ruff's default settings.

## The Workflow Explained

This repository is configured to run a check on every push to the `main` branch. The workflow performs the following steps:

1.  Checks out the repository's code.
2.  Sets up a specific version of Python.
3.  Installs Ruff.
4.  Runs `ruff check .` to find potential errors.
5.  Runs `ruff format --check .` to verify the code's style.
6.  The workflow will pass if no issues are found, or fail if Ruff reports any problems.

## Technology Used

* [Python](https://www.python.org/)
* [Ruff](https://docs.astral.sh/ruff/)
* [GitHub Actions](https://github.com/features/actions)