---
sort: 6
has_children: true
---

# Metadata Generation

{% assign these_integrations = site.integrations | where: "integration_type", 'metadata' | sort: "name" %}

{% for integration in these_integrations %}

### [{{integration.name | capitalize }}]({{ integration.url }})

{{ integration.description }}

[Github Repository]({{ integration.repository }})

{% endfor %}

{% if these_integrations.size == 0 %}
_Publicly available Metadata generation integrations coming soon._
{% endif %}