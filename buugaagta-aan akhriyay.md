---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
- 2019
- 2020
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhriyay waqtigii lasoo dhaafay ama aan akhrinayo hadda.


{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==page.sanadakhris %}
<h2> {{buug.sanadakhris}}
{{ buug.title }} &emsp; <span class="date">{{ buug.lang }}</span> <br>
{{buug.author}} <a href="{{buug.link}}"></a>
{% endfor %}