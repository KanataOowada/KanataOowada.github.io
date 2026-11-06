<h2 id="preprints" style="margin: 2px 0 -15px;">Preprints</h2><div class="publications">
  <ol class="bibliography">
  {% for paper in site.data.preprints.main %}
    <li>
      <div class="pub-row">
        <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
          {% if paper.image %}
            <img src="{{ paper.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto;" alt="Preprint thumbnail">
            {% if paper.conference_short %}
              <abbr class="badge">{{ paper.conference_short }}</abbr>
            {% endif %}
          {% endif %}
        </div>
        <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
          <div class="title">
            {% if paper.pdf %}<a href="{{ paper.pdf }}">{{ paper.title }}</a>{% else %}{{ paper.title }}{% endif %}
          </div>
          <div class="author">{{ paper.authors }}</div>
          {% if paper.conference %}
            <div class="periodical"><em>{{ paper.conference }}</em></div>
          {% endif %}
          <div class="links">
            {% if paper.pdf %}<a href="{{ paper.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">PDF</a>{% endif %}
            {% if paper.code %}<a href="{{ paper.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Code</a>{% endif %}
            {% if paper.page %}<a href="{{ paper.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Project Page</a>{% endif %}
            {% if paper.bibtex %}<a href="{{ paper.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">BibTeX</a>{% endif %}
            {% if paper.notes %}<strong><i style="color:#e74d3c">{{ paper.notes }}</i></strong>{% endif %}
            {% if paper.others %}{{ paper.others }}{% endif %}
          </div>
        </div>
      </div>
    </li>
    <br>
  {% endfor %}
  </ol>
</div>
