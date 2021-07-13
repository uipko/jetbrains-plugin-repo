############################
JETBRAINS PLUGIN REPO MIRROR
############################

.. image:: https://github.com/uipko/jetbrains-plugin-repo/actions/workflows/pylint.yml/badge.svg?branch=main
   :target: https://github.com/uipko/jetbrains-plugin-repo/actions/workflows/pylint.yml
   :alt: Pylint

.. image:: https://github.com/uipko/jetbrains-plugin-repo/actions/workflows/mypy.yml/badge.svg?branch=main
   :target: https://github.com/uipko/jetbrains-plugin-repo/actions/workflows/mypy.yml
   :alt: Mypy

.. image:: https://img.shields.io/badge/python-3.7+-blue.svg
   :alt: Python 3.7+
   :target: https://www.python.org/downloads/

*****************
Table of contents
*****************

- `Introduction`_

- `Installing`_
    - `Setup environment`_

- `Usage`_
    - `Run script`_
    - `Updating dependencies`_

- `Wishlist`_


************
Introduction
************
Simple scripts to mirror a given set of JetBrains plugins.

This script makes it easy to populate your own, offline, JetBrains Plugin library.

**********
Installing
**********
If you want to use this script just clone the repo and run it.

Go to an appropriate folder and clone this repository.

.. code:: bash

    $ git clone git@github.com:uipko/jetbrains-plugin-repo.git

Setup environment
=================
Setup an virtual environment and install the dependencies.

.. code:: bash

    $ python -m venv .venv && . .venv/bin/activate
    $ pip install -r requirements.txt

*****
Usage
*****

Run script
==========
Download plugins and generate updatePlugins.xml.

.. code:: bash

    $ python -u ./repo.py


Updating dependencies
=====================
After installing a new dependency run the following to update requirements.txt.

(See how it works out when we do not pin versions for the required dependencies.)

.. code:: bash

    $ pip-chill --no-version > requirements.txt

********
Wishlist
********
The following features must, should, could be implemented.

Must

* Define needed plugins
* Download all (or X most recent) versions of plugins
* Only download new versions
* Generate updatePlugins.xml
  - use relative paths or URL placeholder

Should

* Move config to config file
* create tests

Could

* Add other static type checkers (to test differences)
