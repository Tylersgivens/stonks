# Local Login + Admin Web App

Simple Flask app designed for a Raspberry Pi Zero 2 W running on a local network.

## Features

- Login page with initial credentials: `user` / `password`.
- Session-based auth.
- Admin page for account management.
- Ability to create non-admin (or admin) accounts.
- SQLite database stored locally at `data/accounts.db`.

## Run

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

Open `http://<pi-ip>:8080` from another device on the same network.

## Security notes

- Change `SECRET_KEY` in production:
  ```bash
  export SECRET_KEY='set-a-strong-random-secret'
  ```
- Initial account is created only if it doesn't already exist.
