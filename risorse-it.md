---
language: it
layout: default
title: "Risorse del corso"
year: 2022
permalink: /it/risorse
menuitems:
  - label: Sillabo
    url: "/it/info#sillabo"
  - label: Testi
    url: "/it/info#testi"
  - label: Software
    url: "#software"
  - label: Slides
    url: "/it/info#slides"
  - label: Progetti
    url: "/it/info#progetti"	
  - label: Esempi
    url: "/it/info#esempi"
  - label: Altre risorse
    url: "#links"    
---

{%include pageglobal.html %}


## Risorse online

### Software  {#software}

> Applicazioni utili legate agli argomenti del corso. Per facilitare lo sviluppo, prima di installare il software leggete la guida sulla [creazione di un workspace software privato](/it/workspace)

<ul>
{% for s in site.data.info.software %}<li> 
<a href="{{ s.url }}">{{ s.nome }}</a>
{% if s.commento[language] %}   <br/><em>{{ s.commento[language] }}</em>
{% elsif s.commento['all'] %}   <br/><em>{{ s.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

### Contenti di Approfondimento {#links}

> Raccolta non ordinata e spesso anche poco aggiornata di link utili per studiare e approfondire il vasto panorama delle tecnologie del web!

<ul>
{% for s in site.data.info.links %}<li> 
<a href="{{ s.url }}">{% if s.nome[language] %}{{ s.nome[language] }}
{% elsif s.nome['all'] %}{{ s.nome['all'] }}{% endif %}</a>
{% if s.commento[language] %}   <br/><em>{{ s.commento[language] }}</em>
{% elsif s.commento['all'] %}   <br/><em>{{ s.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

