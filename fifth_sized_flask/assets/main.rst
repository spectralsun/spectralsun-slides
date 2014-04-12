.. code-block:: python

    # /appname/main.py
    from flask.ext.asstes import Environment
    from appname.assets import js
    # ...
    assets = Environment(app)
    assets.register('js', js)