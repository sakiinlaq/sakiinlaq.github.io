---
permalink: /buugaag/
sanadakhris: 
- 2019
---

Jaaxid wuxuu qoray:
>Intee laga helaa saaxiib hurda marka aad hurudo, kula hadla hadba marka aad doontid. [...] ma jiro deris ka wanaagsan, saaxiib ka cadaaladsan, ka taageerid badan, macallin ka daacadsan, buug

Olof Lagercrantz wuxuu ku qoray buuggiisa *Om konsten att skriva och läsa*:
>Vad sker när vi läser? Ögat följer svarta bokstavstecknet på det vita pappret från vänster till höger, åter och åter. Och varelser, natur eller tankar som annan tänkt, nyss eller för tusen år sen stiger fram i vår inbillning...Det finns människor som vi möter i böcker liknar de levande. De talar som vi, andas som vi, gråter och skrattar som vi. Men sträcker vi ut armarna för att omfamna dem griper vi i tomma luften.


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
<i>{{ buug.title }}</i>. <span class="booklang"> {{ buug.lang }}</span>


{% endif %}
{% endfor %}
{% endfor %}
