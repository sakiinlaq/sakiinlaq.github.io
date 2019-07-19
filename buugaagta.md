---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
- 2019
---
> Intee laga helaa saaxiib hurda marka aad hurudo, kula hadla hadba marka aad doontid. [...] ma jiro deris ka wanaagsan, saaxiib ka cadaaladsan, ka taageerid badan, macallin ka daacadsan, buug




Halkaan waxaan kusoo bandhigayaa buugaagta aan akhrinayo hadda ama aan akhriyay waqtigii lasoo dhaafay.


## Buugaagta aan hadda akhrinayo:
{% for sanad in page.sanadakhris %}

<h3>{{ sanad }}</h3>

{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad and buug.akhriyay==false %}

{{ buug.author }} ({{ buug.year }}). 
<i>{{ buug.title }}</i>. <span class="booklang"> {{ buug.lang }}</span>


{% endif %}
{% endfor %}
{% endfor %}

## Buugaagta aan akhriyay:
{% for sanad in page.sanadakhris %}
<h3>{{ sanad }}</h3>

{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad and buug.akhriyay %}


{{ buug.author }} ({{ buug.year }}). 
<i>{{ buug.title }}</i>. <span> {{ buug.lang }}</span>


{% endif %}
{% endfor %}
{% endfor %}
