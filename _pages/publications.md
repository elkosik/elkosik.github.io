---
title: "publications"
permalink: /pubs/
layout: single
header:
    overlay_image: '/assets/images/shore.jpg'
classes: wide
author_profile: true
read_time: false
---

Also available on [Google Scholar](https://scholar.google.com/citations?user=LsgTxkEAAAAJ&hl=en&oi=ao).

{% assign in_press = site.publications | where: "status", "in_press" %}
{% assign articles = site.publications | where: "category", "article" | where_exp: "pub", "pub.status != 'in_press'" | sort: "date" | reverse %}
{% assign posters = site.publications | where: "category", "poster" | sort: "date" | reverse %}

{% if in_press.size > 0 %}
## In Press

{% for pub in in_press %}
**{{ pub.title }}**<br>
{{ pub.authors }}<br>
*{{ pub.venue }}*
{% if pub.paperurl %} &nbsp;|&nbsp; [Paper]({{ pub.paperurl }}){% endif %}
{% if pub.pdf %} &nbsp;|&nbsp; [PDF]({{ pub.pdf }}){% endif %}

{% endfor %}
{% endif %}

## Published Articles

{% assign current_year = "" %}
{% for pub in articles %}
{% assign pub_year = pub.date | date: "%Y" %}
{% if pub_year != current_year %}
{% assign current_year = pub_year %}
### {{ pub_year }}
{% endif %}
**{{ pub.title }}**<br>
{{ pub.authors }}<br>
*{{ pub.venue }}*
{% if pub.paperurl %} &nbsp;|&nbsp; [Paper]({{ pub.paperurl }}){% endif %}
{% if pub.pdf %} &nbsp;|&nbsp; [PDF]({{ pub.pdf }}){% endif %}

{% endfor %}

## Selected Conference Posters

{% assign current_year = "" %}
{% for pub in posters %}
{% assign pub_year = pub.date | date: "%Y" %}
{% if pub_year != current_year %}
{% assign current_year = pub_year %}
### {{ pub_year }}
{% endif %}
**{{ pub.title }}**<br>
*{{ pub.venue }}*
{% if pub.pdf %} &nbsp;|&nbsp; [PDF]({{ pub.pdf }}){% endif %}

{% endfor %}
