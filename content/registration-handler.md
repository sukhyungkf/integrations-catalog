---
sort: 4
has_children: true
---

# Registration Handler

{% assign these_integrations = site.integrations | where: "integration_type", 'registration-handler' | sort: "name" %}

{% for integration in these_integrations %}

<h3 style="display:flex">
    <a href="{{site.baseurl}}{{integration.url}}">{{integration.name | capitalize }}</a>
</h3>

{{ integration.description }}

[Github Repository]({{ integration.repository }})

{% endfor %}

{% if these_integrations.size == 0 %}
_Publicly available Registration Handler integrations coming soon._
{% endif %}