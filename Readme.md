# Simple Flask App

This project is a minimal Flask web application that serves a single page at the root URL.

## What the app does

The app creates a Flask application instance and defines a route for `/`.

When you open the homepage in a browser, the server responds with:

> Hello, World!

This is a very common beginner example used to demonstrate how Flask routes and views work.

## Project files

- `app.py` – contains the Flask app and the route definition

## Requirements

Before running the app, make sure Python and Flask are installed. Please use a virtual environment to install your dependences in this environment.

```bash
pip install flask
```

## Run the app

From the project folder, start the server:

```bash
python app.py
```

Then open this URL in your browser:

```text
http://127.0.0.1:5000/
```

You should see the text `Hello, World!` displayed.

## How it works

The main parts of the code are:

```python
from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "Hello, World!"
```

### Explanation

- `Flask(__name__)` creates the Flask application instance.
- `@app.route("/")` tells Flask that the function below should handle requests to the homepage.
- `return "Hello, World!"` sends the response text back to the browser.

The last section:

```python
if __name__ == "__main__":
    app.run(debug=True)
```

starts the web server when the script is run directly. The `debug=True` option enables debug mode, which is useful during development because it reloads the app automatically when code changes.

## Stopping the server

To stop the app, press:

```text
Ctrl + C
```

## Summary

This is a beginner-friendly Flask app that shows the basic structure of a web application:

- create a Flask app
- define a URL route
- return a response
- run the server
