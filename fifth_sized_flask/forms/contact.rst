.. code-block:: python
    
    # /appname/main.py 
    from flask import Flask, request, render_template
    from appname.forms import ContactForm
    # ...
    @app.route('/contact')
    def contact():
        form = ContactForm(request.form, prefix='contact_')
        if form.validate():
            # send email
        return render_template('contact.jinja')