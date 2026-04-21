---
title: "publications"
permalink: /pubs/
layout: single
classes: wide
author_profile: true
read_time: false
---

Also available on [Google Scholar](https://scholar.google.com/citations?user=LsgTxkEAAAAJ&hl=en&oi=ao).

{% assign articles = site.publications | where: "category", "article" | sort: "date" | reverse %}

{% assign current_year = "" %}
{% for pub in articles %}
{% assign pub_year = pub.date | date: "%Y" %}
{% if pub_year != current_year %}
{% assign current_year = pub_year %}
### {{ pub_year }}
{% endif %}
{{ pub.title }}<br>
<span style="font-size: 0.85em;">{{ pub.authors }}</span><br>
*{{ pub.venue }}*
{% if pub.paperurl %} &nbsp;|&nbsp; [Paper]({{ pub.paperurl }}){% endif %}
{% if pub.pdf %} &nbsp;|&nbsp; [PDF]({{ pub.pdf }}){% endif %}

{% endfor %}
