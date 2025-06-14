# 🎨 Portfolio

Something novel and cool, which makes up a part of me 😊

<div class="portfolio-grid">
  {% for post in site.portfolio %}
    <article class="portfolio-item">
      <a class="portfolio-image-link" href="{{ post.url | relative_url }}">
        <div class="portfolio-image-wrapper">
          <img class="portfolio-image" src="{{ post.image | default: '/images/500x300.png' | relative_url }}" alt="{{ post.title }}">
        </div>
      </a>
      <div class="portfolio-info">
        <p class="portfolio-title">
          <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
        </p>
        {% if post.excerpt %}
          <p class="portfolio-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 200 }}</p>
        {% endif %}
        <!-- {% if post.date %}
          <p class="portfolio-date">{{ post.date | date: "%B, %Y" }}</p>
        {% endif %} -->
        {% if post.start_date and post.end_date %}
          <p class="portfolio-date">{{ post.start_date | date: "%B, %Y" }} ~ {{ post.end_date | date: "%B, %Y" }}</p>
        {% endif %}
        {% if post.pdf %}
          <a style = "color: #3c47e7" href="{{ post.pdf }}" target="_blank" rel="noopener">[PDF]</a>
        {% endif %}
        {% if post.code %}
          <a style = "color: #3c47e7" href="{{ post.code }}" target="_blank" rel="noopener">[CODE]</a>
        {% endif %}
      </div>
    </article>
  {% endfor %}
</div>