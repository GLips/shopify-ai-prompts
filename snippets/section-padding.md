Title: Add Padding Control to Shopify Section
Description: The style tag and schema settings that need to be added to Shopify sections to have admin-updatable top and bottom padding.
Body:

{%- liquid
  assign padding_top = section.settings.padding_top
  assign padding_bottom = section.settings.padding_bottom
  assign padding_top_mobile = section.settings.padding_top_mobile
  assign padding_bottom_mobile = section.settings.padding_bottom_mobile
-%}

{%- style -%}
#shopify-section-{{ section.id }} {
  --padding-top: {{ padding_top }};
  --padding-bottom: {{ padding_bottom }};

  @media screen and (max-width: 750px) {
    --padding-top: {{ padding_top_mobile }};
    --padding-bottom: {{ padding_bottom_mobile }};
  }
}
{%- endstyle -%}

{%- schema -%}
{
    "class": "section-vertical-spacer",
    "settings": [
            // All other settings...
        {
            "type": "header",
            "content": "Padding"
        },
        {
            "type": "range",
            "id": "padding_top",
            "min": 0,
            "max": 3,
            "step": 0.1,
            "unit": "x",
            "label": "Padding top",
            "default": 1
        },
        {
            "type": "range",
            "id": "padding_bottom",
            "min": 0,
            "max": 3,
            "step": 0.1,
            "unit": "x",
            "label": "Padding bottom",
            "default": 1
        },
        {
            "type": "range",
            "id": "padding_top_mobile",
            "min": 0,
            "max": 3,
            "step": 0.1,
            "unit": "x",
            "label": "Padding top (mobile)",
            "default": 1
        },
        {
            "type": "range",
            "id": "padding_bottom_mobile",
            "min": 0,
            "max": 3,
            "step": 0.1,
            "unit": "x",
            "label": "Padding bottom (mobile)",
            "default": 1
        }
    ]
}
{%- endschema -%}
