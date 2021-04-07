---
sort: 5
has_children: true
---

# Approval Handler

{% assign these_integrations = site.integrations | where: "integration_type", 'approval-handler' | sort: "name" %}

{% for integration in these_integrations %}

### [{{integration.name | capitalize }}](/integrations/{{integration.name}})

{{ integration.description }}

[Github Repository]({{ integration.repository }})

{% endfor %}

{% if these_integrations.size == 0 %}
_Publicly available Approval Handler integrations coming soon._
{% endif %}