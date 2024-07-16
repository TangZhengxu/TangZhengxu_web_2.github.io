## Projects

### Bioinformatics

{% for link in site.data.projects.bioinformatics %}
<div class="project-item">
  <img src="{{ link.image }}" class="project-image" alt="{{ link.title }}">
  <div class="project-details">
    <h4 class="project-title"><a href="{{ link.pdf }}">{{ link.title }}</a></h4>
    <p class="project-authors">{{ link.authors | replace: "Zhengxu Tang", "<strong>Zhengxu Tang</strong>" }}</p>
    <p class="project-field"><em>{{ link.field }}</em></p>
    <div class="project-links">
      {% if link.pdf %}<a href="{{ link.pdf }}" class="btn">PDF</a>{% endif %}
      {% if link.code %}<a href="{{ link.code }}" class="btn">Code</a>{% endif %}
      {% if link.page %}<a href="{{ link.page }}" class="btn">Project Page</a>{% endif %}
    </div>
    {% if link.notes %}<p class="project-notes">{{ link.notes }}</p>{% endif %}
  </div>
</div>
{% endfor %}

### Computational Neuroscience

{% for link in site.data.projects.computational_neuroscience %}
<div class="project-item">
  <img src="{{ link.image }}" class="project-image" alt="{{ link.title }}">
  <div class="project-details">
    <h4 class="project-title"><a href="{{ link.pdf }}">{{ link.title }}</a></h4>
    <p class="project-authors">{{ link.authors | replace: "Zhengxu Tang", "<strong>Zhengxu Tang</strong>" }}</p>
    <p class="project-field"><em>{{ link.field }}</em></p>
    <div class="project-links">
      {% if link.pdf %}<a href="{{ link.pdf }}" class="btn">PDF</a>{% endif %}
      {% if link.code %}<a href="{{ link.code }}" class="btn">Code</a>{% endif %}
      {% if link.page %}<a href="{{ link.page }}" class="btn">Project Page</a>{% endif %}
    </div>
    {% if link.notes %}<p class="project-notes">{{ link.notes }}</p>{% endif %}
  </div>
</div>
{% endfor %}

### Mathematics Modeling

{% for link in site.data.projects.mathematics_modeling %}
<div class="project-item">
  <img src="{{ link.image }}" class="project-image" alt="{{ link.title }}">
  <div class="project-details">
    <h4 class="project-title"><a href="{{ link.pdf }}">{{ link.title }}</a></h4>
    <p class="project-authors">{{ link.authors | replace: "Zhengxu Tang", "<strong>Zhengxu Tang</strong>" }}</p>
    <p class="project-field"><em>{{ link.field }}</em></p>
    <div class="project-links">
      {% if link.pdf %}<a href="{{ link.pdf }}" class="btn">PDF</a>{% endif %}
      {% if link.code %}<a href="{{ link.code }}" class="btn">Code</a>{% endif %}
      {% if link.page %}<a href="{{ link.page }}" class="btn">Project Page</a>{% endif %}
    </div>
    {% if link.notes %}<p class="project-notes">{{ link.notes }}</p>{% endif %}
  </div>
</div>
{% endfor %}