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

.. include:: flask_large/prereq/recommended.rst

Prerequisite Knowledge
======================

.. include:: flask_large/prereq/recommended.rst

.. include:: flask_large/prereq/optional.rst


Simple Flask Project
====================

.. include:: flask_large/simple/tree.rst

Simple Flask Project
====================

.. include:: flask_large/simple/tree.rst

.. include:: flask_large/simple/python.rst

Simple Flask Project
====================

.. include:: flask_large/simple/tree.rst

.. include:: flask_large/simple/python.rst

.. include:: flask_large/simple/bash.rst

Structure of a Large Flask Project
==================================
 
.. include:: flask_large/structure/django.rst

Structure of a Large Flask Project
==================================
 
.. include:: flask_large/structure/django.rst

.. include:: flask_large/structure/alternate.rst

Flask-Script: Manage.py
=======================

.. include:: flask_large/manage/install.rst

Flask-Script: Manage.py
=======================

.. include:: flask_large/manage/install.rst

.. include:: flask_large/manage/example.rst


Flask-Script: Manage.py
=======================

.. include:: flask_large/manage/install.rst

.. include:: flask_large/manage/example.rst

.. include:: flask_large/manage/init_db.rst


Flask-Script: Manage.py
=======================

.. include:: flask_large/manage/install.rst

.. include:: flask_large/manage/example.rst

.. include:: flask_large/manage/init_db.rst

.. include:: flask_large/manage/runserver.rst

Blueprints: Modular Applications
================================

.. include:: flask_large/blueprints/users.rst

Blueprints: Modular Applications
================================

.. include:: flask_large/blueprints/users.rst

.. include:: flask_large/blueprints/main.rst

Forms
=====

.. include:: flask_large/forms/install.rst

Forms
=====

.. include:: flask_large/forms/install.rst

.. include:: flask_large/forms/forms.rst

Forms
=====

.. include:: flask_large/forms/install.rst

.. include:: flask_large/forms/forms.rst

.. include:: flask_large/forms/contact.rst

Rendering Forms 
===============

.. code-block:: jinja

    {% macro render_field(field) %}
        <div id="{{ field.id }}_row" class="form-group">
            {{ field.label(class_='col-lg-2 control-label') }}
            <div class="col-lg-10">
                {{ field(class_="form-control") }}
            </div>
        </div>
    {% endmacro %}

.. code-block:: jinja

    {% macro render_form(form) %}
        {% for field in form %}
            {{ render_field(field) }}
        {% endfor %}
    {% endmacro %}



Forms with SQL Alchemy
======================


Assets
======

Cache
=====

Users
=====


Web Sockets
===========


Uploading Multiple files via AJAX?
==================================

No problem!