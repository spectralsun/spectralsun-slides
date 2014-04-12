.. code-block:: python

    # /appname/main.py
    # ...
    from appname.controllers import users
    # ...
    app.register_blueprint(users.bp, '/users')