---
layout: page
title: Participants
participants:
  - {name: Ruth Hoffmann, affiliation: University of St Andrews, Scotland}
  - {name: Max Horn, affiliation: University of Kaiserslautern-Landau, Germany}
---

<ol>{% assign participants = page.participants | sort: "name" %}
{% for p in participants %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.affiliation != null %} ({{ p.affiliation }}){% endif %}
    {% if p.links != null %}
        {% for item in p.links %}
            <a href="{{ item[1] }}">({{ item[0] }})</a>
        {% endfor %}
    {% endif %}
    <br/>
      {% if p.talk != null %} Talk: {{ p.talk }}{% endif %}
  </li>
{% endfor %}
</ol>

{% if site.data.feedback.size > 0 %}

<ul>
{% for p in site.data.feedback %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.package != null %} (author of {{ p.package }}){% endif %}
    <br/>
    {% if p.feedback != null %} {{ p.feedback }}{% endif %}
  </li>
{% endfor %}
</ul>

{% endif %}
<!-- 
$# Conference photo
<img src="{{ site.baseurl }}/public/conference-photo.jpg" />
-->