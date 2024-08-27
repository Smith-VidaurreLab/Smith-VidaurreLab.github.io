---
title: Research Team
permalink: /team/
classes: wide
header:
    overlay_color: "#000"
    overlay_filter: "0"
    overlay_image: /assets/images/TAN_4812.JPG
    caption: "@Tania Molina"
---

<div>
{% for member in site.data.team.members %}
    <figure>
    {% if member.url %}
        <a href=
            {% if member.url contains "://" %}
              "{{ member.url }}"
            {% else %}
              "{{ member.url | relative_url }}"
            {% endif %}
            title="{{ member.name }}">
        <img class="thumb" src=
          {% if member.image_path contains "://" %}
            "{{ member.image_path }}"
          {% else %}
            "{{ member.image_path | relative_url }}"
          {% endif %}>
        </a>
    {% else %}
        <img class="thumb" src=
          {% if member.image_path contains "://" %}
            "{{ member.image_path }}"
          {% else %}
            "{{ member.image_path | relative_url }}"
          {% endif %}
          alt="{{ member.name }}">
    {% endif %}
    <figcaption>
        <strong>{{member.name}}</strong><br>
        {{member.title}}<br>
        {{member.subject}}<br>
    </figcaption>
    <subcaption>
        <strong>Outside of the Lab:</strong> {{member.interests}}
    </subcaption>
    </figure>
{% endfor %}
</div>
<div>
    <h3>Alumni</h3>
    <ul>
{% for member in site.data.team.alumni %}
    {% if member.url %}
	<li><a href="{{ member.url}}" target="_blank">{{member.name}}</a>        
    {% else %}
    <li>{{member.name}}
    }
    {% endif %}
    {% if member.now %}
        ({{member.now}})
    {% endif %}
    </li>
{% endfor %}
</ul>
</div>
