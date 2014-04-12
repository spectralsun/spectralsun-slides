=================
Fifth-Sized Flask
=================

by spectralsun 

revised: 04/11/2013

http://spectralsun.com

.. figure:: /_static/images/fifth-sized-flask.png
    :align: center

source: https://github.com/spectralsun/spectralsun-slides

Large Apps with Flask

Prerequisite Knowledge
======================

.. include:: fifth_sized_flask/prereq/recommended.rst

Prerequisite Knowledge
======================

.. include:: fifth_sized_flask/prereq/recommended.rst

.. include:: fifth_sized_flask/prereq/optional.rst


Simple Flask Project
====================

.. include:: fifth_sized_flask/simple/tree.rst

Simple Flask Project
====================

.. include:: fifth_sized_flask/simple/tree.rst

.. include:: fifth_sized_flask/simple/python.rst

Simple Flask Project
====================

.. include:: fifth_sized_flask/simple/tree.rst

.. include:: fifth_sized_flask/simple/python.rst

.. include:: fifth_sized_flask/simple/bash.rst

Structure of a Large Flask Project
==================================
 
.. include:: fifth_sized_flask/structure/django.rst

Structure of a Large Flask Project
==================================
 
.. include:: fifth_sized_flask/structure/django.rst

.. include:: fifth_sized_flask/structure/alternate.rst

Flask-Script: Manage.py
=======================

.. include:: fifth_sized_flask/manage/install.rst

Flask-Script: Manage.py
=======================

.. include:: fifth_sized_flask/manage/install.rst

.. include:: fifth_sized_flask/manage/example.rst


Flask-Script: Manage.py
=======================

.. include:: fifth_sized_flask/manage/install.rst

.. include:: fifth_sized_flask/manage/example.rst

.. include:: fifth_sized_flask/manage/init_db.rst


Flask-Script: Manage.py
=======================

.. include:: fifth_sized_flask/manage/install.rst

.. include:: fifth_sized_flask/manage/example.rst

.. include:: fifth_sized_flask/manage/init_db.rst

.. include:: fifth_sized_flask/manage/runserver.rst

Blueprints: Modular Applications
================================

.. include:: fifth_sized_flask/blueprints/users.rst

Blueprints: Modular Applications
================================

.. include:: fifth_sized_flask/blueprints/users.rst

.. include:: fifth_sized_flask/blueprints/main.rst

Forms
=====

.. include:: fifth_sized_flask/forms/install.rst

Forms
=====

.. include:: fifth_sized_flask/forms/install.rst

.. include:: fifth_sized_flask/forms/forms.rst

Forms
=====

.. include:: fifth_sized_flask/forms/install.rst

.. include:: fifth_sized_flask/forms/forms.rst

.. include:: fifth_sized_flask/forms/contact.rst

Rendering Forms 
===============

.. include:: fifth_sized_flask/render_form/field.rst

Rendering Forms 
===============

.. include:: fifth_sized_flask/render_form/form.rst

Rendering Forms 
===============

.. include:: fifth_sized_flask/render_form/form.rst

.. include:: fifth_sized_flask/render_form/use.rst

Forms with SQL Alchemy
======================

.. include:: fifth_sized_flask/form_alchemy/install.rst

Forms with SQL Alchemy
======================

.. include:: fifth_sized_flask/form_alchemy/install.rst

.. include:: fifth_sized_flask/form_alchemy/models.rst

Forms with SQL Alchemy
======================

.. include:: fifth_sized_flask/form_alchemy/install.rst

.. include:: fifth_sized_flask/form_alchemy/models.rst

.. include:: fifth_sized_flask/form_alchemy/form.rst


Assets
======

.. include:: fifth_sized_flask/assets/install.rst

Assets
======

.. include:: fifth_sized_flask/assets/install.rst

.. include:: fifth_sized_flask/assets/assets.rst

Assets
======

.. include:: fifth_sized_flask/assets/install.rst

.. include:: fifth_sized_flask/assets/assets.rst

.. include:: fifth_sized_flask/assets/main.rst

Assets
======

.. include:: fifth_sized_flask/assets/install.rst

.. include:: fifth_sized_flask/assets/assets.rst

.. include:: fifth_sized_flask/assets/main.rst

.. include:: fifth_sized_flask/assets/jinja.rst

..Cache
..=====


Users
=====

.. code-block:: bash

    $ pip install Flask-Login

.. code-block:: python

   # ...

   class User(Model):
        __tablenanme__ = 'users'
        id = Column(Integer, primary_key=True)
        username = Column(String(255), unique=True)

        def is_authenticated():
            return true 


.. code-block:: python

    login_manager = LoginManager()
    login_manager.init_app(app)

Using Users
===========

.. code-block:: python

    @app.route("/login", methods=["GET", "POST"])
    def login():
        form = LoginForm()
        if form.validate_on_submit():
            # login and validate the user...
            login_user(user)
            flash("Logged in successfully.")
            return redirect(request.args.get("next") or url_for("index"))
        return render_template("login.html", form=form)

.. code-block:: python

    @app.route("/settings")
    @login_required
    def settings():
        pass

Web Sockets
===========

.. code-block:: bash
    
    $ pip install flask-socketio





Uploading Multiple files via AJAX?
==================================

No problem!