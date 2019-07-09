---
layout: page
title: Buugaagta
permalink: /buugaag/
sanadakhris: 
		- 2019
		- 2020
		- 2021
		- 2022
---

Halkaan waxaan kusoo bandhigayaa buugaagta aan akhriyay waqtigii lasoo dhaafay ama aan akhrinayo hadda.

### 2019

#### Akhrinayaa hadda

{% for sanad in page.sanadakhris %}
 <div class="sanadakhris"></div>
 {%for buug in  site.data.buugaag %}
 	{% if buug.sanadkhris==sanad%}
 	<h2>sanad</h2>
 		<p>{{ buug.title }}, qoraa {{ buug.author}} &emsp;<span class="date">{{ buug.lang }}</span> <br><a href={{ buug.link }}>link</a>  </p>

   
	{% endif %}
	{% endfor %}
	{% endfor %}

<!---
## Publications

{% for pubyear in page.pubyears %}
<div class="pubyear">{{ pubyear }}</div>
{% for publication in site.data.publications  %}

{% if publication.year == pubyear %}
<b>{{ publication.title }}</b>
&emsp;<span class="date">{{ publication.type }}</span><br>
{{ publication.ref | markdownify | remove: '<p>' | remove: '</p>' }}
<details style="margin-top: -.7em; margin-left: 1em">
<summary>
 abstract {% if publication.abstract %}
 <a>abstract</a>
 {% else %}
 <span style="color: $gray"> abstract </span>
{% endif %} |
 pdf -
{% if publication.pdf %}
 <a href="{{ publication.pdf }}">pdf</a>
  {% else %} 
  <span style="color: $gray">pdf</span>
{% endif %} |
 link 
{% if publication.link %}
 <a href="{{ publication.link }}">link</a>
 {% else %}
 <span style="color: $gray">link</span>
{% endif %}
</summary>
{% if publication.abstract %}
  <span class="date">{{ publication.abstract | markdownify }}</span>
{% endif %}
</details>

{% endif %}
{% endfor %}
{% endfor %}

<br/>

## Other documents

These documents are subject to continuous tinkering. The latest version can always be found here. Please report any errors in these documents and they will be corrected ASAP.

{% for docpost in site.posts | reversed %}
{% if docpost.document %} 


{% if docpost.minidoc %}
<a href="{{ docpost.document }}"><img style="width: 3em; height: 3em; float: left; margin-right: 30px" src="{{ docpost.minidoc }}"></a>
  {% else %}
<a href="{{ docpost.document }}"><img style="width: 3em; height: 3em; float: left; margin-right: 30px" src="{{ docpost.thumbnail }}"></a>
{%  endif %}
{% if docpost.documenttitle %}
  {{ docpost.documenttitle }}
  {% else %}
  {{ docpost.title }}
{% endif %}<
--{% if docpost.lang == 'sv'%}
<span class="date">(Swedish)</span>
{% endif %}<br>
<span class="publink">[pdf]({{ docpost.document }}) | [Blog post]({{ site.url }}{{ docpost.url }})</span>
<!- <span class="date"> 
<! &emsp;{% for tag in docpost.tags %} -{{tag}}{% endfor %} -
<- </span> --


{% endif %}
{% endfor %}

<--
Taariikhda Afka iyo Bulshada Soomaaliyeed, Cabdalla C. Mansuur, [link](https://books.google.se/books?id=vABdswEACAAJ) _Af-Soomaali_

Africa’s First Democrats: Somalia’s Aden A. Osman and Abdirazak H. Hussen, Cabdi Ismaaciil Samatar, [link](https://books.google.se/books?id=4Yt2DQAAQBAJ&dq) _Af-Ingiriis_


 كشف السدود عن تاريخ الصومال ومماليكهم السبعة، احمد عبدالله ريراش [link](http://hdl.handle.net/2307/3037) _af-Carabi_



De kommer att drunkna i sina mödrars tårar, [link](https://books.google.se/books?id=cXIvDgAAQBAJ) _Af-Iswiidhish_

-->
