---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
- 2019
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhriyay waqtigii lasoo dhaafay ama aan akhrinayo hadda.

{% for sanad in page.sanadakhris %}
<div class="sanad">{{ sanad }}</div>
{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad %}

{{ buug.title }}, {{ buug.lang }}, {{buug.author}}

{% endif %}
{% endfor %}
{% endfor %}