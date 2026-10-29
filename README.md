# Back-End-Development-Pictures

Flask Pictures REST service based on the IBM Skills Network starter template.

## Implemented endpoints

GET /health, GET /count, GET /picture, GET /picture/<id>, POST /picture,
PUT /picture/<id>, and DELETE /picture/<id>.

## Local verification

Tested with Python 3.12 in `.venv312`, Flask 2.1.2 and Werkzeug 2.1.2.
Run `python -m pytest -v` from an environment with Flask, Werkzeug and pytest installed.
All 11 supplied tests pass. State is held in memory and resets on restart.

## Cloud lab setup

The original `bin/setup.sh` is included for the course Cloud IDE setup.
Pictures was built and deployed to IBM Code Engine; its API is used by the deployed Django application.

Implementation assistance: OpenAI Codex.

## Environment Setup

This repository was created from the IBM Skills Network starter template:
https://github.com/ibm-developer-skills-network/luggb-Back-End-Development-Pictures
The starter was cloned locally and the implemented source published here.

The revised `bin/setup.sh` was successfully executed in the Cloud IDE using
the official `python:3.9.16-slim` container (Python 3.9.16). It creates the
`backend-pics-venv` virtual environment, installs requirements, and runs `pip check`.
The observed result was `No broken requirements found.` followed by
`Environment setup completed successfully: backend-pics-venv`.

```bash
bash bin/setup.sh
source backend-pics-venv/bin/activate
python --version
```

For the same isolated setup used during verification:
```bash
docker run --rm -v "$PWD:/app" -w /app python:3.9.16-slim bash bin/setup.sh
```
The setup script avoids modifying global shell configuration or starting an unrelated database.
