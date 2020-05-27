{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}
{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}

{% if is_open_source %}
.. image:: https://img.shields.io/pypi/v/{{ cookiecutter.project_slug }}.svg
        :target: https://pypi.python.org/pypi/{{ cookiecutter.project_slug }}

.. image:: https://img.shields.io/travis/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}.svg
        :target: https://travis-ci.org/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}

.. image:: https://readthedocs.org/projects/{{ cookiecutter.project_slug | replace("_", "-") }}/badge/?version=latest
        :target: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status

.. image:: https://coveralls.io/repos/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/badge.svg
        :alt: Coverage Status
        :target: https://coveralls.io/r/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}

.. image:: https://codecov.io/gh{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/branch/master/graphs/badge.svg?branch=master
        :alt: Coverage Status
        :target: https://codecov.io/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}

{%- endif %}


{{ cookiecutter.project_short_description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.open_source_license }}
{% if cookiecutter.create_docs == 'y' %}
* Documentation: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io.
{% endif %}
{% endif %}

Features
--------

* TODO

Credits
-------

This package was created with Cookiecutter_ and the `mateuspontesm/cookiecutter-poetry`_ project template,
a fork of `johanvergeer/cookiecutter-poetry`_ project template

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`johanvergeer/cookiecutter-poetry`: https://github.com/johanvergeer/cookiecutter-poetry
.. _`mateuspontesm/cookiecutter-poetry`: https://github.com/mateuspontesm/cookiecutter-poetry
