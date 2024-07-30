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
  - {name: Shaun Alan Isherwood, affiliation: "University of Aberdeen, Scotland"}
  - {name: Lukas Schnelle, affiliation: "SLA, ART at RWTH Aachen, Germany"}
  - {name: Leila Ghanbari, affiliation: "University of Tehran, Iran"}
  - {name: Jan De Beule, affiliation: "Vrije Universiteit Brussel, Belgium"}
  - {name: Manuel Delgado, affiliation: "University of Porto, Portugal"}
  - {name: Joseph Edwards, affiliation: "University of St Andrews, Scotland"}
  - {name: Peiran Wu, affiliation: "University of St Andrews, Scotland"}
  - {name: Wilf Wilson}
  - {name: Jung Won Cho, affiliation: "University of St Andrews, Scotland"}
  - {name: Meike Weiß, affiliation: "RWTH Aachen University, Germany"}
  - {name: Kamil Zabielski, affiliation: "Bialystok University of Technology, Poland"}
  - {name: Leonard Soicher, affiliation: "Queen Mary University of London, England"}
  - {name: Tianrun Yang, affiliation: "University of St Andrews, Scotland"}
  - {name: Fatemeh Koorepazan Moftakhar, affiliation: "Sharif University of Technology, Iran"}
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
