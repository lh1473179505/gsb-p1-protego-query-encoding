# Offline development environment

Python ≥3.10 (verified on 3.11/3.12). The trial uses the upstream source without functional patches.

Recreate the environment:

```sh
python3 -m venv .venv
.venv/bin/python -m pip install -U pip
.venv/bin/python -m pip install -r requirements-trial.txt
.venv/bin/python -m pip install --no-build-isolation --no-deps -e .
```

Run the offline regression suite from the repository root:

```sh
.venv/bin/python -m pytest -q tests
```

The baseline result is: 4406 passed in 10.43s.
External network is not required for this suite.
