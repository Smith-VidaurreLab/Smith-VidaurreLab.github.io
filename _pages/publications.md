---
title: Publications
permalink: /publications/
classes: wide
---
{% for category in site.data.publications.categories %}
  <h2>{{category.heading}}</h2>
  <ol reversed>
  {% for pub in category.pubs %}
    <li><strong>{{pub.title}}</strong>.
    <br>
    {% for author in pub.authors %}
      {% if forloop.last %}
        {{author}}.
    {% else %}
        {{author}},
    {% endif %}
    {% endfor %}
    <br>
    <em>{{pub.venue}}</em>,
    {% if pub.volumeissue %}
      {{pub.volumeissue}},
    {% endif %}
    ({{pub.year}}).
    {% if pub.links %}
    <br>
      {% for link in pub.links %}
        [<a href="{{link.url}}">{{link.text}}</a>]
      {% endfor %}
    {% endif %}
    <br><br></li>
  {% endfor %}
  </ol>
{% endfor %}

\* denotes student mentees
