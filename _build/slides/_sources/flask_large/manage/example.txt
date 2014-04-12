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