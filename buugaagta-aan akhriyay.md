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

{% if buug.sanadakhris==sanad  %}
<h2>{{ sanad }}</h2>

{{ buug.title }}, {{ buug.lang }}, {{buug.author}}
{% endif %}

{% elseif %}

{{ buug.title }}, {{ buug.lang }}, {{buug.author}}

{% endif %}
{% endfor %}
{% endfor %}
