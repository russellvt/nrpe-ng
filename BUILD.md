# Building and Installing NRPE-NG from Source

Currently NRPE-NG is not a package that is easily installable directly
from [PyPi](https://pypi.org/) - but I am working to update the package
to be more PyPi friendly. This document is intended to help others along
similar paths, as well as a place for me to track that migration, as it
happens.

##  Virtual Environments

It is highly recommended that when working with this package (or any
other current Python3 package/module), that you use [the built-in "venv"
module](https://docs.python.org/3/library/venv.html) to separate your
Python environments from each other, as well as from your system's
default Python installation, itself.

For my own tinkerings, I'm going to use a "dev" environment created
under Python 3.9, while I work on cleaning up the module. By definition,
this is more than you'd need or want in a production system. So, I have
started by splitting up the "requirements" files between what `nrpe-ng`
needs, and what we use in our development environment.

So, to construct the build environment, all I need is something like:

```
python3 -m venv venv-nrpe-ng
pip install pip --upgrade
pip install -r requirements-dev.txt
```

Note that the gitignore file automatically ignores anything named with
the four letters "venv" (so it won't be checked in to your repostiory).

## Building NRPE-NG

The "old days" of Python (primarily Python2 and early Python3), modules
were generally build with a `setup.py` script. However, [this has largely been
depracated](https://blog.ganssle.io/articles/2021/10/setup-py-deprecated.html)
(and for good reason - read the link if you want to know more about the
history).

Right now, you can use the Python Build module to compile `nrpe-ng` in
to and installable module. The `requirements-dev.txt` file contains the
list of modules you'll need, and is installed with `pip`, above.

Then, simply:

```
python3 -m build 
```

You'll end up with something like the following new files:

```
./nrpe_ng.egg-info/
./nrpe_ng.egg-info/top_level.txt
./nrpe_ng.egg-info/PKG-INFO
./nrpe_ng.egg-info/SOURCES.txt
./nrpe_ng.egg-info/dependency_links.txt
./nrpe_ng.egg-info/requires.txt
./nrpe_ng.egg-info/entry_points.txt
./dist/
./dist/nrpe-ng-0.2.0.tar.gz
./dist/nrpe_ng-0.2.0-py3-none-any.whl
```

