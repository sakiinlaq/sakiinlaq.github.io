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
<h2>{{ sanad }}</h2>

{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad %}

{{ buug.title }}, {{buug.author}}, {{ buug.lang }}
{% if buug.akhriyay %}
<span><em>Hadda ayaan akhrinayaa</em></span>
{% endif %}

{% endif %}
{% endfor %}
{% endfor %}
