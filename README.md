# flask-blog-tutorial

This is a Python Flask tutorial for a workshop at Habibi Works. This workshop
will take one through setting up a basic Flask server, and then creating a very
basic blog page.

# Part 1: Getting Flask Setup

## Installation

We want to start off by setting up a basic flask server. To run flask, one must
have Python and pip installed.

[TODO: Add installation instructions].

## Running Flask

Now we'll start off by creating a file called `server.py` in this folder. As the
name suggests, this file will be where we write our server code. In this file,
we start off by importing Flask and initializing an application...

```[python]
from flask import Flask
app = Flask(__name__)
```

[TODO: Explain how those lines work]

[TODO: Explain what routes are]

Next, we want to respond to traffic to our website by adding a route for `/`. We
will respond by returning "Hello World!" to the client. We'll add the following
lines...

```[python]
@app.route('/')
def hello_world():
    return "Hello World!"
```

All together, `server.py` should have...

```[python]
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return "Hello World!"
```

Next, we will run our server. To do so, we need to set an environment variable
so that the computer knows where to find our server file. We can do so by
running the following lines in the terminal...

```[bash]
// For Linux and MacOS
$ export FLASK_APP=server.py

// For Windows CMD
C:\path\to\app>set FLASK_APP=server.py

// For Windows PowerShell
PS C:\path\to\app> $env:FLASK_APP = "server.py"
```

To run the server, we need to execute `flask run`. Now one can go to
`localhost:5000` in their browser and see their server!
