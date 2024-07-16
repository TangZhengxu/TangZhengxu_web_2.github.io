## Projects

{% for category in site.data.projects %}
### {{ category[0] | capitalize | replace: "_", " " }}

{% for link in category[1] %}
<div class="project-item" style="display: flex; margin-bottom: 20px; align-items: flex-start;">
  <div style="flex: 0 0 25%; padding-right: 15px;">
    <img src="{{ link.image }}" class="project-image" alt="{{ link.title }}" style="width: 100%; border-radius: 5px;">
  </div>
  <div class="project-details" style="flex: 1;">
    <h4 class="project-title" style="margin-top: 0;"><a href="{{ link.pdf }}">{{ link.title }}</a></h4>
    <p class="project-authors">{{ link.authors | replace: "Zhengxu Tang", "<strong>Zhengxu Tang</strong>" }}</p>
    <p class="project-field"><em>{{ link.field }}</em></p>
    <div class="project-links">
      {% if link.pdf %}<a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank">PDF</a>{% endif %}
      {% if link.code %}<a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Code</a>{% endif %}
      {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Project Page</a>{% endif %}
    </div>
    {% if link.notes %}<p class="project-notes"><strong><i style="color:#e74d3c">{{ link.notes }}</i></strong></p>{% endif %}
  </div>
</div>
{% endfor %}

{% endfor %}