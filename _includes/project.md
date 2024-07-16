---
layout: page
title: Projects
permalink: /projects/
description: A growing collection of my cool projects.
nav: true
nav_order: 2
---

## Projects

<div class="publications">
<ol class="bibliography">
{% for category in site.data.projects %}
  <h3>{{ category[0] | capitalize | replace: "_", " " }}</h3>
  {% for link in category[1] %}
  <li>
    <div class="pub-row">
      <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
        <img src="{{ link.image | relative_url }}" class="teaser img-fluid z-depth-1" alt="{{ link.title }}">
        <abbr class="badge">{{ link.field_short }}</abbr>
      </div>
      <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
        <div class="title"><a href="{{ link.pdf | relative_url }}">{{ link.title }}</a></div>
        <div class="author">{{ link.authors }}</div>
        <div class="periodical"><em>{{ link.field }}</em></div>
        <div class="links">
          {% if link.pdf %}<a href="{{ link.pdf | relative_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>{% endif %}
          {% if link.code %}<a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>{% endif %}
          {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>{% endif %}
          {% if link.notes %}<strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>{% endif %}
        </div>
      </div>
    </div>
  </li>
  {% endfor %}
{% endfor %}
</ol>
</div>