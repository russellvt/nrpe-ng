# Install NRPE-NG

Currently a stub document for how to install nrpe-ng, particularly via
regular Python mechanisms.

## Virtual Environments

Python 3 intrroduced native virtual environments with the `venv`
module. Users are encouraged to use an isolated virtual environment
for services rather than depending (or modifying) the system Python
modules.

## Getting Started with venv

For this project, we are going to use `venv.nrpe-ng` as the directory
location. Most other modules tend to use the `venv` directory as the
default.

* `python3 -m venv venv.nrpe-ng`
* `. ./venv.nrpe-ng/bin/activate`
* `pip install --upgrade pip setuptools wheel`

This now gives you a self-contained virtual environment in the `venv`
directory. To activate the environment, simply source the `activate`
file in the `bin` directory (you will need to do this prior to running
the servive, as well). Once you are done working within the environment,
you only need to run the `deactivate` command (again within that same
`bin` directory - which should be on your path)... and that will return
your environment to default.

