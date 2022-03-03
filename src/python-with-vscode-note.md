
# Setup VS Code

Use "Ctrl+Shift+P" to invoke Command Palette, for configuration of interpreter, color theme, and etc.

Use "Ctrl+`" to launch Terminal, Debug Console, and etc.

For executing commands, use "Ctrl+Shift+P" to open new terminal by selecting "Terminal: Create New Terminal".

Use "Ctrl+Shift+P" to select Python interpreter by selecting "Python: Select Interpreter".

# Configure & Use Packages

PIP is a package manager for Python. It is usually installed with Python environment. Common used commands includes:

```shell
# check PIP version
pip --version

# download install Python package (module)
pip install matplotlib

# uninstall Python package
pip uninstall matplotlib

# list all installed packages
pip list
```

# Virtual Environments

In Python, different applications can use different virtual environments. The module used to create and manage virtual environments is called venv, which comes with Python installation.

```shell
# create a virtual environment "demo-env"
# command will create a directory "demo-env" under current directory
venv demo-env

# activate virtual environment
{.\Scripts} activate

# deactivate virtual environment
{.\Scripts} deactivate
```

Once activating the virtual environment, the line below "{.\Scripts} activate" command will has "({env-name})" as prefix.

Once deactivating the virtual environment, the "({env-name})" prefix will disappear.

```shell
# verify if virtual environment is activated
pip -V
```

After activating the virtual environment, command "pip -V" will give the path of current workspace: "{env-name}\lib\site-packages\pip ({python-version})", instead of the Python installation path.

```shell
# install module in virtual environment
pip intall matplotlib
```

After installation, all modules will be installed within the "{env-name}\Lib\site-packages".
