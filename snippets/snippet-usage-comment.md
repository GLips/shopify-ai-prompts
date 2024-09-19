Title: Add or update a comment in a Liquid snippet file about its usage
Description: Add or updates the comment at the top of a Liquid snippet file, describing usage and showing an example
Body:

{%- comment -%}
Renders a ${1:component name}

Accepts:

- ${2:param_name} {${3:type}} - ${4:Description of the parameter}

Usage:
{%- render '${5:file-name}', ${2}: ${2} -%}
{%- endcomment -%}

### Example

{%- comment -%}
Renders a contact form

Accepts:

- block {block} - Block object

Usage:
{%- render 'block-contact', block: block -%}
{%- endcomment -%}
