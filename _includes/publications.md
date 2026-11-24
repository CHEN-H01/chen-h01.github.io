<h2 id="publications" style="margin: 2px 0px 15px;">Selected Publications</h2>

<p class="publication-note">* Equal contribution <span aria-hidden="true">·</span> † Project leader</p>

<div class="publications">
<ul class="bibliography" role="list">

{% for link in site.data.publications.main -%}

<li>
  <article class="pub-card">
    {% if link.image -%}
    <a class="publication-image" href="{{ link.page | default: link.pdf }}" target="_blank" rel="noopener noreferrer" aria-label="{{ link.title | escape }}">
      <img src="{{ link.image | relative_url }}" alt="{{ link.image_alt | escape }}" width="{{ link.image_width }}" height="{{ link.image_height }}" loading="lazy" decoding="async">
    </a>
    {% endif -%}
    <div class="publication-content">
    <div class="title">
      {% if link.pdf -%}
      <a href="{{ link.pdf }}" target="_blank" rel="noopener noreferrer">{{ link.title }}</a>
      {% else -%}
      {{ link.title }}
      {% endif -%}
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
    {% if link.pdf or link.code or link.page or link.bibtex or link.notes or link.others -%}
    <div class="links">
      {% if link.pdf -%}
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">PDF</a>
      {% endif -%}
      {% if link.code -%}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Code</a>
      {% endif -%}
      {% if link.page -%}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Project Page</a>
      {% endif -%}
      {% if link.bibtex -%}
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">BibTex</a>
      {% endif -%}
      {% if link.notes -%}
      <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif -%}
      {% if link.others -%}
      {{ link.others }}
      {% endif -%}
    </div>
    {% endif -%}
    </div>
  </article>
</li>

{% endfor -%}

</ul>
</div>
