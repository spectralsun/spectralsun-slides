.. code-block:: python

    # /appname/controllers/users.py
    from flask import Blueprint, render_template

    bp = Blueprint('users', __name__)

    @bp.route('/login')
    def route():
        # ...
        return render_template('users/login.jinja')