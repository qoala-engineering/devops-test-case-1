# Qoala Devops Test Case 1

# Before you begin (Python >= 3.8)

## pipenv

### Install pipenv

If `pipenv` is not yet installed, please do by `brew install pipenv` or `pip install pipenv`.
To bootstrap the project after pipenv is installed, do `pipenv install`. To activate the python virtual environment use `pipenv shell`

### Activate python shell with pipenv

This project uses `pipenv` to manage the python environment. And should be initialized with `Python>=3.8` by doing:
`pipenv --python 3.8`

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

# Instructions:

## Create deployable app with docker & docker-compose

The project consists of boto3, mypy, black formatter bootstrapping and a main file `create_s3_bucket.py`

- Create Dockerfile to run the project that will run the file `create_s3_bucket.py`
- Run a localstack
- Create `docker-compose.yml` file that will setup the [localstack](https://github.com/localstack/localstack) as well as running the the dockerized project
- The expectation of this finished project is that running the `docker-compose up` will run the `create_s3_bucket.py` python file with the following logs:
  - Success run log:
    ```
    list buckets created: ['test1', 'test2']
    list buckets after delete: []
    ```
  - Failed run log:
    ```
    Error: Could not connect to the endpoint URL: "http://localhost:4572/test1"
    ```
    or any other errors not matching the success run log

Please fork this repository and share us the link to your repository when you're done.
You can extend any of the scripts to introduce some features such as creating an API out of this.
