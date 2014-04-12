.. code-block:: python

    # /appname/config.py
    import redis

    CACHE = redis.StrictRedis(host='localhost', port=6379, db=0)