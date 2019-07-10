---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
- 2019
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhrinayo hadda ama aan akhriyay waqtigii lasoo dhaafay.

{% for sanad in page.sanadakhris %}
{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad and buug.akhriyay %}
<p> Buugaagta aan akhriyay
<h2>{{ sanad }}</h2>

{{ buug.title }}, {{ buug.lang }}, {{buug.author}}
{% else %}

<p> Buugaagta aan hadda akhrinayo
<h2>{{ sanad }}</h2>

{{ buug.title }}, {{ buug.lang }}, {{buug.author}}

{% endif %}
{% endfor %}
{% endfor %}
