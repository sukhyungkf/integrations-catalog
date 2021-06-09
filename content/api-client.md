---
sort: 8
has_children: true
---

# API Client

{% assign these_integrations = site.integrations | where: "integration_type", 'api-client' | sort: "name" %}

{% for integration in these_integrations %}

### [{{integration.name | capitalize }}]({{ integration.url }})

{{ integration.description }}

[Github Repository]({{ integration.repository }})

{% endfor %}

{% if these_integrations.size == 0 %}
_Publicly available API Client integrations coming soon._
{% endif %}