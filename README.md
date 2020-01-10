# Before you begin (Python >= 3.7)

## pipenv

### Install pipenv

If `pipenv` is not yet installed, please do by `brew install pipenv` or `pip install pipenv`.
To bootstrap the project after pipenv is installed, do `pipenv install`. To activate the python virtual environment use `pipenv shell`

### Activate python shell with pipenv

This project uses `pipenv` to manage the python environment. And should be initialized with `Python>=3.7` by doing:
`pipenv --python 3.7`

## pre-commit hook

This project also uses `pre-commit` hook to do autoformat with `black` and lint with `autopep8`. To initialize the `pre-commit`, please install by `brew install pre-commit` or `pip install pre-commit`, and then do `pre-commit` install

### Formatter

Uses `black`

### Linter

Uses `flake8`

### Mypy

This project uses mypy to have a typed hint and checks in the codebase. This will create the codebase to be more maintainable

### Vscode

There exists a `.vscode` folder that will contain the standard settings for this project that will configure the formatter and linter.
The default settings are:

```json
{
  "editor.formatOnSave": true,
  "python.linting.flake8Enabled": true,
  "python.linting.enabled": true,
  "python.formatting.provider": "black",
  "python.linting.mypyEnabled": true
}
```
