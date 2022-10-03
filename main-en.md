---
language: en
layout: default
title: "Course info"
year: 2022
permalink: /en/info
menuitems:
  - label: Syllabus
    url: "#sillabo"
  - label: Textbooks
    url: "#testi"
  - label: Software
    url: "#software"
  - label: Slides and Projects
    url: "#materiale"
  - label: Examples
    url: "#esempi"
---

{%include pageglobal.html %}

## Syllabus {#sillabo}

{% assign a =  site.data.info.sillabo  %}
<ol>
{% for credito in a %} 
<li> {% for argomento in credito %}
{% if argomento[language] %}   {{ argomento[language] }}
{% elsif argomento['all'] %}   {{ argomento['all'] }}
{% endif %}. 
{% endfor %}</li>
 {% endfor %}</ol>


## Textbooks  {#testi}


<ul>
{% for testo in a %}<li> <em>{{ testo.autori }}</em>, {{ testo.titolo }}, {{ testo.editore }}   
{% if testo.commento[language] %}   <br/><em>{{ testo.commento[language] }}</em>
{% elsif testo.commento['all'] %}   <br/><em>{{ testo.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

## Resources

### Software  {#software}

> Useful applications related to the course topics. To ease the development, before installing any software please read the guode about the [creation of a private software workspace](/en/workspace)

<ul>
{% for s in site.data.info.software %}<li> 
<a href="{{ s.url }}">{{ s.nome }}</a>
{% if s.commento[language] %}   <br/><em>{{ s.commento[language] }}</em>
{% elsif s.commento['all'] %}   <br/><em>{{ s.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

### Didactic Material  {#materiale}

> Material used during the lectures, in PDF format.  
> The Web Engineering course is currently given in Italian. The following slide sets contain an English translation of all the slides used during the course lectures. Such a translation is the first result of a long and complex adaptation work. Therefore, the slides may still contain some errors, typos and poorly readable statements. I'll do my best to refine them, but it takes time. Suggestions are always appreciated!  
> TERMS OF USE: This material has been compiled for the students of the Web Engineering course. Since knowledge *should* be considered everyone's heritage, my slides are available to anyone who wants to study the web application development techniques. However, the material provided on this pages *cannot* be used, even in part, for other purposes, for example as educational material in other courses, without my explicit permission and without citing the source. The knowledge must be free, but the work must be paid, even only with a 'thank you'. 

* [Course slides](https://github.com/WebEngineering-Univaq/WE_Lecture_Slides)
* [Final project specifications](https://github.com/WebEngineering-Univaq/Project_Specifications)  
  *A collection of all the final course projects for each academic year*

### Examples  {#esempi}

> Examples developed or illustrated during the lectures

* [HTML 5](https://github.com/WebEngineering-Univaq/HTML_Examples)  
  *HTML files showing the syntax of the most common language elements*
* [Cascading Style Sheets](https://github.com/WebEngineering-Univaq/CSS_Examples)  
  *Examples used to demonstrate che CSS features*
* [Java Servlets](https://github.com/orgs/WebEngineering-Univaq/repositories?q=Java_&type=all&language=&sort=name)  
  *Examples of Java web applications, packed as Maven projects, compatible with all the most common IDEs*
* [Javascript](https://github.com/orgs/WebEngineering-Univaq/repositories?q=JS_&type=all&language=&sort=name)  
  *Script examples (to execute them, open the corresponding HTML file in any browser)*


### Useful links

> Unordered and often not updated collection of useful links to deepen your knowledge about web technologies!

<ul>
{% for s in site.data.info.links %}<li> 
<a href="{{ s.url }}">{% if s.nome[language] %}{{ s.nome[language] }}
{% elsif s.nome['all'] %}{{ s.nome['all'] }}{% endif %}</a>
{% if s.commento[language] %}   <br/><em>{{ s.commento[language] }}</em>
{% elsif s.commento['all'] %}   <br/><em>{{ s.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

