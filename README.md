# 👖🐍🍪 Pants Python Cookiecutter

A Cookiecutter template for Python projects managed with the [Pants](https://www.pantsbuild.org/) bulid system.

## Quick start

1. `pip install cookiecutter`
2. `cookiecutter gh:MichalOleszak/pants-python-cookiecutter`
3. Fill-in project details as requested by the prompt. 

## About

Recently, I have repeatedly found myself recreating boilerplate code to set up Python projects. This template is intended to save myself some time. It sets up a Pants-managed Python repo including some continuous integration features:

* pre-commit hooks,
* PR validation using GitHub Actions,
* linting of GitHub PR titles.

See the project's [default README]({{cookiecutter.project_slug}}/README.md) for more details.

If you find it useful, please let me know!

This project is created and maintained by [Michal Oleszak](michaloleszak.com).

