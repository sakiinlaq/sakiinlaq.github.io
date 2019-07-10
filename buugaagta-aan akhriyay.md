---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
- 2019
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhrinayo hadda ama aan akhriyay waqtigii lasoo dhaafay.

{% for sanad in page.sanadakhris %}
<div class="sanad">{{ sanad }}</div>
{% for buug in site.data.buugaag_akhrinayo %}
{% if buug.sanadakhris==sanad %}

{{ buug.title }}, {{ buug.lang }}, {{buug.author}}

{% endif %}
{% endfor %}
{% endfor %}

{% for sanad in page.sanadakhris %}
<div class="sanad">{{ sanad }}</div>
{% for buug in site.data.buugaag_akhriyay %}
{% if buug.sanadakhris==sanad %}

{{ buug.title }}, {{ buug.lang }}, {{buug.author}}

{% endif %}
{% endfor %}
{% endfor %}