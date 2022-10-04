---
language: en
layout: default
title: "Course info"
permalink: /en/info
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

{% assign a =  site.data.info.testi | where_exp: "testo","testo.lingua == language" %}
<ul>
{% for testo in a %}<li> <em>{{ testo.autori }}</em>, {{ testo.titolo }}, {{ testo.editore }}   
{% if testo.commento[language] %}   <br/><em>{{ testo.commento[language] }}</em>
{% elsif testo.commento['all'] %}   <br/><em>{{ testo.commento['all'] }}</em> 
{% endif %}</li>{% endfor %}
</ul>

## Resources


### Didactic Material  

> Material used during the lectures, in PDF format.  
> The Web Engineering course is currently given in Italian. The following slide sets contain an English translation of all the slides used during the course lectures. Such a translation is the first result of a long and complex adaptation work. Therefore, the slides may still contain some errors, typos and poorly readable statements. I'll do my best to refine them, but it takes time. Suggestions are always appreciated!  
> TERMS OF USE: This material has been compiled for the students of the Web Engineering course. Since knowledge *should* be considered everyone's heritage, my slides are available to anyone who wants to study the web application development techniques. However, the material provided on this pages *cannot* be used, even in part, for other purposes, for example as educational material in other courses, without my explicit permission and without citing the source. The knowledge must be free, but the work must be paid, even only with a 'thank you'. 

### Slides  {#slides}

* [Course slides repository](https://github.com/WebEngineering-Univaq/WE_Lecture_Slides)  
  *Always check for updates!*

### Final Course Projects  {#progetti}

* [Final project specifications repository](https://github.com/WebEngineering-Univaq/Project_Specifications)  
  *A collection of all the final course projects for each academic year*

### Examples  {#esempi}

> Before trying to run or modify these examples, read the [/it/risorse#software](Software) section
and set-up all the required software

* [HTML 5](https://github.com/WebEngineering-Univaq/HTML_Examples)  
  *HTML files showing the syntax of the most common language elements*
* [Cascading Style Sheets](https://github.com/WebEngineering-Univaq/CSS_Examples)  
  *Examples used to demonstrate che CSS features*
* [Java Servlets](https://github.com/orgs/WebEngineering-Univaq/repositories?q=Java_&type=all&language=&sort=name)  
  *Examples of Java web applications, packed as Maven projects, compatible with all the most common IDEs*
* [Javascript](https://github.com/orgs/WebEngineering-Univaq/repositories?q=JS_&type=all&language=&sort=name)  
  *Script examples (to execute them, open the corresponding HTML file in any browser)*