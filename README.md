# Devilfish Flotilla

## Prerequisites

- [Python 3](https://www.python.org/)
- [Virtualenv](https://virtualenv.pypa.io/)

## Virtual Environment

In the `devilfish-flotilla` directory run

    virtualenv venv

This creates a directory `venv` that holds the virtual environment's data. To enter the virtual environment run

    source venv/bin/activate

We can see that we are inside the virtual environment because the shell prompt has a `(venv)` prefix. Now, install the necessary software.

    pip3 install sphinx

To leave the virtual environment run

    deactivate

## Build

In the virtual environment run:

    make html
