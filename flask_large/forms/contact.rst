.. code-block:: python
    
    # ...
    @app.route('/contact')
    def contact():
        form = ContactForm(request.form, prefix='contact_')
        if form.validate():
            # send email