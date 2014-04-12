.. code-block:: jinja
    
    {# /appname/templates/macros/form.jinja #}
    {% macro render_field(field) %}
        <div id="{{ field.id }}_row" class="form-group">
            {{ field.label(class_='col-lg-2 control-label') }}
            <div class="col-lg-10">
                {{ field(class_="form-control") }}
            </div>
        </div>
    {% endmacro %}

    {% macro render_form(form) %}
        {% for field in form %}
            {{ render_field(field) }}
        {% endfor %}
    {% endmacro %}