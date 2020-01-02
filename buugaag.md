---
permalink: /buugaag/
layout: page
sanadakhris: 
- 2020
- 2019
---

[al-Jaaxid](https://al-maktaba.org/author/787){:target="_blank"} al-Kanaani al-Basri (163H - 255H) (780m - 869m) wuxuu ku qoray buugiisa **[kitaab al Xayawaan](https://al-maktaba.org/book/23775){:target="_blank"}**:
>Intee laga helaa saaxiib hurda marka aad hurudo, kula hadla hadba marka aad doontid. [...] ma jiro deris ka wanaagsan, saaxiib ka cadaaladsan, ka taageerid badan, macallin ka daacadsan, buug


Olof Lagercrantz wuxuu ku qoray buuggiisa **Om konsten att skriva och läsa**:

>Vad sker när vi läser? Ögat följer svarta bokstavstecknet på det vita pappret från vänster till höger, åter och åter. Och varelser, natur eller tankar som annan tänkt, nyss eller för tusen år sen stiger fram i vår inbillning...Det finns människor som vi möter i böcker liknar de levande. De talar som vi, andas som vi, gråter och skrattar som vi. Men sträcker vi ut armarna för att omfamna dem griper vi i tomma luften.
>>
Maxaa dhaca marka aan wax akhrinayno? Ishu waxay raacdaa xarafaha madow ee ku qoran warqadda cad, laga bilaabo bidix ilaa midig, mar iyo marar badan. Bahalo, deegaan ama fikirro qof kale fikiray, hadda ama kun sano ka hor ayaa kasoo maaxanaya mala awaalkeenna...Waxaa jira dad aan kula kulmeeno buugaagta oo u eg kuwa nool. Sida annago oo kale ayay u hadlaan, u neefsadaan sideenna. Una ooyaan, oo dhoola caddeeyaan sideenna. Balse hadaan gacmaha kor u qaadno si aan laabta u gelino waxaan qabanaynaa hawo maran.


Halkaan waxaan kusoo bandhigayaa buugaagta aan akhrinayo hadda ama aan akhriyay waqtigii lasoo dhaafay.


## Buugaagta aan hadda akhrinayo:
{% for sanad in page.sanadakhris %}


{% if sanad == 2020 %}
<h3>{{ sanad }}</h3>
{% endif %}

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
