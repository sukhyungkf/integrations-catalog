---
sort: 7
has_children: true
---

# Alert Handler

{% assign these_integrations = site.integrations | where: "integration_type", 'alert-handler' | sort: "name" %}

{% for integration in these_integrations %}

### [{{integration.name | capitalize }}]({{ integration.url }})

{{ integration.description }}

[Github Repository]({{ integration.repository }})

{% endfor %}

{% if these_integrations.size == 0 %}
_Publicly available Alert Handler integrations coming soon._
{% endif %}