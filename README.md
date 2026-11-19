# Flask REST Tutorial

A small Flask tutorial for reading JSON requests and returning JSON responses. The question list lives in the server process and resets when it restarts.

## Run locally

Use Python 3.11 and Pipenv.

```sh
pipenv sync
pipenv run python app.py
```

Open http://127.0.0.1:5000/questions to list questions. To add one, send a JSON payload with a `name` field.

```sh
curl -X POST http://127.0.0.1:5000/questions \
  -H "Content-Type: application/json" \
  -d '{"name":"What should we build next?"}'
```

[`app.py`](app.py) defines both routes. The development server binds to localhost with debugging disabled. If adapting the tutorial for deployment, use a production WSGI server and add authentication and input validation.
