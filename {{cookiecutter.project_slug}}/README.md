# {{cookiecutter.project_name}}
{{cookiecutter.project_description}}

## Build system

This repository uses [Pants](https://www.pantsbuild.org/) as a build system. To set it up for the first time:

1. Run:
    ```bash
    make init
    ```
2. Add Pants to PATH: `PATH=$PATH:~/.local/bin:/builder/home/.local/bin/pants`
3. Create a lockfile for CI tools: `pants generate-lockfiles --resolve=ci_tools`

## Continuous Integration

Both in local pre-commit hooks and on a GitHub PR, the following checks are executed and required to pass:

* code formatting with Black
* code formatting with Flake8
* code formatting with Autoflake
* code formatting with Docformatter
* code formatting with isort
* unit tests with pytest
* static typing check with mypy

Additionally, GitHub PR title are required to start with one of the [allowed prefixes](ci/lint_pr_title.py). With the "squash and merge" merging strategy where PR titles become commit messages on main (recommended), this enforces cleaner commit history on main.


### Frequently used Pants commands

| | |
| ------------- | ------------- |
| `pants --version`  | check setup correctness by printing Pants version  |
| `pants lint ::`  | check code style (does not make changes)  |
| `pants fix ::` | fix code issues (makes changes) |
| `pants test ::` | run unit tests |
| `pants check ::` | check typing |
| `pants generate-lockfiles --resolve={resolve}` | generate lockfile for a resolve |
| `pants run {goal}` | run a Python script |
| `pants package {goal}` | build a Docker image |
| `pants publish {goal}` | build & push a Docker image |

## Author

This project is created and maintained by [{{cookiecutter.author}}]({{cookiecutter.author_url}}).