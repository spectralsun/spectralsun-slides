=============================
Large Applications with Flask
=============================

spectralsun 04/11/2013


Prerequisite knowledge
======================

Having this knowledge is recommended, but may not be necessary for you to gain value:

* Python
* Pip

Having knowledge is optional, but will help you gain more value:

* Flask
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

Structure of a Large App
========================

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
                layout.jinja
                index.jinja
                login.jinja
        ...
    manage.py

Manage.py
=========

.. code-block:: bash
    
    $ pip install Flask-script


Blueprints
==========
