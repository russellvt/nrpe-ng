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

    python3 -m venv venv.nrpe-ng
    . ./venv.nrpe-ng/bin/activate
    pip install --upgrade pip setuptools wheel

This now gives you a self-contained virtual environment in the `venv`
directory.

To activate the environment, simply source the `activate` file in the
`venv.nrtpe-ng/bin` directory (similar to above). This will preprend
the `bin` directory to your system path as well as update your prompt
(to remind you that you're in a `venv`).

Running `nrpe-ng` will require that this environment is properly
activated prior to invoking the daemon.

Python venv also provides `activate` scripts for csh, fish and
PowerShell in that same `bin` directory.

You can simply run the `activate` tool to remove the `venv` environment
from your system variables in your current shell.


## Installing from source code control

If you use the `venv` setup, above, as suggested, you can continue with
the general Pythonic installation within this distribution.

    pip install -r requirements.txt
    python setup.py install

You should now have `nrpe-ng` in `venv.nrpe-ng/bin` directory.
