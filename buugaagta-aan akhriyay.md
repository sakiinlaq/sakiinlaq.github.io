---
layout: page
title: Buugaagta
permalink: /buugaag/
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhrinayo hadda ama aan akhriyay waqtigii lasoo dhaafay.

<p>Buugaagta aan akhriyay</p>

{% for buug in site.data.buugaag %}

{% if buug.akhriyay %}

<h2>{{ buug.sanadakhris }}</h2>

{{ buug.title }}, {{buug.author}}, {{ buug.lang }}

{% endif %}


{% endfor %}
