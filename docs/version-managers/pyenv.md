# pyenv

Simple Python version management

- [github.com/pyenv/pyenv](https://github.com/pyenv/pyenv){:target="_blank"}

## Installation

[pyenv installer](https://github.com/pyenv/pyenv-installer){:target="_blank"} is used to install [pyenv](https://github.com/pyenv/pyenv){:target="_blank"} and [friends](https://github.com/pyenv/pyenv-virtualenv){:target="_blank"}.

```shell
curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
```

Restart your shell so the path changes take effect.

```shell
exec $SHELL
```

## Configuration

Zsh note: Modify your ~/.zshrc file instead of ~/.bashrc.

```shell
$ vim ~/.bashrc
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

Restart your shell so the path changes take effect.

```shell
exec $SHELL
```

## Usage

### Create Virtual Environment

```shell
pyenv install 3.8.12
pyenv virtualenv 3.8.12 <virtualenv>-3.8.12
pyenv local <virtualenv>-3.8.12
pyenv shell <virtualenv>-3.8.12
```

### Integration with visual studio code

Open the command palette in each project and change the interpreter.

- Python: Select Interpreter
- Jupyter: Select Interpreter to start Jupyter server

Open Kernel Options in your Jupyter notebook and change the interpreter.

- Select kernel

### Troubleshooting

Python command not found.

```shell
$ vim ~/.bashrc
alias python="$(pyenv which python)"
alias pip="$(pyenv which pip)"
```

If the virtual environment does not appear in the interpreter, reopen the file or terminal.

## Commands

Lists all Python versions known to pyenv.

```shell
pyenv versions
```

To list the all available versions of Python, including Anaconda, Jython, pypy, and stackless.

```shell
pyenv install --list
```

Then install the desired versions.

```shell
pyenv install 3.8.12
```

Sets the global version of Python.

```shell
pyenv global 3.8.12
exec $SHELL
python --version
```

Using pyenv virtualenv with pyenv.

```shell
pyenv virtualenv 3.8.12 <virtualenv>-3.8.12
```

Sets a local application-specific Python version by writing the version name to a .python-version file in the current directory.

```shell
pyenv local <virtualenv>-3.8.12
```

Sets a shell-specific Python version by setting the PYENV_VERSION environment variable in your shell.

```shell
pyenv shell <virtualenv>-3.8.12
```

Activate and deactivate a pyenv virtualenv manually.

```shell
pyenv activate <virtualenv>-3.8.12
pyenv deactivate
```

Uninstall a specific Python version.

```shell
pyenv uninstall <virtualenv>-3.8.12
```

## Command Reference

Like git, the [pyenv command](https://github.com/pyenv/pyenv/blob/master/COMMANDS.md){:target="_blank"} delegates to subcommands based on its first argument.
