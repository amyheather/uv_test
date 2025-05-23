## Install uv

linux: curl -LsSf https://astral.sh/uv/install.sh | sh

from: https://docs.astral.sh/uv/getting-started/installation/

check installed by running: uv version

## Create new uv project

uv init

this created:
.
├── .python-version
├── README.md
├── main.py
└── pyproject.toml

## Run main.py

uv run main.py

>> Using CPython 3.10.14 interpreter at: /home/amy/mambaforge/bin/python3.10
Creating virtual environment at: .venv
Hello from uv-test!

Whenever use uv run, it checks that everything is up-to-date: lockfile matches pyproject.toml, environment matches lockfile.

Can use `uv sync` to manually update.

## Add packages

uv add simpy

uv add pytest

## Change python version

nano .python-version

change the version in there

then run uv sync

## Export to requirements.txt

Possible but they recommend against it... just use lock file.

## Add specific package version

uv add nbqa==1.9.0

## Files

pyproject.toml - simpler list, just those you said uv add, with versions, either >= or == if specified

uv.lock - full details on every package in environment
