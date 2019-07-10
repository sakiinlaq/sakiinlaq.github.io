---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
- 2019
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhrinayo hadda ama aan akhriyay waqtigii lasoo dhaafay.


## Buugaagta aan hadda akhrinayo:
{% for sanad in page.sanadakhris %}
{% if sanad and buug.akhriyay==false %}

<h3>{{ sanad }}</h3>
{% endif %}

{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad and buug.akhriyay==false %}

{{ buug.title }}, {{buug.author}}, {{ buug.lang }}

{% endif %}
{% endfor %}
{% endfor %}

## Buugaagta aan akhriyay:
{% for sanad in page.sanadakhris %}

{% if sanad and buug.akhriyay %}
<h3>{{ sanad }}</h3>
{% endif %}

{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad and buug.akhriyay %}

{{ buug.title }}, {{buug.author}}, {{ buug.lang }}

{% endif %}
{% endfor %}
{% endfor %}
