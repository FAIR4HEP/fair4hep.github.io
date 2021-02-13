---
title: "FAIR4HEP - Team"
layout: gridlay
excerpt: "FAIR4HEP: Team members"
sitemap: false
permalink: /team/
---

**We are often looking for new PhD students, Postdocs, Professionals and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

## **Senior Personnel**

{% assign previous_institution = "" %}
{% assign number_printed = 0 %}
{% for member in site.data.team_senior %}

{% if member.institution == "uiuc" %}
  {% if previous_institution != "uiuc" %}
### *University of Illinois at Urbana-Champaign*  
  {% endif %}
  {% assign previous_institution = "uiuc" %}
{% endif %}

{% if member.institution == "umn" %}
  {% if previous_institution != "umn" %}
  {% assign number_printed = 0 %}
  </div>
### *University of Minnesota*
  <div>
  {% endif %}
  {% assign previous_institution = "umn" %}
{% endif %}

{% if member.institution == "mit" %}
  {% if previous_institution != "mit" %}
  </div>
  <div class="row">
### *Massachusetts Institute of Technology*
  {% endif %}
  {% assign previous_institution = "mit" %}
{% endif %}

{% if member.institution == "ucsd" %}
  {% if previous_institution != "ucsd" %}
### *University of California at San Diego*
{% assign even_odd = 1 %}
  {% endif %}
  {% assign previous_institution = "ucsd" %}
{% endif %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
  <div class="row">
{% endif %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="36%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  {% if member.number_addinfo == 1 %}
  {{ member.addinfo1 }}
  {% endif %}
  {% if member.number_addinfo == 2 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }}
  {% endif %}
  {% if member.number_addinfo == 3 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }} <br>
  {{ member.addinfo3 }}
  {% endif %}
  {% if member.number_addinfo == 4 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }} <br>
  {{ member.addinfo3 }} <br>
  {{ member.addinfo4 }}
  {% endif %}
  email: <{{ member.email }}>
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
  </div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## **Postdoctoral Fellows**

{% assign number_printed = 0 %}
{% for member in site.data.team_postdocs %}
{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
  <div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="36%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  {% if member.number_addinfo == 1 %}
  {{ member.addinfo1 }}
  {% endif %}
  {% if member.number_addinfo == 2 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }}
  {% endif %}
  {% if member.number_addinfo == 3 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }} <br>
  {{ member.addinfo3 }}
  {% endif %}
  {% if member.number_addinfo == 4 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }} <br>
  {{ member.addinfo3 }} <br>
  {{ member.addinfo4 }}
  {% endif %}
  email: <{{ member.email }}>
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
  </div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## **Graduate Students**

{% assign number_printed = 0 %}
{% for member in site.data.team_grad_students %}
{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
  <div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="36%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  {% if member.number_addinfo == 1 %}
  {{ member.addinfo1 }}
  {% endif %}
  {% if member.number_addinfo == 2 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }}
  {% endif %}
  {% if member.number_addinfo == 3 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }} <br>
  {{ member.addinfo3 }}
  {% endif %}
  {% if member.number_addinfo == 4 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }} <br>
  {{ member.addinfo3 }} <br>
  {{ member.addinfo4 }}
  {% endif %}
  email: <{{ member.email }}>
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
  </div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
