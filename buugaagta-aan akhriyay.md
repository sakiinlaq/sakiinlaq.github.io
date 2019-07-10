---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
- 2019
- 2020
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhrinayo hadda ama aan akhriyay waqtigii lasoo dhaafay.

{% for sanad in page.sanadakhris %}

{% for buug in site.data.buugaag %}

<p>Buugaagta aan akhriyay</p>
{% if buug.akhriyay %}

<h2>{{ sanad }}</h2>
{% if buug.sanadakhris==sanad  %}

{{ buug.title }}, {{buug.author}}, {{ buug.lang }}
{% endif %}


{% endif %}
{% endfor %}
{% endfor %}
