---
sort: 3
has_children: true
---

# CA Gateway

{% assign these_integrations = site.integrations | where: "integration_type", 'ca-gateway' | sort: "name" %}

{% for integration in these_integrations %}

<h3 style="display:flex">
    <a href="{{site.baseurl}}{{integration.url}}">{{integration.name | capitalize }}</a>
</h3>

{{ integration.description }}

[Github Repository]({{ integration.repository }})

{% endfor %}

{% if these_integrations.size == 0 %}
_Publicly available CA Gateway integrations coming soon._
{% endif %}