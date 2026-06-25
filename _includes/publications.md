<h2 id="publications" style="margin: 2px 0px 15px;">Selected Publications</h2>

<b><i style="color:#002D72; margin: 0px 0px -10px">* Equal contribution, † Project leader,  # Corresponding author</i></b>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
  <article class="pub-card">
    <div class="title">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" target="_blank" rel="noopener noreferrer">{{ link.title }}</a>
      {% else %}
      {{ link.title }}
      {% endif %}
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
    <div class="links">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">PDF</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Code</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Project Page</a>
      {% endif %}
      {% if link.bibtex %}
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">BibTex</a>
      {% endif %}
      {% if link.notes %}
      <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %}
      {{ link.others }}
      {% endif %}
    </div>
  </article>
</li>

{% endfor %}

</ol>
</div>
