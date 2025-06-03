---
permalink: /
title: "About me" 
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
extra_css: "/assets/css/portfolio.css"
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

<!-- # About Me

Hi there👋, I'm a forth year undergraduate student at Northeastern University, China. My research interests include AI4Science (especially AI4Chemistry), Multimodal-LLMs, and Computer Vision. I am fortunate to be advised by Prof. Benyou Wang, and deeply appreciative of my former mentor, Prof. Dayan Guan, who guided me into scientific research. Previously, I had a wonderful experience working with Prof. Miao Fang at NEU.

You can find my full CV here: [📄](/assets/files/Zhengzhao_CV_en.pdf). -->

<!-- My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>). -->


<!-- # 🔥 News -->
<!-- - *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  -->
<!-- - *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  -->
<!-- - *2024.08*: &nbsp;  -->

<!-- # 📝 Publications -->

<!-- <div class='paper-box'> -->
  <!-- <div class='paper-box-image'>
    <div>
      <div class="badge">CVPR 2016</div>
      <img src='images/500x300.png' alt="sym" width="100%">
    </div>
  </div> -->
  <!-- <div class='paper-box-text' markdown="1"> -->

  <!-- [Deep Residual Learning for Image Recognition](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf) -->

  <!-- <u>Zhengzhao Lai</u>, Xiangyu Zhang, Shaoqing Ren, Jian Sun \| ![Static Badge](https://img.shields.io/badge/Under_Review-green) -->

  <!-- [**Project**](https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=DhtAFkwAAAAJ&citation_for_view=DhtAFkwAAAAJ:ALROH1vI_8AC) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong> -->
  <!-- - Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. -->

  <!-- </div> -->
<!-- </div> -->

<!-- 
- [Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet](https://github.com), A, B, C, **CVPR 2020** -->


<!-- # 🎨 Portfolio
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
</div> -->

<!-- # 🎖 Honors and Awards
#### Scholarship:
- Third-class Scholarship (Top 25%)

#### Competition:
- *2024.08* 🥉 National Third Prize — 23rd National RoboMaster Competition.
- *2023.12* 🥈 National Second Prize — 5th National Campus AI Algorithm Elite Competition.
- *2023.08* 🥉 National Third Prize — 22nd National RoboMaster Competition. -->

<!-- # 🎓 Educations
- *2024.08 - Present*, Visiting Student, The Chinese University of Hong Kong, Shenzhen, China.
- *2021.09 - 2025.06 (Expected)*, Undergraduate, Northeastern University, China. -->

<!-- # 💬 Invited Talks
- *2021.06*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2021.03*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  \| [\[video\]](https://github.com/) -->

<!-- # 💻 Internships
- *2024.01 - 2024.02*, [Shenyang YaTrans](https://niutrans.com/), China. -->


{% include_relative intro.md %}

{% include_relative news.md %}

{% include_relative pub.md %}

{% include_relative portfolio.md %}

{% include_relative awards.md %}

{% include_relative edu.md %}

{% include_relative intern.md %}

---
