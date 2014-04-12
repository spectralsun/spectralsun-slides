.. code-block:: python
    
    # /appname/forms.py
    from flask_wtf import Form
    from wtforms import TextField, TextAreaField
    from wtforms.validators import DataRequired

    class ContactForm(Form):
        name = TextField('name', validators=[DataRequired()])
        message = TextAreaField('email', validators=[DataRequired()])