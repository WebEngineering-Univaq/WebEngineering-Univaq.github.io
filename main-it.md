---
language: it
layout: default
title: "Informazioni sul corso"
year: 2022
permalink: /it/info
menuitems:
  - label: Sillabo
    url: "#sillabo"
  - label: Testi
    url: "#testi"
  - label: Software
    url: "#software"
  - label: Slides e Progetti
    url: "#materiale"
  - label: Esempi
    url: "#esempi"
---

{%include pageglobal.html %}



## Sillabo {#sillabo}

{% assign a =  site.data.info.sillabo  %}
<ol>
{% for credito in a %} <li> {% for argomento in credito %}
{% if argomento[language] %}   {{ argomento[language] }}{% elsif argomento['all'] %}   {{ argomento['all'] }}{% endif %}. {% endfor %}</li>{% endfor %}</ol>


## Libri di Testo  {#testi}
{% assign a =  site.data.info.testi | where_exp: "testo","testo.lingua == language" %}
<ul>
{% for testo in a %}<li> <em>{{ testo.autori }}</em>, {{ testo.titolo }}, {{ testo.editore }}   
{% if testo.commento[language] %}   <br/><em>{{ testo.commento[language] }}</em>
{% elsif testo.commento['all'] %}   <br/><em>{{ testo.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

## Risorse

### Software  {#software}

> Applicazioni utili legate agli argomenti del corso. Per facilitare lo sviluppo, prima di installare il software leggete la guida sulla [creazione di un workspace software privato](/it/workspace)

<ul>
{% for s in site.data.info.software %}<li> 
<a href="{{ s.url }}">{{ s.nome }}</a>
{% if s.commento[language] %}   <br/><em>{{ s.commento[language] }}</em>
{% elsif s.commento['all'] %}   <br/><em>{{ s.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

### Materiale Didattico  {#materiale}

> Materiale usato a lezione, in formato PDF.  
> CONDIZIONI D'USO: Questo materiale è dedicato agli studenti del corso di Ingegneria del Web. Visto che la conoscenza **deve** essere considerata un patrimonio di tutti, le mie slides sono a disposizione di chiunque voglia servirsene per studiare le tecniche di realizzazione delle applicazioni web. Tuttavia, il materiale fornito su queste pagine, e sulle pagine dei corsi, *non può essere usato, neppure in parte, per altri scopi, primo fra tutti come materiale didattico di altri corsi* senza il mio esplicito consenso e senza citare la provenienza del materiale stesso. La conoscenza è gratuita, ma il lavoro va remunerato, anche solo con un ringraziamento.

* [Slides del corso](https://github.com/WebEngineering-Univaq/WE_Lecture_Slides)
* [Progetti di fine corso](https://github.com/WebEngineering-Univaq/Project_Specifications)  
  *Questa raccolta contiene tutti i progetti di fine corso, divisi per anno accademico*

### Esempi  {#esempi}

> Esempi mostrati o sviluppati in aula
* [HTML 5](https://github.com/WebEngineering-Univaq/HTML_Examples)  
  *Alcuni file HTML che dimostrano la sintassi di tutti i più importanti elementi del linguaggio e permettono di verificarne la funzionalità nei browser*
* [Cascading Style Sheets](https://github.com/WebEngineering-Univaq/CSS_Examples)  
  *Esempi usati in aula per mostrare le caratteristiche dei CSS e testarne la compatibilità*
* [Java Servlets](https://github.com/orgs/WebEngineering-Univaq/repositories?q=Java_&type=all&language=&sort=name)  
  *Esempi di Java web application forniti sotto forma di progetti Maven, compatibili con tutti i più diffusi IDE*
* [Javascript](https://github.com/orgs/WebEngineering-Univaq/repositories?q=JS_&type=all&language=&sort=name)  
  *Esempi di script eseguibili aprendo in qualsiasi browser il file HTML che li accompagna*

### Link utili

> Raccolta non ordinata e spesso anche poco aggiornata di link utili per approfondire il vasto panorama delle tecnologie del web!

<ul>
{% for s in site.data.info.links %}<li> 
<a href="{{ s.url }}">{% if s.nome[language] %}{{ s.nome[language] }}
{% elsif s.nome['all'] %}{{ s.nome['all'] }}{% endif %}</a>
{% if s.commento[language] %}   <br/><em>{{ s.commento[language] }}</em>
{% elsif s.commento['all'] %}   <br/><em>{{ s.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

