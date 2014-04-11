=============================
Large Applications with Flask
=============================

by spectralsun 

revised: 04/11/2013

http://spectralsun.com

.. figure:: /_static/images/flask-logo.png
    :align: center

source: https://github.com/spectralsun/spectralsun-slides

Prerequisite Knowledge
======================

Having this knowledge is recommended, but may not be necessary for you to gain value:

* Python
* Pip

Having this knowledge is optional, but with it you may gain more value:

* Flask/Django
* Virtual Environments (virtualenv)
* SQL/SQLAlchemy
* HTML/CSS/Javascript

Simple Server
=============

.. code-block:: bash

    /appname
        main.py
        /static
            style.css
        /templates
            index.jinja
            ...

main.py:

.. code-block:: python

    from flask import Flask, render_template
    app = Flask(__name__)

    @app.route("/")
    def hello():
        return render_template('index.jinja')

    if __name__ == "__main__":
        app.run()

Start it up:

.. code-block:: bash

    $ mkvirtualenv appname 
    $ pip install Flask
    $ python main.py
        * Running on http://localhost:5000/

Structure of a Large Flask Project
==================================

Django-Inspired Example:

.. code-block:: bash

    /appname
        main.py
        database.py
        /appmodule
            __init__.py
            controller.py
            models.py
            /static
                style.css
            /templates
                index.jinja
        ...
    config.py
    manage.py

An Alternative Example:

.. code-block:: bash

    /appname
        main.py
        database.py
        models.py
        /controllers
            __init__.py
            users.py
            admin.py
        /templates
            /users
                login.jinja
            /admin
                backend.jinja
        /static
            /users
                login.css
            /admin
                backend.css
        ...
    config.py
    manage.py

Manage.py
=========

.. code-block:: bash
    
    $ pip install Flask-script

Blueprints
==========
