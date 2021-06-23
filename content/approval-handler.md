---
sort: 5
has_children: true
---

# Approval Handler

{% assign these_integrations = site.integrations | where: "integration_type", 'approval-handler' | sort: "name" %}

{% for integration in these_integrations %}

<h3 style="display:flex">
    <a href="{{site.baseurl}}{{integration.url}}">{{integration.name | capitalize }}</a>
</h3>

{{ integration.description }}

{% if integration.link_github == true %}
[Github Repository]({{ integration.repository }})
{% endif %}

{% endfor %}

{% if these_integrations.size == 0 %}
_Publicly available Approval Handler integrations coming soon._
{% endif %}
