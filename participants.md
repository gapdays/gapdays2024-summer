---
layout: page
title: Participants
participants:
  - {name: Mun See Chang, affiliation: "University of St Andrews, Scotland"}
  - {name: Ruth Hoffmann, affiliation: "University of St Andrews, Scotland"}
  - {name: Max Horn, affiliation: "University of Kaiserslautern-Landau, Germany"}
  - {name: Olexandr Konovalov, affiliation: "University of St Andrews, Scotland"}
  - {name: Rhys Evans, affiliation: "Institute of Mathematics, Physics and Mechanics, Ljubljana, Slovenia"} 
  - {name: Markus Pfeiffer, affiliation: "Huawei R&D Edinburgh, Scotland"}
  - {name: Michael Young, affiliation: "University of St Andrews, Scotland"}
  - {name: James Mitchell, affiliation: "University of St Andrews, Scotland"}
  - {name: Surinder Kaur, affiliation: "SRM University-AP, India"}
  - {name: Shaun Alan Isherwood, affiliation: "University of Aberdeen, Scotland"}
  - {name: Lukas Schnelle, affiliation: "SLA, ART at RWTH Aachen, Germany"}
  - {name: Manoj Kumar, affiliation: "Harish-Chandra Research Institute,  Prayagraj, India"}
  - {name: Suraj Singh Khurana, affiliation: "Department of Mathematics, SRM University AP, Andhra Pradesh, India"}
  - {name: Leila Ghanbari, affiliation: "University of Tehran, Iran"}
  - {name: Jan De Beule, affiliation: "Vrije Universiteit Brussel, Belgium"}
  - {name: Manuel Delgado, affiliation: "University of Porto, Portugal"}
  - {name: Joseph Edwards, affiliation: "University of St Andrews, Scotland"}
  - {name: Peiran Wu, affiliation: "University of St Andrews, Scotland"}
  - {name: Wilf Wilson}
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
