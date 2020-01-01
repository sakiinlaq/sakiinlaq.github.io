---
permalink: /buugaag/
layout: page
sanadakhris: 
- 2020
- 2019
---

[al-Jaaxid](https://ar.wikipedia.org/wiki/%D8%A7%D9%84%D8%AC%D8%A7%D8%AD%D8%B8) al-Kanaani al-Basri (159H - 255H) (776m - 868m) wuxuu ku qoray buugiisa **[kitaab al Xaywaan](https://ar.wikipedia.org/wiki/%D9%83%D8%AA%D8%A7%D8%A8_%D8%A7%D9%84%D8%AD%D9%8A%D9%88%D8%A7%D9%86)**:
>Intee laga helaa saaxiib hurda marka aad hurudo, kula hadla hadba marka aad doontid. [...] ma jiro deris ka wanaagsan, saaxiib ka cadaaladsan, ka taageerid badan, macallin ka daacadsan, buug

Olof Lagercrantz wuxuu ku qoray buuggiisa **Om konsten att skriva och läsa**:

*svenska*
>Vad sker när vi läser? Ögat följer svarta bokstavstecknet på det vita pappret från vänster till höger, åter och åter. Och varelser, natur eller tankar som annan tänkt, nyss eller för tusen år sen stiger fram i vår inbillning...Det finns människor som vi möter i böcker liknar de levande. De talar som vi, andas som vi, gråter och skrattar som vi. Men sträcker vi ut armarna för att omfamna dem griper vi i tomma luften.

*af-Soomaali*
>Maxaa dhaca marka aan wax akhrinayno? Ishu waxay raacdaa xarafaha madow ee ku qoran warqadda cad, bidix ilaa midig, mar iyo marar badan. Bahalo, deegaan ama fikiro qof kale fikiray, hadda ama kun sano ka hor ayaa kasoo maaxanaya mala awaalkeena...Waxaa jira dad aan kula kulmeeno buugaagta oo u eg kuwa nool. Sida annago oo kale ayay u hadlaan, u neefsadaan sideenna, una ooyaa, oo noola caddeeyaan sideenna. Balse hadaan gacmaha kor u qaadno si aan laabta u gelino waxaa qabanaa hawo maran.


Halkaan waxaan kusoo bandhigayaa buugaagta aan akhrinayo hadda ama aan akhriyay waqtigii lasoo dhaafay.


## Buugaagta aan hadda akhrinayo:
{% for sanad in page.sanadakhris %}

<h3>{{ sanad }}</h3>

{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad and buug.akhriyay==false %}

{{ buug.author }} ({{ buug.year }}). 
<i>{{ buug.title }}</i>. <span class="buuglang"> {{ buug.lang }}</span> <span class="buuglink"><a href ="{{ buug.link }}" target="_blank">link </a> </span> 


{% endif %}
{% endfor %}
{% endfor %}

## Buugaagta aan akhriyay:
{% for sanad in page.sanadakhris %}
<h3>{{ sanad }}</h3>

{% for buug in site.data.buugaag %}
{% if buug.sanadakhris==sanad and buug.akhriyay %}


{{ buug.author }} ({{ buug.year }}). 
<i>{{ buug.title }}</i>. <span class="buuglang"> {{ buug.lang }}</span> <span class="buuglink"><a href ="{{ buug.link }}" target="_blank"> link </a> </span> 


{% endif %}
{% endfor %}
{% endfor %}
