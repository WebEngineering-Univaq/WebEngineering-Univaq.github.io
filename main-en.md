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

