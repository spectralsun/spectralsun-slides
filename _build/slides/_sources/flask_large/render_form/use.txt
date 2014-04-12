.. code-block:: jinja
    
    {# /appname/templates/contact.jinja #}
    {% from "macros/form.jinja" import render_form %}
    <form method="post">{{ render_form(form) }}</form>