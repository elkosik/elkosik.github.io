---
title: ""
permalink: /
layout: single
author_profile: true
read_time: false
share: false
---

<h2 id="about">About Me</h2>

I received my Ph.D. in [Cognitive Science](https://cogsci.ucsd.edu/graduates/phd-program/index.html) in [Dr. Bradley Voytek's lab](https://voyteklab.com/) at the University of California, San Diego. My dissertation quantified respiratory waveform shape across a population and measured its coupling to neural activity. Together, this work uses breathing as a window into brain-body interactions at the resolution of a single cycle.

During my Ph.D. I had the privilege of interning across many industry domains working on novel hardware sensing capabilities at [Oura](https://ouraring.com/), multi-modal bio-signal data at [Apple](https://www.apple.com/), clinical trial wearable data at [Takeda](https://www.takeda.com/), and large-scale, qualitative survey data at [Fidelity](https://www.fidelity.com/). 

Before graduate school, I worked at UCSF's [Memory and Aging Center](https://memory.ucsf.edu/) with [Dr. Virginia Sturm](https://canlab.ucsf.edu/), studying emotion dysfunction in neurodegenerative disease via autonomic signals, MRI, and facial expression coding. I received my B.A. from [UC Berkeley](https://cogsci.berkeley.edu/home), where I completed an honors thesis in [Dr. Robert Knight's lab](https://knightlab.neuro.berkeley.edu/) on event-related potential responses in scalp and intracranial EEG.

<section id="news">
<h2>Recent News</h2>
<div class="news-scroll">
  <ul>
    <li>
      <div class="news-date">Sep 2026</div>
      <div class="news-text">Successfully defended Ph.D. dissertation: "The Shape of Breathing: Cycle-by-Cycle Waveforms in Respiration-Brain Interactions".</div>
    </li>
    <li>
      <div class="news-date">Sep 2026</div>
      <div class="news-text">First-author manuscript published in the <a href="https://doi.org/10.1523/JNEUROSCI.0731-26.2026"><em>Journal of Neuroscience</em></a>: "Cycle-by-cycle respiration waveforms are coupled with the shape of neural oscillations".</div>
    </li>
    <li>
      <div class="news-date">Jun 2026</div>
      <div class="news-text">Began 3-month internship on the Algorithms team at <a href="https://ouraring.com/">Oura</a>!</div>
    </li>
    <li>
      <div class="news-date">Apr 2026</div>
      <div class="news-text">First-author preprint posted to <a href="https://doi.org/10.64898/2026.04.13.718339"><em>bioRxiv</em></a>: "Cycle-by-cycle respiration waveforms are coupled with the shape of neural oscillations".</div>
    </li>
    <li>
      <div class="news-date">Mar 2026</div>
      <div class="news-text">First-author manuscript from <a href="https://www.takeda.com/">Takeda</a> internship published in <a href="https://doi.org/10.1159/000551257"><em>Digital Biomarkers</em></a>: "Methods for Wearable-Derived Pulse Rate Measures and Their Application to Modeling the Relationship Between Pulse Rate and Motor Activity in Narcolepsy Type 1".</div>
    </li>
    <li>
      <div class="news-date">Mar 2025</div>
      <div class="news-text">Received the <a href="https://ucsdcollab.atlassian.net/wiki/spaces/GDCP/pages/565740040/Rita+L.+Atkinson+Graduate+Fellowship">Rita L. Atkinson Graduate Fellowship</a>.</div>
    </li>
    <li>
      <div class="news-date">Mar 2025</div>
      <div class="news-text">Manuscript published in <a href="https://doi.org/10.1016/j.chpulm.2024.100102"><em>CHEST Pulmonary</em></a>: "Sleep Parameters of Breathing and Cognitive Function in a Diverse Hispanic/Latino Cohort"</div>
    </li>
    <li>
      <div class="news-date">Jan 2025</div>
      <div class="news-text">Began 8-month internship on the Neuro team at Apple!</div>
    </li>
  </ul>
</div>
</section>


<section id="publications" markdown="1">
<h2>Publications</h2>

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
{{ pub.authors }}<br>
{% if pub.note %}<small>{{ pub.note }}</small><br>{% endif %}
*{{ pub.venue }}*
{% if pub.paperurl %} &nbsp;|&nbsp; [Paper]({{ pub.paperurl }}){% endif %}
{% if pub.pdf %} &nbsp;|&nbsp; [PDF]({{ pub.pdf }}){% endif %}

{% endfor %}
</section>
