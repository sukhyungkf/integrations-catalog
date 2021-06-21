---
sort: 2
has_children: true
---

# Orchestrator Registration

{% assign these_integrations = site.integrations | where: "integration_type", 'orchestrator-registration' | sort: "name" %}

{% for integration in these_integrations %}

### <a href="{{ integration.url }}">{{integration.name | capitalize }}</a>

{{ integration.description }}

[Github Repository]({{ integration.repository }})

{% endfor %}

{% if these_integrations.size == 0 %}
_Publicly available Orchestrator Registration integrations coming soon._
{% endif %}