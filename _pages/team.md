---
title: "FAIR4HEP - Team"
layout: gridlay
excerpt: "FAIR4HEP: Team members"
sitemap: false
permalink: /team/
---

**We are often looking for new PhD students, Postdocs, Professionals and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

## **Senior Personnel**

{% assign institution_printed = 0 %}
{% assign number_printed = 0 %}
{% for member in site.data.team_senior %}

{% if institution_printed == 0 %}
{% if member.institution == "uiuc" %}
### *University of Illinois at Urbana-Champaign*
{% endif %}
{% if member.institution == "umn" %}
### *University of Minnesota*
{% endif %}
{% if member.institution == "mit" %}
### *Massachusetts Institute of Technology*
{% endif %}
{% if member.institution == "ucsd" %}
### *University of California at San Diego*
{% endif %}
{% assign institution_printed = 1 %}
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
