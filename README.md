# Install dependencies
## Install homebrew: 
https://www.funkyspacemonkey.com/how-to-install-homebrew-on-m1-macs-running-macos-monterey

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

To check: 

```
brew --version
```

Expect:
```
Homebrew 3.6.11
Homebrew/homebrew-core (git revision 6b5f0c30885; last commit 2022-11-15)
Homebrew/homebrew-cask (git revision 686a535347; last commit 2022-11-15)
```

## Install python:

```
brew install python
```

To check: 
```
python3 --version
```

Expect:
```
Python 3.9.13
```

## Install pipenv: 
https://docs.python-guide.org/dev/virtualenvs/#virtualenvironments-ref

```
brew install pipenv
```

To check: 
```
pipenv --version
```

Expect:
```
/opt/homebrew/Cellar/pipenv/2022.9.24/libexec/lib/python3.11/site-packages/pipenv/vendor/attr/_make.py:876: RuntimeWarning: Running interpreter doesn't sufficiently support code object introspection.  Some features like bare super() or accessing __class__ will not work with slotted classes.
set_closure_cell(cell, cls)
pipenv, version 2022.9.24
```

## Install virtualenv:

```
brew install virtualenv
```

To check:
```
virtualenv --version
```

Expect:
```
virtualenv 20.16.7 from /opt/homebrew/Cellar/virtualenv/20.16.7/libexec/lib/python3.10/site-packages/virtualenv/__init__.py
```

## Create a virtual environment for a project:

```
cd [project_folder]
```
```
virtualenv venv
```

### Use python 3 in our virtual environment:

```
virtualenv -p /usr/bin/python3 venv
```

### Inside our project, it needs to be activated:

```
source venv/bin/activate
```

## Install Anaconda:

```
brew install --cask anaconda
```

### Add in ~/.zshrc:

```
export PATH="[environment location]/bin:$PATH"
```

### To get the environment location:

```
brew install --cask anaconda
==> Downloading https://repo.anaconda.com/archive/Anaconda3-2022.10-MacOSX-arm64.sh
Already downloaded: /Users/ajurado/Library/Caches/Homebrew/downloads/855f17415a9c99a94a8116fab49149b0823c24a243c85d8b853063a127f4c16c--Anaconda3-2022.10-MacOSX-arm64.sh
==> Installing Cask anaconda
==> Running installer script 'Anaconda3-2022.10-MacOSX-arm64.sh'
PREFIX=/opt/homebrew/anaconda3
Unpacking payload ...
Collecting package metadata (current_repodata.json): ...working... done                                               
Solving environment: ...working... done

## Package Plan ##

  environment location: /opt/homebrew/anaconda3
```

```
source ~/.zshrc
```

To check:

```
conda --version
```
Expect:
```
conda 22.9.0
```

## Install Pandas
```
conda install pandas
```

## VSCode plugins:

- Python.

Then, when running a code in a file ```.ipynb``` it will suggest you to install all the other plugins for Jupyter in one click (Jupyter, Jupyter Keymap, Jupyter notebook renderers, Pylance)



