.. code-block:: python

    # /appname/forms.py 
    from wtforms_alchemy import ModelForm
    from appname.models import Todo

    class TodoForm(ModelForm):
        class Meta:
            model = Todo