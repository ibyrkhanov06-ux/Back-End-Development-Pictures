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
Cloud setup and deployment have not yet been verified.

Implementation assistance: OpenAI Codex.
