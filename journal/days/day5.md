# Day 5 - Web development in Python

Python is quite capable when it comes to web development, and there are a variety of frameworks and modules are available for it. These can be used to create web applications.
Flask, Django, and Pyramid are a few well-known frameworks. The choice of framework will rely on the project's requirements. Each of these frameworks has advantages and disadvantages of its own.

## Creating a basic web app using Flask:

Creating a basic web application using Flask: Flask is a micro web framework for Python that is easy to learn and use. It provides a simple way to create web applications and APIs using Python. Here are some examples of Flask code for creating a basic web application:


``` python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!' 
```



