---
show_sorted: false
has_children: true
---

# Catalog

We are currently in the process of making all of our integrations available publicly and we will be updating this catalog as each is released.  Each publicly available Keyfactor integration's source code is available to modify and distribute in accordance with the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

{% assign types = "orchestrator, gateway, approval-handler, orchestrator-registration, metadata, registration-handler" | split: ", " %}
{% for int_type in types %}
{% assign ints_for_type = site.integrations | where: "integration_type", int_type | sort: "name" %}
{% unless ints_for_type.size == 0 %}

## {{ int_type | replace: "-", " " | capitalize }}

{% for integration in ints_for_type %}  
 - [{{ integration.name | capitalize }}]({{ integration.repository }})
 {% endfor %}
{% endunless %}
{% endfor %}
