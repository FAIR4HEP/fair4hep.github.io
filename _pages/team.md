---
title: "FAIR4HEP - Team"
layout: gridlay
excerpt: "FAIR4HEP: Team members"
sitemap: false
permalink: /team/
---

# Group Members

 **We are often looking for new PhD students, Postdocs, Professionals and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

## Senior Personnel
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

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
  {% if member.number_addinfo == 5 %}
  {{ member.addinfo1 }} <br>
  {{ member.addinfo2 }} <br>
  {{ member.addinfo3 }} <br>
  {{ member.addinfo4 }} <br>
  {{ member.addinfo5 }}
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

## Undergraduate Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}
  {% endfor %}

  </ul>
</div>



{% if even_odd == 1 %}
</div>
{% endif %}
