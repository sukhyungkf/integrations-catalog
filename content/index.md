---
show_sorted: false
has_children: true
---

# Catalog


{% assign types = "orchestrator, gateway, approval-handler, orchestrator-registration, metadata, registration-handler" | split: ", " %}

{% for int_type in types %}

## {{ int_type | replace: "-", " " }}
{% assign ints_for_type = site.integrations | where: "integration_type", int_type | sort: "name" %}
{% for integration in ints_for_type %}  
 - [{{ integration.name | capitalize }}](/integrations/{{ integration.name }})
 {% endfor %}
--
{% endfor %}
