# 📦 pip - Python package installer(Deep dive)
> `pip` is pythons official package manager.if python is sword, 'pip' is the armory behind it.

## What is pip?
- `pip` stands for **"Pip installs packages"**
- It installs libraries from the **Python Package index(PyPI)** by default 
-It supports:
    - Installing, uninstalling, upgrading packages
    - dependency resolution
    - working with requirement files


---

## common commands
bash
pip install <package-name>              #install a package

pip uninstall <package-name>  #uninstall a package

pip list   #list all the packages

pip show <package-name> #info about a specific package

pip freeze  #exact versions(used in requirements.txt)

pip install -r requirements.txt #install packages from file

# Install a specific version:
> pip install requests==2.25.1

# upgrade a package:
> pip install --upgrade numpy

# save installed packages:
> pip freeze > requirements/txt

# install from github:
> pip install git+https://github.com/psf/requests.git

# local package in editabe mode
> pip install -e.

## 🧠 Pro Tips
# Tip	Description
- --no-cache-dir	Prevents pip from caching packages
- --no-deps	Skip installing dependencies
- --pre	Allow pre-release versions
- --upgrade-strategy eager	Upgrades sub-dependencies too
- pip  check	Checks for broken dependencies

## bts
- `pip` installs packages into:
    - the active virtualenv
    - or the system-wide Python site-pacakges

> python -m site    

## security 
- use pip install --require-hashes to lock in exact versions + integrity
- run pip-audit to check for vulnerabilities
