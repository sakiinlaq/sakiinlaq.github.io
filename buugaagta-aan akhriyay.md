---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
- 2019
- 2020
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhriyay waqtigii lasoo dhaafay ama aan akhrinayo hadda.

{% for sanad in page.sanadakhris %}
<div class="sanad">{{ sanad }}</div>
{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad %}
<h2> {{buug.sanadakhris}}</h2>
{{ buug.lang }}, {{buug.author}}

{% endif %}
{% endfor %}
{% endfor %}