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

Simple Flask Project
====================

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

    config.py
    manage.py
    /appname
        __init__.py
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
        
    

An Alternative Example:

.. code-block:: bash

    config.py
    manage.py
    /appname
        __init__.py
        main.py
        database.py
        models.py
        /controllers
            __init__.py
            users.py
            admin.py
        /templates
            index.jinja
            /users
                login.jinja
        /static
            index.css
            /users
                login.css
        
    

Flask-Script: Manage.py
=======================

.. code-block:: bash
    
    $ pip install Flask-Script

.. code-block:: python
    
    from flask.ext.script import Manager

    from appname import main, database

    manager = Manager(main.app)

    @manager.command
    def init_db():
        database.init_db()
        print "* Successfully initialized database."

    if __name__ == "__main__":
        manager.run()

.. code-block:: bash

    $ python manage.py runserver -t 0.0.0.0 -p 4000
        * Running on http://0.0.0.0:4000/

.. code-block:: bash
    
    $ python manage.py init_db
        * Successfully initialized database.

Blueprints: Modular Applications
================================


Forms
=====


Forms with SQL Alchemy
======================


Assets
======


Users
=====


Web Sockets
===========


Uploading Multiple files via AJAX?
==================================

No problem!