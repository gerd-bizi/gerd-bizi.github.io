---
title: "Blog Posts"
layout: archive
permalink: /blog_posts/
author_profile: true
---
{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.blog reversed %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}

## {{ year }}

{% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}