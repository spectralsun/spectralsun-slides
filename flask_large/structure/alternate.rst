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