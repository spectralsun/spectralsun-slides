.. code-block:: python

    # /appname/assets.py
    from flask.ext.assets import Bundle
    js = Bundle('js/jquery.min.js', 'js/index.js', output='script.js')