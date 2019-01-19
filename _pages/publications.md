---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
   {% assign currentYear = post.date | date: "%Y" %}
   {% if currentYear != myYear %}
     ## {{currentYear}}
     {% assign myYear = currentYear %}
   {% endif %}
   
   {% include archive-single.html %}
{% endfor %}
