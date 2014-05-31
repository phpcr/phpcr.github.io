---
layout: default
title: Implementations
---

This page lists all known PHPCR implementations:

{% for implementation in site.data.implementations|where:"stability","foonar" %}
- **{{ implementation.stability }}**: [{{ implementation.name }}](#{{ implementation.name|downcase|replace: ' ', '_' }})
{% endfor %}

{% for implementation in site.data.implementations %}
## {{ implementation.name }}

{{ implementation.description }}

- **Website**: [{{ implementation.website }}](implementation.website)
- **Github**: [{{ implementation.github }}](implementation.github)
- **Stability**: {{ implementation.stability }}

{% if implementation.descriptors %}
The following table lists the supported features as reported by the implementation (see the [JCR Spec](http://www.day.com/specs/jcr/2.0/24_Repository_Compliance.html) for more information):

<table class="pure-table">
    <thead>
        <tr>
            <th>Feature</th>
            <th>Support</th>
        </tr>
    </thead>
    <tbody>
    {% for descriptor in implementation.descriptors %}
            <tr>
                {% assign value = descriptor[1] %}
                {% if value == "true" %}
                    {% assign class = 'supported' %}
                {% elsif descriptor[1] == 'false' %}
                    {% assign class = 'notsupported' %}
                {% endif %}

                <td>{{ descriptor[0] }}</td>
                <td class="support {{ class }}">{{ value }}</td>
            </tr>
    {% endfor %}
    </tbody>
</table>
{% endif %}
{% endfor %}
