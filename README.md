# Python Environments
There are several options available to manage python environments. In this article, I am going to show how to use `pyenv` and `pipenv` to use a python environment

# pyenv
`pyenv` can be used to install multiple versions of Python on a machine and use a version required.
* `pyenv install 3.11.4` - installs a specific version of python
* `pyenv install --list` - shows the list of python versions that can be installed using `pyenv`
* `pyenv versions` - shows the list of python versions installed using pyenv
* `pyenv local 3.11.4` - sets the version of python to 3.11.4 to current directory and its sub directories
* `pyenv global 3.11.4` - sets the version of python to 3.11.4 at a global scope
* `echo "3.11.4" > .python-version` - this is similar to `pyenv local 3.11.4`
* `pyenv which python` - should show the full version of python used by `pyenv`

# pipenv
`pipenv` is a tool for managing Python project environments, which wraps around the package manager, pip, and the virtual environment tool, venv or virtualenv
* `pip install --user pipenv` - install `pipenv` using the version of python managed by `pyenv`
* `pipenv --python /Users/username/.pyenv/versions/3.11.4/bin/python` or `pipenv --python $(pyenv which python)` - explicitly telling `pipenv` to use a specific version of python managed by `pyenv`
* `pipenv install matplotlib` - installs a python package using pipenv, it also creates Pipfile and Pipfile.lock in the directory this command is executed from
* `pipenv --venv` - shows the virtual environment created using `pipenv`. This command should be executed from the same location where a Pipfile exists. Virtual environments managed by `pipenv` is created at `~/.local/share/virtualenvs/<name-of-virtual-env>`. Name of virtual environment is prefixed with the name of the folders this command is executed from.
* `pipenv shell` - this will activate the virtual environment created by the above command
