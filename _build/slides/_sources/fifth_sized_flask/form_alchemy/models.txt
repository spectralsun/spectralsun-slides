.. code-block:: python
    
    # /appname/models.py
    from sqlalchemy import Column, String
    from appname.database import Model

    class Todo(Model):
        __tablename__ = 'event'
        name = Column(String(255))