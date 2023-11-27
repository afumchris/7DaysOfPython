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

This code creates a Flask application and defines a single route for the root URL (/). When the user visits the URL, the hello_world() function is called and returns the string 'Hello, World!'. Below is the codes breakdown:

  - Importing Flask: `from flask import Flask`, This line imports the `Flask` class from the Flask module. Flask is a web framework for Python.
  - Creating an Application Instance: `app = Flask(__name__)`, This line creates an instance of the Flask class, typically named `app`. The `__name__` argument is used to determine the root path for the application.
  - Defining a Route and a View Function:
    ```python
    @app.route('/')
    def hello_world():
    return 'Hello, World!'
    ```
      - `@app.route('/')`: This is a decorator that associates the URL path `'/'` with the `hello_world` function. When a user accesses the root path of the application (e.g., `http://localhost:5000/`), Flask will invoke the associated function.
      - `def hello_world():`: This is a view function that will be executed when the specified route is accessed. In this case, it returns the string `'Hello, World!'`.


## Working with databases:

The majority of online applications need some sort of permanent storage, and Python offers a number of modules and frameworks for doing so. Popular options include Django ORM, Peewee, and SQLAlchemy. Here is an illustration of how to work with a SQLite database using SQLAlchemy:

``` python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///test.db'
db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(50))

@app.route('/')
def index():
    users = User.query.all()
    return render_template('index.html', users=users)
```
This code creates a SQLite database and a User table using SQLAlchemy. The index() function queries the database for all users and passes them to the template for rendering.

   


    



