# Python Environments
There are several options available to manage python environments. In this article, I am going to show how to use `pyenv` and `pipenv` to use a python environment

# pyenv
`pyenv` can be used to install multiple versions of Python on a machine and use a version required.
* `pyenv install 3.11.4` - installs a specific version of python
* `pyenv install --list` - shows the list of python versions installed using `pyenv`
* `pyenv local 3.11.4` - sets the version of python to 3.11.4 to current directory and its sub directories
* `pyenv shell 3.11.4` - sets the version of python to 3.11.4 in the current shell
* `echo "3.11.4" > .python-version` - this is similar to `pyenv local 3.11.4`

# pipenv
* `pip install --user pipenv` - install `pipenv` using the version of python managed by `pyenv`
* `pipenv --python /Users/username/.pyenv/versions/3.11.4/bin/python` - explicitly telling `pipenv` to use a specific version of python
* `pipenv install matplotlib` - installs a python package using pipenv, it also creates Pipfile and Pipfile.lock in the directory this command is executed from
* `pipenv --venv` - shows the virtual environment created using `pipenv`. This command should be executed from the same location where a Pipfile exists. Virtual environments managed by `pipenv` is created at `~/.local/share/virtualenvs/<name-of-virtual-env>`. Name of virtual environment is prefixed with the name of the folders this command is executed from.
* `pipenv shell` - this will activate the virtual environment created by the above command
